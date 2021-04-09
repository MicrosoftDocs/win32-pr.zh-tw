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
# <a name="advanced-rotation"></a><span data-ttu-id="2a4b6-109">先進旋轉</span><span class="sxs-lookup"><span data-stu-id="2a4b6-109">Advanced Rotation</span></span>

<span data-ttu-id="2a4b6-110">本節說明如何根據使用者執行旋轉操作的位置來旋轉物件。</span><span class="sxs-lookup"><span data-stu-id="2a4b6-110">This section explains how to rotate an object based on where the user is performing the rotation manipulation.</span></span>

<span data-ttu-id="2a4b6-111">下圖說明兩種可旋轉物件的不同方式。</span><span class="sxs-lookup"><span data-stu-id="2a4b6-111">The following image illustrates two different ways that an object can be rotated.</span></span>

![顯示兩種類型的單一手指旋轉的圖例：圍繞在中央或邊緣，邊緣都牽涉到旋轉和平移](images/rotation.png)

<span data-ttu-id="2a4b6-113">在範例 A 中，物件是在物件的中心點周圍操作。</span><span class="sxs-lookup"><span data-stu-id="2a4b6-113">In example A, the object is manipulated around the center point of the object.</span></span> <span data-ttu-id="2a4b6-114">在 B 範例中，物件會圍繞操作的中心點旋轉。</span><span class="sxs-lookup"><span data-stu-id="2a4b6-114">In example B, the object is rotated around the center point of the manipulation.</span></span> <span data-ttu-id="2a4b6-115">若要針對物件中心點以外的點支援操作，您必須執行可同時執行旋轉和轉譯的複合操作。</span><span class="sxs-lookup"><span data-stu-id="2a4b6-115">To support manipulation around a point other than the center point of the object, you must perform a compound manipulation that performs both rotation and translation.</span></span> <span data-ttu-id="2a4b6-116">下列程式碼顯示如何執行和計算此操作。</span><span class="sxs-lookup"><span data-stu-id="2a4b6-116">The following code shows how this manipulation is performed and calculated.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="2a4b6-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="2a4b6-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a4b6-118">Advanced 操作</span><span class="sxs-lookup"><span data-stu-id="2a4b6-118">Advanced Manipulations</span></span>](advanced-manipulations.md)
</dt> <dt>

[<span data-ttu-id="2a4b6-119">操作</span><span class="sxs-lookup"><span data-stu-id="2a4b6-119">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> </dl>

 

 




