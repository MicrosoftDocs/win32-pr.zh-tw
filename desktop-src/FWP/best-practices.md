---
title: " (Windows 篩選平台) 的最佳作法"
description: 下列清單包含使用 Windows 篩選平台 (WFP) API 來開發應用程式的最佳做法。
ms.assetid: 017ff210-8666-466e-8424-c95e750fd5ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac43f103e0076945d566e26a1706bdec22916db
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104508248"
---
# <a name="best-practices-windows-filtering-platform"></a> (Windows 篩選平台) 的最佳作法

下列清單包含使用 Windows 篩選平台 (WFP) API 來開發應用程式的最佳做法。

-   使用動態會話。

    許多應用程式會在一開始就新增篩選原則物件，然後在停止時刪除這些物件。 藉由使用動態會話，您保證即使應用程式當機，也會刪除這些物件。 此外，只要在停止時關閉引擎控制碼，會比進行個別呼叫來刪除每個物件更有效率。

-   請正常處理交易超時，或將會話 **txnWaitTimeoutInMSec** 設為無限以防止超時。

    即使您未使用明確交易，大部分的呼叫仍會在隱含交易下執行，因此可能會超時。

-   使用明確交易，將相關的「新增」或「刪除」作業合併為單一交易。

    這會更有效率，並可讓您輕鬆地在錯誤路徑中清除部分結果。

-   使用符合 MUI 規範的字串。

    所有可當地語系化的字串都會儲存在 common data 結構中： [**FWPM \_ DISPLAY \_ DATA0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwpm_display_data0)。 此結構內的字串可以是 [**SHLoadIndirectString**](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring)所支援型別的間接字串。 在任何函式傳回 **FWPM \_ 顯示 \_ DATA0** 結構之前，會使用呼叫端的地區設定，將間接字串解析為指定的字串資源。

-   將所有物件與提供者產生關聯。

    當系統上安裝了多個提供者時，診斷工具可以更輕鬆地判斷加入的物件。

-   將篩選準則新增至您自己的子層。

    一旦達到子層中的終止篩選器，就不會評估該子層中的任何篩選。 因此，如果您將篩選新增至與另一個提供者相同的子層，您可能會防止叫用彼此的篩選，而導致非預期的結果。

-   使用應用層強制 (ALE) ，而不是封包導向的篩選。

    封包層的篩選速度很慢。

-   在產生 ICMP 錯誤和 RST 事件之前，先進行篩選。

    這樣會更有效率地在產生這些事件之後篩選這些事件。

-   在 Stream/資料包資料層執行封包檢查，而不是在傳輸層。

    這適用于開發標注。 如需詳細資訊，請參閱 Windows 驅動程式套件 (WDK) 的注標 [驅動程式設計考慮](/windows-hardware/drivers/network/callout-driver-programming-considerations) 。

-   使用複雜的篩選器時，請考慮效能的影響。

    從 Windows 7 和 Windows Server 2008 R2 開始，可以使用多個使用相同欄位索引鍵的條件來建立篩選。 這可讓您以較少的篩選準則建立複雜的原則。 不過，這類複雜的篩選器可能會產生較慢的效能，讓 WFP 篩選引擎進行分類。 您應該進行評估，以判斷使用這類篩選是否會造成對您解決方案的整體效能造成負面影響。

 

 
