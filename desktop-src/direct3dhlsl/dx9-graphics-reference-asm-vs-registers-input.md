---
title: 輸入暫存器
description: 輸入暫存器
ms.assetid: 7cd8e555-4e69-4905-a541-62e09b41a602
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 983f0520ccc50fa1683d4b8254ac436fff7491a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932358"
---
# <a name="input-register"></a>輸入暫存器

頂點著色器輸入暫存器。

使用一或多個輸入頂點資料流程的每個頂點 (的資料) 會在執行頂點著色器之前載入至頂點輸入暫存器。 輸入暫存器由 16 4-元件浮點向量所組成，指定為 v0 到 v15。 這些暫存器是唯讀的。 輸入暫存器會透過頂點宣告系結至頂點資料。

下列暫存器屬性會控制每個註冊的行為：



| 屬性        | 描述                                                                                   |
|-----------------|-----------------------------------------------------------------------------------------------|
| Name            | v \[ n \] -n 是選擇性的註冊編號。 如果省略，則預設值為0。     |
| Count           | 最多16個暫存器，v0-v15。                                                          |
| I/o 許可權 | 唯讀。 此暫存器無法由 API 或在著色器中寫入。                   |
| 讀取埠      | 1. 這是在單一指令內可以讀取暫存器的次數。 請參閱下文。 |



 

任何單一指令都只能存取一個頂點輸入暫存器。 不過，指令中的每個來源都可以獨立地 swizzle，並在該向量被讀取時對其進行否定。

## <a name="example"></a>範例

以下範例使用頂點宣告來系結2D 頂點位置資料，以註冊 v0。

頂點宣告屬於應用程式：


```
D3DVERTEXELEMENT9 decl[] =
{
    { 0, 0, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
      D3DDECL_END()
};
```



以下是對應的頂點著色器宣告：


```
dcl_position v0
```





| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2個 \_ sw | 2 \_ x | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| 位置註冊      | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器暫存器](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




