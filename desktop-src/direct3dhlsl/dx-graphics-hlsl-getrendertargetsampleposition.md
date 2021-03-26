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
ms.openlocfilehash: 3b0cd944b175522ab7d722ae791f3548c6633b71
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678051"
---
# <a name="getrendertargetsampleposition"></a>GetRenderTargetSamplePosition

取得給定範例索引的取樣位置 (x，y) 。



|                                                                                  |
|----------------------------------------------------------------------------------|
| float<2> GetRenderTargetSamplePosition ( in int<1> Index<br/>); |



 

## <a name="parameters"></a>參數



| 項目                                                                                       | 描述                                  |
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
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md)           | 不可以        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md)           | 不可以        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md)           | 不可以        |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**(DirectX HLSL) 內建函式**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





