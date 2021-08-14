---
title: GetRenderTargetSamplePosition
description: 取得給定範例索引的取樣位置 (x，y) 。
ms.assetid: 07f14d1c-4fe5-4838-acce-d664cdc641e6
keywords:
- GetRenderTargetSamplePosition HLSL
topic_type:
- apiref
api_name:
- GetRenderTargetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a406fcbd023d0688baf51cabbfea53438f3d58a6fba4d1fc7d1bf8d33077262
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118514332"
---
# <a name="getrendertargetsampleposition"></a>GetRenderTargetSamplePosition

取得給定範例索引的取樣位置 (x，y) 。

float<2> GetRenderTargetSamplePosition ( in int<1> Index<br/>);



 

## <a name="parameters"></a>參數



| Item                                                                                       | 描述                                  |
|--------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="Index"></span><span id="index"></span><span id="INDEX"></span>*指數*<br/> | \[以 \] 零為基底的範例索引。<br/> |



 

## <a name="return-value"></a>傳回值

給定範例的 (x，y) 位置。

## <a name="remarks"></a>備註

您可以使用此函數和 [**GetRenderTargetSampleCount**](dx-graphics-hlsl-getrendertargetsamplecount.md) ，找出轉譯目標的取樣位置數目和位置。

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                        | 支援 |
|---------------------------------------------------------------------|-----------|
| [著色器模型 4](dx-graphics-hlsl-sm4.md) 和更高的著色器模型 | 是       |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md)           | 否        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md)           | 否        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md)           | 否        |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**(DirectX HLSL) 內建函式**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





