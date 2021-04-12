---
title: GetRenderTargetSampleCount
description: 取得呈現目標的樣本數。
ms.assetid: e813134e-c58c-4845-b519-c1074993801e
keywords:
- GetRenderTargetSampleCount HLSL
topic_type:
- apiref
api_name:
- GetRenderTargetSampleCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 96c159a2ed63684b4bad2cbc6fa789c2dbd76edf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104462585"
---
# <a name="getrendertargetsamplecount"></a>GetRenderTargetSampleCount

取得呈現目標的樣本數。



| *UINT* GetRenderTargetSampleCount ()  |
|-------------------------------------|



 

## <a name="parameters"></a>參數



| 項目                                                                                 | 描述 |
|--------------------------------------------------------------------------------------|-------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span>沒有<br/> |             |



 

## <a name="return-value"></a>傳回值

樣本數。

## <a name="remarks"></a>備註

您可以使用此函數和 [**GetRenderTargetSamplePosition**](dx-graphics-hlsl-getrendertargetsampleposition.md) ，找出轉譯目標的取樣位置數目和位置。

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

 

 





