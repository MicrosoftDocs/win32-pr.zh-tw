---
title: StructuredBuffer
description: 唯讀緩衝區，它可以採用結構的 T 型別。
ms.assetid: fe2ec0b8-0e19-42b6-9dad-c992ecdeb19e
keywords:
- StructuredBuffer HLSL
topic_type:
- apiref
api_name:
- StructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 524078780ac28d691c4999491bed146a04d34439
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990927"
---
# <a name="structuredbuffer"></a>StructuredBuffer

唯讀緩衝區，它可以採用結構的 T 型別。



| 方法                                                             | 描述                            |
|--------------------------------------------------------------------|----------------------------------------|
| [**GetDimensions**](sm5-object-structuredbuffer-getdimensions.md) | 取得資源維度。          |
| [**載入**](structuredbuffer-load.md)                              | 讀取緩衝區資料。                     |
| [**運算子\[\]**](sm5-object-structuredbuffer-operatorindex.md)  | 傳回唯讀的資源變數。 |



 

系結到此資源的 UAV 格式必須以 DXGI \_ 格式 \_ 未知格式建立。

若要瞭解 [結構化緩衝區](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources)的詳細資訊，請參閱總覽材質。

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此物件。



| 著色器模型                                                                                                                                                                                                            | 支援 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| [著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型 4 (可用於某些 direct3d 10 裝置上 direct3d 11 中的計算和圖元著色 [器](dx-graphics-hlsl-sm4.md) 。 ) <br/> | 是       |



 

下列著色器類型支援此物件。



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器模型5物件](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

