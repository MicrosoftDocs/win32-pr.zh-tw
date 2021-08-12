---
description: 函式是以高階語言建立之著色器的組建區塊。 如果您想要以 C 樣式的語言撰寫著色器，而不是以組合語言撰寫，您會想要撰寫函數。
ms.assetid: vs|directx_sdk|~\functions.htm
title: " (Direct3D 9) 的效果函數語法"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b9de680f2f892e59f49e1dfd0850a128ca9ba34e2588e416059251d5058c44c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118297106"
---
# <a name="effect-function-syntax-direct3d-9"></a> (Direct3D 9) 的效果函數語法

函式是以高階語言建立之著色器的組建區塊。 如果您想要以 C 樣式的語言撰寫著色器，而不是以組合語言撰寫，您會想要撰寫函數。

## <a name="syntax"></a>Syntax


```
type id ( [ parameters ] )  
    { body }
```



函數不會變更效果中的參數值。

-   type-HLSL 型別的任何有效 [參考](../direct3dhlsl/dx-graphics-hlsl-reference.md) 。
-   識別碼-唯一的名稱。
-   參數函數參數。
-   body-函式的主體。

函式是從高階語言建立的。 請參閱 [HLSL 的參考](../direct3dhlsl/dx-graphics-hlsl-reference.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[效果格式](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
