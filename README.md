# TI_AES_128_CSharp
C# implementation of Texas Instruments (TI) AES 128 bit library (http://www.ti.com/tool/AES-128)

There are two files in this repository. One of them is the original implementation of AES 128 bit ECB in C programming language. Other file is the C# implementation to be used with any C# projects.

For details on usage of the C library please refer to the original documentation provided by Texas Instruments http://www.ti.com/lit/an/slaa397a/slaa397a.pdf

C# file has two main function:
1) void aes_enc_dec(ref byte[] state, ref byte[] key, bool dir)
        This takes in the bytes that need to be encrypted (state), key to be used for encryption in byte format and direction to specify           encryption or decryption. Note that state and key are passed by reference and they will change after the operation is completed.           Set dir to false for encryption and true for decryption.
        state will be the result of encryption.
  
2)  byte[] aes_enc_dec(byte[] stateIN, byte[] keyIN, bool dir)
        This takes in the bytes that need to be encrypted (state), key to be used for encryption in byte format and direction to specify           encryption or decryption. 
        Set dir to false for encryption and true for decryption.
        This function will return byte array containing the result of encryption.
