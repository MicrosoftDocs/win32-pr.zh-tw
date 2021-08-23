---
title: '述詞 Register (HLSL 與參考) '
description: 此頂點著色器輸出暫存器包含每個通道的布林值。
ms.assetid: 4b06e19a-78c7-4886-a0e2-225d419282e7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 28392f7bb9c2f59bd766e42ec21fb87a854b08bedd8336ebb6f7249b7eccb940
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119572"
---
# <a name="predicate-register-hlsl-vs-reference"></a>述詞 Register (HLSL 與參考) 

此頂點著色器輸出暫存器包含每個通道的布林值。

下列版本支援述詞註冊。



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2個 \_ sw | 2 \_ x | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| 述詞註冊     |      |      |       | x    | x    | x     |



 

以下是註冊屬性。



| 註冊類型 | 計數 | R/W | \# 讀取埠 | \# 讀取/inst | 尺寸 | RelAddr | Defaults | 需要 DCL |
|---------------|-------|-----|---------------|---------------|-----------|---------|----------|--------------|
| 述詞 (p)   | 1     | R/W | 1             | 1             | 4         | N/A     | 無     | N            |



 

您可以使用 [setp \_ 複合-vs](setp-comp---vs.md)來修改述詞註冊。此暫存器沒有預設值，因此應用程式必須在使用之前先設定註冊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器暫存器](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




