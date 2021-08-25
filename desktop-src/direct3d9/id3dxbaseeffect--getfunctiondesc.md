---
description: 取得函數描述。
ms.assetid: a1a0ccf4-2428-4e60-9af0-07dc2132a367
title: 'ID3DXBaseEffect：： GetFunctionDesc 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFunctionDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b8f74715b163b3d197f62274c6aa6bf52ae872254db9df8225e061dc54900964
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893718"
---
# <a name="id3dxbaseeffectgetfunctiondesc-method"></a>ID3DXBaseEffect：： GetFunctionDesc 方法

取得函數描述。

## <a name="syntax"></a>語法


```C++
HRESULT GetFunctionDesc(
  [in]  D3DXHANDLE        hFunction,
  [out] D3DXFUNCTION_DESC *pDesc
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hFunction* \[在\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

函數控制碼。 請參閱 [處理 (Direct3D 9) ](handles.md)。

</dd> <dt>

*pDesc* \[擴展\]
</dt> <dd>

類型： **[ **D3DXFUNCTION \_ DESC**](d3dxfunction-desc.md)\***

傳回函數的描述。 請參閱 [**D3DXFUNCTION \_ DESC**](d3dxfunction-desc.md)。

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

 

 




