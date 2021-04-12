---
description: 函式是以高階語言建立之著色器的組建區塊。 如果您想要以 C 樣式的語言撰寫著色器，而不是以組合語言撰寫，您會想要撰寫函數。
ms.assetid: vs|directx_sdk|~\functions.htm
title: " (Direct3D 9) 的效果函數語法"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21e239359877813e64acea8b5f404a6ade59c992
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509888"
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

 

 
