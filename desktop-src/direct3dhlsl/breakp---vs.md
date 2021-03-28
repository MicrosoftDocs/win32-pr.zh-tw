---
title: breakp-vs
description: 有條件地在最接近的 endloop （vs 或 endrep）中斷目前的迴圈。請使用述詞註冊的其中一個元件做為條件，以判斷是否要執行指令。
ms.assetid: 940252a0-6f6a-45d8-9d2f-315cc97686ca
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dbd0d5e20040bc2d353287eb4243c9e9d6d21dc8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022820"
---
# <a name="breakp---vs"></a>breakp-vs

有條件地中斷最接近 [endloop-vs](endloop---vs.md) 或 [endrep-vs](endrep---vs.md)的目前迴圈。使用述詞註冊的其中一個元件做為條件，以判斷是否要執行指令。

## <a name="syntax"></a>Syntax



| breakp \[ ！ \]P。版|x|#a1|w |
|-----------------------------|



 

其中：

-   \[!\] 選擇性的布林值。
-   p0 是述詞註冊。 請參閱述詞 [註冊](dx9-graphics-reference-asm-vs-registers-predicate.md)。
-   {x \| y \| z \| w} 是 p0 上所需的複寫 swizzle。

## <a name="remarks"></a>備註



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| breakp                 |      |      | x    | x     | x    | x     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




