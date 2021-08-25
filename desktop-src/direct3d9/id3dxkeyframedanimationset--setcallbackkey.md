---
description: 設定動畫集中特定回呼的相關資訊。
ms.assetid: 899f3a85-c878-4eeb-8bda-fc4e9083bd1f
title: 'ID3DXKeyframedAnimationSet：： SetCallbackKey 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.SetCallbackKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5998842927019868249278465eaf7bf9bd4ab62c3bfe83537a0eba420f87aeb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847758"
---
# <a name="id3dxkeyframedanimationsetsetcallbackkey-method"></a>ID3DXKeyframedAnimationSet：： SetCallbackKey 方法

設定動畫集中特定回呼的相關資訊。

## <a name="syntax"></a>語法


```C++
HRESULT SetCallbackKey(
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

 

 
