---
description: 取得傳遞描述。
ms.assetid: 44c65a82-bcf4-49f5-9312-8320e133bb2f
title: 'ID3DXBaseEffect：： GetPassDesc 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPassDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 74106bc38367e13cd70af94d0ad12016165aaae24693f19386e69ebe1d7a5cb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987748"
---
# <a name="id3dxbaseeffectgetpassdesc-method"></a>ID3DXBaseEffect：： GetPassDesc 方法

取得傳遞描述。

## <a name="syntax"></a>語法


```C++
HRESULT GetPassDesc(
  [in]  D3DXHANDLE    hPass,
  [out] D3DXPASS_DESC *pDesc
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hPass* \[在\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Pass 控制碼。 請參閱 [處理 (Direct3D 9) ](handles.md)。

</dd> <dt>

*pDesc* \[擴展\]
</dt> <dd>

類型： **[ **D3DXPASS \_ DESC**](d3dxpass-desc.md)\***

傳回指定之傳遞的描述。 請參閱 [**D3DXPASS \_ DESC**](d3dxpass-desc.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

> [!Note]  
> 如果使用 [D3DXFX \_ NOT \_ CLONEABLE](d3dxfx.md)建立效果，這個方法將會傳回 **Null** 指標 (在 [**D3DXPASS \_ DESC**](d3dxpass-desc.md)) 至著色器函式。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 




