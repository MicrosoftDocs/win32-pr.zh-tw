---
description: 取得注釋的控制碼。
ms.assetid: 433d73b7-9371-4d76-8b34-a64c608eb1a3
title: 'ID3DXBaseEffect：： GetAnnotation 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetAnnotation
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c35deeb04e7cf21be429976c102fdf7c3126b1691b3f63725fc994ef79f7ad42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279008"
---
# <a name="id3dxbaseeffectgetannotation-method"></a>ID3DXBaseEffect：： GetAnnotation 方法

取得注釋的控制碼。

## <a name="syntax"></a>語法


```C++
D3DXHANDLE GetAnnotation(
  [in] D3DXHANDLE hObject,
  [in] UINT       Index
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hObject* \[在\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

技術、傳遞或最上層參數的控制碼。 請參閱 [處理 (Direct3D 9) ](handles.md)。

</dd> <dt>

*索引* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

批註索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

傳回指定之注釋的控制碼，如果索引無效，則 **為 Null** 。 請參閱 [處理 (Direct3D 9) ](handles.md)。

## <a name="remarks"></a>備註

批註是使用者特定的資料，可附加至任何技術、傳遞或參數。 請參閱 [處理 (Direct3D 9) ](handles.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
