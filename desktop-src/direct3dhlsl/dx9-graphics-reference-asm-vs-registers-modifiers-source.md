---
title: 頂點著色器來源登錄修飾詞
description: 您可以套用來源修飾詞，以修改指令使用資料之前，從來源暫存器讀取的資料。
ms.assetid: 516ff7ca-0071-44ac-a246-612a9faa7e7b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3f50942d32691d9dc76aa30ddcef36df390fccfe058c31af3527c0eafe0d7df0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067978"
---
# <a name="vertex-shader-source-register-modifiers"></a>頂點著色器來源登錄修飾詞

您可以套用來源修飾詞，以修改指令使用資料之前，從來源暫存器讀取的資料。

## <a name="negate"></a>Negate

否定來源暫存器的內容。



| 元件修飾詞 | 描述     |
|--------------------|-----------------|
| \- R               | 來源否定 |



 

不能在這些指示的第二個來源登錄上使用否定修飾詞： [m3x2-vs](m3x2---vs.md)、 [m3x3-vs](m3x3---vs.md)、 [m3x4-vs](m3x4---vs.md)、 [m4x3-vs](m4x3---vs.md)、 [m4x4-vs](m4x4---vs.md)。



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| \-                     | x    | x    | x    | x     | x    | x     |



 

## <a name="absolute-value"></a>絕對值

取得註冊的絕對值。



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| abs                    |      |      |      |       | x    | x     |



 

如果任何第3版著色器從一或多個常數浮點數暫存器 (c \#) 讀取，下列其中一個條件必須為 true。

-   所有常數浮點數暫存器都必須使用 abs 修飾詞。
-   沒有常數浮點數暫存器可以使用 abs 修飾詞。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器暫存器修飾詞](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




