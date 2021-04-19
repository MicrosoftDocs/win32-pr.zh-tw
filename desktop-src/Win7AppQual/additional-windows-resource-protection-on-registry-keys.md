---
description: .
ms.assetid: 25d07e42-b5eb-4f72-b4b1-0ebb881644ba
title: 登錄機碼上的額外 Windows 資源保護
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb048a45324e52c9b9319f52f95b64361b95bbfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979416"
---
# <a name="additional-windows-resource-protection-on-registry-keys"></a>登錄機碼上的額外 Windows 資源保護

## <a name="platform"></a>平台

**客戶** 端-Windows 7  
**伺服器** -Windows Server 2008 R2  









## <a name="feature-impact"></a>功能影響

**嚴重性** -中  
**頻率** -低  


## <a name="description"></a>Description

額外的系統資源已在 Windows 7 中新增 Windows 資源保護 (WRP) 設定，使其成為唯讀設定。 大部分接收新增保護的資源都是系統 COM 伺服器金鑰，雖然有些功能已新增目標資源保護。 Microsoft 變更了這些資源，以保護系統和其他應用程式免于彼此中斷，並提供一致且穩定的平臺，讓應用程式可在其上可靠地執行。 在過去，應用程式可以提供自訂檔案，並使用未受保護的 COM 註冊來變更系統。 在舊版的應用程式中，這可能會降級系統執行時間，或變更其他應用程式需要正常運作的介面。 在最糟的情況下，這類安裝可能會導致系統失敗或一段時間的降級。 為了提供更好的體驗和更穩定的應用程式平臺，我們鎖定了這些註冊，因此只有 Microsoft update 可以變更系統元件。

因為大部分的資源變更都是系統所使用的 COM 金鑰，所以這項變更不會影響大部分的應用程式。 雖然我們預期大部分的應用程式在 Windows 7 上都有更佳的體驗，因為這些變更的結果，應用程式的一小部分可能會受到負面影響。 系統的應用程式相容性層級會自動通知應用程式變更設定，即使因為它是受保護的資源而失敗，也會自動解決安裝問題。 這可防止應用程式設定中斷，但如果需要變更設定才能讓應用程式正常運作，則可能會造成問題。

## <a name="manifestation"></a>表現

在 Windows 7 之前，應用程式可能已修改這些設定。 在 Windows 7 上安裝時，應用程式可能會發現某些功能不再適用，因為這些設定未反映出應用程式的預期。

在兩種情況下，應用程式可能會遇到與此新增保護相關的問題：

-   可能已使用現在保護的設定做為資料存放區，或做為罕見或非預期的擴充點的應用程式
-   在罕見的情況下，用來識別應用程式設定的偵測機制可能無法辨識特定的設定，因此可能不會套用應用程式相容性緩和層

## <a name="mitigation"></a>降低

風險降低的主要方法是系統的應用程式相容性層，在偵測到應用程式時，它會自動套用至應用程式的相容性層。 您也可以使用應用程式屬性中的 [相容性] 索引標籤，手動將它套用至任何應用程式。

這一層會藉由攔截登錄作業來解決此問題。 如果應用程式嘗試修改唯讀 (WRP) 設定，即使設定未真正變更，該層仍一律會傳回成功。 針對大部分的應用程式，這不會造成任何問題。 不過，應用程式可能需要變更該設定才能正常運作，也就是上述的第一種案例。

## <a name="solution"></a>解決方法

在上述兩個案例中：

-   如果應用程式需要可寫入的金鑰才能運作或使用資料存放區，則除了變更應用程式之外，不會再寫入至該位置的解決方案。
-   如果相容性層未套用至安裝程式，則應該偵測並提供安裝失敗，並將其提供給應用程式並重新執行。 應用程式也可以在相容性模式下執行，在這種情況下，一律會套用緩和層。

## <a name="compatibility-tests"></a>相容性測試

如何偵測應用程式是否已套用 WRP 緩和：

-   Windows Installer 知道 WRP;它會自動且無訊息地忽略寫入或修改受保護資源的嘗試。 如果應用程式是隨 Windows Installer 安裝，且已啟用記錄功能，則會記錄每個登錄機碼寫入作業的警告，因為它是受 WRP 保護的資源，所以會被忽略。
-   WRP API 會併入 SfCIsKeyProtected，可查詢登錄機碼是否在目前的系統上受到 WRP 保護。 如需使用此 API 的詳細資訊，請參閱下列連結中的 WRP 專案。

## <a name="links-to-other-resources"></a>其他資源的連結

<dl>

[Windows 資源保護](/windows/desktop/Wfp/windows-resource-protection-portal)  
</dl>

 

 
