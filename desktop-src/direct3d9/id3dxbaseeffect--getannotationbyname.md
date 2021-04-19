---
description: 藉由查詢名稱來取得批註的控制碼。
ms.assetid: da4e2805-5f06-4a9b-836f-85a8c154c502
title: 'ID3DXBaseEffect：： GetAnnotationByName 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetAnnotationByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 00698030488b8f4ae788367f87b8d569476292ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981858"
---
# <a name="id3dxbaseeffectgetannotationbyname-method"></a>ID3DXBaseEffect：： GetAnnotationByName 方法

藉由查詢名稱來取得批註的控制碼。

## <a name="syntax"></a>語法


```C++
D3DXHANDLE GetAnnotationByName(
  [in] D3DXHANDLE hObject,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hObject* \[在\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

技術、傳遞或最上層參數的控制碼。 請參閱 [處理 (Direct3D 9) ](handles.md)。

</dd> <dt>

*pName* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

包含批註名稱的字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

傳回指定之注釋的控制碼，如果找不到名稱，則 **為 Null** 。 請參閱 [處理 (Direct3D 9) ](handles.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
