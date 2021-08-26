---
title: 片段
description: 片段
ms.assetid: bc400251-32c4-4477-ba0c-a0046fe85327
keywords:
- OpenGL、片段
- OpenGL 處理管線，片段
- 段 OpenGL
- framebuffers，修改圖元的片段
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ab5d4124445455e518e4f091730e6e38e899442785b9f86ef73a230b99fbd41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082408"
---
# <a name="fragments"></a>片段

只有當它通過下列測試時，才會在畫面格緩衝區中修改對應的圖元：

-   [圖元擁有權測試](pixel-ownership-test.md)
-   [剪式測試](scissor-test.md)
-   [Alpha 測試](alpha-test.md)
-   [樣板測試](stencil-test.md)
-   [深度緩衝區測試](depth-buffer-test.md)

如果通過，片段的資料可以取代現有的畫面格緩衝區值，或者您可以將它與畫面格緩衝區中現有的資料結合，視特定模式的狀態而定。 您可以透過下列方式將片段與畫面格緩衝區中的資料結合：

-   [混合](blending.md)
-   [抖動](dithering.md)
-   [邏輯作業](logical-operations.md)

 

 




