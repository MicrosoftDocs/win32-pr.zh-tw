---
title: SV_InsideTessFactor
description: 定義修補程式介面內的鑲嵌量。
ms.assetid: f0762aca-d84d-44c0-a163-9737ef92c1e5
keywords:
- SV_InsideTessFactor HLSL
topic_type:
- apiref
api_name:
- SV_InsideTessFactor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 043d1a43186623e81cb529d2906d4475291547d326bf2d75758c8ee696a812b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118285504"
---
# <a name="sv_insidetessfactor"></a>SV \_ InsideTessFactor

定義修補程式介面內的鑲嵌量。

## <a name="type"></a>類型



|  類型          | 輸入拓撲               |
|------------|----------------|
| float \[ 2\] | 四個修補程式     |
| FLOAT      | 三個修補程式      |
| unused     | 等值 線        |



 

鑲嵌式因數必須宣告為數組;它們無法封裝成單一向量。

## <a name="remarks"></a>備註

此值必須在輪廓著色器的 patch 常數函式期間定義。

如果使用四或三個修補程式，則為輪廓著色器所需的輸出值。 此值是網域著色器的必要輸入，以便硬體透過鑲嵌來比對簽章。

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[語意](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




