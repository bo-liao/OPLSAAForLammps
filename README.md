# OPLSAAForLammps
根据opls序号自动批量查找对应的pair-coeff。


首先准备名为pair.data的文件，包含一系列的opls序号，如下格式：

 opls_137 
 opls_136 
 opls_239   
 opls_140  
 opls_235  
 opls_236  
 opls_135 
 opls_241  
 opls_154 
 opls_155 
 
 然后在linux下运行，bash sub-replace-paircoeff-opls.sh
 
 然后你将得到一个新的pair.data文件，并在文件中获得opls力场下对应的pair_coeffs:
 
  opls_137       CT       0.066       3.5    
  opls_136       CT       0.066       3.5    
  opls_239       N       0.17       3.25      
  opls_140       HC       0.03       2.5     
  opls_235       C       0.105       3.75     
  opls_236       O       0.21       2.96     
  opls_135       CT       0.066       3.5    
  opls_241       H       0       0     
  opls_154       OH       0.17       3.12    
  opls_155       HO       0       0    
  
  最后两列数据为epsilon(kcal/mol)和sigma(Å)
