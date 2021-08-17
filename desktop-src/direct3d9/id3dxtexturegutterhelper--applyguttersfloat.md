---
description: 將裝訂邊套用至 FLOAT 材質緩衝區。
ms.assetid: 822483d7-ae62-498a-bce7-3a925ab21c04
title: 'ID3DXTextureGutterHelper：： ApplyGuttersFloat 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ApplyGuttersFloat
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6c0401a6d0692331adf9e80c800530690e59eeec5e6a9463b57425af1a3f9330
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800361"
---
# <a name="id3dxtexturegutterhelperapplyguttersfloat-method"></a>ID3DXTextureGutterHelper：： ApplyGuttersFloat 方法

將裝訂邊套用至 FLOAT 材質緩衝區。

## <a name="syntax"></a>語法


```C++
HRESULT ApplyGuttersFloat(
  [in] FLOAT *pDataIn,
  [in] UINT  *NumCoeffs,
  [in] UINT  *Width,
  [in] UINT  *Height
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDataIn* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

FLOAT 材質資料緩衝區的指標。

</dd> <dt>

*NumCoeffs* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

記憶體中用來儲存範例的每個顏色通道的純量數目。 每個材質都包含 NumCoeffs 浮點值。

</dd> <dt>

*寬度* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

從 [**ID3DXTextureGutterHelper：： GetWidth**](id3dxtexturegutterhelper--getwidth.md)取得之材質的寬度（以圖元為單位）。

</dd> <dt>

*高度* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

從 [**ID3DXTextureGutterHelper：： GetHeight**](id3dxtexturegutterhelper--getheight.md)取得的材質高度（以圖元為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則會傳回下列值。D3DERR \_ INVALIDCALL

## <a name="remarks"></a>備註

[**類別2材質**](id3dxtexturegutterhelper.md) 是藉由重新取樣類別1和4材質所產生。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
