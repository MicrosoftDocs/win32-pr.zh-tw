---
description: 定義描述轉換狀態值的常數。
ms.assetid: 53535d9f-246a-42cf-82a2-fb3cf6d4ebac
title: 'D3DTRANSFORMSTATETYPE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTRANSFORMSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 299246ef890015a6d7de465ecc7c00251a52432d276a87f3d5f336b63d563737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986988"
---
# <a name="d3dtransformstatetype-enumeration"></a>D3DTRANSFORMSTATETYPE 列舉

定義描述轉換狀態值的常數。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DTRANSFORMSTATETYPE { 
  D3DTS_VIEW         = 2,
  D3DTS_PROJECTION   = 3,
  D3DTS_TEXTURE0     = 16,
  D3DTS_TEXTURE1     = 17,
  D3DTS_TEXTURE2     = 18,
  D3DTS_TEXTURE3     = 19,
  D3DTS_TEXTURE4     = 20,
  D3DTS_TEXTURE5     = 21,
  D3DTS_TEXTURE6     = 22,
  D3DTS_TEXTURE7     = 23,
  D3DTS_FORCE_DWORD  = 0x7fffffff
} D3DTRANSFORMSTATETYPE, *LPD3DTRANSFORMSTATETYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**D3DTS \_ 視圖**
</dt> <dd>

識別要設定為視圖轉換矩陣的轉換矩陣。 預設值為 **Null** (標識矩陣) 。

</dd> <dt>

<span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**D3DTS \_ 投射**
</dt> <dd>

識別要設定為投影轉換矩陣的轉換矩陣。 預設值為 **Null** (標識矩陣) 。

</dd> <dt>

<span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**D3DTS \_ TEXTURE0**
</dt> <dd>

識別要為指定的材質階段設定的轉換矩陣。

</dd> <dt>

<span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**D3DTS \_ >texture1**
</dt> <dd>

識別要為指定的材質階段設定的轉換矩陣。

</dd> <dt>

<span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**D3DTS \_ TEXTURE2**
</dt> <dd>

識別要為指定的材質階段設定的轉換矩陣。

</dd> <dt>

<span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**D3DTS \_ TEXTURE3**
</dt> <dd>

識別要為指定的材質階段設定的轉換矩陣。

</dd> <dt>

<span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**D3DTS \_ TEXTURE4**
</dt> <dd>

識別要為指定的材質階段設定的轉換矩陣。

</dd> <dt>

<span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**D3DTS \_ TEXTURE5**
</dt> <dd>

識別要為指定的材質階段設定的轉換矩陣。

</dd> <dt>

<span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**D3DTS \_ TEXTURE6**
</dt> <dd>

識別要為指定的材質階段設定的轉換矩陣。

</dd> <dt>

<span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**D3DTS \_ TEXTURE7**
</dt> <dd>

識別要為指定的材質階段設定的轉換矩陣。

</dd> <dt>

<span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS \_ 強制 \_ DWORD**
</dt> <dd>

強制此列舉的大小編譯為32位。 如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。 不使用這個值。

</dd> </dl>

## <a name="remarks"></a>備註

範圍256到511的轉換狀態是保留來儲存最多256世界矩陣，可使用 D3DTS \_ WORLDMATRIX 和 D3DTS 世界宏來編制索引 \_ 。



| 巨集                                                  | 描述                                                                                                                                                                      |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3DTS \_ 世界**](d3dts-world.md)                     | 相當於 D3DTS \_ WORLDMATRIX (0) 。                                                                                                                                  |
| [**D3DTS \_WORLDMATRIX**](d3dts-worldmatrix.md) (索引)  | 識別要為位於索引的世界矩陣設定的轉換矩陣。 多個世界矩陣只用于頂點混色。 否則只 \_ 會使用 D3DTS WORLD。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 列舉](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::GetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[**IDirect3DDevice9::MultiplyTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[**D3DTS \_ 世界**](d3dts-world.md)
</dt> <dt>

[**D3DTS \_ WORLDn**](d3dts-worldn.md)
</dt> <dt>

[**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md)
</dt> </dl>

 

 
