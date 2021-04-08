---
title: IAgentAudioOutputProperties GetUsingSoundEffects
description: IAgentAudioOutputProperties GetUsingSoundEffects
ms.assetid: 3ccf90b1-a2aa-482a-9f96-85d735532c11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e83314acfc67ce8bea4a0f0d305f6d5d490a92e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673292"
---
# <a name="iagentaudiooutputpropertiesgetusingsoundeffects"></a>IAgentAudioOutputProperties::GetUsingSoundEffects

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetUsingSoundEffects(
long * pbUsingSoundEffects  // address of variable sound effects output 
);                          // setting 
```

抓取值，指出是否已啟用音效效果輸出。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbUsingSoundEffects"></span><span id="pbusingsoundeffects"></span><span id="PBUSINGSOUNDEFFECTS"></span>*pbUsingSoundEffects*
</dt> <dd>

如果目前已啟用音效效果輸出，則為收到 **True** 之變數的位址，如果停用，則為 **False** 。

</dd> </dl>

在 Microsoft 代理程式字元編輯器中，會指派字元動畫的音效效果。 因為這項設定會影響所有字元的音效效果輸出，所以只有使用者可以在 Microsoft Agent 屬性工作表中變更這個屬性。

 

 




