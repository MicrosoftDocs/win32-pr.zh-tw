---
description: 驗證技巧。
ms.assetid: d69eaafa-da4d-4599-86fb-83d72e1664cc
title: 'ID3DXEffect：： ValidateTechnique 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.ValidateTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b48ffa8707a3f78e76555d57225c11f89160fdd7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997615"
---
# <a name="id3dxeffectvalidatetechnique-method"></a>ID3DXEffect：： ValidateTechnique 方法

驗證技巧。

## <a name="syntax"></a>語法


```C++
HRESULT ValidateTechnique(
  [in] D3DXHANDLE hTechnique
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hTechnique* \[在\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

唯一識別碼。 請參閱 [處理 (Direct3D 9) ](handles.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DERR \_ CONFLICTINGRENDERSTATE、D3DERR \_ CONFLICTINGTEXTUREFILTER、D3DERR \_ DEVICELOST、D3DERR \_ DRIVERINTERNALERROR、D3DERR \_ TOOMANYOPERATIONS、D3DERR UNSUPPORTEDALPHAARG、 \_ D3DERR \_ \_ \_ \_ \_ UNSUPPORTEDALPHAOPERATION、D3DERR UNSUPPORTEDCOLORARG、D3DERR UNSUPPORTEDCOLOROPERATION、D3DERR UNSUPPORTEDFACTORVALUE、D3DERR UNSUPPORTEDTEXTUREFILTER 和 D3DERR \_ WRONGTEXTUREFORMAT。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect::SetTechnique**](id3dxeffect--settechnique.md)
</dt> </dl>

 

 




