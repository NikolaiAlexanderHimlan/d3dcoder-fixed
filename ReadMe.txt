As the examples from d3dcoder.net all come broken, please upload fixed versions here.

Identified problems:

*Project Properties: 

VC++ Directories: 
Include Directories should be - 
C:\Program Files %28x86%29\Microsoft DirectX SDK %28June 2010%29\Include;$(IncludePath)

Library Directories should be - 
C:\Program Files %28x86%29\Microsoft DirectX SDK %28June 2010%29\Lib\x86;$(LibraryPath)

Linker->Input: 
in Additional Dependancies, you need to change 
DxErr9.lib to DxErr.lib


*include for #include <dxerr9.h> to <dxerr.h>


*Around line 90 in d3dUtil.h, you will need to comment out out 
//const float INFINITY = FLT_MAX;

