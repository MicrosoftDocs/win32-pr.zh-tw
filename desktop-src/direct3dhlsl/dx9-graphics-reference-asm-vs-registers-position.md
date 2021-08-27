---
title: 位置註冊
description: 此頂點著色器輸出暫存器包含每個頂點的位置資料。
ms.assetid: 98f71027-d94b-4dd0-a6b6-4b263954eff9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cda82431990ed3ea545adfcc5e6eb2801be0607d8bac45aa1bcd8c0e121f3d68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023898"
---
# <a name="position-register"></a>位置註冊

此頂點著色器輸出暫存器包含每個頂點的位置資料。



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2個 \_ sw | 2 \_ x | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| 位置註冊      | x    | x    | x     | x    | x    | x     |



 

暫存器包含的屬性會決定每個註冊的行為。



| 屬性        | 描述 |
|-----------------|-------------|
| 名稱            | oPos        |
| 計數           | 1個向量    |
| I/o 許可權 | 唯寫。 |



 

值是同質剪切空間中的位置。 這個值必須由頂點著色器撰寫。

範例


```
    dcl_position v0
    
    def c40, 0.0f,0.0f,0.0f,0.0f;
    // transform into projection space
    m4x4 r0,v0,c8
    max r0.z,c40.z,r0.z //clamp to 0
    max r0.w,c12.x,r0.w //clamp to near clip plane
    mov oPos,r0   
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器暫存器](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




