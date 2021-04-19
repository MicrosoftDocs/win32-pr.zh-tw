---
title: Windows Update 上適用的圖形驅動程式可用性
description: 這些驅動程式在 Windows Update (WU) 的可用性將會決定是否要自動提供使用者從 Windows 7、Windows 8 或 Windows 8.1 升級為 Windows 10。
ms.assetid: 166C0FE3-CB9D-4895-91AC-6E57EC1D8B21
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 208e984199c8de63dfa49133a255865035c84bdd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968220"
---
# <a name="availability-of-applicable-graphics-drivers-on-windows-update"></a>Windows Update 上適用的圖形驅動程式可用性

這些驅動程式在 Windows Update (WU) 的可用性將會決定是否要自動提供使用者從 Windows 7、Windows 8 或 Windows 8.1 升級為 Windows 10。 如果硬體掃描顯示電腦上的圖形介面卡 Windows Update 沒有可用的圖形驅動程式，則不會提供使用者更新的 Windows 10 OS。 不過，使用者仍然可以透過其他來源取得 Windows 10，並手動執行升級。

有些使用者不確定它們在其他人的情況下未提供升級的原因，即使 Upgrade Advisor 解釋沒有任何圖形驅動程式可供他們的硬體使用也是一樣。

此外，某些使用者強制進行升級，然後發現其圖形功能和效能因為缺乏硬體驅動程式而發生。

## <a name="mitigations"></a>風險降低

若要減輕這個問題，使用者可以手動安裝較舊的驅動程式，也就是從 Windows 7、Windows 8 或 Windows 8.1，方法是前往 IHV 或 OEM 網站，並明確下載驅動程式。 這必須在升級之後完成，而且不保證可以運作。 如果 WU 無法使用適當的圖形驅動程式，則不支援任何解決方案。 使用者必須決定是否要：

-   保留在先前的作業系統;
-   接受軟體驅動程式的限制，Microsoft 基本顯示器介面卡 (MSBDA) ;或
-   購買具有支援之 Windows 10 驅動程式的新圖形配接器。

## <a name="solutions"></a>方案

Ihv 和 Oem 將其 Windows 10 graphics 驅動程式上傳至適用于任何想要支援之硬體的 WU 是很重要的。

請注意，已到達存留 (EOL) 的硬體在 WU 上可能沒有驅動程式。 在此情況下沒有解決方案-使用者必須選擇上述 [緩和措施] 下的其中一個選項。

 

 




