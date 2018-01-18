
Xcode obfuscator-llvm plugin
==================



> Obfuscator-LLVM is a project initiated in June 2010 by the information security group of the University of Applied Sciences and Arts Western Switzerland of Yverdon-les-Bains (HEIG-VD).

>The aim of this project is to provide an open-source fork of the LLVM compilation suite able to provide increased software security through code obfuscation and tamper-proofing. As we currently mostly work at the Intermediate Representation (IR) level, our tool is compatible with all programming languages (C, C++, Objective-C, Ada and Fortran) and target platforms (x86, x86-64, PowerPC, PowerPC-64, ARM, Thumb, SPARC, Alpha, CellSPU, MIPS, MSP430, SystemZ, and XCore) currently supported by LLVM.
		
		
Xcode ollvm 插件，安装前请修改下面的clang路径为你自己的ollvm clang路径。
	
		
		BuiltinJambaseRuleName = ProcessC;
		ExecPath = "/Users/obaby/Soft/obfuscator/build/bin/clang";
		
修改完成后将整个Obfuscator.xcplugin 复制到 /Applications/Xcode.app/Contents/PlugIns/Xcode3Core.ideplugin/Contents/SharedSupport/Developer/Library/Xcode/Plug-ins/ 目录下然后重启Xcode即可。

如果出现clang-4.0: error: cannot specify -o when generating multiple output files

禁用Enable Indexing while building即可

已知问题，xcode9.2 无法编译iOS项目。目前还没找到解决方案

更多信息： [http://www.h4ck.org.cn/2018/01/xcode-9-2-集成obfuscator-llvm/]( http://www.h4ck.org.cn/2018/01/xcode-9-2-集成obfuscator-llvm/)
