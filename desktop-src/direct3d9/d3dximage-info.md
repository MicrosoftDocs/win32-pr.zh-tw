---
description: D3DXIMAGE_INFO 結構-傳回影像檔案原始內容的描述。
ms.assetid: d6cbd5b7-642e-43ce-a2ed-11a400c5bdc1
title: 'D3DXIMAGE_INFO 結構 (D3dx9tex .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIMAGE_INFO
api_type:
- HeaderDef
api_location:
- d3dx9tex.h
ms.openlocfilehash: ede879b288569b503257abeb189d93316ed2bd96dd4db99f6e22f32bbb4f98b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607818"
---
# <a name="d3dximage_info-structure"></a>D3DXIMAGE \_ 資訊結構

傳回影像檔案原始內容的描述。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXIMAGE_INFO {
  UINT                 Width;
  UINT                 Height;
  UINT                 Depth;
  UINT                 MipLevels;
  D3DFORMAT            Format;
  D3DRESOURCETYPE      ResourceType;
  D3DXIMAGE_FILEFORMAT ImageFileFormat;
} D3DXIMAGE_INFO, *LPD3DXIMAGE_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**寬度**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

原始影像的寬度（以圖元為單位）。

</dd> <dt>

**高度**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

原始影像的高度（以圖元為單位）。

</dd> <dt>

**深度**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

原始影像的深度（以圖元為單位）。

</dd> <dt>

**MipLevels**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

原始影像中的 mip 層級數目。

</dd> <dt>

**格式**
</dt> <dd>

類型： **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

[D3DFORMAT](d3dformat.md)列舉型別中最能描述原始影像中資料的值。

</dd> <dt>

**ResourceType**
</dt> <dd>

類型： **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

表示儲存在檔案中的材質類型。 它可以是 D3DRTYPE \_ 材質、D3DRTYPE \_ VOLUMETEXTURE 或 D3DRTYPE \_ CubeTexture。

</dd> <dt>

**ImageFileFormat**
</dt> <dd>

類型： **[ **D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)**

</dd> <dd>

代表影像檔案的格式。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9tex。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
