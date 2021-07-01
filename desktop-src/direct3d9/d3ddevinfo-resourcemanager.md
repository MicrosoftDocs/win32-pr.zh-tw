---
description: 資源使用量統計資料。
ms.assetid: e43de550-2025-4210-a420-e41d14620704
title: 'D3DDEVINFO_RESOURCEMANAGER 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_RESOURCEMANAGER
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b0a9fc461564280e4e36dde6bf73e68a78cf1609
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129977"
---
# <a name="d3ddevinfo_resourcemanager-structure"></a>D3DDEVINFO \_ RESOURCEMANAGER 結構

資源使用量統計資料。

## <a name="syntax"></a>語法


```C++
typedef struct _D3DDEVINFO_RESOURCEMANAGER {
  D3DRESOURCESTATS stats[D3DRTYPECOUNT];
} D3DDEVINFO_RESOURCEMANAGER, *LPD3DDEVINFO_RESOURCEMANAGER;

```



## <a name="members"></a>成員

<dl> <dt>

**統計**
</dt> <dd>

類型： **[ **D3DRESOURCESTATS**](d3dresourcestats.md)**

</dd> <dd>

資源統計資料元素的陣列。 請參閱 [**D3DRESOURCESTATS**](d3dresourcestats.md)。

</dd> </dl>

## <a name="remarks"></a>備註

D3DRTYPECOUNT 指的是 [**D3DRESOURCETYPE**](./d3dresourcetype.md)中的列舉數目。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
