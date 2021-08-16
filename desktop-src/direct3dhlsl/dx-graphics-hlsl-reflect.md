---
title: 反映
description: 使用事件光線和曲面法線傳回反映向量。
ms.assetid: e321b399-f382-4585-83a6-a7da1f7b2327
keywords:
- 反映 HLSL
topic_type:
- apiref
api_name:
- reflect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2abc7100eae846fc3d2f21b013676aa3dbc64574a7e8cdb8a14dc492ceb33f75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725942"
---
# <a name="reflect"></a>反映

使用事件光線和曲面法線傳回反映向量。



| *ret* 反映 (*i*， *n*)  |
|-------------------------|



 

## <a name="parameters"></a>參數



| 項目                                                   | 描述                                          |
|--------------------------------------------------------|------------------------------------------------------|
| <span id="i"></span><span id="I"></span>*我*<br/> | \[在 \] 浮點事件向量中。<br/> |
| <span id="n"></span><span id="N"></span>*n-1*<br/> | \[在 \] 浮點的一般向量中。<br/>   |



 

## <a name="return-value"></a>傳回值

浮點數、反映向量。

## <a name="remarks"></a>備註

此函數會使用下列公式來計算反映向量： v = i-2 \* n \* 點 (i n) 。

## <a name="type-description"></a>類型描述



| 名稱  | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md) | 大小                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *i*   | [**向量**](dx-graphics-hlsl-intrinsic-functions.md) | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 任意                            |
| *n*   | [**向量**](dx-graphics-hlsl-intrinsic-functions.md) | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 相同維度 (s) 為輸入 *i* |
| *Ret* | [**向量**](dx-graphics-hlsl-intrinsic-functions.md) | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 相同維度 (s) 為輸入 *i* |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                       | 支援 |
|------------------------------------------------------------------------------------|-----------|
| [著色器模型 1 (DIRECTX HLSL) ](dx-graphics-hlsl-sm1.md) 和更高的著色器模型 | 是       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**(DirectX HLSL) 內建函式**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

