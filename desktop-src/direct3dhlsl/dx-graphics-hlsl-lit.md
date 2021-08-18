---
title: 點燃
description: 傳回光源係數向量。
ms.assetid: 6ae116df-41b7-42f1-96cb-da480a7c1bab
keywords:
- 亮 HLSL
topic_type:
- apiref
api_name:
- lit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d3f941fe3aad52f352f5a36d3642141b31e08ef00c25dd8687c8fc7a8ed2de3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118791622"
---
# <a name="lit"></a>點燃

傳回光源係數向量。



| *ret* 燈亮 (*n \_ 點 \_ l*、 *n \_ 點 \_ h*、 *m*)  |
|------------------------------------------|



 

此函式會傳回光源係數向量 (環境、漫射、反光、1) where：

-   環境 = 1
-   擴散 = n ·l < 0？ 0： n ·我
-   反射 = n ·l < 0 \| \| n · h < 0？ 0： (n ·h) ^ m

其中向量 n 是一般向量，l 是淺色的方向，h 是半向量。

## <a name="parameters"></a>參數



| 項目                                                                       | 描述                                                                              |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="n_dot_l"></span><span id="N_DOT_L"></span>*n \_ 點 \_ l*<br/> | \[在 \] 正規化曲面標準和燈光向量的點乘積。<br/> |
| <span id="n_dot_h"></span><span id="N_DOT_H"></span>*n \_ 點 \_ h*<br/> | \[在 \] 半形向量和曲面法線的點乘積。<br/>       |
| <span id="m"></span><span id="M"></span>*m*<br/>                     | \[在 \] 反射指數中。<br/>                                                   |



 

## <a name="return-value"></a>傳回值

光源係數向量。

## <a name="type-description"></a>類型描述



| 名稱        | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md) | 大小 |
|-------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *n \_ 點 \_ l* | [**標量**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *n \_ 點 \_ h* | [**標量**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *m*         | [**標量**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *Ret*       | [**向量**](dx-graphics-hlsl-intrinsic-functions.md) | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

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

 

