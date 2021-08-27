---
description: 使用緩衝區中的資料來設定常數資料表。
ms.assetid: 55cf5456-8f23-405d-9329-8ff737c5c139
title: 'ID3DXTextureShader：： SetValue 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetValue
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9ba652d4fd295103409c073287264d3a01b6352c465532719f01e427ad4dedcd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095638"
---
# <a name="id3dxtextureshadersetvalue-method"></a>ID3DXTextureShader：： SetValue 方法

使用緩衝區中的資料來設定常數資料表。

## <a name="syntax"></a>語法


```C++
HRESULT SetValue(
  [in] D3DXHANDLE hConstant,
  [in] LPCVOID    pData,
  [in] UINT       Bytes
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hConstant* \[在\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

常數的唯一識別碼。 請參閱 [D3DXHANDLE](d3dxfx.md)。

</dd> <dt>

*.pdata* \[在\]
</dt> <dd>

類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**

包含常數資料之緩衝區的指標。

</dd> <dt>

*位元組* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

緩衝區的大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Shader。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 
