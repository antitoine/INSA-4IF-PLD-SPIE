# Run the entire production process from cleaning to building

MAKE=make
ECHO=@echo
MKDIR=@mkdir
TOUCH=@touch
CP=@cp
RM=@rm

all: clean build show

build:
	$(MAKE) -C common/ build
	$(MAKE) -C specific/ build

show:
	$(MAKE) -C specific/ show

clean:
	$(MAKE) -C common/ clean
	$(MAKE) -C specific/ clean

mkpro:
	$(ECHO) "Making specific : ${PRO}"
	$(MKDIR) specific/${PRO}
	$(MKDIR) specific/${PRO}/figures
	$(CP) common/templates/Makefile specific/${PRO}/
	$(CP) common/templates/main.tex specific/${PRO}/
	$(ECHO) "Done !"

rmpro:
	$(ECHO) "Removing project : ${PRO}"
	$(RM) -rf specific/${PRO}
	$(ECHO) "Done !"

help:
	$(ECHO) "Available rules: "

.PHONY: mkpro clean show help
