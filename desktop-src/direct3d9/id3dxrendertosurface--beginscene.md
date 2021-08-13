---
description: 開始場景。
ms.assetid: 8125c592-b985-42f7-8644-59ba93a1c517
title: 'ID3DXRenderToSurface：： BeginScene 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.BeginScene
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ce6e120361972ac1ff4dbed5d37808dffa0f010af64feda365f65aad8dd393f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118293103"
---
# <a name="id3dxrendertosurfacebeginscene-method"></a>ID3DXRenderToSurface：： BeginScene 方法

開始場景。

## <a name="syntax"></a>語法


```C++
HRESULT BeginScene(
  [in]       LPDIRECT3DSURFACE9 pSurface,
  [in] const D3DVIEWPORT9       *pViewport
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSurface* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**

[**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)介面的指標，表示呈現介面。

</dd> <dt>

*pViewport* \[在\]
</dt> <dd>

Type： **Const [**D3DVIEWPORT9**](d3dviewport9.md) \***

[**D3DVIEWPORT9**](d3dviewport9.md)結構的指標，描述場景的區。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL。D3DERR \_ OUTOFVIDEOMEMORY D3DXERR \_ INVALIDDATA E \_ OUTOFMEMORY

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXRenderToSurface](id3dxrendertosurface.md)
</dt> <dt>

[**ID3DXRenderToSurface::EndScene**](id3dxrendertosurface--endscene.md)
</dt> </dl>

 

 
