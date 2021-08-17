---
title: IAgentCharacter GetTTSSpeed
description: IAgentCharacter GetTTSSpeed
ms.assetid: 25526ef7-581f-489c-a299-bd3b5ac9ea61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e7fbe4cbba7eaed22f49865e1a0f0994c512867fb6f233ef2bbfa01dcaafcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609868"
---
# <a name="iagentcharactergetttsspeed"></a>IAgentCharacter::GetTTSSpeed

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GetTTSSpeed(
   long * pdwSpeed  // address of variable for character TTS output speed
);
```

抓取字元的 TTS 輸出速度設定。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pdwSpeed"></span><span id="pdwspeed"></span><span id="PDWSPEED"></span>*pdwSpeed*
</dt> <dd>

每分鐘接收字元輸出速度的變數位址（以單字為單位）。

</dd> </dl>

雖然您的應用程式無法寫入此值，但您可以將速度標記包含在輸出文字中，以暫時加速特定語句的輸出。

這個屬性會傳回字元的目前說話輸出速度設定。 針對使用 TTS 輸出的字元，屬性會傳回字元的實際 TTS 輸出。 如果未啟用 TTS 或字元不支援 TTS 輸出，此設定會反映輸出速度的使用者設定。

 

 




