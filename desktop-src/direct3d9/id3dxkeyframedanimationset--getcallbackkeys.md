---
description: ID3DXKeyframedAnimationSet：： GetCallbackKeys 方法-使用用於主要畫面格動畫的回呼金鑰資料來填滿陣列。
ms.assetid: 2a2aa04a-a889-415b-8aa2-cc5f2bed1f9a
title: 'ID3DXKeyframedAnimationSet：： GetCallbackKeys 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetCallbackKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ee5a86fa5f016bd6707ec4464c79b1dc182e1ebebde80fa9f73d62e3bba3a13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118294984"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkeys-method"></a>ID3DXKeyframedAnimationSet：： GetCallbackKeys 方法

使用主要畫面格動畫所用的回呼金鑰資料來填滿陣列。

## <a name="syntax"></a>語法


```C++
HRESULT GetCallbackKeys(
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCallbackKeys* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXKEY \_ 回呼**](d3dxkey-callback.md)**

方法用來填滿回呼資料的 [**D3DXKEY \_ 回呼**](d3dxkey-callback.md) 結構之使用者配置陣列的指標。

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
</dt> <dt>

[**ID3DXKeyframedAnimationSet::GetNumCallbackKeys**](id3dxkeyframedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




