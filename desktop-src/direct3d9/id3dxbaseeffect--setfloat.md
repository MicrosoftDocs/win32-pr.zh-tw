---
description: 設定浮點值。
ms.assetid: f49fb4d2-6e3d-4452-8102-76200c55cf1f
title: 'ID3DXBaseEffect：： SetFloat 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetFloat
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f55ede140e324daa52b5bafc24cc7004a75163a96bdf2e75d4e4be5e7a4c4b39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893698"
---
# <a name="id3dxbaseeffectsetfloat-method"></a>ID3DXBaseEffect：： SetFloat 方法

設定浮點值。

## <a name="syntax"></a>語法


```C++
HRESULT SetFloat(
  [in] D3DXHANDLE hParameter,
  [in] FLOAT      f
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hParameter* \[在\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

唯一識別碼。 請參閱 [處理 (Direct3D 9) ](handles.md)。

</dd> <dt>

*f* \[ in\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

浮點值。

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

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**GetFloat**](id3dxbaseeffect--getfloat.md)
</dt> </dl>

 

 
