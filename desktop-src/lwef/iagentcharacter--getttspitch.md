---
title: IAgentCharacter GetTTSPitch
description: IAgentCharacter GetTTSPitch
ms.assetid: b21ae1f1-daf6-42e5-9c52-f28722180021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dff1bb7999795cf27e29a7d064dd500b47bb419
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966418"
---
# <a name="iagentcharactergetttspitch"></a>IAgentCharacter::GetTTSPitch

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

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

 

 




