---
description: 起始球形環境對應的呈現。
ms.assetid: b0634120-f5ad-48b3-979a-30b0a53d22a2
title: 'ID3DXRenderToEnvMap：： BeginSphere 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginSphere
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f8bc555e3ea4f4fbb895c42f5c7a407cea88aedeacb9604ad1e78c7003bdf34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118801288"
---
# <a name="id3dxrendertoenvmapbeginsphere-method"></a>ID3DXRenderToEnvMap：： BeginSphere 方法

起始球形環境對應的呈現。

## <a name="syntax"></a>語法


```C++
HRESULT BeginSphere(
  [in] LPDIRECT3DTEXTURE9 pTex
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pTex* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

[**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)介面的指標，該介面表示要呈現的材質。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL。E \_ 失敗

## <a name="remarks"></a>備註

請參閱 [**ID3DXRenderToEnvMap：：臉部**](id3dxrendertoenvmap--face.md) 以繪製臉部。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> <dt>

[**ID3DXRenderToEnvMap：： End**](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 
