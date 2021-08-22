---
title: 'frexp (Corecrt \_ math .h) '
description: 傳回指定之浮點值的尾數和指數。
ms.assetid: 9252feff-da85-4b3e-97db-1fcddd786695
keywords:
- frexp HLSL
topic_type:
- apiref
api_name:
- frexp
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f77ab30f525c37fcb2243bb6f634722420836f3893a4550edbb6604c8769773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119276618"
---
# <a name="frexp"></a>frexp

傳回指定之浮點值的尾數和指數。



| *ret* frexp (*x*， *exp*)  |
|-------------------------|



 

傳回值是尾數，而 *exp* 參數所傳回的值是指數。

## <a name="parameters"></a>參數



| 項目                                                         | 描述                                                                                                                                      |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/>       | \[在 \] 指定的浮點值中。 如果 *x* 參數為0，則此函式會針對尾數和指數傳回0。<br/> |
| <span id="exp"></span><span id="EXP"></span>*exp*<br/> | \[輸出 \] *x* 參數的傳回指數。<br/>                                                                                   |



 

## <a name="return-value"></a>傳回值

*X* 參數的尾數。

## <a name="type-description"></a>類型描述



| Name  | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md) | 大小                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | 純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣** | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 任意                            |
| *exp* | 與輸入 *x* 相同                                                                                              | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | ) 為輸入 *x* 的相同維度 (s |
| *Ret* | 與輸入 *x* 相同                                                                                              | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | ) 為輸入 *x* 的相同維度 (s |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                       | 支援           |
|------------------------------------------------------------------------------------|---------------------|
| [著色器模型 3 (DIRECTX HLSL) ](dx-graphics-hlsl-sm3.md) 和更高的著色器模型 | 是                 |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md)                          | 是 (ps \_ 2 \_ x 僅)  |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md)                          | 否                  |



 

## <a name="remarks"></a>備註

## <a name="requirements"></a>需求



| 需求 | 值 |
|-------------------|--------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Corecrt \_ math。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**(DirectX HLSL) 內建函式**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

