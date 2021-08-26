---
title: '述詞 register (HLSL PS 參考) '
description: 這個圖元著色器輸出暫存器包含每個通道的布林值。
ms.assetid: dc5bff90-4efa-4390-b744-dd1e894ff540
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8cc8404c9a6be87951142ff3473b283a57f4814b729a8ad5a462f9069b20f3ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950028"
---
# <a name="predicate-register-hlsl-ps-reference"></a>述詞 register (HLSL PS 參考) 

這個圖元著色器輸出暫存器包含每個通道的布林值。

下列版本支援述詞註冊：



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2個 \_ sw | 2 \_ x | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| 述詞註冊    |      |      |      |      |      |       | x    | x    | x     |



 

以下是註冊屬性。



| 註冊類型 | 計數 | R/W | \# 讀取埠 | \# 讀取/inst | 尺寸 | RelAddr | Defaults | 需要 DCL |
|---------------|-------|-----|---------------|---------------|-----------|---------|----------|--------------|
| 述詞 (p)   | 1     | R/W | 1             | 1             | 4         | N/A     | 無     | N            |



 

您可以使用 [setp 的 \_ 複合-ps](setp-comp---ps.md)來修改述詞註冊。 此註冊沒有預設值;應用程式必須先設定註冊才能使用。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[寄存 器](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




