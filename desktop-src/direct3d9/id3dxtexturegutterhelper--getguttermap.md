---
description: 接收材質類別值，指出根據每個材質位置的材質類別。
ms.assetid: 450739a8-e30c-4e56-9560-8cb705a75672
title: 'ID3DXTextureGutterHelper：： GetGutterMap 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetGutterMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9d973e716c598eaceaf7f75e6694a35691df4266
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982024"
---
# <a name="id3dxtexturegutterhelpergetguttermap-method"></a>ID3DXTextureGutterHelper：： GetGutterMap 方法

接收材質類別值，指出根據每個材質位置的材質類別。

## <a name="syntax"></a>語法


```C++
HRESULT GetGutterMap(
  [in, out] BYTE *pGutterData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pGutterData* \[in、out\]
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

## <a name="remarks"></a>備註

應用程式必須配置和管理 pGutterData，其大小指定為：


```
texture width * texture height * sizeof(BYTE)
```



紋理寬度和高度是由 [**ID3DXTextureGutterHelper：： GetWidth**](id3dxtexturegutterhelper--getwidth.md) 和 [**ID3DXTextureGutterHelper：： GetHeight**](id3dxtexturegutterhelper--getheight.md)傳回。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
