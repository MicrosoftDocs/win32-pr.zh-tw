---
title: Advanced 擴充
description: Advanced 擴充
ms.assetid: 29db15a1-fa56-441a-af99-9e858d143804
keywords:
- Windows觸控、擴充
- WindowsTouch，advanced 擴充
- Windows觸控、操作
- 操作，擴充
- 操作，advanced 擴充
- 展開，advanced
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27e176d91c08bd0d39383e2aba269bbdb5629cfe6b7c2d20eb1ac955786bef2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881498"
---
# <a name="advanced-expansion"></a>Advanced 擴充

下圖顯示可展開物件的兩種方式。

![圖例顯示物件中心點周圍的簡單展開，以及圍繞操作中心點的先進展開](images/expansion.png)

例如，簡單的展開範例中，物件會圍繞其中心點展開。 在 B 範例中，物件是在操作中心點周圍展開。 若要啟用此功能，您必須在展開時轉譯物件。 您將轉譯物件的數量，與從物件中央到手勢中心點的距離相同。 很直覺地，它就像是從展開筆勢的中心點展開物件，然後將它移動，使其仍位於與其初始位置相同的中心點。 下列程式碼示範如何套用這個概念，以啟用中心點周圍的擴充。


```C++
    if(m_fFactor != 1.0f)
    {
        // We represent our vectors as an array.
        // x: vx[0], y: vx[1]

        FLOAT v1[2];
        v1[0] = this->get_CenterX() - fOffset[0];
        v1[1] = this->get_CenterY() - fOffset[1];

        FLOAT v2[2];
        v2[0] = v1[0] * m_fFactor;
        v2[1] = v1[1] * m_fFactor;
        
        m_fdX += v2[0] - v1[0];
        m_fdY += v2[1] - v1[1];
    }
   
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[操作](getting-started-with-manipulations.md)
</dt> </dl>

 

 




