---
title: 變為
description: 調換指定的輸入矩陣。
ms.assetid: 2a2ff2fb-73f0-4bb8-af83-38fe0567d122
keywords:
- 換位 HLSL
topic_type:
- apiref
api_name:
- transpose
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e6e545e657e6d9eaded92affba5bbb52a22222db2bf87acd5dddb72335a17ab0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119752"
---
# <a name="transpose"></a>變為

調換指定的輸入矩陣。



| ret 變換 (*x*)  |
|--------------------|



 

## <a name="parameters"></a>參數



| 項目                                                   | 描述                             |
|--------------------------------------------------------|-----------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[在 \] 指定的矩陣中。<br/> |



 

## <a name="return-value"></a>傳回值

*X* 參數的已轉換值。

## <a name="remarks"></a>備註

如果來源矩陣的維度是 rows 資料 *行，則* 產生的矩陣會是資料 *行* 資料 *列*。

## <a name="type-description"></a>類型描述



| 名稱 | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md)                                                         | 大小                                                                                   |
|------|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| *x*  | [**矩陣**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)、 [**int**](/windows/desktop/WinProg/windows-data-types)、 [**bool**](/windows/desktop/WinProg/windows-data-types) | 任意                                                                                    |
| Ret  | [**矩陣**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)、 [**int**](/windows/desktop/WinProg/windows-data-types)、 [**bool**](/windows/desktop/WinProg/windows-data-types) | rows = 與輸入 *x* 相同數目的資料行，資料行 = 與輸入 *x* 相同的資料列數目 |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                       | 支援 |
|------------------------------------------------------------------------------------|-----------|
| [著色器模型 1 (DIRECTX HLSL) ](dx-graphics-hlsl-sm1.md) 和更高的著色器模型 | 是       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**(DirectX HLSL) 內建函式**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

