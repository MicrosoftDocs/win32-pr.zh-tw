---
description: 頂點快取優化提示。
ms.assetid: 891624cd-03dd-4ddd-93f5-4899e1470325
title: 'D3DDEVINFO_VCACHE 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_VCACHE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3e065c981cc42db6adbad8cfa7a14e415712aae74942e9f3aab3ecb0b353f5ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894498"
---
# <a name="d3ddevinfo_vcache-structure"></a>D3DDEVINFO \_ VCACHE 結構

頂點快取優化提示。

## <a name="syntax"></a>語法


```C++
typedef struct D3DDEVINFO_VCACHE {
  DWORD Pattern;
  DWORD OptMethod;
  DWORD CacheSize;
  DWORD MagicNumber;
} D3DDEVINFO_VCACHE, *LPD3DDEVINFO_VCACHE;
```



## <a name="members"></a>成員

<dl> <dt>

**模式**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

位模式。 傳回值必須是 FOURCC ( ' C '、' A '、' C '、' H ' ) 。

</dd> <dt>

**OptMethod**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

優化方法。 使用0可取得最長的停車線。 使用1可優化頂點快取使用。

</dd> <dt>

**CacheSize**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

用來作為優化目標的快取大小。 只有當 OptMethod 是1時，才需要此項。

</dd> <dt>

**MagicNumber**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

由內部優化方法用來決定何時要重新開機停車。 這無法由使用者設定或修改。 只有當 OptMethod 是1時，才需要此項。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
