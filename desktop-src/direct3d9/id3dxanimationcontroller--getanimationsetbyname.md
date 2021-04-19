---
description: 取得動畫集合，並指定其名稱。
ms.assetid: 4c3f3002-45f6-49b2-8a42-18d5824fb36f
title: 'ID3DXAnimationController：： GetAnimationSetByName 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetAnimationSetByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d520625e457a50fe962ae74d6e25fc17e2beb729
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982893"
---
# <a name="id3dxanimationcontrollergetanimationsetbyname-method"></a>ID3DXAnimationController：： GetAnimationSetByName 方法

取得動畫集合，並指定其名稱。

## <a name="syntax"></a>語法


```C++
HRESULT GetAnimationSetByName(
  [in]  LPCSTR             pName,
  [out] LPD3DXANIMATIONSET *ppAnimSet
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

字串，包含動畫集合的名稱。

</dd> <dt>

*ppAnimSet* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)\***

[**ID3DXAnimationSet**](id3dxanimationset.md)動畫集合的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

動畫控制器包含動畫集合的陣列。 這個方法會傳回具有指定名稱的動畫集。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
