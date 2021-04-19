---
description: 設定材質類別值，指出根據每個材質位置的材質類別。
ms.assetid: cb2e6afb-4b6a-4b01-aaa8-1fd2d1f2bfa1
title: 'ID3DXTextureGutterHelper：： SetGutterMap 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetGutterMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8d3c0b7c7e33664f3e078eca82a6f39b1294992a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992741"
---
# <a name="id3dxtexturegutterhelpersetguttermap-method"></a>ID3DXTextureGutterHelper：： SetGutterMap 方法

設定材質類別值，指出根據每個材質位置的材質類別。

## <a name="syntax"></a>語法


```C++
HRESULT SetGutterMap(
  [in] BYTE *pGutterData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pGutterData* \[在\]
</dt> <dd>

類型： **[**位元組**](../winprog/windows-data-types.md)\***

材質類別的指標。 可能的材質類別如下所示。 沒有材質類別3。



| 材質類別 | 材質位置                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0           | 不正確點;將不會使用材質。                                                                                                                                                                                                                                                                                                                                        |
| 1           | 在三角形內。                                                                                                                                                                                                                                                                                                                                                              |
| 2           | 在裝訂邊內。                                                                                                                                                                                                                                                                                                                                                                |
| 4           | 內部裝訂邊;材質將會評估為 [**ID3DXTextureGutterHelper：： ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md)、 [**ID3DXTextureGutterHelper：： ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)或 [**ID3DXTextureGutterHelper：： ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) 方法中的完整範例。 |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則會傳回下列值。D3DERR \_ INVALIDCALL

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
