# From Blueprint to Reality: A Beginner's Guide to the SDAccel to OpenCL Migration 


This document unveils the pioneering journey of porting a complex engineering project from one hardware platform, Xilinx SDAccel, to another, Intel-Altera OpenCL. Spearheaded by the visionary engineer Sakinder Ali in 2017, this initiative's ultimate goal was to transcend the limitations of a single-vendor solution and establish a 'repeatable cross-vendor workflow' for future high-performance computing tasks.
What is an FPGA? A Simple Analogy
An FPGA, or Field-Programmable Gate Array, is a specialized type of microchip used for "hardware acceleration"—making software run exceptionally fast by providing it with a dedicated, custom-built hardware circuit. Unlike a standard processor that is fixed in its design, an FPGA is like a digital LEGO set. An engineer can write code (using a language like OpenCL) and use a compiler to transform it into a hardware executable (.aocx file) that physically reconfigures the chip's internal logic. This creates a specialized hardware circuit perfectly tailored to a specific task, from airborne image processing to high-speed data analysis.
In this project, harnessing the power of these reconfigurable chips required a methodical, four-phase approach to ensure success.

The Four Phases of the Project
The project was meticulously broken down into four logical phases, with some overlap reflecting the iterative nature of research and development. It moved methodically from initial planning and hardware setup to prototyping and final cross-platform migration, ensuring every step was carefully considered and executed.

Phase 1: Preparation - Laying the Groundwork
	
Dates	May 13 – May 16, 2017
Primary Goal	Define the project's scope, create a technical roadmap, and establish success criteria for hardware acceleration.
Key Deliverable	A resource wiki and a detailed roadmap document.
This initial phase was critical for establishing a solid foundation for the entire project. Before any hardware was powered on, this stage involved defining clear goals, researching the interoperability between the two competing platforms, and creating a detailed plan. This roadmap ensured that the engineering work remained focused and that the outcome could be measured against the original success metrics.

Phase 2: Board Bring-Up - Powering On the Hardware
	
Dates	May 16 – May 19, 2017
Primary Goal	Initialize the Xilinx KU115 hardware and verify that the host computer can communicate correctly with the FPGA board.
Key Deliverable	A version-controlled repository with verified code proving the hardware was functional.
The "bring-up" phase is a fundamental step in any hardware project. The core achievement here was successfully powering on the Xilinx KU115 FPGA board and confirming that the basic communication pathways between the central computer (the host) and the FPGA (the device) were working. This validated that the hardware was ready for the custom code that would be developed in the next phase.

Phase 3: SDAccel Implementation - Building the Prototype
	
Dates	May 12 – May 20, 2017
Primary Goal	Develop, optimize, and validate computational kernels on the Xilinx SDAccel platform to create a functional prototype and assess performance scaling.
Key Deliverable	A working FPGA acceleration prototype with baseline performance data.
In this phase, the theoretical design became a tangible reality. The computational kernels—the core pieces of code designed for hardware acceleration—were developed and tested on the Xilinx platform. The result was a functional prototype that served as a baseline, or benchmark, for performance. This working model proved the design was sound and set the performance standard that the final ported version would have to meet or exceed.

Phase 4: The OpenCL Port - Crossing the Bridge
	
Dates	July – November 2017
Primary Goal	Working prototype platform for the Intel-Altera OpenCL environment.
Key Deliverable	A fully functional and verified OpenCL implementation on Intel-Altera hardware.
This final and longest phase represented the core of a consulting engagement Sakinder undertook at Fast Fit Technologies. It involved a series of meticulous steps: installing and configuring a completely new Intel-Altera toolchain, using its Offline Compiler to generate the hardware executable files (.aocx) mentioned earlier, adapting the computational kernels and host interfaces to run on the new hardware, and performing extensive debugging. The phase culminated in successfully porting the code to the Intel FPGA and validating that its performance was equivalent to that of the original Xilinx prototype, proving the design was truly portable.
These four phases logically built upon one another, starting with a blueprint, moving to a functional prototype on one platform, and culminating in a successful migration to a second, competing platform.

Conclusion: A Repeatable Workflow for the Future

Ultimately, Sakinder Ali successfully created a functional SDAccel prototype on a Xilinx board and ported it to the Intel-Altera OpenCL platform, achieving performance parity between the two. But the project delivered more than just a single working solution.
The most important achievement was establishing a documented, repeatable engineering workflow for future multi-vendor FPGA-acceleration projects. This means that future engineers can now follow a proven methodology to move hardware-accelerated code between competing ecosystems, enabling greater flexibility and preventing lock-in to a single hardware vendor.

