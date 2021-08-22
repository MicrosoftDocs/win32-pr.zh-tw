---
description: ID3DXSkinInfo：： GetFVF 方法-取得固定的函式頂點值。
ms.assetid: 9b80c4b9-2e5b-4965-99b9-ad6c459ef413
title: 'ID3DXSkinInfo：： GetFVF 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e7419e116cddd20aebfc61d7813ea2bd403ce04b897aa821f03a2ad48eae6965
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492288"
---
# <a name="id3dxskininfogetfvf-method"></a>ID3DXSkinInfo：： GetFVF 方法

取得固定的函式頂點值。

## <a name="syntax"></a>語法


```C++
DWORD GetFVF();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

傳回彈性頂點格式 (FVF) 代碼。

## <a name="remarks"></a>備註

如果頂點格式無法直接對應至 FVF 程式碼，則這個方法會傳回0。 這會發生在從頂點宣告所建立的網格中，這些 FVF 碼沒有相同的順序和元素支援。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::SetFVF**](id3dxskininfo--setfvf.md)
</dt> </dl>

 

 
