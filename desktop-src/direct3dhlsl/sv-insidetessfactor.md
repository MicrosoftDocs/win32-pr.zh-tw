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
ms.openlocfilehash: 90d31aa6a11ce8e2bdd75ff1171705cc9b3de437
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826612"
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



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[語意](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




