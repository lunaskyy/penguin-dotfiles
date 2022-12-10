# Surface Laptop 4 - AMD

### BIOS Modifications
- Secure Boot - **Disabled**
- Enable IPv6 for PXE Network Boot Option - **Disabled** (unrelated to linux)

### Workarounds Required!
Due to issues with the amdgpu module with IOMMU enabled in passthrough mode, it will need to be disabled to boot. You can do this by setting `amd_iommu=off iommu=off`. There are reports of getting it to work with `amd_iommu=force_isolation`, however this is unconfirmed and may introduce stability issues. You can read more about it [here](https://github.com/linux-surface/linux-surface/wiki/Surface-Laptop-4#screen-freezes-with-corruption-on-boot).