---
title: RaytracingAccelerationStructure
description: 可以在 HLSL 中宣告並傳遞至 TraceRay 的資源類型，以表示使用 BuildRaytracingAccelerationStructure 建立的最上層加速資源。
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: 4728e167fe9fbc353c51accaa92d9b9d4086a0bfff3f098f43b93523cd63a792
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123616"
---
# <a name="raytracingaccelerationstructure"></a>RaytracingAccelerationStructure

可以在 HLSL 中宣告並傳遞至 [**TraceRay**](traceray-function.md) 的資源類型，以表示使用 **BuildRaytracingAccelerationStructure** 建立的最上層加速資源。 它會系結為描述中繼資料表或根描述項 SRV 中的原始緩衝區 SRV。  HLSL 中的宣告如下所示：


```
RaytracingAccelerationStructure MyScene[] : register(t3,space1);
```

此範例顯示加速結構的無限制大小陣列，這表示來自描述元堆積，因為無法編制根目錄描述元的索引。

**RaytracingAccelerationStructure** 是不透明的資源，沒有任何可供著色器使用的方法。


 

 




