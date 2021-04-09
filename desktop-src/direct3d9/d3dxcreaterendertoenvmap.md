---
description: 建立轉譯環境對應。
ms.assetid: 5ca10602-5ab1-4766-a350-706c46c55df2
title: 'D3DXCreateRenderToEnvMap 函式 (D3dx9core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateRenderToEnvMap
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6829d53f53bd6a4783f5873eeed614e48bbe1088
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035352"
---
# <a name="d3dxcreaterendertoenvmap-function"></a>D3DXCreateRenderToEnvMap 函式

建立轉譯環境對應。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCreateRenderToEnvMap(
  _In_  LPDIRECT3DDEVICE9    pDevice,
  _In_  UINT                 Size,
  _In_  UINT                 MipLevels,
  _In_  D3DFORMAT            Format,
  _In_  BOOL                 DepthStencil,
  _In_  D3DFORMAT            DepthStencilFormat,
  _Out_ LPD3DXRENDERTOENVMAP *ppRenderToEnvMap
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，也就是與呈現介面相關聯的裝置。

</dd> <dt>

*大小* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

呈現介面的大小。

</dd> <dt>

*MipLevels* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

Mipmap 層級的數目。

</dd> <dt>

*格式* \[在\]
</dt> <dd>

類型： **[D3DFORMAT](d3dformat.md)**

[D3DFORMAT](d3dformat.md)列舉型別的成員，其描述環境對應的像素格式。

</dd> <dt>

*DepthStencil* \[在\]
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

若 **為 TRUE**，表示呈現介面支援深度樣板表面。 否則，此成員會設定為 **FALSE**。

</dd> <dt>

*DepthStencilFormat* \[在\]
</dt> <dd>

類型： **[D3DFORMAT](d3dformat.md)**

如果 DepthStencil 設定為 **TRUE**，這個參數就是 [D3DFORMAT](d3dformat.md) 列舉型別的成員，它會描述環境對應的深度樣板格式。

</dd> <dt>

*ppRenderToEnvMap* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXRENDERTOENVMAP**](id3dxrendertoenvmap.md)\***

[**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md)介面指標的位址，表示所建立的呈現環境對應。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般用途函數](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
