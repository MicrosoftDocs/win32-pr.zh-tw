---
description: 從單一通道緩衝區解壓縮係數資料，並將資料加入至 ID3DXMesh 物件。
ms.assetid: 4fada987-ddd7-4c02-a177-dd81f3790588
title: 'ID3DXPRTBuffer：： ExtractToMesh 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ExtractToMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c838a146a390aa72ac24781ca6f136b028ad41a6ee94fb4210ec4bd3f557acdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120612"
---
# <a name="id3dxprtbufferextracttomesh-method"></a>ID3DXPRTBuffer：： ExtractToMesh 方法

從單一通道緩衝區解壓縮係數資料，並將資料加入至 [**ID3DXMesh**](id3dxmesh.md) 物件。

## <a name="syntax"></a>語法


```C++
HRESULT ExtractToMesh(
  [in] UINT         NumCoefficients,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         UsageIndexStart,
  [in] LPD3DXMESH   pScene
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*NumCoefficients* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要從緩衝區中解壓縮的係數數目。 使用球面調和 (SH) 預先計算 radiance transfer (PRT) 時，係數的數目應該是 Order ²。 順序必須在 [D3DXSH \_ MINORDER](other-d3dx-constants.md) 到 D3DXSH \_ MAXORDER （含）的範圍內。

</dd> <dt>

*使用* \[ 方式在\]
</dt> <dd>

類型： **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

網格的頂點使用方式描述。 請參閱 [**D3DDECLUSAGE**](./d3ddeclusage.md)。

</dd> <dt>

*UsageIndexStart* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

開始要儲存在網格中之係數的索引。

</dd> <dt>

*pScene* \[在\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)**

[**ID3DXMesh**](id3dxmesh.md)網格物件的指標，該物件會儲存係數。

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

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 
