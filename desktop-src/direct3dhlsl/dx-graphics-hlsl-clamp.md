---
title: 鉗
description: 將指定的值個至指定的最小和最大範圍。
ms.assetid: bcfafcec-3f9c-4b65-950c-da34184d5cdb
keywords:
- 夾具 HLSL
topic_type:
- apiref
api_name:
- clamp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a0350127a26b0c65762e6c927ea38ca944101dcd646026713de231e33e987fb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043836"
---
# <a name="clamp"></a>鉗

將指定的值個至指定的最小和最大範圍。



| *ret* 夾具 (*x*、 *min*、 *max*)  |
|--------------------------------|



 

## <a name="parameters"></a>參數



| 項目                                                         | 描述                                    |
|--------------------------------------------------------------|------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/>       | \[在 [夾具] 中 \] 的值。<br/>            |
| <span id="min"></span><span id="MIN"></span>*化*<br/> | \[在 \] 指定的最小範圍內。<br/> |
| <span id="max"></span><span id="MAX"></span>*麥克斯*<br/> | \[在 \] 指定的最大範圍內。<br/> |



 

## <a name="return-value"></a>傳回值

*X* 參數的壓制值。

## <a name="remarks"></a>備註

若為-INF 或 INF 的值，則會如預期般運作。 不過，若為 NaN 的值，則結果為未定義。

## <a name="type-description"></a>類型描述



| 名稱  | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md)                 | 大小                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| *x*   | 純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣** | [**float**](/windows/desktop/WinProg/windows-data-types)、 [ **int**](/windows/desktop/WinProg/windows-data-types) | 任意                            |
| *min* | 與輸入 *x* 相同                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types)、 [ **int**](/windows/desktop/WinProg/windows-data-types) | ) 為輸入 *x* 的相同維度 (s |
| *max* | 與輸入 *x* 相同                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types)、 [ **int**](/windows/desktop/WinProg/windows-data-types) | ) 為輸入 *x* 的相同維度 (s |
| *Ret* | 與輸入 *x* 相同                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types)、 [ **int**](/windows/desktop/WinProg/windows-data-types) | ) 為輸入 *x* 的相同維度 (s |



 

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

 

