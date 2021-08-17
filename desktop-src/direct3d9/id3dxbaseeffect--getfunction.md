---
description: 取得函數的控制碼。
ms.assetid: 97c82c28-4402-4605-8247-44d6f38bfa20
title: 'ID3DXBaseEffect：： GetFunction 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFunction
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ff3627c27ce6fa4eac0e166276a94dd5f4c1dd62bc4f8b38ccdd52c365a332fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118094165"
---
# <a name="id3dxbaseeffectgetfunction-method"></a>ID3DXBaseEffect：： GetFunction 方法

取得函數的控制碼。

## <a name="syntax"></a>語法


```C++
D3DXHANDLE GetFunction(
  [in] UINT Index
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

函數索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

傳回指定之函數的控制碼，如果索引無效，則 **為 Null** 。 請參閱 [處理 (Direct3D 9) ](handles.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
