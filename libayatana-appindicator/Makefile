VERSION=0.5

all: libayatana-appindicator-gtk3-introspection-$(VERSION).json libayatana-appindicator-gtk3-$(VERSION).json libayatana-appindicator-gtk2-$(VERSION).json

libayatana-appindicator-gtk3-introspection-$(VERSION).json: libayatana-appindicator.json.in
	sed -e 's/@GTK_VER@/3/g' -e 's/@SUFFIX@/3/g' -e 's/@INTROSPECTION@/yes/g' $< > $@

libayatana-appindicator-gtk3-$(VERSION).json: libayatana-appindicator.json.in
	sed -e 's/@GTK_VER@/3/g' -e 's/@SUFFIX@/3/g' -e 's/@INTROSPECTION@/no/g' $< > $@

libayatana-appindicator-gtk2-$(VERSION).json: libayatana-appindicator.json.in
	sed -e 's/@GTK_VER@/2/g' -e 's/@SUFFIX@//g' -e 's/@INTROSPECTION@/no/g' $< > $@
