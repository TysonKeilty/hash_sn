# Hash_sn

## C++ implementation
  
  The Boost library is needed for the compilation (https://www.boost.org/).
  
  Example on windows command line:  
  
  Compilation: g++ main.cpp hash_sn.cpp -I"include" -o hash_sn.exe  
  
  Execution:  
  C:\path> hash_sn.exe digest_message.txt  
  Reading file...  
  Digesting message...  
  Hash of digest_message.txt: 528a81a97baa7d4f4a08465852ce7369  

## Python implementation of hash_sn + empirical tests.
  
  hash_sn.py                  -> Hashing algorithm    
  hash_aux.py                 -> Auxiliary functions for hash_sn  
  hash_testing.py             -> Empirical tests on the S_n constructions (>>, <<)  
  two_block_attack_hash_sn.py -> Simulate 2-block attack for small sizes (16-bit, 24-bit etc),  
  finite_field_arithmetic.py  -> Compute inverses modulo a prime using Fermat's little theorem.  
  
  Parameters:  
  m -> String to hash  
  s -> Block size (128,256,512,1024...)  
  t -> Factorial for embedding in the symmetric group. If s=128, then t>34.  
  p -> Prime between s and t!.    

  Example:  
  \>>> import hash_sn  
  \>>> hash_sn.hash_sn('hello',128,35,2**132-347).hash()  
  'e9aad33fac20ca525bec545487db3456' 

