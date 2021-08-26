---
title: 新增-vs
description: 新增兩個向量。 |新增-vs
ms.assetid: f66d3264-68be-4a4f-84fc-cc0f6c4245c9
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2a8b38a0858a4410c18fead1d0123b97c041bf8368be40a08fed4220f8fee3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983558"
---
# <a name="add---vs"></a>新增-vs

新增兩個向量。

## <a name="syntax"></a>Syntax



| 新增 dst、src0、src1 |
|---------------------|



 

其中

-   dst 是目的地註冊。
-   src0 是來源註冊。
-   src1 是來源註冊。

## <a name="remarks"></a>備註



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| add                    | x    | x    | x    | x     | x    | x     |



 

下列程式碼片段會顯示已執行的作業。


```
dest.x = src0.x + src1.x;
dest.y = src0.y + src1.y;
dest.z = src0.z + src1.z;
dest.w = src0.w + src1.w;
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




