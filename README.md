# AI Generated Response


The contents of sboot.bin  (Samsung Exynos 2100 bootloader image from `BL_G990EXXUIHYJ2`) have been analyzed, unpacked, and extracted into the directory [`/home/sc0/Projects/extractor/sboot_extracted/`](file:///home/sc0/Projects/extractor/sboot_extracted/).

The extraction script [`extract_sboot.py`](file:///home/sc0/Projects/extractor/extract_sboot.py) and a detailed manifest [`manifest.json`](file:///home/sc0/Projects/extractor/sboot_extracted/manifest.json) have also been generated.

---

### Image Overview & Cryptographic Verification

* **Device / Hardware:** Samsung Galaxy S21 FE (`SM-G990E`), Board HW: `EVT01`, Platform: Samsung Exynos 2100 (`EXYNOS2100`)
* **Firmware Version:** `G990EXXUIHYJ2` (`SM-G990E_SEA_XME_EKEY0`), Build Date: `2025-10-10 19:40:54`
* **Total Image Size:** `4,194,304` bytes (4.00 MiB)
* **AVB Verified Bootloader Payload:** `3,994,416` bytes (`0x3cf330`)
  * **AVB Salt:** `9d800566dd739da8ff42d7bd33a79ca463b1b99f044ccc6fc51e033ddb26a8b2`
  * **AVB SHA256 Digest:** `26cd08a973e219a29b31cd4e7edca3296c15c79f99eb4599c98989349ed25d70`
  * **Integrity Status:** **Verified Match** (identical to descriptor #11 in [`vbmeta.img`](file:///home/sc0/Projects/extractor/BL_G990EXXUIHYJ2_G990EXXUIHYJ2_MQB102219315_REV01_user_low_ship_MULTI_CERT/vbmeta.img) and the internal AVB block).

---

### Extracted Components

All extracted files are located in [`/home/sc0/Projects/extractor/sboot_extracted/`](file:///home/sc0/Projects/extractor/sboot_extracted/):

| File | Offset Range | Size | Description |
| :--- | :--- | :--- | :--- |
| [`01_epbl.bin`](file:///home/sc0/Projects/extractor/sboot_extracted/01_epbl.bin) | `0x000000` - `0x002bc0` | 11.0 KB | **Early Primary Boot Loader (EPBL)**: Initial SoC reset vectors, UART status output, and Samsung LSI header (`SLSI`) with RSA signature block (`0x26e0`). |
| [`02_dram_init.bin`](file:///home/sc0/Projects/extractor/sboot_extracted/02_dram_init.bin) | `0x002bc0` - `0x016000` | 77.1 KB | **DRAM Configuration & Calibration**: Memory parameters (`daeh` header), clock gating, and signed calibration tables (`0x15df0`). |
| [`03_bl2.bin`](file:///home/sc0/Projects/extractor/sboot_extracted/03_bl2.bin) | `0x016000` - `0x08c000` | 472 KB | **Secondary Boot Loader (BL2)**: Runtime Exynos 2100 hardware setup, DMC/DVFS/PLL controller init, UFS storage bring-up, and secure boot validation (`0x8bdf0`). |
| [`04_device_tree.dtb`](file:///home/sc0/Projects/extractor/sboot_extracted/04_device_tree.dtb) | `0x0ea000` - `0x0eaa84` | 2.7 KB | **Device Tree Blob (DTB)**: Standard Flattened Device Tree overlay defining DPM, memory logger policies, and debug history crash dumping. |
| [`04_device_tree.dts`](file:///home/sc0/Projects/extractor/sboot_extracted/04_device_tree.dts) | *Decompiled* | 2.6 KB | **Decompiled Device Tree Source (DTS)**: Human-readable device tree source overlay decompiled using `dtc`. |
| [`05_main_sboot.bin`](file:///home/sc0/Projects/extractor/sboot_extracted/05_main_sboot.bin) | `0x0ec000` - `0x38edf0` | 2.64 MB | **Main SBOOT Bootloader OS**: Core Little Kernel (LK) OS implementing Odin download mode, PIT (Partition Information Table) parsing, AVB 2.0 verification runtime, display/USB drivers, and keystorage (`0x38edf0`). |
| [`06_athens_coproc_fw.bin`](file:///home/sc0/Projects/extractor/sboot_extracted/06_athens_coproc_fw.bin) | `0x38f000` - `0x3cedf0` | 255.5 KB | **Athens Coprocessor Firmware**: Co-processor firmware stage `v1.5(release):Athens-RP1A-1A19R1-1-gbfac7c7 Built : Sep 3 2024` with signature block (`0x3cedf0`). |
| [`07_samsung_signer_footer.bin`](file:///home/sc0/Projects/extractor/sboot_extracted/07_samsung_signer_footer.bin) | `0x3cf000` - `0x3cf330` | 816 B | **Samsung SignerVer03 Metadata Block**: Board and build tracking metadata (`SM-G990E`, `EVT01`, `G990EXXUIHYJ2`) with Samsung RSA signature (`0x3cf120`). |
| [`08_bootloader_signed_payload.bin`](file:///home/sc0/Projects/extractor/sboot_extracted/08_bootloader_signed_payload.bin) | `0x000000` - `0x3cf330` | 3.81 MB | **Verified Bootloader Partition Payload**: The complete 3,994,416-byte signed bootloader partition verified by AVB. |
| [`09_avb_vbmeta.img`](file:///home/sc0/Projects/extractor/sboot_extracted/09_avb_vbmeta.img) | `0x3d0000` - `0x3d0840` | 2.06 KB | **AVB 1.1 VBMeta Block**: Android Verified Boot structure validating the `bootloader` partition. |
| [`09_avb_public_key.bin`](file:///home/sc0/Projects/extractor/sboot_extracted/09_avb_public_key.bin) | Embedded | 1,032 B | **AVB Public Key (Raw)**: 4096-bit RSA public key structure (`AvbRSAPublicKeyHeader`). |
| [`09_avb_public_key.pem`](file:///home/sc0/Projects/extractor/sboot_extracted/09_avb_public_key.pem) | *Converted* | 800 B | **AVB Public Key (PEM)**: Standard X.509 SubjectPublicKeyInfo PEM format for cryptographic verification tools. |
| [`10_avb_footer.bin`](file:///home/sc0/Projects/extractor/sboot_extracted/10_avb_footer.bin) | `0x3fffc0` - `0x400000` | 64 B | **AVB Partition Footer (`AVBf`)**: Points to original image size `0x3cf330`, VBMeta offset `0x3d0000`, and VBMeta size `0x840`. |
| [`manifest.json`](file:///home/sc0/Projects/extractor/sboot_extracted/manifest.json) | — | 3.5 KB | **Manifest File**: JSON manifest detailing hashes, sizes, and offsets. |

---

### Reproducing or Re-running the Extraction

To re-run or inspect the extraction at any time:
```bash
python3 /home/sc0/Projects/extractor/extract_sboot.py
```
