---
title: rsq-ps
description: 將交互平方根 (計算來源純量的) 。 |rsq-ps
ms.assetid: deb1bd12-6347-4b1e-b21b-f3ef48da4c13
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 48a36715113678e199b3da22be9cdf118f385c15397a16ddd39bdd83622f76f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788698"
---
# <a name="rsq---ps"></a>rsq-ps

將交互平方根 (計算來源純量的) 。

## <a name="syntax"></a>Syntax



| rsq dst、src |
|--------------|



 

其中

-   dst 是目的地註冊。
-   src 是來源暫存器。 來源暫存器需要明確使用複寫 swizzle，也就是，只有其中一個. x、. y、a-z、w swizzle 元件 (或 r、g.、b.。必須指定對應的) 。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| rsq                   |      |      |      |      | x    | x    | x     | x    | x     |



 

在處理之前，會先取得絕對值。

精確度至少應該是 1.0/ (2 ²²) 範圍 (1.0，4.0) 的絕對錯誤，因為常見的實作為會分隔尾數和指數。

如果輸入正好是1.0，則輸出必須正好為1.0。 0.0 的來源會產生無限大。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




