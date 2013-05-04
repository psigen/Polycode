Additional notes on compiling everything:    

  168  sudo apt-get install libsdl1.2-dev 
  175  sudo apt-get install python-ply

  181  sudo rm /usr/lib/x86_64-linux-gnu/libGL.so 
  182  sudo ln -s /usr/lib/libGL.so.1 /usr/lib/x86_64-linux-gnu/libGL.so 

  157  mkdir -p Build/Debug
  158  cd Build/Debug/
  173  cmake -G "Unix Makefiles" -DCMAKE_BUILD_TYPE=Debug -DPOLYCODE_BUILD_BINDINGS=ON -DPOLYCODE_BUILD_PLAYER=ON ../..
  177  make; make PolycodeLua; make install
  178  cd ../..

  183  mkdir -p Build/Release
  184  cd Build/Release/
  185  cmake -G "Unix Makefiles" -DCMAKE_BUILD_TYPE=Release -DPOLYCODE_BUILD_BINDINGS=ON -DPOLYCODE_BUILD_PLAYER=ON ../..
  186  make; make PolycodeLua; make install
  189  cd ../..

