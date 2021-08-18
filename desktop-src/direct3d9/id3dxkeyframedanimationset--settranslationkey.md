---
description: 設定動畫集中特定主要畫面格的翻譯資訊。
ms.assetid: 4a926c0f-6d57-48d4-bb3b-60766fc78e40
title: 'ID3DXKeyframedAnimationSet：： SetTranslationKey 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.SetTranslationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4f699a1988c53fc52b4ce413e4c0a655b7d943ddabc0c8e5fcb25ad627e32667
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987338"
---
# <a name="id3dxkeyframedanimationsetsettranslationkey-method"></a>ID3DXKeyframedAnimationSet：： SetTranslationKey 方法

設定動畫集中特定主要畫面格的翻譯資訊。

## <a name="syntax"></a>語法


```C++
HRESULT SetTranslationKey(
  [in] UINT              Animation,
  [in] UINT              Key,
  [in] LPD3DXKEY_VECTOR3 pTranslationKey
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*動畫* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

動畫索引。

</dd> <dt>

*金鑰* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

主要畫面格。

</dd> <dt>

*pTranslationKey* \[在\]
</dt> <dd>

類型： **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**

轉譯資料的指標。 請參閱 [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)。

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

 

 
