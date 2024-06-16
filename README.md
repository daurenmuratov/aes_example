*** AES Encrypt and Decrypt Example using OpenSSL library ***

// Compilation
g++ -o main main.cpp -lssl -lcrypto
// Run linux
./main


// Linux
sudo apt-get install libssl-dev

// Windows
https://slproweb.com/products/Win32OpenSSL.html

Download Win64 OpenSSL v3.3.1
EXE | MSI	217MB Installer
https://slproweb.com/download/Win64OpenSSL-3_3_1.msi

install to C:\OpenSSL-Win64

in c_cpp_properties.json:

{
    "configurations": [
        {
            "name": "Win32",
            "includePath": [
                "${workspaceFolder}/**",
                "C:/OpenSSL-Win64/include" <-- add this line
            ],
            "defines": [
                "_DEBUG",
                "UNICODE",
                "_UNICODE"
            ],
            "windowsSdkVersion": "10.0.19041.0",
            "compilerPath": "cl.exe",
            "cStandard": "c17",
            "cppStandard": "c++17",
            "intelliSenseMode": "windows-msvc-x64"
        }
    ],
    "version": 4
}

tasks.json

in args:
                "-lssl", <-- Add theese lines
                "-lcrypto", <--

build