---
description: 描述頂點緩衝區。
ms.assetid: 0ae8f976-d0ca-4d55-b6db-5be85fa3c799
title: 'D3DVERTEXBUFFER_DESC 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXBUFFER_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b2c0838743f8190eeb0e5c825e7125d2e48c0b6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514649"
---
# <a name="d3dvertexbuffer_desc-structure"></a>D3DVERTEXBUFFER \_ DESC 結構

描述頂點緩衝區。

## <a name="syntax"></a>語法


```C++
typedef struct D3DVERTEXBUFFER_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Size;
  DWORD           FVF;
} D3DVERTEXBUFFER_DESC, *LPD3DVERTEXBUFFER_DESC;
```



## <a name="members"></a>成員

<dl> <dt>

**格式**
</dt> <dd>

類型： **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

[D3DFORMAT](d3dformat.md)列舉型別的成員，描述頂點緩衝區資料的表面格式。

</dd> <dt>

**型別**
</dt> <dd>

類型： **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

[**D3DRESOURCETYPE**](./d3dresourcetype.md)列舉型別的成員，將此資源識別為頂點緩衝區。

</dd> <dt>

**使用量**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

一或多個 [**D3DUSAGE**](d3dusage.md) 旗標的組合。

</dd> <dt>

**集區**
</dt> <dd>

類型： **[ **D3DPOOL**](./d3dpool.md)**

</dd> <dd>

[**D3DPOOL**](./d3dpool.md)列舉型別的成員，指定配置給這個頂點緩衝區的記憶體類別。

</dd> <dt>

**大小**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

頂點緩衝區的大小（以位元組為單位）。

</dd> <dt>

**FVF**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

描述此緩衝區中頂點頂點格式的 [D3DFVF](d3dfvf.md) 組合。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-getdesc)
</dt> <dt>

[ (Direct3D 9) 的頂點緩衝區 ](vertex-buffers.md)
</dt> </dl>

 

 
