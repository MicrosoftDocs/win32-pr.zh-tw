---
title: IAgentAudioOutputProperties GetEnabled
description: IAgentAudioOutputProperties GetEnabled
ms.assetid: a1e555e1-98f1-4a3d-b6ba-4cd35348db2b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e86b82c720971ae1e14ee294e6d097fd35ca80a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021406"
---
# <a name="iagentaudiooutputpropertiesgetenabled"></a>IAgentAudioOutputProperties：： GetEnabled

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetEnabled(
long * pbEnabled  // address of variable for audio output Enabled setting 
);                      
```

抓取值，指出是否已啟用字元語音輸出。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*
</dt> <dd>

如果目前已啟用語音輸出，則為收到 **True** 之變數的位址，如果停用，則為 **False** 。

</dd> </dl>

因為此設定會影響所有字元的 (TTS 和音效檔) 的語音輸出，所以只有使用者可以在 Microsoft Agent 屬性工作表中變更這個屬性。

 

 




