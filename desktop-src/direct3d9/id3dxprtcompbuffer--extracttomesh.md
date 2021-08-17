---
description: 從 ID3DXPRTCompBuffer 壓縮的資料緩衝區中，將每個範例主體元件分析 (PCA) 投影係數，然後將資料新增至 ID3DXMesh 物件。
ms.assetid: 0680d626-f07a-43d3-acb9-e8db82b5e933
title: 'ID3DXPRTCompBuffer：： ExtractToMesh 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractToMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 410ec268da89ad4033c88a90c2b37bfa8e78a7b9c229cab72c8ad07e666fce42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730034"
---
# <a name="id3dxprtcompbufferextracttomesh-method"></a>ID3DXPRTCompBuffer：： ExtractToMesh 方法

從 [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) 壓縮的資料緩衝區中，將每個範例主體元件分析 (PCA) 投影係數，然後將資料新增至 [**ID3DXMesh**](id3dxmesh.md) 物件。

## <a name="syntax"></a>語法


```C++
HRESULT ExtractToMesh(
  [in] UINT         NumPCA,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         UsageIndexStart,
  [in] LPD3DXMESH   pScene
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*NumPCA* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要從緩衝區中解壓縮的 PCA 係數數目。

</dd> <dt>

*使用* \[ 方式在\]
</dt> <dd>

類型： **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

網格的頂點使用方式描述。 請參閱 [**D3DDECLUSAGE**](./d3ddeclusage.md)。

</dd> <dt>

*UsageIndexStart* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

開始將 PCA 係數的索引儲存在網格中。

</dd> <dt>

*pScene* \[在\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)**

[**ID3DXMesh**](id3dxmesh.md)網格物件的指標，該物件會儲存 PCA 係數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
