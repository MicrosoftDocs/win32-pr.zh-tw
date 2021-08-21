---
description: 取得動畫集中特定主要畫面格的縮放資訊。
ms.assetid: 7f4a0bf3-2922-4fd7-bb85-b387d3e983a7
title: 'ID3DXKeyframedAnimationSet：： GetScaleKey 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetScaleKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 199b5596e05bd013f3384c2a182bbe8e905cb609ae869c194d811fb97d3d254b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121155"
---
# <a name="id3dxkeyframedanimationsetgetscalekey-method"></a>ID3DXKeyframedAnimationSet：： GetScaleKey 方法

取得動畫集中特定主要畫面格的縮放資訊。

## <a name="syntax"></a>語法


```C++
HRESULT GetScaleKey(
  [in] UINT              Animation,
  [in] UINT              Key,
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

*金鑰* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

主要畫面格。

</dd> <dt>

*pScaleKeys* \[在\]
</dt> <dd>

類型： **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**

調整資料的指標。 請參閱 [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)。

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

 

 
