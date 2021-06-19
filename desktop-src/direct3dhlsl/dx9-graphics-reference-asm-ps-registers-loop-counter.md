---
title: '迴圈計數器 register (HLSL PS 參考) '
description: 瞭解圖元著色器的迴圈計數器暫存器。 此銀行中唯一的註冊是) 註冊 (aL 的目前迴圈計數器。
ms.assetid: 36999873-a251-4939-aac0-faa7f910bc33
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2a2f7f42c83308fa72ceae2875c35c600dfd7db
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405511"
---
# <a name="loop-counter-register-hlsl-ps-reference"></a>迴圈計數器 register (HLSL PS 參考) 

此銀行中唯一的註冊是) 註冊 (aL 的目前迴圈計數器。 它會在每次執行[迴圈 ps](loop---ps.md) / [endloop-ps](endloop---ps.md)區塊時自動遞增。 因此，它可以在區塊中用於相對定址（如有需要），而且在迴圈外使用它是不正確。



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2個 \_ sw | 2 \_ x | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| 迴圈計數器暫存器 |      |      |      |      |      |       |      | x    | x     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[寄存 器](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




