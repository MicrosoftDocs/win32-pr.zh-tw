---
description: 設定動畫集中特定主要畫面格的旋轉資訊。
ms.assetid: b31edc88-0d77-49f3-b4c4-39cd866e1379
title: 'ID3DXKeyframedAnimationSet：： SetRotationKey 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.SetRotationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2375167b9c848c0ccec10853f04c2f1aa7b59992d3198164df46c0ba7c08b68c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856598"
---
# <a name="id3dxkeyframedanimationsetsetrotationkey-method"></a>ID3DXKeyframedAnimationSet：： SetRotationKey 方法

設定動畫集中特定主要畫面格的旋轉資訊。

## <a name="syntax"></a>語法


```C++
HRESULT SetRotationKey(
  [in] UINT                 Animation,
  [in] UINT                 Key,
  [in] LPD3DXKEY_QUATERNION pRotationKeys
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

*pRotationKeys* \[在\]
</dt> <dd>

類型： **[ **LPD3DXKEY \_ 四元數**](d3dxkey-quaternion.md)**

旋轉資料的指標。 請參閱 [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)。

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

 

 
