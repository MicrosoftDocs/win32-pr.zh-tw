---
title: 網路存取保護
description: 請注意，從 Windows 10 網路存取保護開始，無法使用網路存取保護平臺 (NAP) 是一組作業系統元件，可提供保護私人網路存取的平臺。
ms.assetid: f562f5f1-c05a-4e4e-bcd9-a302c61f2a5e
keywords:
- 網路存取保護
- 網路存取保護，起始頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1e5b5121566c3626ee7a9f2ba5d85efc1bf6cff17b412cd99874ae9b346780
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939126"
---
# <a name="network-access-protection"></a>網路存取保護

## <a name="purpose"></a>目的

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

網路存取保護 (NAP) 是一組作業系統元件，可提供保護私人網路存取的平臺。 NAP 平臺提供了一種整合方式，可評估網路用戶端的系統健全狀況狀態，嘗試連線到網路或在網路上通訊，以及限制網路用戶端的存取，直到達到健康原則需求為止。

NAP 是可延伸的平臺，可提供基礎結構和 API 集，以新增儲存、報告、驗證和修正電腦系統健全狀態的元件。 NAP 平臺本身不會提供元件來累積和評估電腦健全狀況狀態的屬性。 其他元件（稱為系統健康狀態代理程式） (Sha) 和系統健康狀態驗證 (Shv) ，可提供網路原則驗證和網路原則合規性。

## <a name="where-applicable"></a>適用時

NAP 是設計成可擴充的。 它可以與任何提供 Sha 和 Shv 或辨識其已發佈 API 集的廠商軟體交互操作。 NAP 有助於提供適用于下列常見案例的解決方案：

-   檢查漫遊膝上型電腦的健康情況和狀態。
-   確定桌上型電腦的健全狀況。
-   確認遠端辦公室電腦的相容性和健康情況。
-   判斷造訪筆記本電腦的健康情況。
-   確認未受管理的家用電腦的相容性和健康情況。

## <a name="developer-audience"></a>開發人員對象

NAP API 是針對 C/c + + 開發人員所設計。 針對 NAP 強制方法，程式設計人員應該熟悉網路通訊協定和技術，例如遠端驗證撥入使用者服務 (RADIUS) 、動態主機設定通訊協定 (DHCP) 、虛擬私人網路 (Vpn) 、有線和無線存取的 IEEE 802.1 X 標準，以及網際網路通訊協定安全性 (IPsec) 。

## <a name="run-time-requirements"></a>執行階段需求求

nap 平臺需要執行 Windows Server 2008 或更新版本的 nap 基礎結構伺服器，以及執行 Windows XP Service Pack 3 (SP3) 、Windows Vista 或更新版本作業系統的 nap 用戶端。 如需哪些作業系統支援特定程式設計專案的特定資訊，請參閱 NAP 參考檔中 NAP Api 的需求章節。

## <a name="in-this-section"></a>本節內容



| 主題                                         | 描述                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------|
| [關於 NAP](about-nap.md)<br/>         | NAP API 的一般資訊。<br/>                                     |
| [使用 NAP](using-nap.md)<br/>         | NAP API 的使用範例。<br/>                                            |
| [NAP 參考](nap-reference.md)<br/> | NAP 介面、結構和其他程式碼元素的檔。<br/> |



 

 

 





