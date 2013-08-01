name=icsmod-storecollector
all:
	mkdir -p ~/gems_build
	ruby-env ruby1.9.3 bundle install --path ~/gems_build --local || ruby-env ruby1.9.3 bundle install --path ~/gems_build
	ruby-env ruby1.9.3 bundle pack
	#ruby-env ruby1.9.3 bundle install --local --path vendor/bundle
clean:
	
install:	
	mkdir -p $(DESTDIR)/usr/lib/ruby/ics/$(name)
	mkdir -p $(DESTDIR)/usr/local/libdata/ICSGrapery/modules
	mkdir -p $(DESTDIR)/etc/ics/
	cp ./$(name) $(DESTDIR)/usr/local/libdata/ICSGrapery/modules
	cp -a ./vendor $(DESTDIR)/usr/lib/ruby/ics/$(name)
	cp -a ./Gemfile $(DESTDIR)/usr/lib/ruby/ics/$(name)
	cp -a ./etc/* $(DESTDIR)/etc/ics/
	#cp -a ./Gemfile.lock $(DESTDIR)/usr/lib/ruby/ics/$(name)
copy:
	cp -a ./$(name) $(DESTDIR)/
	cp -a ./Gemfile $(DESTDIR)/Gemfile
	mkdir -p $(DESTDIR)/etc
	cp -a ./etc $(DESTDIR)
	#cp -a ./Gemfile.lock $(DESTDIR)/Gemfile.lock