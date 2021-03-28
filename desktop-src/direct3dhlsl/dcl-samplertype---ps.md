---
title: 'dcl_samplerType (sm2、sm3-ps asm) '
description: 宣告圖元著色器取樣器。
ms.assetid: c90ff5b6-f89a-4993-8a5d-dbbc4a7896b0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 934931d6063ac264a2e6685104f8ed6fbdaaa64e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022855"
---
# <a name="dcl_samplertype-sm2-sm3---ps-asm"></a>dcl \_ samplerType (sm2、sm3-ps asm) 

宣告圖元著色器取樣器。

## <a name="syntax"></a>Syntax



|                      |
|----------------------|
| dcl \_ samplerType s\# |



 

其中：

-   \_samplerType 會定義取樣器資料類型。 這會決定取樣時，每個材質座標需要多少座標。 會定義下列紋理座標維度。
    -   \_二 維和
    -   \_立方體
    -   \_體積
-   s \# 會識別一個取樣器，其中 s 是取樣器的縮寫，而 \# 是取樣器數目。 取樣器是虛擬暫存器，因為您無法直接讀取或寫入它們。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dcl \_ samplerType      |      |      |      |      | x    | x    | x     | x    | x     |



 

所有 \_ 的 dcl samplerType 指令都必須出現在第一個可執行指令之前。

## <a name="example"></a>範例


```
dcl_cube t0.rgb;  // Define a 3D texture map.

add r0, r0, t0;   // Perturb texture coordinates. 
texld r0, s0, r0; // Load r0 with a color sampled from stage0
                  //   at perturbed texture coordinates r0.
                  // This is a dependent texture read.
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




