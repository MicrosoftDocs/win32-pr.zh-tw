---
description: 取得任意參數或注釋的值，包括簡單類型、結構、陣列、字串、著色器和紋理。 這個方法可以用來取代 ID3DXBaseEffect 中幾乎所有的 Getxxx 呼叫。
ms.assetid: 41343922-99a7-486f-b4b0-1aa07f339664
title: 'ID3DXBaseEffect：： GetValue 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 166635b22875692da0396f1c7c2145f13ca08df3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992290"
---
# <a name="id3dxbaseeffectgetvalue-method"></a>ID3DXBaseEffect：： GetValue 方法

取得任意參數或注釋的值，包括簡單類型、結構、陣列、字串、著色器和紋理。 這個方法可以用來取代 [**ID3DXBaseEffect**](id3dxbaseeffect.md)中幾乎所有的 Getxxx 呼叫。

## <a name="syntax"></a>語法


```C++
HRESULT GetValue(
  [in]  D3DXHANDLE hParameter,
  [out] LPVOID     pData,
  [in]  UINT       Bytes
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hParameter* \[在\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

唯一識別碼。 請參閱 [處理 (Direct3D 9) ](handles.md)。

</dd> <dt>

*.pdata* \[擴展\]
</dt> <dd>

類型： **[ **LPVOID**](../winprog/windows-data-types.md)**

傳回包含值的緩衝區。

</dd> <dt>

*位元組* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

\[緩衝區中的 \] 位元組數目。 \_如果您知道您的緩衝區夠大而足以包含整個參數，且您想要略過大小驗證，則會傳入 D3DX 預設值。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Shader。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**SetValue**](id3dxbaseeffect--setvalue.md)
</dt> </dl>

 

 
