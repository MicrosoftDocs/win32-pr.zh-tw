---
title: acos
description: 傳回指定之值的反余弦值。
ms.assetid: c9bc33b8-d586-4c64-9453-5ab97396f2cf
keywords:
- acos HLSL
topic_type:
- apiref
api_name:
- acos
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 155915f1a9163b8569b9c92a396161659df2addfc7e27f2acde8f05bf49808d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673608"
---
# <a name="acos"></a>acos

傳回指定之值的反余弦值。



| *ret* acos (*x*)  |
|-----------------|



 

## <a name="parameters"></a>參數



| 項目                                                   | 描述                                                                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[在 \] 指定的值中。 每個元件都應該是介於-1 到1範圍內的浮點值。<br/> |



 

## <a name="return-value"></a>傳回值

*X* 參數的反余弦。

## <a name="type-description"></a>類型描述



| 名稱  | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md) | 大小                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | 純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣** | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 任意                            |
| *Ret* | 與輸入 *x* 相同                                                                                              | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | ) 為輸入 *x* 的相同維度 (s |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                       | 支援     |
|------------------------------------------------------------------------------------|---------------|
| [著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型 | 是           |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md)                          | \_ \_ 僅限 vs 1 1 |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**(DirectX HLSL) 內建函式**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

