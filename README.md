# 💻 Hackintosh EFI - Intel i5-10210U + Broadcom Wi-Fi/Bluetooth

Configuração testada e validada com sucesso em notebook com as seguintes especificações:

## 🧬 Especificações do Hardware

| Componente             | Detalhes                                |
|------------------------|------------------------------------------|
| Processador            | Intel Core i5-10210U (10ª geração)       |
| GPU integrada          | Intel UHD Graphics (iGPU)                |
| Tela                  | 15.6" Full HD IPS LCD                    |
| Memória RAM           | 12GB DDR4 SDRAM                           |
| Wi-Fi / Bluetooth     | Broadcom nativa                          |
| Touchpad              | Funcional                                |
| HDMI                  | Funcional                                |
| Áudio                 | ALC255            |

---

## ✅ Funcionalidades Testadas

| Funcionalidade       | Status | Observações |
|----------------------|--------|-------------|
| Vídeo (iGPU)         | ✔️      | `WhateverGreen.kext` + `AAPL,ig-platform-id` compatível |
| HDMI                 | ✔️      | Funciona 100% via `WhateverGreen` |
| Wi-Fi (Broadcom)     | ✔️      | Nativo, sem necessidade de kexts adicionais |
| Bluetooth (Broadcom) | ✔️      | Nativo, sem kexts — requer mapeamento de porta USB correta |
| Touchpad             | ✔️      | Suporte via `VoodooI2C.kext` ou `VoodooPS2.kext` |
| Sleep/Wake           | ✔️       |  ajustes finos de ACPI |
| Áudio                | ✔️       | Alc 255
---

## 🔧 Considerações Especiais

- ✅ **Wi-Fi & Bluetooth:** Broadcom 100% nativa, sem uso de `itlwm` ou `IntelBluetoothFirmware`.
- 🔌 **Mapeamento USB:** Necessário mapear as portas corretamente com `USBMap.kext` ou similar.
---

## 🗂️ Kexts Utilizados

- AMFIPass.kext
- AppleALC.kext
- BrightnessKeys.kext
- CPUFriend.kext
- CPUFriendDataProvider.kext
- CputscSync.kext
- ECEnabler.kext
- Hibernation Fixup.kext
- IntelMausi.kext
- 1080211FamilyLegacy.kext
- IOSkywalkFamily.kext
- Lilu.kext
- NVMeFix.kext
- RealtekRTL8111.kext
- RestrictEvents.kext
- SMCBatteryManager.kext SMCLightSensor.kext
- SMCProcessor.kext
- USBMap.kext
- VirtualSMC.kext
- Voodool2C.kext
- Voodool2CHID.kext
- VoodooPS2Controller.kext
- WhateverGreen.kext
- XHCI-unsupported.kext
---

## 📘 Notas Finais

- Certifique-se de usar a versão correta do `AirportItlwm.kext` caso mude para Intel Wi-Fi.
- Use `ProperTree` com o `OC Snapshot` sempre que atualizar kexts ou drivers.
- Verifique com o `Hackintool` as portas USB e o codec de áudio correto.
- O `config.plist` precisa conter o SMBIOS correto (MacBookPro16,2 por exemplo).

---

🚀 **Desenvolvido por Emerson 
