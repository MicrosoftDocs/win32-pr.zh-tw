---
description: 描述磁片區。
ms.assetid: c0224f4e-3d32-4bdd-b56c-4e8aa291bb27
title: 'D3DVOLUME_DESC 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVOLUME_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 1ddf80819818bf23985c5ca81e2d26e80b51662388ec5808579c74146c152ea8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300176"
---
# <a name="d3dvolume_desc-structure"></a>D3DVOLUME \_ DESC 結構

描述磁片區。

## <a name="syntax"></a>語法


```C++
typedef struct D3DVOLUME_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Width;
  UINT            Height;
  UINT            Depth;
} D3DVOLUME_DESC, *LPD3DVOLUME_DESC;
```



## <a name="members"></a>成員

<dl> <dt>

**格式**
</dt> <dd>

類型： **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

[D3DFORMAT](d3dformat.md)列舉型別的成員，描述磁片區的介面格式。

</dd> <dt>

**類型**
</dt> <dd>

類型： **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

[**D3DRESOURCETYPE**](./d3dresourcetype.md)列舉型別的成員，將此資源識別為磁片區。

</dd> <dt>

**使用量**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

目前未使用。 一律傳回為0。

</dd> <dt>

**集區**
</dt> <dd>

類型： **[ **D3DPOOL**](./d3dpool.md)**

</dd> <dd>

[**D3DPOOL**](./d3dpool.md)列舉型別的成員，指定配置給這個磁片區的記憶體類別。

</dd> <dt>

**寬度**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

磁片區的寬度（以圖元為單位）。

</dd> <dt>

**高度**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

磁片區的高度（以圖元為單位）。

</dd> <dt>

**深度**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

磁片區的深度（以圖元為單位）。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-getdesc)
</dt> <dt>

[**GetLevelDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-getleveldesc)
</dt> </dl>

 

 
