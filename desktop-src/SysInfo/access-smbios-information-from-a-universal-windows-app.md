---
description: 如何從通用 Windows 應用程式存取系統管理 BIOS (SMBIOS) 資訊。
ms.assetid: 4D185319-C093-4B1B-A182-E845E72FEA5D
title: 從通用 Windows 應用程式存取 SMBIOS 資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76791622ad4bcba15ddd889f36a6f0feeb5e3dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513540"
---
# <a name="access-smbios-information-from-a-universal-windows-app"></a>從通用 Windows 應用程式存取 SMBIOS 資訊

> 記某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。

如何從通用 Windows 應用程式存取系統管理 BIOS (SMBIOS) 資訊。

## <a name="access-smbios-information-from-a-universal-windows-platform-app"></a>從通用 Windows 平臺應用程式存取 SMBIOS 資訊

從 Windows 10 開始，1803版的通用 Windows 應用程式可以使用 [GetSystemFirmwareTable](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable) 和 [EnumSystemFirmwareTables](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables) ，藉由在應用程式資訊清單中宣告 **SMBIOS** 限制功能來存取 SMBIOS 資訊。

> [!IMPORTANT]
> 通用 Windows 應用程式只支援存取原始 SMBIOS (RSMB) 固件資料表。 **存取 \_** 如果您嘗試從通用 Windows 應用程式存取其他固件資料表類型，則會傳回拒絕。

 

若要在應用程式資訊清單中宣告 **smbios** 限制功能，請新增 **rescap** 命名空間和 **smbios** 功能，如下所示：

``` syntax
<Package
  ...
  xmlns:rescap="http://schemas.microsoft.com/appx/manifest/foundation/windows10/restrictedcapabilities"
  IgnorableNamespaces="uap mp rescap">  
  ...
  <Capabilities>
    <rescap:Capability Name="smbios"/>
  </Capabilities>
</Package>
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[特殊和受限制的功能](/windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities)
</dt> <dt>

[GetSystemFirmwareTable](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable)
</dt> <dt>

[EnumSystemFirmwareTables](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables)
</dt> <dt>

[從通用 Windows 應用程式存取 UEFI 固件變數](access-uefi-firmware-variables-from-a-universal-windows-app.md)
</dt> </dl>

 

 
