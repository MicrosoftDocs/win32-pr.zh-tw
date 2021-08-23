---
description: 如果您不亮著頂點著色器或圖元著色器，則可以選擇在執行時間中使用光源引擎。
ms.assetid: vs|directx_sdk|~\lighting_state.htm
title: " (Direct3D 9) 的燈光狀態"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5935590c46776c621535968f4d457f3738d83d02342ffddf832cbf0278bbd9ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674268"
---
# <a name="lighting-state-direct3d-9"></a> (Direct3D 9) 的燈光狀態

如果您不亮著頂點著色器或圖元著色器，則可以選擇在執行時間中使用光源引擎。 光源引擎要求頂點資料必須包含每個頂點的法線：沒有一般資料的頂點會在所有光源計算中產生一個零的點乘積。 光源計算在 [ (Direct3D 9) 的數學數學 ](mathematics-of-lighting.md)中有更詳細的討論。

若要啟用光源引擎，請使用：


```
SetRenderState(D3DRS_LIGHTING, TRUE); 
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉譯狀態](render-states.md)
</dt> </dl>

 

 



