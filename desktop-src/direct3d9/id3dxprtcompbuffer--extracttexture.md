---
description: 從 ID3DXPRTCompBuffer 壓縮的資料緩衝區中，將每個範例主體元件分析 (PCA) 投影係數，然後將資料新增至 IDirect3DTexture9 物件。
ms.assetid: 2159e57d-b8e5-421f-b20a-ac58b29e3c45
title: 'ID3DXPRTCompBuffer：： ExtractTexture 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractTexture
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6b6dd2f0a366cf371347d1f8f7289e1ad3c782e069dcd9f7007abbd7c1a5c33d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985648"
---
# <a name="id3dxprtcompbufferextracttexture-method"></a>ID3DXPRTCompBuffer：： ExtractTexture 方法

從 [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) 壓縮的資料緩衝區中，將每個範例主體元件分析 (PCA) 投影係數，然後將資料新增至 [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) 物件。

## <a name="syntax"></a>語法


```C++
HRESULT ExtractTexture(
  [in] UINT               StartPCA,
  [in] UINT               NumPCA,
  [in] LPDIRECT3DTEXTURE9 pTexture
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*StartPCA* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要從中解壓縮紋理資料之緩衝區係數的起始值。

</dd> <dt>

*NumPCA* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要從緩衝區中解壓縮的 PCA 係數數目。

</dd> <dt>

*pTexture* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

[**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)紋理物件的指標，該物件會儲存 PCA 係數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則會傳回下列值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
