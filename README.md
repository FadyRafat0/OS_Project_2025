# OS Project 2025

A custom x86 Operating System kernel implementation with bootloader, kernel, and user-space programs.

## 📋 Overview

This project implements a functional operating system from scratch, including:
- **Bootloader** - Low-level boot code for x86 systems
- **Kernel** - Core OS kernel with essential functionality
- **Libraries** - System libraries for kernel and user programs
- **User Programs** - User-space applications and utilities

The OS is designed to run on the Bochs x86 emulator, making it ideal for learning OS concepts and kernel development.

## 🛠️ Technology Stack

| Component | Details |
|-----------|---------|
| **Primary Language** | C (98%) |
| **Assembly** | x86 Assembly (1.1%) |
| **Build System** | GNU Make |
| **Emulator** | Bochs x86 Emulator |
| **Debugger** | GDB (with configuration) |
| **Target Architecture** | x86 (32-bit) |

## 📁 Project Structure

```
.
├── boot/                 # Bootloader code
├── kern/                 # Kernel implementation
├── lib/                  # System libraries
├── user/                 # User-space programs
├── inc/                  # Header files
├── conf/                 # Configuration files
├── GNUmakefile          # Build configuration
├── .bochsrc             # Bochs emulator configuration
├── .bochsrc-debug       # Bochs debug configuration
└── .gdbinit             # GDB debugger initialization
```

## 🚀 Getting Started

### Prerequisites

- **GCC Compiler** - For compiling C code
- **GNU Make** - For building the project
- **Bochs** - x86 emulator for running the OS
- **GDB** - GNU Debugger for debugging (optional)
- **NASM** - Netwide Assembler (if assembling x86 code)

### Building the Project

1. **Clone the repository:**
   ```bash
   git clone https://github.com/FadyRafat0/OS_Project_2025.git
   cd OS_Project_2025
   ```

2. **Build the kernel:**
   ```bash
   make
   ```

3. **Clean build artifacts:**
   ```bash
   make clean
   ```

### Running the OS

**Standard execution:**
```bash
bochs -f .bochsrc
```

**Debug execution (with GDB):**
```bash
bochs -f .bochsrc-debug
```

This will launch the Bochs emulator with the compiled OS kernel. The emulator will boot your OS and allow you to interact with it.

## 🔧 Development

### Debugging

The project includes GDB configuration for kernel debugging. Use the debug Bochs configuration to connect GDB and step through kernel execution.

**Tips for debugging:**
- Use `.gdbinit` for automatic breakpoints and symbol loading
- The `.bochsrc-debug` file enables debugging features in Bochs
- Set breakpoints in kernel code and inspect memory/registers

### Modifying the Kernel

- **Kernel code** - Located in `kern/` directory
- **User programs** - Located in `user/` directory
- **Header files** - Place declarations in `inc/` directory
- **Configuration** - Modify compiler flags in `GNUmakefile`

### Build Configuration

Edit `GNUmakefile` to adjust:
- Compiler flags and optimization levels
- Source file includes
- Output binary names and locations
- Build dependencies

## 📝 Notes

- This project uses modern GCC, which may require adjustments from older compiler versions
- Refer to `Readme_Project_Port_To_ModernGCC.txt` for compatibility notes
- BIOS files are included in the repository for Bochs emulation

## 🎓 Learning Outcomes

This project demonstrates:
- Bootloader and low-level CPU initialization
- Memory management and paging
- Interrupt handling and exception processing
- Process/thread management basics
- System call interface design
- User/kernel mode separation

## 📚 References

- [Bochs Emulator Documentation](http://bochs.sourceforge.net/)
- [x86 Assembly Language](https://en.wikibooks.org/wiki/X86_Assembly)
- [Operating Systems Concepts](https://www.os-book.com/)
- [GDB Debugger Guide](https://sourceware.org/gdb/documentation/)

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs and issues
- Suggest improvements
- Submit pull requests with enhancements
- Improve documentation

## 📄 License

[Specify your license here - e.g., MIT, GPL, etc.]

## 👤 Author

**Fady Rafat**

## 📞 Support

For questions or issues:
- Check existing [GitHub Issues](https://github.com/FadyRafat0/OS_Project_2025/issues)
- Review the documentation files in the repository
- Consult the references section above

---

**Last Updated:** 2025  
**Project Status:** Active Development
