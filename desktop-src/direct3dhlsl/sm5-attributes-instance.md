---
title: instance
description: 使用這個屬性來建立幾何著色器的實例。
ms.assetid: 0e487e52-53d0-4193-99b2-fd018a061b42
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77c19b26107228bb04007d1c2c69ac34b464c7c361966ac9858d9bcdb09b4c4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986158"
---
# <a name="instance"></a>instance

使用這個屬性來建立幾何著色器的實例。


```
instance(X)   
```



## <a name="remarks"></a>備註

X 是一個整數索引，表示要針對每個繪製的專案執行的實例數目 (例如，針對每個三角形) 。 使用這個屬性時，請使用 [SV \_ GSInstanceID](sv-gsinstanceid.md) 來識別正在執行之幾何著色器的實例。

下列著色器類型支援此屬性：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        | x        |       |         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型5屬性](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




