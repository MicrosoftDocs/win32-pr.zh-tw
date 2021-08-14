---
title: 動畫設計
description: 動畫設計
ms.assetid: 8812e4cc-9062-4c65-81ef-229bd29534cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 225a500d94b4de6f9133650a6aed415a49329585bc9bc9f83dec028668e51215
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118752289"
---
# <a name="animation-design"></a>動畫設計

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

### <a name="image-design"></a>影像設計

設計您的字元時，請使用 Microsoft Office 調色板，以將任何可能的調色板實現問題降至最低。 請避免選取與您在檔中使用的色彩類似的透明色彩。

### <a name="sounds"></a>音效

Microsoft 代理程式可讓您在動畫中播放音效。 建議您不要包含 **閒置** 動畫的音效。 這是因為如果 Agent 必須載入系統多媒體 DLL，則動畫中間不會有延遲。

### <a name="frame-size"></a>畫面格大小

典型的 Office 助理是 123 x 93 圖元。 雖然您可以建立其他大小的字元，但它們會在助理資源庫中調整為 123 x 93。

### <a name="frame-transition"></a>框架轉換

除了 **再見**、 **問候**、 **顯示** 和 **隱藏** 以外的所有動畫，都應該以 RestPose 動畫作為開頭和結尾。 Microsoft Office 不會 **播放明確的** 傳回動畫，因此您不應該定義它們。 所有動畫也都應該有結束分支。 「結束分支」可讓我們在呼叫下一個動畫之前，先「趕上並完成」目前的動畫。 如果您未提供結束分支，則動畫之間的轉換可能會停用。

### <a name="character-properties"></a>字元屬性

Microsoft 代理程式可讓您設定字元的 [**名稱**](name-property.md)、 [**描述**](description-property.md) 及 [**ExtraData**](extradata-property.md) 屬性。 Microsoft Office 使用 **ExtraData** 欄位來保存一或多個簡介片語和提醒片語。 Microsoft Office 從其他簡介片語中挑選，以放入助理資源庫中的語音氣球。 當您收到 Outlook 的提醒時，我們會使用提醒片語。

[**ExtraData**](extradata-property.md)欄位的格式如下：

IntroPhrase1~~IntroPhrase2~~IntroPhrase3 ^ ^ ReminderPhrase1~~ReminderPhrase2~~ReminderPhrase3

簡介片語會以成對的波狀字元字元分隔， (~) ，後面接著提醒片語。 這些提醒片語也會以成對的波狀字元字元分隔。 這兩組片語會以兩個插入號字元分隔 (^^) 。 每一種片語的數目都沒有限制，不同之處在于每個片語都必須至少有一個。

 

 




