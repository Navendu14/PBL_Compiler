# PBL_Compiler

Break into Pieces: We split the .ll file into smaller modules — one for each function.

Smart Caching: Before compiling, we check if that function’s code has changed by calculating a unique hash (like a fingerprint). If it’s the same as before, we reuse the old compiled version (the .o file).

Compile in Parallel: We compile all changed functions at the same time using multiple CPU cores, which speeds things up.

Link Everything: Finally, we combine all the compiled pieces into one final executable.
