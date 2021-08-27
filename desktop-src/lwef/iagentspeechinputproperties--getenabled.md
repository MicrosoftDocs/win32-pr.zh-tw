---
title: IAgentSpeechInputProperties GetEnabled
description: IAgentSpeechInputProperties GetEnabled
ms.assetid: 5731f9ad-eb2e-4a79-a724-b3c263235c8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 404bd6f0348487c8e039c247f5a9368359133be9e3df76b884115679a2961a97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114668"
---
# <a name="iagentspeechinputpropertiesgetenabled"></a>IAgentSpeechInputProperties：： GetEnabled

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GetEnabled(
   long * pbEnabled  // address of variable for speech recognition engine 
);                   // Enabled setting
```

抓取值，指出是否已啟用安裝的語音辨識引擎。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*
</dt> <dd>

如果語音引擎目前已啟用，則為收到 **True** 之變數的位址，如果停用，則為 **False** 。

</dd> </dl>

 

 




