---
title: IAgentCharacter GetTTSPitch
description: IAgentCharacter GetTTSPitch
ms.assetid: b21ae1f1-daf6-42e5-9c52-f28722180021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c91d4ebc4f55da6a0e102c30a8c2a16eab12beaf283ff4b5e023d15d3a17b05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117693144"
---
# <a name="iagentcharactergetttspitch"></a>IAgentCharacter::GetTTSPitch

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GetTTSPitch(
   long * pdwPitch  // address of variable for character TTS pitch
);
```

抓取字元的 TTS 輸出間距設定。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pdwPitch"></span><span id="pdwpitch"></span><span id="PDWPITCH"></span>*pdwPitch*
</dt> <dd>

以赫茲為單位接收字元目前 TTS 間距設定的變數位址。

</dd> </dl>

雖然您的應用程式無法寫入此值，但您可以在輸出文字中包含音調標記，以暫時增加特定語句的音調。 這個方法只適用于為 TTS 輸出設定的字元。 如果未啟用語音合成 (TTS) 引擎 (或已安裝) 或字元不支援 TTS 輸出，則這個方法會傳回零 (0) 。

 

 




