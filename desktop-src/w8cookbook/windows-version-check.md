---
title: Windows 版本檢查
description: 作業系統版本已隨著 Windows 10 作業系統版本而遞增。
ms.assetid: 55BB7B44-1AFD-456D-9380-38B4D26E5EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710f59313f05dac95e5953c6013108987dc9bf8ad84d7eb7d8bca67a5391996b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007878"
---
# <a name="windows-version-check"></a>Windows 版本檢查

作業系統版本已隨著 Windows 10 作業系統版本而遞增。 這表示 Windows 10 的內部版本號碼也已變更為10.0。 在過去，於 OS 版本變更之後，我們需要竭盡全力地維持應用程式與裝置相容性。 對於大部分的應用程式類別 (沒有任何核心相依性) 變更將不會對應用程式功能造成負面影響，而且現有的應用程式在 Windows 10 上將繼續正常運作。

## <a name="manifestations"></a>表現

此變更的表現是依 App 而定。 這表示任何會特別檢查 OS 版本的 app 將會取得較高的版本號碼，這可能導致下列一或多種情況：

-   App 安裝程式可能無法安裝 app，且 app 可能無法啟動。
-   App 可能會不穩定或當機。
-   App 可能會產生錯誤訊息，但會繼續正常運作。

某些 app 會執行版本檢查，並傳遞警告給使用者。 不過，有些 app 會與版本檢查緊密繫結 (於驅動程式或是核心模式中以避免偵測)。 在這些情況中，如果找到不正確的版本，app 將會失敗。 相較於版本檢查，我們建議下列其中一種方法：

-   如果 app 依存於特定的 API 功能，請確定您有將正確的 API 版本作為目標。
-   NTDDI (NT 設備磁碟機介面) 版本號碼會在 API 中的目標功能變更時遞增。 請確定您透過 APISet 或功能小組所建立的其他公開 API 偵測到變更，而且不使用版本作為某些功能或修正的 proxy。 如果有重大變更，且並未適當檢查，該變更就會變成是錯誤。
-   確定應用程式不會以奇怪的方式檢查版本，例如透過登錄、檔案版本、位移、核心模式、驅動程式或其他方式。 如果應用程式確實需要檢查版本，請使用 GetVersion Api，這應該會傳回主要、次要和組建編號。
-   如果您使用 GetVersion API 或其他版本協助程式函式（例如[VerifyVersionInfo](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa)），請記住此 API 的行為已從 Windows 8.1 開始變更。 如需詳細資訊，請參閱 [API 檔](../SysInfo/version-helper-apis.md) 。
-   如果您擁有像是反惡意程式碼或防火牆的應用程式，則應該透過 Windows 測試人員程式來完成您一般的意見反應通道。

## <a name="declaring-windows-10-compatibility-with-an-app-manifest"></a>宣告與應用程式資訊清單 Windows 10 的相容性

如果您的應用程式與 Windows 10 相容，則可在應用程式的可[執行檔) 資訊清單](/windows/compatibility/application-executable-manifest)中宣告這項事實 (可執行檔。 這會告訴系統您的應用程式瞭解 Windows 10 的系統版本號碼 10.0 (因此，GetVersion API 不會傳回舊版) ，也可讓系統關閉未宣告 Windows 10 相容性之應用程式的其他相容性行為。

若要在應用程式資訊清單中宣告 Windows 10 相容性，您必須加入資訊清單的 [ **&lt; 相容性 &gt;** 區段](../SbsCs/application-manifests.md#compatibility)（如果尚未存在），然後新增 Windows 10 的 **&lt; supportedOS &gt;** 元素，以及您想要宣告的應用程式所支援的其他每個 Windows 版本。

下列範例會顯示應用程式的應用程式資訊清單檔，以支援從 Windows Vista 到 Windows 10 的所有 Windows 版本：

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
            <!-- Windows 10 -->
            <supportedOS Id="{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}"/> <!-- * ADD THIS LINE * -->
            <!-- Windows 8.1 -->
            <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/>
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

上方標示的 `* ADD THIS LINE *` 程式碼顯示如何正確地以應用程式為目標，以進行 Windows 10。

在舊版作業系統上執行您的應用程式時，在您的應用程式資訊清單中宣告 Windows 10 的支援將不會有任何作用。

## <a name="resources"></a>資源

-   [應用程式相容性工具組下載：下載適用于 Windows 10 的 Windows ADK](https://download.microsoft.com/download/9/A/E/9AE69DD5-BA93-44E0-864E-180F5E700AB4/adk/adksetup.exe)
-   [已知的相容性修正程式、相容性模式和 AppHelp 訊息](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))
-   [版本協助程式 API](../sysinfo/version-helper-apis.md)