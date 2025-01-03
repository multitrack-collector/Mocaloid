English translation by [BigScience BLOOM](https://huggingface.co/bigscience/bloom):
## About Mocaloid

Mocaloid is an experimental engine that replaces DaisyBell with Moresample engine. It will try to use an integrated method to get necessary samples and label information from VoiceBank and deliver them to Moresample to synthesize sound.

## Knowledge base

This repository references the following open source projects:

File structure and sample decompression:

1. https://github.com/641i130/ddb-extraction
2. https://github.com/yuukawahiroshi/ddb-tools

Label, pitch, and TextGrideLabel information

3. https://github.com/shmishtopher/VAU
4. https://github.com/RigoLigoRLC/ddiview

Other references:
5. https://github.com/praat/praat

## Other
About compilation

- 1. The main program uses AvaloniaUI + VS2022(.net8) to compile. Windows platform uses IDE/VSCode to compile with Nuget, Linux/Mac platform uses dotnet command/VSCode to compile.
- 
- 2. libddi parsing library uses an environment based on QT5.15 to compile. Currently provides 2 kinds of compilation configurations:
  - 2.1 VC110-windows compilation
         To simplify the release, the code is statically compiled and carries QTCore library, and in windows you can use VC110 to directly compile the 32-bit version.

  - 2.2 QTCreator compilation
         Considering cross-platform requirements, you can download and install QT5.15 development environment, use QTCreator to open libddi.pro file to compile, supporting MingGW/GCC/VC compilation. Compile the libddi.dll file and copy it to MocaloidApi.dll in the same directory.

- PS: libddi's platform and the main program should be consistent, either x86 or x64.

This repository is an analysis and experimental repository, and is not allowed to be used for any commercial purpose.
