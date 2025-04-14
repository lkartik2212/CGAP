TAR = mcpat

.PHONY: dbg opt depend clean clean_dbg clean_opt

all: opt

dbg: $(TAR).mk obj_dbg
	@$(MAKE) TAG=dbg -C . -f $(TAR).mk

opt: $(TAR).mk obj_opt
	@$(MAKE) TAG=opt -C . -f $(TAR).mk

obj_dbg:
	mkdir -p $@

obj_opt:
	mkdir -p $@

depend:
	@$(MAKE) TAG=opt -C . -f $(TAR).mk depend

clean: 	
	rm -rf build/*.o build/mcpat build/Makefile.makedepend.bak
