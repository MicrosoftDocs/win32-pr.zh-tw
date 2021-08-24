---
description: 描述點陣狀態。
ms.assetid: f7b5b714-8fc8-47b8-adec-1089b8d07081
title: 'D3DRASTER_STATUS 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRASTER_STATUS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: fc8a1e2995a9353a02df120b109eb32ad0914821e5690440c7228fbc8e7b6c8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676398"
---
# <a name="d3draster_status-structure"></a>D3DRASTER \_ 狀態結構

描述點陣狀態。

## <a name="syntax"></a>語法


```C++
typedef struct D3DRASTER_STATUS {
  BOOL InVBlank;
  UINT ScanLine;
} D3DRASTER_STATUS, *LPD3DRASTER_STATUS;
```



## <a name="members"></a>成員

<dl> <dt>

**InVBlank**
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

如果點陣處於垂直空白期間，**則為 TRUE** 。 如果點陣不在垂直空白句號內，則 **為 FALSE** 。

</dd> <dt>

**ScanLine**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

如果 InVBlank 為 **FALSE**，則這個值會是大約對應到點陣所繪製之目前掃描行的整數。 掃描行的編號方式與 Direct3D 介面座標相同：0是主要表面的頂端，會延伸至顯示器底部)  (高度的值。

如果 InVBlank 為 **TRUE**，則此值會設定為零，而且可以忽略。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetRasterStatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrasterstatus)
</dt> </dl>

 

 
