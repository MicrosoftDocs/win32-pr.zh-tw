---
description: 取得參數的常值狀態。 常值參數的值不會在效果的存留期間變更。
ms.assetid: 417abbee-5193-462e-b0d1-b4928ad0a041
title: 'ID3DXEffectCompiler：： GetLiteral 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.GetLiteral
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c16e3798ab66a34e12812a3560572c45b9206b30
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986081"
---
# <a name="id3dxeffectcompilergetliteral-method"></a>ID3DXEffectCompiler：： GetLiteral 方法

取得參數的常值狀態。 常值參數的值不會在效果的存留期間變更。

## <a name="syntax"></a>語法


```C++
HRESULT GetLiteral(
  [in]  D3DXHANDLE hParameter,
  [out] BOOL       *pLiteral
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hParameter* \[在\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

參數的唯一識別碼。 請參閱 [處理 (Direct3D 9) ](handles.md)。

</dd> <dt>

*pLiteral* \[擴展\]
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)\***

如果參數是常值，則傳回 True，否則傳回 False。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

這種方法只會變更參數是否為常值。 若要變更參數的值，請使用 [**ID3DXBaseEffect：： SetBool**](id3dxbaseeffect--setbool.md) 或 [**ID3DXBaseEffect：： SetValue**](id3dxbaseeffect--setvalue.md)之類的方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Shader。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXEffectCompiler](id3dxeffectcompiler.md)
</dt> <dt>

[ (Direct3D 9) 的使用方式和常值 ](usages-and-literals.md)
</dt> <dt>

[**ID3DXEffectCompiler::SetLiteral**](id3dxeffectcompiler--setliteral.md)
</dt> </dl>

 

 
