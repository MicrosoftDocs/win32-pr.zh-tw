---
description: 設定要傳遞至裝置的陣列範圍。
ms.assetid: 43f1c258-770c-4756-9033-e5667b379fe6
title: 'ID3DXBaseEffect：： SetArrayRange 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetArrayRange
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1cf4f51bfca29f1aa46238197818bb10bc4d0fe811218e5cedc59c24deb2446f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987628"
---
# <a name="id3dxbaseeffectsetarrayrange-method"></a>ID3DXBaseEffect：： SetArrayRange 方法

設定要傳遞至裝置的陣列範圍。

## <a name="syntax"></a>語法


```C++
HRESULT SetArrayRange(
  [in] D3DXHANDLE hParameter,
  [in] UINT       Start,
  [in] UINT       Stop
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hParameter* \[在\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

唯一識別碼。 請參閱 [處理 (Direct3D 9) ](handles.md)。

</dd> <dt>

*開始* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

開始索引。

</dd> <dt>

*停止* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

停止索引。

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
</dt> </dl>

 

 
