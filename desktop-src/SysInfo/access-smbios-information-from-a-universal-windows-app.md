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
# <a name="access-smbios-information-from-a-universal-windows-app"></a><span data-ttu-id="b1c4b-103">從通用 Windows 應用程式存取 SMBIOS 資訊</span><span class="sxs-lookup"><span data-stu-id="b1c4b-103">Access SMBIOS information from a Universal Windows App</span></span>

> <span data-ttu-id="b1c4b-104">記某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="b1c4b-104">[NOTE] Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b1c4b-105">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。</span><span class="sxs-lookup"><span data-stu-id="b1c4b-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="b1c4b-106">如何從通用 Windows 應用程式存取系統管理 BIOS (SMBIOS) 資訊。</span><span class="sxs-lookup"><span data-stu-id="b1c4b-106">How to access System Management BIOS (SMBIOS) information from a Universal Windows app.</span></span>

## <a name="access-smbios-information-from-a-universal-windows-platform-app"></a><span data-ttu-id="b1c4b-107">從通用 Windows 平臺應用程式存取 SMBIOS 資訊</span><span class="sxs-lookup"><span data-stu-id="b1c4b-107">Access SMBIOS information from a Universal Windows Platform App</span></span>

<span data-ttu-id="b1c4b-108">從 Windows 10 開始，1803版的通用 Windows 應用程式可以使用 [GetSystemFirmwareTable](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable) 和 [EnumSystemFirmwareTables](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables) ，藉由在應用程式資訊清單中宣告 **SMBIOS** 限制功能來存取 SMBIOS 資訊。</span><span class="sxs-lookup"><span data-stu-id="b1c4b-108">Starting with Windows 10, version 1803, Universal Windows apps can use [GetSystemFirmwareTable](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable) and [EnumSystemFirmwareTables](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables) to access SMBIOS information by declaring the **smbios** restricted capability in the app manifest.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b1c4b-109">通用 Windows 應用程式只支援存取原始 SMBIOS (RSMB) 固件資料表。</span><span class="sxs-lookup"><span data-stu-id="b1c4b-109">Only access to raw SMBIOS (RSMB) firmware tables is supported from a Universal Windows app.</span></span> <span data-ttu-id="b1c4b-110">**存取 \_** 如果您嘗試從通用 Windows 應用程式存取其他固件資料表類型，則會傳回拒絕。</span><span class="sxs-lookup"><span data-stu-id="b1c4b-110">**ACCESS\_DENIED** will be returned if you try to access other firmware table types from a Universal Windows app.</span></span>

 

<span data-ttu-id="b1c4b-111">若要在應用程式資訊清單中宣告 **smbios** 限制功能，請新增 **rescap** 命名空間和 **smbios** 功能，如下所示：</span><span class="sxs-lookup"><span data-stu-id="b1c4b-111">To declare the **smbios** restricted capability in the app manifest, add the **rescap** namespace and **smbios** capability as follows:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="b1c4b-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="b1c4b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1c4b-113">特殊和受限制的功能</span><span class="sxs-lookup"><span data-stu-id="b1c4b-113">Special and restricted capabilities</span></span>](/windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities)
</dt> <dt>

[<span data-ttu-id="b1c4b-114">GetSystemFirmwareTable</span><span class="sxs-lookup"><span data-stu-id="b1c4b-114">GetSystemFirmwareTable</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable)
</dt> <dt>

[<span data-ttu-id="b1c4b-115">EnumSystemFirmwareTables</span><span class="sxs-lookup"><span data-stu-id="b1c4b-115">EnumSystemFirmwareTables</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables)
</dt> <dt>

[<span data-ttu-id="b1c4b-116">從通用 Windows 應用程式存取 UEFI 固件變數</span><span class="sxs-lookup"><span data-stu-id="b1c4b-116">Access UEFI firmware variables from a Universal Windows App</span></span>](access-uefi-firmware-variables-from-a-universal-windows-app.md)
</dt> </dl>

 

 
