---
title: dst-vs
description: 計算距離向量。 |dst-vs
ms.assetid: 4315a29f-58e7-427f-aaa0-1fe1a81eb392
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d75eb61dd498d7a2f1d6bd9c5bd0dd9c52f3fd56625cb41b0026e9acce431ec6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068348"
---
# <a name="dst---vs"></a>dst-vs

計算距離向量。

## <a name="syntax"></a>Syntax



| dst dest、src0、src1 |
|----------------------|



 

其中

-   dest 是目的地暫存器。
-   src0 是來源註冊。
-   src1 是來源註冊。

## <a name="remarks"></a>備註



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Dst                    | x    | x    | x    | x     | x    | x     |



 

下列程式碼片段會顯示執行的作業：


```
dest.x = 1;
dest.y = src0.y * src1.y;
dest.z = src0.z;
dest.w = src1.w;
```



第一個來源運算元 (src0) 會假設為向量 (忽略、d \* d、d \* d、忽略) ，而第二個來源運算元 (src1) 會假設為向量 (忽略、1/d、忽略、1/d) 。 目的地 (dest) 是結果向量 (1、d、d \* d、1/d) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




