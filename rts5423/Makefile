VENDOR=Realtek
PROJECT_NAME=RTS5423
VERSION=1.19
FIRMWARE_FILE=rts5423_hub_typec_128k_with_timeinfo_sign_crc.bin
METAINFO_FILE=rts5423.metainfo.xml

all: $(VENDOR)-$(PROJECT_NAME)-$(VERSION).cab

clean:
	rm -f *.cab *.zip *.dfu

check: $(METAINFO_FILE)
	appstream-util validate-relax $(METAINFO_FILE)

%.cab: $(FIRMWARE_FILE) $(METAINFO_FILE)
	gcab --create --nopath $@ $(FIRMWARE_FILE) $(METAINFO_FILE)
