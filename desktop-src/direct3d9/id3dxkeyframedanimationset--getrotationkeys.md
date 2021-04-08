---
description: 使用主要畫面格動畫所用的旋轉金鑰資料來填滿陣列。
ms.assetid: 9ae8bc28-d231-4d50-98f0-762b2d2c04e8
title: 'ID3DXKeyframedAnimationSet：： GetRotationKeys 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetRotationKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: af9242ccf75bc1e5443f040399ffbd8a939ed92e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696816"
---
# <a name="id3dxkeyframedanimationsetgetrotationkeys-method"></a>ID3DXKeyframedAnimationSet：： GetRotationKeys 方法

使用主要畫面格動畫所用的旋轉金鑰資料來填滿陣列。

## <a name="syntax"></a>語法


```C++
HRESULT GetRotationKeys(
  [in] UINT                 Animation,
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

*pRotationKeys* \[在\]
</dt> <dd>

類型： **[ **LPD3DXKEY \_ 四元數**](d3dxkey-quaternion.md)**

[**D3DXKEY \_ 四元**](d3dxkey-quaternion.md)數四元數之使用者配置陣列的指標，此方法是用來填滿動畫旋轉資料。

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

[**ID3DXKeyframedAnimationSet::GetNumRotationKeys**](id3dxkeyframedanimationset--getnumrotationkeys.md)
</dt> </dl>

 

 
