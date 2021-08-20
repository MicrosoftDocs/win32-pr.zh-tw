---
title: earlydepthstencil
description: 在著色器執行之前強制進行深度樣板測試。
ms.assetid: f8a9fee7-4a8a-4a34-bf7c-56906592caac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ed108d4f8e9d8d719d36fc859d5cc01a2317db4756bfbc6b0a548b669d9ca025
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986168"
---
# <a name="earlydepthstencil"></a>earlydepthstencil

在著色器執行之前強制進行深度樣板測試。


```
earlydepthstencil   
```



## <a name="remarks"></a>備註

深度樣板測試通常是在圖元著色器的圖元處理期間進行。 強制較早深度樣板測試會導致在著色器執行之前完成測試;其目的是要藉由剔除/減少/避免不必要的圖元處理來改善每個圖元的效能。

應用程式可以藉由提供屬性來強制進行早期深度樣板測試，或者硬體可能會執行較早的深度樣板測試，但前提是不會寫入任何深度值，而且不會在著色器中執行任何未排序的存取作業作為優化。

下列著色器類型支援此屬性：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型5屬性](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




