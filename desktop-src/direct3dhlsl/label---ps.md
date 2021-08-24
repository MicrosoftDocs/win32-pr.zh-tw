---
title: 標籤-ps
description: 將下一個指令標示為具有標籤索引。 |標籤-ps
ms.assetid: 21afa062-c536-4891-ba69-ca5284b0539c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 921abbc0518182eaef17326082a395e5c5729d8ab550610fe71c8dfabe46dd4e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854198"
---
# <a name="label---ps"></a>標籤-ps

將下一個指令標示為具有標籤索引。

## <a name="syntax"></a>Syntax



| 標籤 l\# |
|-----------|



 

其中會 \# 識別標籤號碼。

若是 ps \_ 2 \_ x，標籤編號必須介於0到15之間。

針對 ps \_ 2 \_ sw、ps \_ 3 \_ 0 和 ps \_ 3 \_ sw，標籤編號必須介於0到2047之間。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| label                 |      |      |      |      |      | x    | x     | x    | x     |



 

此指令會定義位於下一個著色器指令的標籤。 標籤指令只能直接存在於 [ret](ret---ps.md) 指令之後， (定義上一個副程式或主要程式) 的結尾。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




