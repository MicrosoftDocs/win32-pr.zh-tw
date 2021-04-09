---
description: 取得固定的函式頂點值。
ms.assetid: ed56ff2d-0366-426c-9f9a-7d1a7c5d1a7c
title: 'ID3DXBaseMesh：： GetFVF 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7ee76292c30b3dfb0a2e38b060f50ef643ae07ae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946138"
---
# <a name="id3dxbasemeshgetfvf-method"></a>ID3DXBaseMesh：： GetFVF 方法

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

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
