# krunker-ahnum

this.ahNum = (this.ahNum + 31) & 255;  // add 31, wrap at 255

const ahNumBytes = Buffer.from([                                                                                                                                                               
    (ahNum >> 4) & 0x0F,   // high nibble                                                                                                                                                        
    ahNum & 0x0F           // low nibble                                                                                                                                                         
  ]);



packet 1: ahNum = 31   (0 + 31)                                                                                                                                                                
packet 2: ahNum = 62   (31 + 31)                                                                                                                                                               
packet 3: ahNum = 93   (62 + 31) wrapped                                                                                                                                                               
