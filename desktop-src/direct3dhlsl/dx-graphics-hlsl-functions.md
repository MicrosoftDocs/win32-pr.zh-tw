---
title: '函數 (HLSL 參考) '
description: 函數會封裝 HLSL 語句。
ms.assetid: b6f934e5-eac7-4859-b1d0-698632011e1d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37086a030ad902f2bfb5deab52ffba620e97890bd13e7c6957170572087ce7c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118514576"
---
# <a name="functions-hlsl-reference"></a>函數 (HLSL 參考) 

函數會封裝 HLSL 語句。 這可讓您先對一組函數進行偵錯工具，然後在著色器或效果之間重複使用它們。 您可能會想要建立一個函式，以封裝頂點著色器、圖元著色器或紋理著色器的功能。 有時候，您可能會想要撰寫 helper 函式來執行一些常用的工作，然後從您的著色器函式呼叫該 helper 函式。 針對 HLSL 撰寫著色器函式的規則，與撰寫 C 函數非常類似。

-   [語法](dx-graphics-hlsl-function-syntax.md)
-   [參數](dx-graphics-hlsl-function-parameters.md)
-   [Return 陳述式](dx-graphics-hlsl-return.md)
-   [簽章](dx-graphics-hlsl-signatures.md)

HLSL 也有一些內建的 [**內建函式 (DIRECTX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)。 因為所有內建函式都會經過測試且效能優化，所以最好盡可能使用內建函式，而不是建立自己的函式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (DirectX HLSL 的語言語法) ](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 




