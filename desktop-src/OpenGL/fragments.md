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
ms.openlocfilehash: 00e2b4c2dc36e24c4fd9baa82b28fa4d336f69b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106984930"
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

 

 




