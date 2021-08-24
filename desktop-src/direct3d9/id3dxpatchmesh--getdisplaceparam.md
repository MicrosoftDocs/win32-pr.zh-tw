---
description: 取得網狀幾何置換參數。
ms.assetid: 155724ba-71be-4e9f-8c84-bb04f8eec578
title: 'ID3DXPatchMesh：： GetDisplaceParam 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetDisplaceParam
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f079e66f20bfd9b2fab673a0f8c2310a9fd85d84fe4e7d0b8c5ad59d1d61e9e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847448"
---
# <a name="id3dxpatchmeshgetdisplaceparam-method"></a>ID3DXPatchMesh：： GetDisplaceParam 方法

取得網狀幾何置換參數。

## <a name="syntax"></a>語法


```C++
HRESULT GetDisplaceParam(
  [in] LPDIRECT3DBASETEXTURE9 *Texture,
  [in] D3DTEXTUREFILTERTYPE   *MinFilter,
  [in] D3DTEXTUREFILTERTYPE   *MagFilter,
  [in] D3DTEXTUREFILTERTYPE   *MipFilter,
  [in] D3DTEXTUREADDRESS      *Wrap,
  [in] DWORD                  *dwLODBias
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*材質* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)\***

包含置換資料的材質。

</dd> <dt>

*MinFilter* \[在\]
</dt> <dd>

類型： **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***

縮制層級。 如需詳細資訊，請參閱 [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)。

</dd> <dt>

*MagFilter* \[在\]
</dt> <dd>

類型： **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***

放大層級。 如需詳細資訊，請參閱 [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)。

</dd> <dt>

*MipFilter* \[在\]
</dt> <dd>

類型： **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***

Mip 篩選層級。 如需詳細資訊，請參閱 [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)。

</dd> <dt>

*換行* \[在\]
</dt> <dd>

類型： **[ **D3DTEXTUREADDRESS**](./d3dtextureaddress.md)\***

材質位址換行模式。 如需詳細資訊，請參閱 [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md)。

</dd> <dt>

*dwLODBias* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

詳細資料偏差值的層級。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

置換地圖只能是2D 紋理。 Nonadaptive 鑲嵌會忽略 mipmap。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
