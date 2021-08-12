---
description: ID3DXKeyframedAnimationSet：： GetCallbackKey 方法-取得動畫集中特定回呼的相關資訊。
ms.assetid: a1d3ca96-2852-420a-aa5c-a434970e5523
title: 'ID3DXKeyframedAnimationSet：： GetCallbackKey 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetCallbackKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5036ca9e00da3231677fe41e179bb9c27d1a4bbbd145f3e15bc6e4160902e9b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118295168"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkey-method"></a>ID3DXKeyframedAnimationSet：： GetCallbackKey 方法

取得動畫集中特定回呼的相關資訊。

## <a name="syntax"></a>語法


```C++
HRESULT GetCallbackKey(
  [in]  UINT               Animation,
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*動畫* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

動畫索引。

</dd> <dt>

*pCallbackKeys* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXKEY \_ 回呼**](d3dxkey-callback.md)**

[**回呼函數**](d3dxkey-callback.md)的指標。

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

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
