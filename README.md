# VMPStatic
A static VMProtect unpacker for PE files, compatible with VMProtect 1.x–3.x and capable of reconstructing decompressed PE images

Unlike dynamic unpacker, this tool works without executing the target file. The goal is to recover a usable PE image that can be further analyzed in tools such as IDA, Ghidra, x64dbg, or similar software.

<img width="1113" height="626" alt="image" src="https://github.com/user-attachments/assets/8fea91d2-7340-4973-8a11-d635fc37ef59" />

## Features

- Static VMProtect unpacking  
- Compatible with VMProtect 1.x, 2.x, and 3.x patterns (Until 3.10.x, VMP stopped using LZMA as compression algorithm)
- Analysis of PE headers and sections  
- Detection of VMProtect sections and stubs  
- Reconstruction of packed images  
- Recovers data hidden by packing, such as strings, resources, and embedded PE files  

## Limitations

- Does not include an import address table fixer  
- Does not include automatic OEP recovery for all samples  
- Does not include de-virtualization  
- Some protected samples may still require manual repair after unpacking  

## Usage

```bash
vmpstatic.exe packed.exe unpacked.exe
