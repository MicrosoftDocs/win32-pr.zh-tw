---
title: smoothstep
description: 如果 x 位於0到1的範圍內，則傳回介於0和1之間的平滑 Hermite 插補。
ms.assetid: 6a879d82-f5ab-4e9b-bc9c-8988cbe6aa82
keywords:
- smoothstep HLSL
topic_type:
- apiref
api_name:
- smoothstep
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 64e828b52a4d4517e53ba1f1aaf0f687255ad02b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971708"
---
# <a name="smoothstep"></a>smoothstep

如果 *x* 位於 \[ *min*、 *max* 的範圍內，則傳回0和1之間的平滑 Hermite 插補 \] 。



| *ret* smoothstep (*min*， *max*， *x*)  |
|-------------------------------------|



 

## <a name="parameters"></a>參數



| 項目                                                         | 描述                                               |
|--------------------------------------------------------------|-----------------------------------------------------------|
| <span id="min"></span><span id="MIN"></span>*化*<br/> | \[在 \] *x* 參數的最小範圍內。<br/> |
| <span id="max"></span><span id="MAX"></span>*麥克斯*<br/> | \[在 \] *x* 參數的最大範圍內。<br/> |
| <span id="x"></span><span id="X"></span>*X*<br/>       | \[\]指定要插入的值。<br/> |



 

## <a name="return-value"></a>傳回值

如果 *x* 小於 *最小值*，則傳回 0;如果 *x* 大於 *最大值*，則為1。否則，如果 *x* 是在 \[ *min*、 *max* 的範圍內，則介於0和1之間的值 \] 。

## <a name="remarks"></a>備註

使用 **smoothstep** HLSL 內建函式可在兩個值之間建立順暢的轉換。 例如，您可以使用此函數順暢地混合兩種色彩。

## <a name="type-description"></a>類型描述



| Name  | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md) | 大小                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | 純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣** | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 任意                            |
| *min* | 與輸入 *x* 相同                                                                                              | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | ) 為輸入 *x* 的相同維度 (s |
| *max* | 與輸入 *x* 相同                                                                                              | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | ) 為輸入 *x* 的相同維度 (s |
| *Ret* | 與輸入 *x* 相同                                                                                              | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | ) 為輸入 *x* 的相同維度 (s |



 

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

 

