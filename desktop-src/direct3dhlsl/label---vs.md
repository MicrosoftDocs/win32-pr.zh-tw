---
title: 標籤-vs
description: 將下一個指令標示為具有標籤索引。 |標籤-vs
ms.assetid: e1aee8bc-4655-4bd5-8012-bd7a2d46e712
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 81c36c3db93acdc82d725c9cf7893c52d7177bbe70e16378c3b86f39ec4d6a2e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854178"
---
# <a name="label---vs"></a>標籤-vs

將下一個指令標示為具有標籤索引。

## <a name="syntax"></a>Syntax



| 標籤 l\# |
|-----------|



 

其中會 \# 識別標籤號碼。

針對 vs \_ 2 \_ 0 和 vs \_ 2 \_ x，標籤編號必須介於0到15之間。

針對 vs \_ 2 \_ sw、vs \_ 3 \_ 0 和 vs \_ 3 \_ sw，標籤編號必須介於0到2047之間。

## <a name="remarks"></a>備註



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| label                  |      | x    | x    | x     | x    | x     |



 

此指令會定義位於下一個著色器指令的標籤。 標籤指令只能直接存在於 [ret](ret---vs.md) 指令之後， (定義上一個副程式或主要程式) 的結尾。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




