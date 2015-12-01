# Run the entire production process from cleaning to building

MAKE=make

all: clean build show

build:
	@for a in $$(ls); do \
      	  if [ -d $$a ]; then \
	    $(MAKE) -C $$a build; \
	  fi; \
	done;

show:
	@for a in $$(ls); do \
	  if [ -d $$a ]; then \
	    $(MAKE) -C $$a show; \
	  fi; \
	done;

clean:
	@for a in $$(ls); do \
	  if [ -d $$a ]; then \
	    $(MAKE) -C $$a clean; \
	  fi; \
	done;

.PHONY: clean show
