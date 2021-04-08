---
description: 將裝訂邊套用至 ID3DXPRTBuffer 緩衝區物件。
ms.assetid: db09aa50-3175-4588-8433-dad6bd37cf0c
title: 'ID3DXTextureGutterHelper：： ApplyGuttersPRT 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ApplyGuttersPRT
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5a99d0cb5d54207d292398468e16b6c35deb4562
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696691"
---
# <a name="id3dxtexturegutterhelperapplyguttersprt-method"></a>ID3DXTextureGutterHelper：： ApplyGuttersPRT 方法

將裝訂邊套用至 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 緩衝區物件。

## <a name="syntax"></a>語法


```C++
HRESULT ApplyGuttersPRT(
  [in] LPD3DXPRTBUFFER pBuffer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pBuffer* \[在\]
</dt> <dd>

類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

[**ID3DXPRTBuffer**](id3dxprtbuffer.md)緩衝區物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則會傳回下列值。D3DERR \_ INVALIDCALL

## <a name="remarks"></a>備註

[**類別2材質**](id3dxtexturegutterhelper.md) 是藉由重新取樣類別1和4材質所產生。

材質的寬度和高度必須與 [**ID3DXTextureGutterHelper：： GetWidth**](id3dxtexturegutterhelper--getwidth.md) 和 [**ID3DXTextureGutterHelper：： GetHeight**](id3dxtexturegutterhelper--getheight.md)傳回的寬度和高度相同。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




