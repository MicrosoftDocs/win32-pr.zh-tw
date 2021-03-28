---
title: breakp-ps
description: 有條件地在最接近的 endloop-ps 或 endrep-ps 中斷目前的迴圈。 使用述詞註冊的其中一個元件做為條件，以判斷是否要執行指令。
ms.assetid: be219239-fccb-4561-8b71-083c47ba915b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6e358debb2377f08574997acd96c11f83d32e66c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373822"
---
# <a name="breakp---ps"></a>breakp-ps

有條件地在最接近的 [endloop-ps](endloop---ps.md) 或 [endrep-ps](endrep---ps.md)中斷目前的迴圈。 使用述詞註冊的其中一個元件做為條件，以判斷是否要執行指令。

## <a name="syntax"></a>Syntax



| breakp \[ ！ \]P。版|x|#a1|w |
|-----------------------------|



 

其中：

-   \[!\] 這是選擇性的否定修飾詞。
-   p0 是述詞 [註冊](dx9-graphics-reference-asm-ps-registers-predicate.md)。
-   {x \| y \| z \| w} 是 p0 上所需的複寫 swizzle。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| breakp                |      |      |      |      |      | x    | x     | x    | x     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




