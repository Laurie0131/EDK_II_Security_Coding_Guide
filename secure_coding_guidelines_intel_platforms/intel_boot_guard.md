### Intel® Boot Guard {#intel-boot-guard}

**#BootGuard.1**: A full secure/verified boot flow MUST include Intel® Boot Guard, OEM Boot Block (OBB) Verification.

**#BootGuard.2**: Intel® Boot Guard SHOULD be used to verify the Initial Boot Block (IBB).

**#BootGuard.3**: If Intel® Boot Guard is used, all IBB portion MUST be signed.

**#BootGuard.4**: If Intel® Boot Guard is used, the verification MUST happen in all boot path, including normal, S3, S4, capsule update, recovery.

**#BootGuard.5**: After the memory is initialized, the code in the IBB flash region MUST not be invoked. Only the memory copy MAY be invoked, including PSI service, PPI, and a callback function.

**#BootGuard.6**: After the memory is initialized, the data in the IBB flash region MUST not be referred. Only the memory copy MAY be referred, including HOB, global data in PPI, system state, GDT, IDT, Firmware Information Table (FIT), Boot Policy Manifest (BPM), Key Manifest (KM), etc.

**#BootGuard.7**: Once Intel® Boot Guard is enabled, there MUST be no way to disable it.

**#ObbVereification.1**: The IBB MUST be used to verify the OEM Boot Block (OBB).

**#ObbVereification.2**: Any OBB Firmware Volume images MUST be signed.

**#ObbVereification.3**: The verification MUST occur for the OBB code in memory.