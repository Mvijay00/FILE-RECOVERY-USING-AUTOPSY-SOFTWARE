# FILE-RECOVERY-USING-AUTOPSY-SOFTWARE

## AIM
To use **Autopsy Digital Forensics Tool** to retrieve deleted files from a disk image.

---

## REQUIREMENTS
- **Operating System**: Windows 10/11, macOS, or Linux
- **Tool**: [Autopsy Digital Forensics](https://www.autopsy.com/)  
- **Test Data**: Disk image file (`disk.dd`, `disk.img`, `.E01`)

---

## ARCHITECTURE DIAGRAM
```mermaid
flowchart TD
    A[Disk Image / Physical Drive] --> B[Install Autopsy]
    B --> C[Create New Case in Autopsy]
    C --> D[Add Data Source: Disk Image]
    D --> E["Run File System & Data Recovery Modules"]
    E --> F[Locate Deleted Files in Results]
    F --> G[Recover and Export Deleted Files]
```
## DESIGN STEPS:
### Step 1:
Open Autopsy and create a new case with appropriate case details.

### Step 2:
Add a disk image as a data source and let Autopsy analyze the content.

### Step 3:
Navigate to the "Deleted Files" section in Autopsy and examine or recover the deleted files.

## PROGRAM:
### Install Autopsy
```bash
# Download Autopsy from:
# https://www.autopsy.com/
# Install following the setup wizard.
```
### Create a New Case
```
# File → New Case
# Enter Case Name: Deleted_File_Recovery
# Choose Base Directory: C:\Cases\Deleted_File_Recovery
# Click Finish
```
### Add Disk Image
```
# Add Data Source → Disk Image or VM File
# Browse to: C:\forensics\disk.dd
# Click Next
```
### Run Ingest Modules
```# Select:
# - File System Analysis
# - Keyword Search (optional)
# - Data Recovery / Carving
# Click Finish
```
### Locate Deleted Files
```
# Navigate to 'Deleted Files' section in the tree view
# Review metadata (size, hash, timestamps)
```
### Export Deleted Files
```
# Right-click → Extract File(s)
# Save to: C:\forensics\Recovered_Files\
```

## OUTPUT:
Recovered Deleted File List and Details

<img width="1600" height="899" alt="image" src="https://github.com/user-attachments/assets/81077b63-9bb7-4432-8278-3b7063b2e51e" />
<img width="1600" height="899" alt="image" src="https://github.com/user-attachments/assets/3f478a46-8dee-48aa-93b4-ea0be0d19f04" />
<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/16da33b1-6fd8-4c26-86f2-b097c3b08060" />
<img width="1600" height="899" alt="image" src="https://github.com/user-attachments/assets/8233ca2d-dfa6-46e6-99a7-301827b1cf7d" />
<img width="1600" height="892" alt="image" src="https://github.com/user-attachments/assets/1bb800bb-9e9a-4361-9c65-5c0e639b8f23" />
<img width="1600" height="899" alt="image" src="https://github.com/user-attachments/assets/7ff36704-369d-48f9-b04d-3d3cad169712" />
<img width="1600" height="898" alt="image" src="https://github.com/user-attachments/assets/00caf66c-e394-4e16-ac0e-75725429b697" />
<img width="1600" height="899" alt="image" src="https://github.com/user-attachments/assets/55021287-d3eb-41e7-b5e1-8078b8848da7" />
<img width="1600" height="895" alt="image" src="https://github.com/user-attachments/assets/29861ebd-a061-4279-81f9-29ce1bba0fc8" />
<img width="1482" height="926" alt="image" src="https://github.com/user-attachments/assets/f0208c0c-5d93-4734-8212-92caf7283422" />











## RESULT:
Deleted files were successfully retrieved and analyzed using Autopsy.
