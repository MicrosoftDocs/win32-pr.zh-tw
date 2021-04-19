---
description: 註冊調整、旋轉和轉譯 (SRT) 動畫的主要畫面格資料。
ms.assetid: 10e5b391-1529-4952-abbb-ef560a35d667
title: 'ID3DXKeyframedAnimationSet：： RegisterAnimationSRTKeys 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.RegisterAnimationSRTKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3098c8e779834daf273d5e85469e3f45b01cb039
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999982"
---
# <a name="id3dxkeyframedanimationsetregisteranimationsrtkeys-method"></a>ID3DXKeyframedAnimationSet：： RegisterAnimationSRTKeys 方法

註冊調整、旋轉和轉譯 (SRT) 動畫的主要畫面格資料。

## <a name="syntax"></a>語法


```C++
HRESULT RegisterAnimationSRTKeys(
  [in]        LPCSTR               pName,
  [in]        UINT                 NumScaleKeys,
  [in]        UINT                 NumRotationKeys,
  [in]        UINT                 NumTranslationKeys,
  [in]  const LPD3DXKEY_VECTOR3    *pScaleKeys,
  [in]  const LPD3DXKEY_QUATERNION *pRotationKeys,
  [in]  const LPD3DXKEY_VECTOR3    *pTranslationKeys,
  [out]       DWORD                *pAnimationIndex
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

動畫名稱的指標。

</dd> <dt>

*NumScaleKeys* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

調整金鑰數目。

</dd> <dt>

*NumRotationKeys* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

輪替索引鍵的數目。

</dd> <dt>

*NumTranslationKeys* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

轉譯金鑰數目。

</dd> <dt>

*pScaleKeys* \[在\]
</dt> <dd>

Type： **Const [**LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) \***

使用者配置的 [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) 向量指標的位址，此方法會以調整資料填滿該陣列。

</dd> <dt>

*pRotationKeys* \[在\]
</dt> <dd>

Type： **Const [**LPD3DXKEY \_ 四元數**](d3dxkey-quaternion.md) \***

[**D3DXKEY \_ 四元**](d3dxkey-quaternion.md)數四元數之使用者配置陣列的指標位址，此方法會以旋轉資料填滿。

</dd> <dt>

*pTranslationKeys* \[在\]
</dt> <dd>

Type： **Const [**LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) \***

使用者配置的 [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) 向量指標的位址，此方法會以轉譯資料填滿該陣列。

</dd> <dt>

*pAnimationIndex* \[擴展\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

傳回動畫索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL

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
</dt> <dt>

[**ID3DXKeyframedAnimationSet::GetNumRotationKeys**](id3dxkeyframedanimationset--getnumrotationkeys.md)
</dt> <dt>

[**ID3DXKeyframedAnimationSet::GetNumTranslationKeys**](id3dxkeyframedanimationset--getnumtranslationkeys.md)
</dt> </dl>

 

 
