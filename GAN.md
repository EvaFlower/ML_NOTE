
## Network Structure
if the loss is binary cross entropy, then structure is like:  
Discriminator:  

|  			Layer 		                    |  			Kernel 		    |  			Output 		   |
|----------------------------|-------------|------------|
|  			X 		                        |  			- 		         |  			3*32*32 		  |
|  			Conv, LeakyReLU(0.2) 		     |  			[4, 2, 1] 		 |  			64*16*16 		 |
|  			Conv, BN, LeakyReLU(0.2) 		 |  			[4, 2, 1] 		 |  			128*8*8 		  |
|  			Conv, BN, LeakyReLU(0.2) 		 |  			[4, 2, 1] 		 |  			256*4*4 		  |
|  			Conv 		                     |  			[4, 1, 0] 		 |  			1*1*1 		    |
|  			CrossEntropyWithLogits 		   |  			  			 		        |  			1 		        |

Generator:  
|  			Layer 		                   |  			Kernel 		    |  			Output 		   |
|---------------------------|-------------|------------|
|  			Z 		                       |  			- 		         |  			128*1*1 		  |
|  			ConvTranspose, BN, ReLU 		 |  			[4, 1, 0] 		 |  			256*4*4 		  |
|  			ConvTranspose, BN, ReLU 		 |  			[4, 2, 1] 		 |  			128*8*8 		  |
|  			ConvTranspose, BN, ReLU 		 |  			[4, 2, 1] 		 |  			64*16*16 		 |
|  			ConvTranspose, Tanh 		     |  			[4, 2, 1] 		 |  			3*32*32 		  |
  
if the loss is wasserstainer distance, then structure is:  
Discriminator:  
|  			Layer 		                    |  			Kernel 		    |  			Output 		   |
|----------------------------|-------------|------------|
|  			X 		                        |  			- 		         |  			3*32*32 		  |
|  			Conv, LeakyReLU(0.2) 		     |  			[4, 2, 1] 		 |  			64*16*16 		 |
|  			Conv, LeakyReLU(0.2) 		 |  			[4, 2, 1] 		 |  			128*8*8 		  |
|  			Conv, LeakyReLU(0.2) 		 |  			[4, 2, 1] 		 |  			256*4*4 		  |
|  			Conv 		                     |  			[4, 1, 0] 		 |  			1*1*1 		    |
|  			CrossEntropyWithLogits 		   |  			  			 		        |  			1 		        |

Generator:  
|  			Layer 		                   |  			Kernel 		    |  			Output 		   |
|---------------------------|-------------|------------|
|  			Z 		                       |  			- 		         |  			128*1*1 		  |
|  			ConvTranspose, BN, ReLU 		 |  			[4, 1, 0] 		 |  			256*4*4 		  |
|  			ConvTranspose, BN, ReLU 		 |  			[4, 2, 1] 		 |  			128*8*8 		  |
|  			ConvTranspose, BN, ReLU 		 |  			[4, 2, 1] 		 |  			64*16*16 		 |
|  			ConvTranspose, Tanh 		     |  			[4, 2, 1] 		 |  			3*32*32 		  |
  
