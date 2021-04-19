---
description: 描述要用於主要畫面格動畫的回呼金鑰。
ms.assetid: aca034f5-6961-49f1-ba7c-addcf016af2b
title: 'D3DXKEY_CALLBACK 結構 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_CALLBACK
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 5c2c4dc90cbb95218268bf673204867f5b5d6636
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997388"
---
# <a name="d3dxkey_callback-structure"></a>D3DXKEY \_ 回呼結構

描述要用於主要畫面格動畫的回呼金鑰。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXKEY_CALLBACK {
  FLOAT  Time;
  LPVOID pCallbackData;
} D3DXKEY_CALLBACK, *LPD3DXKEY_CALLBACK;
```



## <a name="members"></a>成員

<dl> <dt>

**Time**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

主要畫面格時間戳記。

</dd> <dt>

**pCallbackData**
</dt> <dd>

類型： **[ **LPVOID**](../winprog/windows-data-types.md)**

</dd> <dd>

使用者回呼資料的指標。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9anim。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
