---
description: 儲存屬性資料表專案。
ms.assetid: b9f13b12-35ba-4e4c-93ac-3dd44d611b47
title: 'D3DXATTRIBUTERANGE 結構 (D3dx9mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXATTRIBUTERANGE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: a842bbf41847f4b4e65c975e11f3e160cea1422d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992324"
---
# <a name="d3dxattributerange-structure"></a>D3DXATTRIBUTERANGE 結構

儲存屬性資料表專案。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXATTRIBUTERANGE {
  DWORD AttribId;
  DWORD FaceStart;
  DWORD FaceCount;
  DWORD VertexStart;
  DWORD VertexCount;
} D3DXATTRIBUTERANGE, *LPD3DXATTRIBUTERANGE;
```



## <a name="members"></a>成員

<dl> <dt>

**AttribId**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

屬性資料表識別碼。

</dd> <dt>

**FaceStart**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

開始臉部。

</dd> <dt>

**FaceCount**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

臉部計數。

</dd> <dt>

**VertexStart**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

正在啟動頂點。

</dd> <dt>

**VertexCount**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

頂點計數。

</dd> </dl>

## <a name="remarks"></a>備註

屬性工作表用來識別需要以不同紋理、轉譯狀態、材質等等繪製的網格區域。 此外，應用程式也可以使用屬性工作表來隱藏部分網格，而不是在繪製框架時 (AttribId) 繪製指定的屬性識別碼。

LPD3DXATTRIBUTERANGE 型別定義為 **D3DXATTRIBUTERANGE** 結構的指標。


```
typedef D3DXATTRIBUTERANGE* LPD3DXATTRIBUTERANGE;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9mesh。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
