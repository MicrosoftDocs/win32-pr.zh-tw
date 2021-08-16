---
title: 色彩註冊
description: 這些頂點著色器輸出暫存器包含色彩值。
ms.assetid: fd36e207-7312-4c7e-b664-b2de9ba1ebcf
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b19850985002ad9c36a6a6366f744106cb041db858f9df9b755996e114fdf6c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512284"
---
# <a name="color-register"></a>色彩註冊

這些頂點著色器輸出暫存器包含色彩值。 

| 註冊 | Description              |
|----------|--------------------------|
| oD0      | 擴散色彩註冊。  |
| oD1      | 反射色彩註冊。 |



 

OD0 值會插入，並寫入至圖元著色器色彩 register 0 (v0) 。 OD1 值會插入並寫入至圖元著色器色彩註冊 1 (v1) 。 如需圖元著色器色彩暫存器的詳細資訊，請參閱圖元著色器 [輸入色彩註冊](dx9-graphics-reference-asm-ps-registers-input-color.md) 主題。

## <a name="remarks"></a>備註

範例


```
min oD0, r0, c1.x    
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器暫存器](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




