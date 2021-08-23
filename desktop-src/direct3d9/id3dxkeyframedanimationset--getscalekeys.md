---
description: 使用用於主要畫面格動畫的尺規索引鍵資料來填滿陣列。
ms.assetid: 0d595510-6d8c-4bc9-b5ca-0d6f73be3439
title: 'ID3DXKeyframedAnimationSet：： GetScaleKeys 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetScaleKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1158195ae84f8215869571fc400950a6dfd475fc37050572ffb5e3e77f96d719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493508"
---
# <a name="id3dxkeyframedanimationsetgetscalekeys-method"></a>ID3DXKeyframedAnimationSet：： GetScaleKeys 方法

使用用於主要畫面格動畫的尺規索引鍵資料來填滿陣列。

## <a name="syntax"></a>語法


```C++
HRESULT GetScaleKeys(
  [in] UINT              Animation,
  [in] LPD3DXKEY_VECTOR3 pScaleKeys
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*動畫* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

動畫索引。

</dd> <dt>

*pScaleKeys* \[在\]
</dt> <dd>

類型： **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**

[**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)向量的使用者配置陣列指標，此方法是用來填滿動畫尺規資料。

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

[**ID3DXKeyframedAnimationSet::GetNumScaleKeys**](id3dxkeyframedanimationset--getnumscalekeys.md)
</dt> </dl>

 

 
