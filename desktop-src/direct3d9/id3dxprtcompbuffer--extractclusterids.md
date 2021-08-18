---
description: 從 ID3DXPRTCompBuffer 壓縮的資料緩衝區解壓縮每個範例的叢集識別碼。
ms.assetid: d78d82ab-58bc-4b73-9ca0-8b7f06867618
title: 'ID3DXPRTCompBuffer：： ExtractClusterIDs 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractClusterIDs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 94cbf51aaedd8cc0d5505ca91663eb014e2a3d417a631e93d71b8a0ebc600ceb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987178"
---
# <a name="id3dxprtcompbufferextractclusterids-method"></a>ID3DXPRTCompBuffer：： ExtractClusterIDs 方法

從 [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) 壓縮的資料緩衝區解壓縮每個範例的叢集識別碼。

## <a name="syntax"></a>語法


```C++
HRESULT ExtractClusterIDs(
  [in, out] UINT *pClusterIDs
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pClusterIDs* \[in、out\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

寫入識別碼之記憶體位置的指標。 所需的記憶體長度是 [**ID3DXPRTCompBuffer：： GetNumSamples**](id3dxprtcompbuffer--getnumsamples.md)所傳回的值。

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

 

 
