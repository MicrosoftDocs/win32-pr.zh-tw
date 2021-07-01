---
title: SV_TessFactor
description: 在修補程式的每個邊緣上定義鑲嵌量。
ms.assetid: 970ff744-da5b-4933-866c-dd38b85fb48d
keywords:
- SV_TessFactor HLSL
topic_type:
- apiref
api_name:
- SV_TessFactor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 308034fe607283ef9f1213cca1cabb4a7229765e
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118893"
---
# <a name="sv_tessfactor"></a>SV \_ TessFactor

在修補程式的每個邊緣上定義鑲嵌量。

## <a name="type"></a>類型



|  類型          |  輸入拓撲              |
|------------|----------------|
| float \[ 4\] | 四個修補程式     |
| float \[ 3\] | 三個修補程式      |
| float \[ 2\] | 等值 線        |



 

鑲嵌因數必須宣告為數組;它們無法封裝成單一向量。

## <a name="remarks"></a>備註

您必須在輪廓著色器的 patch 常數函式期間定義鑲嵌式因素的值。

如果使用四或三個修補程式，則為輪廓著色器所需的輸出值。 此值也是網域著色器的必要輸入值，可符合鑲嵌式階段之間的修補程式常數資料簽章。

針對等值線，SV TessFactor 中的第一個值 \_ 是行密度鑲嵌因數，第二個值是行詳細資料鑲嵌因數。

### <a name="tri-patch-tessellation-factors"></a>三個修補程式鑲嵌因素

第一個元件針對 patch 的 u = = 0 邊緣提供 tesselation 因素。 第二個元件提供 patch 的 v = = 0 邊緣的 tesselation 因素。 第三個元件針對 patch 的 w = = 0 邊緣提供 tesselation 因素。

### <a name="quad-patch-tessellation-factors"></a>四個修補程式鑲嵌因素

第一個元件針對 patch 的 u = = 0 邊緣提供 tesselation 因素。 第二個元件提供 patch 的 v = = 0 邊緣的 tesselation 因素。 第三個元件針對 patch 的 u = = 1 邊緣提供 tesselation 因素。 第四個元件提供 patch 的 v = = 1 邊緣的 tesselation 因數。 邊緣的順序會以順時針的方式從 u = = 0 邊緣（即修補程式左邊）開始，並從 v = = 0 邊緣（即修補程式頂端）開始。

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

 

 




