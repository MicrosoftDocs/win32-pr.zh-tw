---
title: faceforward
description: 如有需要，請將表面垂直 (翻轉，) 以與 i 相反的方向呈現;傳回 n 中的結果。
ms.assetid: 6530a928-d221-49e4-ab68-6285c3db370f
keywords:
- faceforward HLSL
topic_type:
- apiref
api_name:
- faceforward
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 253d581ef5ea2eddac55c63245039f1ccda6c0e73032468d1598fb919e850a18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950378"
---
# <a name="faceforward"></a>faceforward

如有需要，請將表面垂直 (翻轉，) 以與 i 相反的方向呈現;傳回 n 中的結果。



| *ret* faceforward (*n*、 *i*、 *ng*)  |
|-----------------------------------|



 

此函式會使用下列公式：-*n*  sign (點 (*i*， *ng*) ) 。

## <a name="parameters"></a>參數



| 項目                                                      | 描述                                                                                                     |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span id="n"></span><span id="N"></span>*n-1*<br/>    | \[在 \] 產生的浮點表面標準向量中。<br/>                                           |
| <span id="i"></span><span id="I"></span>*我*<br/>    | \[在 \] 浮點的事件向量中，從視圖位置指向陰影位置。<br/> |
| <span id="ng"></span><span id="NG"></span>*議員*<br/> | \[在 \] 浮點介面標準向量中。<br/>                                                       |



 

## <a name="return-value"></a>傳回值

面向視圖方向的浮點、表面法線向量。

## <a name="type-description"></a>類型描述



| 名稱  | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md) | 大小                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *n*   | [**向量**](dx-graphics-hlsl-intrinsic-functions.md) | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 任意                            |
| *i*   | [**向量**](dx-graphics-hlsl-intrinsic-functions.md) | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 相同維度 (s) 作為輸入 *n* |
| *議員*  | [**向量**](dx-graphics-hlsl-intrinsic-functions.md) | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 輸入 *n* 的相同維度   |
| *Ret* | [**向量**](dx-graphics-hlsl-intrinsic-functions.md) | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 輸入 *n* 的相同維度   |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                       | 支援             |
|------------------------------------------------------------------------------------|-----------------------|
| [著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型 | 是                   |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1 和 ps \_ 1 \_ 4 |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**(DirectX HLSL) 內建函式**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

