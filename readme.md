When pushing a C++ project to GitHub, you typically want to include the necessary files for building and running the project while excluding files that are generated during the build process. Here's a general guideline for files to include and exclude:

Files to Include:
1. Source code files: Include all the C++ source code files (.cpp, .h, .hpp, etc.) required for your project.

2. CMakeLists.txt: Include the CMakeLists.txt file that defines the build instructions for your project. This file is crucial for setting up the build environment and preserving the CMake settings.

3. Readme and Documentation: Include any documentation files, such as a Readme.md, that provide instructions on how to build and use the project.

Files to Exclude:
1. Compiled binaries: Exclude any compiled binary files (.exe, .out, .so, .dll, etc.) generated during the build process. These files can be specific to your local machine and are unnecessary for others to build the project.

2. Build directories: Exclude any build directories created by the build system (e.g., "build", "bin", "out", etc.). These directories contain intermediate and generated files that can be recreated by the build process.

3. IDE-specific files: Exclude any IDE-specific files and directories that are not necessary for building and running the project. These files can include settings, cache, and temporary files specific to your IDE (e.g., Clion's ".idea" directory).

To preserve the CMake settings and set up the project on another computer, follow these steps:

1. Clone the repository: On the other computer, clone the repository from GitHub using Git.

2. Set up the build environment: Install the required dependencies and make sure CMake is installed on the computer.

3. Build the project: Create a build directory (e.g., "build") and navigate into it. Then run the CMake command to generate the build files based on the CMakeLists.txt file. For example:
   ```
   cmake ..
   ```

4. Build the project: Use the appropriate build tool (e.g., make, Visual Studio, etc.) to build the project based on the generated build files.

By following these steps, you should be able to set up the C++ project on another computer while preserving the CMake settings and building the project successfully.