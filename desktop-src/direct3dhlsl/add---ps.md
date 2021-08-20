---
title: 新增-ps
description: 新增兩個向量。 |新增-ps
ms.assetid: f7d29a66-879b-4160-82fd-0a1b2076559a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2e20090b920c75e2fcfef94e9971d447ceb86c50c1d1b6a0d513d3fa2704c3cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117909261"
---
# <a name="add---ps"></a>新增-ps

新增兩個向量。

## <a name="syntax"></a>Syntax



| 新增 dst、src0、src1 |
|---------------------|



 

其中

-   dst 是目的地註冊。
-   src0 是來源註冊。
-   src1 是來源註冊。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| add                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

下列程式碼片段會顯示已執行的作業。


```
dest.x = src0.x + src1.x;
dest.y = src0.y + src1.y;
dest.z = src0.z + src1.z;
dest.w = src0.w + src1.w;
```



## <a name="instruction-information"></a>指示資訊



|   需求                       | 值           |
|--------------------------|------------|
| 最低作業系統 | Windows 98 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




