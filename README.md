# krunker-ahnum

this.ahNum = (this.ahNum + 105) & 255;  // add 105, wrap at 255

const ahNumBytes = Buffer.from([                                                                                                                                                               
    (ahNum >> 4) & 0x0F,   // high nibble                                                                                                                                                        
    ahNum & 0x0F           // low nibble                                                                                                                                                         
  ]);



packet 1: ahNum = 105   (0 + 105)                                                                                                                                                                
packet 2: ahNum = 210   (105 + 105)                                                                                                                                                               
packet 3: ahNum = 60   (210 + 105) wrapped                                                                                                                                                               
