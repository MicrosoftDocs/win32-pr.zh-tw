---
title: 點大小暫存器
description: 此頂點著色器輸出暫存器包含每個頂點的點大小資料。
ms.assetid: 1aa6cd7d-9d29-4e7e-8448-8b9a6b251a02
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6de5c2fba55ce9cdfcee535ec001a89cbebcdddc5e3685224f9eb0c560870534
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119662"
---
# <a name="point-size-register"></a>點大小暫存器

此頂點著色器輸出暫存器包含每個頂點的點大小資料。



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2個 \_ sw | 2 \_ x | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| 點大小暫存器    | x    | x    | x     | x    | x    | x     |



 

暫存器包含的屬性會決定每個註冊的行為。



| 屬性        | 描述                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| 名稱            | 選擇                                                                                            |
| 計數           | 1個向量，只能使用1個元件，而且必須由元件遮罩指定。 |
| I/o 許可權 | 唯寫。                                                                                     |



 

只會使用點大小的純量 x 部分。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器暫存器](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




