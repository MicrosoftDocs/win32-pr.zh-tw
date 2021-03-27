---
title: '暫時註冊 (HLSL PS 參考) '
description: 圖元著色器輸入暫存登錄用來保存中繼結果。
ms.assetid: e61daaa1-0a9b-4b1c-b91c-56573be59ed9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7aebee99a693ac629d9cc8a372fba7589a9e29ef
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "103841716"
---
# <a name="temporary-register-hlsl-ps-reference"></a>暫時註冊 (HLSL PS 參考) 

圖元著色器輸入暫存登錄用來保存中繼結果。

Syntax


```
no declaration is required
```





| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2個 \_ sw | 2 \_ x | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| 暫時註冊    |      |      |      |      | x    | x     | x    | x    | x     |



 

-   有12個圖元著色器暫存暫存器： r0 至 r11。
-   這些暫存器是用來在計算期間儲存中繼結果。
-   如果暫存登錄使用先前程式碼未定義的元件，著色器驗證將會失敗。
-   這些至少是浮點精確度。
-   最多可以在單一指令中使用三個。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[寄存 器](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




