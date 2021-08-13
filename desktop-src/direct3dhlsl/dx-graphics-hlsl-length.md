---
title: 長度
description: 傳回指定之浮點數向量的長度。
ms.assetid: eb06c87c-d536-448e-becb-762783cc2a77
keywords:
- 長度 HLSL
topic_type:
- apiref
api_name:
- length
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1d6c361a7ad16216d686ab71747354a9b1ba3184d88759ed1e994c152c7b3636
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118791724"
---
# <a name="length"></a>長度

傳回指定之浮點數向量的長度。



| *ret* 長度 (*x*)  |
|-------------------|



 

## <a name="parameters"></a>參數



| Item                                                   | 描述                                     |
|--------------------------------------------------------|-------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | 指定的浮點向量。<br/> |



 

## <a name="return-value"></a>傳回值

表示 *x* 參數長度的浮點純量。

## <a name="type-description"></a>類型描述



| 名稱  | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md) | 大小 |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *x*   | [**向量**](dx-graphics-hlsl-intrinsic-functions.md) | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 任意  |
| *Ret* | [**標量**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1    |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                       | 支援           |
|------------------------------------------------------------------------------------|---------------------|
| [著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型 | 是                 |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md)                          | 是 (\_ \_ 只有) 的 vs 1 |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**(DirectX HLSL) 內建函式**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

