Compilation
The code is a Visual Studio 2017 project on Windows x64 platform. To build the project, you need to configure OpenCV on your own PC. (version 3.4.1, however, other versions are acceptable by modifying CommFunc.h).

Usage
Run the program with the following paramters: Usage: [CC_METHOD] [CA_METHOD] [PP_METHOD] [C_ALPHA] [lImg] [rImg] [lDis] [maxDis] [disSc]
*[CC_METHOD] -- cost computation methods，currently only support:
	* IC-- gradient+AD+iFCT
[CA_METHOD] -- cost aggregation methods
	* GF -- guided image filter
	* NL -- non-local cost aggregation
	* ST -- segment-tree cost aggregation	
[PP_METHOD] -- post processing methods，currently only support:
	* SG -- segment based 
[C_ALPHA] -- regularization paramter
[lImg] -- input left color image file name. (all formats supported by OpenCV)
[rImg] -- input right color image file name.
[lDis] -- output left disparity map file name.
[maxDis] -- maximum disparity range
[disSc] -- scale disparity

Hint: to enable post-processing, you must uncomment // #define COMPUTE_RIGHT in CommFunc.h to allow computing right disparity map.