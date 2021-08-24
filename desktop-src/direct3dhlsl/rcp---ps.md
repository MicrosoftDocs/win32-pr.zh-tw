---
title: rcp-ps
description: 計算來源純量的倒數。 |rcp-ps
ms.assetid: d8dfc2b3-4404-47ec-aeaf-1adb7e7a342e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fba443d4a2e05794f8c1965e46a61c65edae50b95845f0f80faa0c0ab6c6bf71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510953"
---
# <a name="rcp---ps"></a>rcp-ps

計算來源純量的倒數。

## <a name="syntax"></a>Syntax



| rcp dst、src |
|--------------|



 

其中

-   dst 是目的地註冊。
-   src 是來源暫存器。 來源暫存器需要明確使用複寫 swizzle，也就是，只有其中一個. x、. y、a-z、w swizzle 元件 (或 r、g.、b.。必須指定對應的) 。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| rcp                   |      |      |      |      | x    | x    | x     | x    | x     |



 

如果輸入正好是1.0，則輸出必須正好為1.0。 0.0 的來源會產生無限大。

純量結果會複寫至目的地寫入遮罩中的所有通道。

精確度至少應該是 1.0/ (2 ²²) 範圍 (1.0，2.0) 的絕對錯誤，因為常見的實作為會分隔尾數和指數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




