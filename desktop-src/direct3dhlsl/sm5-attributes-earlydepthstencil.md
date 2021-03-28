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
ms.openlocfilehash: a7dd8507986970f2066538cc00b53af08807910e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990815"
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



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型5屬性](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




