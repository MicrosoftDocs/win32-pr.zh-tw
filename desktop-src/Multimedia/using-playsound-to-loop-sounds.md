---
title: 使用 PlaySound 來迴圈聲音
description: 使用 PlaySound 來迴圈聲音
ms.assetid: 747b9a76-5ff3-488e-ba85-c4d926e1e723
keywords:
- 波形音訊，PlaySound 函式
- 波形音訊，迴圈聲音
- 波形音訊、fdwSound 參數
- PlaySound 函式，迴圈聲音
- PlaySound 函式，fdwSound 參數
- 迴圈波形-音效
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5373e703c7a02068094e312dee18690a797b330e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104374969"
---
# <a name="using-playsound-to-loop-sounds"></a>使用 PlaySound 來迴圈聲音

如果您 \_ 針對 PlaySound 函式的 fdwSound 參數指定 Operators.snd 迴圈和 Operators.snd \_ 非同步旗[](/previous-versions//dd743680(v=vs.85))標，則音效會持續重複播放，如下列範例所示： 


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_LOOP | SND_ASYNC); 
```



如果您想要迴圈播放音效，則必須以非同步方式播放;您無法使用 OPERATORS.SND \_ 同步旗標搭配 Operators.snd \_ 迴圈旗標。 迴圈的音效會持續播放，直到您呼叫 **PlaySound** 來播放另一個音效為止。 若要停止播放音效 (迴圈或非同步) 而不播放另一個音效，請使用下列語句：


```C++
PlaySound(NULL, NULL, 0); 
```



 

 