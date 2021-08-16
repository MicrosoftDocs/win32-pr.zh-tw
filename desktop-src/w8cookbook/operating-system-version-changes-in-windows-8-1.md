---
title: Windows 8.1 和 Windows Server 2012 R2 中的作業系統版本變更
description: Windows 8.1 和 Windows Server 2012 R2 中的作業系統版本變更
ms.assetid: 3040262A-85EB-4F26-BE34-D2BBD5886E9E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e1fe0972a915d0f13ca3c3f8f52e5dd0559ad9c24e1afd2dd005f4a733373c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882688"
---
# <a name="operating-system-version-changes-in-windows-81-and-windows-server-2012-r2"></a>Windows 8.1 和 Windows Server 2012 R2 中的作業系統版本變更

## <a name="platforms"></a>平台

**用戶端-** Windows 8。1

**伺服器-** Windows Server 2012 R2

## <a name="description"></a>Description

我們對 getversion (的) api 在 Windows 8.1 中的運作方式有所重大變更，是因為在過去的 getversion (範例) api 的使用方式所造成的不良客戶行為。

在舊版 Windows 中，呼叫 GetVersion (例如) api 會傳回作業系統 (作業系統的實際版本) ，除非應用程式相容性填充碼已減輕進程，以提供不同的版本。 這是以暫時性的方式完成，而且相對於 Microsoft 在版本中可合理填充碼的進程數目。 許多應用程式會因為版本檢查的設計不佳而無法填充，所以會有許多應用程式被破解。

進行版本檢查的其中一個原因是要警告使用者應用程式必須在較新版本的 OS 上執行。 不過，因為檢查不佳，應用程式通常會不正確地警告它們必須在 Windows XP 或更新版本上執行，這當然是最新的作業系統。 比起，最新的 OS 會在沒有任何問題的情況下執行應用程式（如果沒有這些檢查的話）。

## <a name="manifestation"></a>表現

在 Windows 8.1 中，GetVersion (例如) api 已被取代。 這表示，雖然您仍可呼叫這些 API 函式，但如果您的應用程式並未特別以 Windows 8.1 為目標，則函式會傳回 Windows 8 版本 (6.2) 。

## <a name="solution"></a>解決方案

### <a name="adding-an-app-manifest"></a>新增應用程式資訊清單

為了讓您的應用程式以 Windows 8.1 為目標，您必須在應用程式的可執行檔[) 資訊清單中包含應用程式 (可執行檔](/windows/compatibility/application-executable-manifest)。 然後，在資訊清單的 [ [ **&lt; 相容性 &gt;** ] 區段](../SbsCs/application-manifests.md#compatibility)中，您必須為您想要宣告應用程式支援的每個 Windows 版本新增 **&lt; supportedOS &gt;** 元素。

下列範例會顯示應用程式的應用程式資訊清單檔，以支援從 Windows Vista 到 Windows 8.1 的所有 Windows 版本：

```XML
<!-- example.exe.manifest -->
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly manifestVersion="1.0" xmlns="urn:schemas-microsoft-com:asm.v1" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
    <assemblyIdentity
        type="win32"
        name="Contoso.ExampleApplication.ExampleBinary"
        version="1.2.3.4"
        processorArchitecture="x86"
    />
    <description>Contoso Example Application</description>
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1">
        <application>
            <!-- Windows 8.1 -->
            <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/> <!-- * ADD THIS LINE * -->
            <!-- Windows 8 -->
            <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
            <!-- Windows 7 -->
            <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
            <!-- Windows Vista -->
            <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        </application>
    </compatibility>
</assembly>
```

上方標示的 `* ADD THIS LINE *` 程式碼顯示如何正確地以應用程式為目標，以進行 Windows 8.1。

在舊版作業系統上執行您的應用程式時，在您的應用程式資訊清單中宣告 Windows 8.1 的支援將不會有任何作用。

### <a name="using-versionhelpers-instead-of-getversionex"></a>使用 VersionHelpers 而非 GetVersion (例如) 

Windows 8.1 引進適用于 GetVersion 的新取代 API 函數 (例如) ，稱為 VersionHelpers。 它們非常容易使用;您只需要這麼做 `#include <VersionHelpers.h>` 。 VersionHelpers .h 標頭檔中提供的內嵌函式可讓您的程式碼詢問作業系統是否為指定版本的 Windows 或更新版本。

**範例** 例如，如果您的應用程式需要 Windows 8 或更新版本，請使用下列測試：

```cpp
#include <VersionHelpers.h>
// ...
    if (!IsWindows8OrGreater())
    {
       MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
    }
```

可用的 VersionHelper API 函數包括：

```c
#define VERSIONHELPERAPI FORCEINLINE BOOL
VERSIONHELPERAPI IsWindowsXPOrGreater();
VERSIONHELPERAPI IsWindowsXPSP1OrGreater();
VERSIONHELPERAPI IsWindowsXPSP2OrGreater();
VERSIONHELPERAPI IsWindowsXPSP3OrGreater();
VERSIONHELPERAPI IsWindowsVistaOrGreater();
VERSIONHELPERAPI IsWindowsVistaSP1OrGreater();
VERSIONHELPERAPI IsWindowsVistaSP2OrGreater();
VERSIONHELPERAPI IsWindows7OrGreater();
VERSIONHELPERAPI IsWindows7SP1OrGreater();
VERSIONHELPERAPI IsWindows8OrGreater();
VERSIONHELPERAPI IsWindows8Point1OrGreater();
VERSIONHELPERAPI IsWindowsServer();
```

根據您提出的問題，這些值會傳回 TRUE 或 FALSE，而您只需要定義所支援的最低層級作業系統。

## <a name="resources"></a>資源

-   [應用程式相容性工具組下載](https://www.microsoft.com/downloads/details.aspx?FamilyId=24DA89E9-B581-47B0-B45E-492DD6DA2971)
-   [已知的相容性修正程式、相容性模式和 AppHelp 訊息](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))
-   [VersionHelpers Api](../sysinfo/version-helper-apis.md)