---
title: 步驟
description: 比較兩個值，並根據值大於的值傳回0或1。
ms.assetid: 1c1c4ec4-ae97-42ce-99af-71903e0b5edf
keywords:
- 步驟 HLSL
topic_type:
- apiref
api_name:
- step
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 27fe6985a4dfb4e77f1052b421a6c46c617395f46b4484f046b33919a935613f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119276508"
---
# <a name="step"></a>步驟

比較兩個值，並根據值大於的值傳回0或1。



| *ret* 步驟 (*y*， *x*)  |
|----------------------|



 

## <a name="parameters"></a>參數



| 項目                                                   | 描述                                                   |
|--------------------------------------------------------|---------------------------------------------------------------|
| <span id="y"></span><span id="Y"></span>*Y*<br/> | \[\]要比較的第一個浮點值。<br/>  |
| <span id="x"></span><span id="X"></span>*X*<br/> | \[\]要比較的第二個浮點值。<br/> |



 

## <a name="return-value"></a>傳回值

如果 *x* 參數大於或等於 *y* 參數，則為1。否則為0。

## <a name="remarks"></a>備註

此函數使用下列公式： (*x*  >=  *y*) ？ 1: 0。 根據 *x* 參數是否大於 *y* 參數，函數會傳回0或1。 若要計算0和1之間的平滑插補，請使用 [**smoothstep**](dx-graphics-hlsl-smoothstep.md) HLSL 內建函式。

## <a name="type-description"></a>類型描述



| Name  | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md) | 大小                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *y*   | 純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣** | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 任意                            |
| *x*   | 與輸入 *y* 相同                                                                                              | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | ) 為輸入 *y* 的相同維度 (s |
| *Ret* | 與輸入 *y* 相同                                                                                              | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | ) 為輸入 *y* 的相同維度 (s |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                       | 支援                   |
|------------------------------------------------------------------------------------|-----------------------------|
| [著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型 | 是                         |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md)                          | 是 (vs \_ 1 \_ 1 和 ps \_ 1 \_ 4)  |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**(DirectX HLSL) 內建函式**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

