---
title: 先進旋轉
description: 本節說明如何根據使用者執行旋轉操作的位置來旋轉物件。
ms.assetid: 56b339b1-a062-4c0e-91c8-aec08a17bc65
keywords:
- Windows Touch，旋轉
- Windows Touch，先進的旋轉
- Windows Touch，操作
- 操作，旋轉
- 操作，先進的旋轉
- 旋轉，advanced
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3a84679f4189d28941262cda2585887b0932c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931931"
---
# <a name="advanced-rotation"></a>先進旋轉

本節說明如何根據使用者執行旋轉操作的位置來旋轉物件。

下圖說明兩種可旋轉物件的不同方式。

![顯示兩種類型的單一手指旋轉的圖例：圍繞在中央或邊緣，邊緣都牽涉到旋轉和平移](images/rotation.png)

在範例 A 中，物件是在物件的中心點周圍操作。 在 B 範例中，物件會圍繞操作的中心點旋轉。 若要針對物件中心點以外的點支援操作，您必須執行可同時執行旋轉和轉譯的複合操作。 下列程式碼顯示如何執行和計算此操作。


```C++
RotateVector(FLOAT *vector, FLOAT *tVector, FLOAT fAngle) {
    FLOAT fAngleRads = fAngle / 180.0f * 3.14159f;
    FLOAT fSin = sin(fAngleRads);
    FLOAT fCos = cos(fAngleRads);

    FLOAT fNewX = (vector[0]*fCos) - (vector[1]*fSin);
    FLOAT fNewY = (vector[0]*fSin) + (vector[1]*fCos);

    tVector[0] = fNewX;
    tVector[1] = fNewY;
}
     
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[Advanced 操作](advanced-manipulations.md)
</dt> <dt>

[操作](getting-started-with-manipulations.md)
</dt> </dl>

 

 




