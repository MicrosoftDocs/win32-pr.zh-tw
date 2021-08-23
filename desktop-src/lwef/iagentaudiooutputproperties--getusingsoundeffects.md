---
title: IAgentAudioOutputProperties GetUsingSoundEffects
description: IAgentAudioOutputProperties GetUsingSoundEffects
ms.assetid: 3ccf90b1-a2aa-482a-9f96-85d735532c11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6750dbfee36039337025a03b9f77573a2134f85d15a56d77b2d512482c7bb0e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751452"
---
# <a name="iagentaudiooutputpropertiesgetusingsoundeffects"></a>IAgentAudioOutputProperties::GetUsingSoundEffects

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

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

 

 




