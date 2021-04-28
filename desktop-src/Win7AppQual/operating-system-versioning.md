---
description: 作業系統版本控制
ms.assetid: 974650d9-504a-4f19-bc71-90fbc92672d9
title: 作業系統版本控制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b2b8c60994eaee7a3becfa9acc03fe2c61fb12
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088036"
---
# <a name="operating-system-versioning"></a>作業系統版本控制

## <a name="affected-platforms"></a>受影響的平臺

**客戶** 端-Windows 7  
**伺服器** -Windows Server 2008 R2  









## <a name="feature-impact"></a>功能影響

**嚴重性** -高  
**頻率** -高  









## <a name="description"></a>Description

Windows 7 和 Windows Server 2008 R2 的內部版本號碼是6.1。 在查詢時，GetVersion 函式現在會將此版本號碼傳回給應用程式。 這對防毒軟體、備份、公用程式和禁止複製來說特別重要。

## <a name="manifestation-of-impact"></a>影響的表現

這項變更的表現是應用程式特定的。 這表示，任何特別檢查作業系統版本的應用程式都會取得較高的版本號碼，而這可能會導致下列一或多個情況：

-   應用程式安裝程式可能無法安裝應用程式，且應用程式可能無法啟動
-   應用程式可能會變得不穩定或損毀
-   應用程式可能會產生錯誤訊息，但會繼續正常運作

## <a name="mitigation"></a>降低

大部分的應用程式在 Windows 7 和 Windows Server 2008 R2 上都能正常運作，因為 Windows 7 和 Windows Server 2008 R2 中的應用程式相容性很高。 不過，Windows 7 和 Windows Server 2008 R2 包含檢查作業系統版本之安裝程式和應用程式的相容性檢視。

若要啟用相容性檢視，使用者可以用滑鼠右鍵按一下快捷方式或可執行檔，然後從 [相容性] 索引標籤套用 Windows XP SP2 或 Windows Vista 相容性檢視。在大多數情況下，這應該可讓應用程式正常運作，而不需要對應用程式進行任何變更。

IT 專業人員也可以套用任何適用的 VersionLie 相容性修正程式，其方式是使用與應用程式相容性工具組一起安裝的相容性系統管理員工具 (ACT) 。 例如，如果應用程式無法運作，因為它正在檢查（但找不到） Windows XP® Service Pack 2 (SP2) 版本資訊，WinXPSP2VersionLie 可以套用至應用程式，以將適當的版本號碼資訊傳回給應用程式，而不論電腦上執行的實際作業系統版本為何。 可用的 VersionLie 相容性修正如下：

-   Win95VersionLie
-   Win98VersionLie
-   WinNT4SP5VersionLie
-   Win2000VersionLie
-   Win2000SP1VersionLie
-   Win2000SP2VersionLie
-   Win2000SP3VersionLie
-   WinXPVersionLie
-   WinXPSP1VersionLie
-   WinXPSP2VersionLie
-   VistaRTMVersionLie
-   VistaSP1VersionLie
-   VistaSP2VersionLie
-   Win2K3RTMVersionLie
-   Win2K3SP1VersionLie

## <a name="solution"></a>解決方法

一般來說，應用程式不應該執行作業系統版本檢查。 如果應用程式需要特定功能，最好先嘗試尋找該功能，而且只有在遺漏所需的功能時才會失敗。 應用程式至少應接受大於或等於最低支援作業系統版本的版本號碼。 只有在有特定的法律、企業或系統元件需求時，才會發生例外狀況。

## <a name="links-to-other-resources"></a>其他資源的連結

-   [應用程式相容性工具組下載](/windows-hardware/get-started/adk-install)
-   [已知的相容性修正程式、相容性模式和 AppHelp 訊息](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))

 

 
