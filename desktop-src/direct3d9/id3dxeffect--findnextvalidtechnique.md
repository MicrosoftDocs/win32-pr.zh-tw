---
description: 搜尋下一個有效的技巧，從指定技術之後的技巧開始。
ms.assetid: 0d2f3f80-90fd-495d-acb8-075f50e9a974
title: 'ID3DXEffect：： FindNextValidTechnique 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.FindNextValidTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: adcaaa5194abeb17d110118de922811eb84af7fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386467"
---
# <a name="id3dxeffectfindnextvalidtechnique-method"></a>ID3DXEffect：： FindNextValidTechnique 方法

搜尋下一個有效的技巧，從指定技術之後的技巧開始。

## <a name="syntax"></a>語法


```C++
HRESULT FindNextValidTechnique(
  [in]  D3DXHANDLE hTechnique,
  [out] D3DXHANDLE *pTechnique
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hTechnique* \[在\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

技術的唯一識別碼。 請參閱 [處理 (Direct3D 9) ](handles.md)。 請為此參數指定 **Null** ，以找出第一個有效的技巧。

</dd> <dt>

*pTechnique* \[擴展\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)\***

下一項技術的識別碼指標。 如果這是最後一項技術，就會傳回 **Null** 。 請參閱 [處理 (Direct3D 9) ](handles.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**D3DXTECHNIQUE \_ DESC**](d3dxtechnique-desc.md)
</dt> <dt>

[**ID3DXEffect::ValidateTechnique**](id3dxeffect--validatetechnique.md)
</dt> </dl>

 

 




