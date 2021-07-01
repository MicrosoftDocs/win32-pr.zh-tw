---
title: 'dcl_samplerType (sm3-vs asm) '
description: 宣告頂點著色器取樣器。
ms.assetid: 733307ac-24ab-4db7-bf70-58a83b4c39b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2fbcb934ad591274d743f09c810de2db42278261
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129866"
---
# <a name="dcl_samplertype-sm3---vs-asm"></a>dcl \_ samplerType (sm3-vs asm) 

宣告頂點著色器取樣器。

## <a name="syntax"></a>Syntax

dcl \_ samplerType s\#



 

其中：

-   \_samplerType 會定義取樣器資料類型。 這會決定取樣時，每個材質座標需要多少座標。 會定義下列紋理座標維度。
    -   \_二 維和
    -   \_立方體
    -   \_體積
-   s \# 會識別一個取樣器，其中 s 是取樣器的縮寫，而 \# 是取樣器數目。 [ (Direct3D 9 asm-vs) ](dx9-graphics-reference-asm-vs-registers-sampler.md)s 的取樣器是虛擬暫存器，因為您無法直接讀取或寫入它們。

## <a name="remarks"></a>備註



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| dcl \_ samplerType       |      |      |      |       | x    | x     |



 

所有 \_ 的 dcl samplerType 指令都必須出現在第一個可執行指令之前。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




