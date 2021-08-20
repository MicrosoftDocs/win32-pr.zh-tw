---
title: 針對舊版 Windows 開發應用程式
description: 說明如何開發在舊版 Windows 上執行的應用程式，並利用適用于 Windows Vista 的平臺更新所支援的 API，以及 Windows Server 2008 的平臺更新。
ms.assetid: 9c46f894-e5cd-46a1-81c8-f63b09504735
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afbb999faf934ae621f80a824eca0289ff3df705ed11d7cfd161935c944947f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549478"
---
# <a name="developing-applications-for-previous-versions-of-windows"></a>針對舊版 Windows 開發應用程式

說明如何開發在舊版 Windows 上執行的應用程式，並利用適用于 Windows Vista 的平臺更新所支援的 API，以及 Windows Server 2008 的平臺更新。

## <a name="required-downloads"></a>必要的下載

如果您想要開發的應用程式使用 Microsoft Windows 軟體開發套件 (SDK) （適用于 Windows 7）所引進的 API，則需要下載並安裝下列各節所述的套件。

### <a name="microsoft-windows-sdk"></a>Microsoft Windows SDK

需要 Windows 7 的 Windows SDK，才能建立應用程式，該應用程式會使用 Windows Vista 的平臺更新所支援的 api，以及 Windows Server 2008 的平臺更新。

如需存取其他資源和資訊，例如下載、論壇文章和 Windows SDK team blog，請參閱[Windows SDK 開發人員中心](https://msdn.microsoft.com/bb980924.aspx) (https://msdn.microsoft.com/bb980924.aspx) 。

### <a name="net-framework"></a>.NET Framework

需要 .NET Framework 3.5 Service Pack 1，才能建立應用程式，以使用 Windows Vista 的平臺更新所支援的 api 和 Windows Server 2008 的平臺更新。

如需其他資源和資訊，請參閱[.NET Framework 開發人員中心](https://msdn.microsoft.com/netframework/default.aspx) (https://msdn.microsoft.com/netframework/default.aspx) 。

### <a name="directx-sdk-required-when-using-direct3d"></a>使用 Direct3D 時需要 DirectX SDK

如果您建立使用 Direct3D 的應用程式，則需要[DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (， https://msdn.microsoft.com/directx/aa937788.aspx) 才能建立使用平臺更新（適用于 Windows Vista）所支援之 api 的應用程式，以及 Windows Server 2008 的平臺更新。

### <a name="update-your-development-computer"></a>更新您的開發電腦

確定您的開發電腦具有來自 Windows Update 的所有最新更新。

如果您要在舊版 Windows 上開發應用程式，您必須從 Windows Update 取得 Windows Vista 的平臺更新或 Windows Server 2008 更新的平臺更新。 安裝其中一個更新可讓您利用 Windows SDK Windows 7 提供的新 API。

如需如何從 Windows Update 取得更新的詳細資訊，請參閱知識庫檔中[有關 Windows Vista (KB 971644)  (的平臺更新](https://support.microsoft.com/kb/971644) https://support.microsoft.com/kb/971644) 。

## <a name="development-environment"></a>開發環境

### <a name="set-the-build-target-to-windows-7"></a>將組建目標設定為 Windows 7

在 Windows Vista 的平臺更新中使用程式庫的所有應用程式都必須針對 Windows 7 目標平臺建立。

將 WINVER 設定為 Windows 7 目標平臺值，可讓您開發應用程式，以在執行 Windows Vista 的開發電腦上，使用適用于 Windows Vista 的平臺更新所支援的 api，或適用于 Windows Server 2008 的平臺更新。

您可以在原始程式碼中，或使用/d 選項搭配 Visual Studio 編譯器，將目標平臺設定為 Windows 7。

下列範例顯示如何在原始程式碼中設定 WINVER。


```C++
#define WINVER 0x0601
```



下列範例顯示如何使用/D 編譯器選項設定 WINVER。

``` syntax
/DWINVER=0x0601
```

## <a name="application-deployment"></a>應用程式部署

如果您使用 Windows 7 的 Windows SDK 所提供的標頭和程式庫來建立應用程式，支援的 api 將會在任何已安裝適用于 Windows Vista 或 Windows Server 2008 平臺更新的 Windows 版本上執行。

> [!Note]  
> Windows Vista 的平臺更新所支援的某些 api 的行為、效能或需求或 Windows Server 2008 的平臺更新，可能會因不同的 Windows 版本而異。 如需有關更新所支援之特定 API 的詳細資訊，請參閱[關於 Windows Vista 的平臺更新](platform-update-for-windows-vista-overview.md)。

 

### <a name="no-redistributable-components"></a>沒有可轉散發元件

您的應用程式不需要安裝可轉散發元件，例如 Dll 或其他執行時間檔案。

### <a name="requires-updated-end-user-computer"></a>需要更新的 End-User 電腦

由於 Windows Server 2008 Windows Vista 和平臺更新的平臺更新是由 Windows Update 所裝載，因此啟用自動更新的使用者很有可能已經有這些更新以及所需的 service pack。

如果使用者的電腦未安裝適用于 Windows Server 2008 Windows Vista 或平臺更新的平臺更新，而且您的應用程式需要支援這些更新的 api，則您的應用程式可能無法在使用者的電腦上執行，或在執行期間可能會發生錯誤。

為了避免使用者電腦過期所造成的問題，您想要在安裝應用程式期間，確認您的使用者電腦具有 Windows Vista 的平臺更新，或 Windows Server 2008 更新的平臺更新。 您可以使用[Windows Update Agent API](/windows/desktop/Wua_Sdk/portal-client)來檢查終端使用者的電腦是否有安裝的更新。 如果使用者尚未安裝更新，您也可以在應用程式安裝期間使用 Windows Update Agent API 來下載並安裝必要的更新。

如需示範如何使用[Windows Update 代理程式 API](/windows/desktop/Wua_Sdk/portal-client)的安裝程式範例，請參閱[DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (中[適用于遊戲開發人員的 Direct3D 11 部署](../direct3darticles/direct3d11-deployment.md) https://msdn.microsoft.com/directx/aa937788.aspx) 。

雖然適用于[遊戲開發人員的 Direct3D 11 部署](../direct3darticles/direct3d11-deployment.md)中所討論的 D3D11InstallHelper 安裝程式範例是針對使用 direct3d 11 的應用程式所撰寫，但它提供了一個很好的範例，說明如何與[Windows Update Agent API](/windows/desktop/Wua_Sdk/portal-client)互動，以起始和追蹤 Windows Update 所裝載的更新下載與安裝。 編譯此範例可能需要 Windows 7 的 Windows SDK。 如需 D3D11InstallHelper 範例的詳細資訊（包括已知問題），請參閱2009年8月的[DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/aa937788.aspx) 版本資訊。 Windows Vista 的平臺更新

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Vista 的平臺更新](platform-update-for-windows-vista-portal.md)
</dt> <dt>

**概觀**
</dt> <dt>

[關於 Windows Vista 的平臺更新](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[有關 Windows Vista (KB 971644 的平臺更新的知識庫文章) ](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 