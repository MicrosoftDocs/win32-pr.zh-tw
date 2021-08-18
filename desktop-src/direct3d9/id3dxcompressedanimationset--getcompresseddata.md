---
description: 取得儲存已壓縮之主要畫面格動畫資料的資料緩衝區。
ms.assetid: cb42a4c8-6420-4694-9921-0d36cfe960e5
title: 'ID3DXCompressedAnimationSet：： GetCompressedData 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet.GetCompressedData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e3290dcc9e9baeaa688117d8a98918e7df814a34812cb66791b2c8021a50f788
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987580"
---
# <a name="id3dxcompressedanimationsetgetcompresseddata-method"></a>ID3DXCompressedAnimationSet：： GetCompressedData 方法

取得儲存已壓縮之主要畫面格動畫資料的資料緩衝區。

## <a name="syntax"></a>語法


```C++
HRESULT GetCompressedData(
  [out] LPD3DXBUFFER *ppCompressedData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppCompressedData* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

[**ID3DXBuffer**](id3dxbuffer.md)資料緩衝區指標的位址，該緩衝區會接收壓縮的主要畫面格動畫資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXCompressedAnimationSet](id3dxcompressedanimationset.md)
</dt> </dl>

 

 




