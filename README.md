# clean-rename
recursive replacing special chars in UNIX-filesystem with most similar alphanumerics

	Špêçïål ©harš in filesÿsteμ/$ù¢κš.e×t -> Special_chars_in_filesystem/Sucks.ext

# demo	

create testfiles

	~/othmar52/clean-rename $ mkdir /tmp/clean-rename-demo
	~/othmar52/clean-rename $ mkdir "/tmp/clean-rename-demo/Špêçïål ©harš in filesÿsteμ"
	~/othmar52/clean-rename $ touch "/tmp/clean-rename-demo/Špêçïål ©harš in filesÿsteμ/$ù¢κš.e×t"
	
run clean-rename

	~/othmar52/clean-rename $ ./clean-rename /tmp/clean-rename-demo
	/tmp/clean-rename-demo/Špêçïål ©harš in filesÿsteμ/$ù¢κš.e×t ---> /tmp/clean-rename-demo/Špêçïål ©harš in filesÿsteμ/Sucks.ext
	/tmp/clean-rename-demo/Špêçïål ©harš in filesÿsteμ ---> /tmp/clean-rename-demo/Special_chars_in_filesystem
	0 errors
	
show result

	~/othmar52/clean-rename $ find /tmp/clean-rename-demo -type f
	/tmp/clean-rename-demo/Special_chars_in_filesystem/Sucks.ext
	
