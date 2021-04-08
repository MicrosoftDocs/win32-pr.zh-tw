---
title: 設計 NDF Helper 類別延伸模組
description: 本主題的目的是要透過 helper 類別擴充程式開發程式來提供一般的指引。
ms.assetid: f5dbd198-7d22-4e7e-830e-6753e9f4d6c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d91ff748d8139aad17fca3710b17e73b5e1eaa14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932091"
---
# <a name="designing-ndf-helper-class-extensions"></a>設計 NDF Helper 類別延伸模組

本主題的目的是要透過 helper 類別擴充程式開發程式來提供一般的指引。 本主題中的指導方針適用于所有 helper 類別的擴充功能。 如需更具體的指引，請參閱 [Windows 篩選平台](windows-filtering-platform-extensible-helper-class.md) 可延伸協助程式類別和 [802.11 無線診斷](802-11-wireless-diagnostics-extensible-helper-classes.md)可延伸協助程式類別。

## <a name="extending-ndf-functionality"></a>擴充 NDF 功能

Windows Vista 和更新版本隨附的各種協助程式類別，可診斷和修復各式各樣的問題。 但有時候，協力廠商開發人員可能會想要擴充這些協助程式類別，以診斷並解決其特定產品和執行的特定問題。

下列 Microsoft NDF 協助程式類別是可擴充的。

-   [Windows 篩選平台](windows-filtering-platform-extensible-helper-class.md)
-   [無線安全性](802-11-wireless-diagnostics-extensible-helper-classes.md)

## <a name="implementing-a-helper-class-extension"></a>執行 Helper 類別延伸模組

Microsoft 發行了兩個介面，可用來開發 NDF 協助程式類別延伸模組。

NDF 會呼叫 [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) 介面，以驗證它是否有所有必要的資訊，以及它是否已選擇正確的 helper 類別。 它是透過 [**GetAttributeInfo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelperinfo-getattributeinfo) 方法來完成。

NDF 會針對診斷程式期間發生的大部分活動呼叫 [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) 介面。 其中有幾個方法是必要的，但有些是選擇性的，而不是特定用途。

必要的方法包括 [**Initialize**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-initialize) 和 [**GetDiagnosticsInfo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getdiagnosticsinfo)。 NDF 呼叫 **initialize** 以將金鑰參數傳送給 helper 類別延伸模組，以將其實例狀態初始化。 **GetDiagnosticsInfo** 可預估診斷可能花費的時間，以及是否需要模擬原始的使用者內容。

另一個方法 [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth)則是呼叫，以在與 helper 類別對應的網路元件上執行診斷。 當 NDF 判斷正在進行的診斷或修復應停止時，就會呼叫 [**Cancel**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-cancel) 。 [**清除**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-cleanup) 作業可讓 ndf 釋放 helper 類別延伸模組在呼叫 [**Initialize**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-initialize) 之後所使用的 ndf 資源。

如需其他方法的詳細資訊，請參閱 [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper)。

NDF 協助程式類別延伸模組是用來診斷和解決與特定應用程式或元件相關聯的連線問題。 它們也會驗證解決嘗試的成功或失敗。

考慮使用 helper 類別延伸模組的開發人員應該執行下列工作。

-   識別診斷和修復動作很有用的使用者案例。
-   提供通常發生連線問題的解決方式。
-   如果需要協助程式類別延伸，請在 NDF 中定義用來代表元件健康情況狀態的元件健全狀況模型。

## <a name="identify-user-scenarios"></a>識別使用者案例

測試和使用應用程式可能已經提供協助程式類別延伸模組可能會診斷並可能修復的明顯模式。 應用程式開發人員可以使用這項資料來判斷最重要的連線問題，並找出可能發生連線問題的使用者案例。

判斷每個問題的根本原因對於這部分的程式來說很重要。 這可能需要廣泛的研究，但將有助於建立更容易使用者和系統管理員使用的軟體。 如果找不到根本原因，則會變得很難或無法使用 helper 類別延伸來提供問題解決方式。

## <a name="provide-resolutions"></a>提供解決方案

在開發小組找出與軟體相關之問題的根本原因之後，下一步就是找出適當的解決措施，協助使用者盡可能有效率地解決問題。

並非所有的解決方案都需要協助程式類別延伸或自動執行的動作。 在某些情況下，小組可能會判斷解決根本原因的最佳方法是修正或更新元件、提供元件的其他說明內容，或開發提供更佳長期解決方案的其他策略。

針對自動化動作很理想的問題，建立 NDF 協助程式類別延伸通常是絕佳的解決方案。

Helper 類別延伸會將根本原因和修復資訊的相關資訊傳回給使用者。 用來描述根本原因和修復資訊的字串，對於非技術使用者來說，必須簡單且容易瞭解。 如需這些字串的詳細資訊，請參閱 [NDF 協助程式類別延伸消費者介面指導方針](user-interface-guidelines-for-ndf-helper-class-extensions.md)。

## <a name="define-a-component-health-model"></a>定義元件健全狀況模型

軟體發展人員應定義與網路問題管理能力相關聯的「健全狀況」等級。 用來開發 helper 類別的健康情況模型只會定義兩個層級的健全狀況：狀況良好和狀況不良。 這些層級也可以套用至 NDF 協助程式類別延伸。

狀況良好的元件表示沒有問題。 元件可能因為其本身的問題而被視為狀況不良，或因為相依的其他元件發生問題。



| 詞彙                                                                                                                             | 描述                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span id="LowHealth"></span><span id="lowhealth"></span><span id="LOWHEALTH"></span>LowHealth<br/>                         | 此狀態表示此元件無法接受的失敗層級，以及元件是否為問題。<br/>    |
| <span id="LowHealth_Below"></span><span id="lowhealth_below"></span><span id="LOWHEALTH_BELOW"></span>LowHealth 如下<br/> | 此狀態表示此元件相依的本機電腦群組件無法接受的失敗層級。<br/> |



 

使用 NDF 進行診斷時，系統會詢問協助程式類別延伸系列的問題，以判斷其健康狀態的狀態。 如果延伸模組回應狀況不良，則 NDF 會詢問問題、嘗試診斷問題、其位置，以及下一步的外觀。 每個協助程式類別都必須能夠回答低健康情況的問題，才能更妥善地導向適當的診斷活動。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 篩選平台可擴充 Helper 類別](windows-filtering-platform-extensible-helper-class.md)
</dt> <dt>

[802.11 無線診斷可延伸的 Helper 類別](802-11-wireless-diagnostics-extensible-helper-classes.md)
</dt> </dl>

 

 





