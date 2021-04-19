---
description: 傳回儲存在 Direct3D (. x) 檔案中的材質資訊。
ms.assetid: dfa021ba-61d8-4f99-9bbb-0cfbe11b787d
title: 'D3DXMATERIAL 結構 (D3dx9mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATERIAL
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 89079b716a8c5808255b2bc660f1d364bb97315f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976456"
---
# <a name="d3dxmaterial-structure"></a>D3DXMATERIAL 結構

傳回儲存在 Direct3D (. x) 檔案中的材質資訊。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXMATERIAL {
  D3DMATERIAL9 MatD3D;
  LPSTR        pTextureFilename;
} D3DXMATERIAL, *LPD3DXMATERIAL;
```



## <a name="members"></a>成員

<dl> <dt>

**MatD3D**
</dt> <dd>

類型： **[ **D3DMATERIAL9**](d3dmaterial9.md)**

</dd> <dd>

描述材質屬性的 [**D3DMATERIAL9**](d3dmaterial9.md)結構。

</dd> <dt>

**pTextureFilename**
</dt> <dd>

類型： **LPSTR**

</dd> <dd>

指定材質檔案名的字串指標。

</dd> </dl>

## <a name="remarks"></a>備註

[**D3DXLoadMeshFromX**](d3dxloadmeshfromx.md)和 [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md)函式會傳回 **D3DXMATERIAL** 結構的陣列，為網格中的每個材質指定材質色彩和材質的名稱。 然後需要應用程式才能載入紋理。

LPD3DXMATERIAL 型別定義為 **D3DXMATERIAL** 結構的指標。


```
typedef struct D3DXMATERIAL* LPD3DXMATERIAL;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9mesh。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXLoadMeshFromX**](d3dxloadmeshfromx.md)
</dt> <dt>

[**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md)
</dt> </dl>

 

 




