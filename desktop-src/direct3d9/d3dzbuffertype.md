---
description: 定義描述深度緩衝區格式的常數。
ms.assetid: 5e5ce48b-8859-43e0-a9b4-5972cf6bf781
title: 'D3DZBUFFERTYPE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DZBUFFERTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 271a278f48c10a89fa6f552c3e1a7b4a83f274f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985889"
---
# <a name="d3dzbuffertype-enumeration"></a>D3DZBUFFERTYPE 列舉

定義描述深度緩衝區格式的常數。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DZBUFFERTYPE { 
  D3DZB_FALSE        = 0,
  D3DZB_TRUE         = 1,
  D3DZB_USEW         = 2,
  D3DZB_FORCE_DWORD  = 0x7fffffff
} D3DZBUFFERTYPE, *LPD3DZBUFFERTYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DZB_FALSE"></span><span id="d3dzb_false"></span>**D3DZB \_ FALSE**
</dt> <dd>

停用深度緩衝。

</dd> <dt>

<span id="D3DZB_TRUE"></span><span id="d3dzb_true"></span>**D3DZB \_ TRUE**
</dt> <dd>

啟用 z 緩衝。

</dd> <dt>

<span id="D3DZB_USEW"></span><span id="d3dzb_usew"></span>**D3DZB \_ USEW**
</dt> <dd>

啟用 w-緩衝。

</dd> <dt>

<span id="D3DZB_FORCE_DWORD"></span><span id="d3dzb_force_dword"></span>**D3DZB \_ 強制 \_ DWORD**
</dt> <dd>

強制此列舉的大小編譯為32位。 如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。 不使用這個值。

</dd> </dl>

## <a name="remarks"></a>備註

此列舉類型的成員會搭配 D3DRS ZENABLE 轉譯 \_ 狀態使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 列舉](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
