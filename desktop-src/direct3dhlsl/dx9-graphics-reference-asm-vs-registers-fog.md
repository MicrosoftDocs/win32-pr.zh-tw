---
title: 霧化暫存器
description: 此頂點著色器輸出暫存器包含每個頂點的霧化色彩。
ms.assetid: b2b06aa9-ad75-48df-857d-fd8719176713
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c3f0e39c0670176b6233f61f0ba50596c92ca4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104971424"
---
# <a name="fog-register"></a>霧化暫存器

此頂點著色器輸出暫存器包含每個頂點的霧化色彩。

暫存器包含的屬性會決定每個註冊的行為。



| 屬性        | 描述                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| Name            | oFog                                                                                            |
| Count           | 一個向量，其中只可使用一個元件，而且必須由元件遮罩指定 |
| I/o 許可權 | 唯寫。                                                                                     |



 

輸出霧化值會註冊。 值是要插入的霧化因數，然後路由傳送至霧化資料表。 只會使用霧化的純量 x 元件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器暫存器](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




