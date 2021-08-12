---
description: 取得參數或注釋描述。
ms.assetid: fd54eb08-a7e4-4106-b0ed-49a4da7fcadc
title: 'ID3DXBaseEffect：： GetParameterDesc 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8c60332909ef601d58cb624201bae6e1934a84699ead1227a5d8a83c2db64dc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118296701"
---
# <a name="id3dxbaseeffectgetparameterdesc-method"></a>ID3DXBaseEffect：： GetParameterDesc 方法

取得參數或注釋描述。

## <a name="syntax"></a>語法


```C++
HRESULT GetParameterDesc(
  [in]  D3DXHANDLE         hParameter,
  [out] D3DXPARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hParameter* \[在\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

參數或注釋控制碼。 請參閱 [處理 (Direct3D 9) ](handles.md)。

</dd> <dt>

*pDesc* \[擴展\]
</dt> <dd>

類型： **[ **D3DXPARAMETER \_ DESC**](d3dxparameter-desc.md)\***

傳回指定之參數或注釋的描述。 請參閱 [**D3DXPARAMETER \_ DESC**](d3dxparameter-desc.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 




