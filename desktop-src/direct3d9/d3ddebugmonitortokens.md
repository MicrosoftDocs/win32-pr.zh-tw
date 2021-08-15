---
description: 定義 debug 監視器權杖。
ms.assetid: c0df4c9f-a232-45cf-b543-e95ee84a4a8d
title: 'D3DDEBUGMONITORTOKENS 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEBUGMONITORTOKENS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: ed64939714c3ee69fb30e56afe23e52e780405287c898e138ee86822f1c5e0b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989068"
---
# <a name="d3ddebugmonitortokens-enumeration"></a>D3DDEBUGMONITORTOKENS 列舉

定義 debug 監視器權杖。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DDEBUGMONITORTOKENS { 
  D3DDMT_ENABLE       = 0,
  D3DDMT_DISABLE      = 1,
  D3DDMT_FORCE_DWORD  = 0x7fffffff
} D3DDEBUGMONITORTOKENS, *LPD3DDEBUGMONITORTOKENS;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DDMT_ENABLE"></span><span id="d3ddmt_enable"></span>**D3DDMT \_ 啟用**
</dt> <dd>

啟用 [調試] 監視器。

</dd> <dt>

<span id="D3DDMT_DISABLE"></span><span id="d3ddmt_disable"></span>**D3DDMT \_ DISABLE**
</dt> <dd>

停用調試監視器。

</dd> <dt>

<span id="D3DDMT_FORCE_DWORD"></span><span id="d3ddmt_force_dword"></span>**D3DDMT \_ 強制 \_ DWORD**
</dt> <dd>

強制此列舉的大小編譯為32位。 如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。 不使用這個值。

</dd> </dl>

## <a name="remarks"></a>備註

此列舉型別中的值是由 D3DRS DEBUGMONITORTOKEN 轉譯狀態所使用 \_ ，而且只與 debug 組建相關。

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

 

 
