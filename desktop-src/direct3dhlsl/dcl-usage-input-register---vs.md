---
title: 'dcl_usage 輸入 (sm1、sm2、sm3-vs asm) '
description: 宣告頂點專案使用方式與頂點著色器輸入暫存器的使用方式索引之間的關聯。
ms.assetid: e0360f4d-1250-4dc5-b790-372b303a37a8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 38113846fe62c37247bb2d3ca522a34dc9282441
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463353"
---
# <a name="dcl_usage-input-sm1-sm2-sm3---vs-asm"></a>dcl \_ 使用方式輸入 (sm1、sm2、sm3-vs asm) 

宣告頂點專案使用方式與頂點著色器輸入暫存器的使用方式索引之間的關聯。

## <a name="syntax"></a>Syntax



|                                |
|--------------------------------|
| dcl \_ 使用方式 \[ 使用方式 \_ 索引 \] v\# |



 

其中：

-   dcl \_ 使用方式會識別如何使用註冊資料。 這與沒有 D3DDECLUSAGE 前置詞的 [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) 成員具有相同的值。
-   使用方式 \_ 索引是介於0到15之間的選擇性整數索引。 它會修改使用方式資料。 索引符合頂點宣告中的使用方式索引。 請參閱 [ (Direct3D 9) 的頂點 ](/windows/desktop/direct3d9/vertex-declaration)宣告。 索引會附加至使用值 (\_ ) 不含空格的使用值。 如果未提供，則會假設為0。
-   v \# 是 [輸入](dx9-graphics-reference-asm-vs-registers-input.md)暫存器。

## <a name="remarks"></a>備註



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| dcl \_ 使用方式             | x    | x    | x    | x     | x    | x     |



 

所有 \_ 的 dcl 使用方式指令都必須出現在第一個可執行指令之前。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 