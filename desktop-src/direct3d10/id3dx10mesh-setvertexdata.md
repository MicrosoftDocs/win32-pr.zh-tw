---
description: 將頂點資料設定為其中一個網格的頂點緩衝區。
ms.assetid: 930cbc49-4202-431f-ac72-386c31acd87e
title: 'ID3DX10Mesh：： SetVertexData 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetVertexData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 68d54c6868e44517d42e0b53159f7a23ef45a05a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981844"
---
# <a name="id3dx10meshsetvertexdata-method"></a>ID3DX10Mesh：： SetVertexData 方法

將頂點資料設定為其中一個網格的頂點緩衝區。

## <a name="syntax"></a>語法


```C++
HRESULT SetVertexData(
  [in]       UINT iBuffer,
  [in] const void *pData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*windows.storage.streams.ibuffer* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要以 .Pdata 填滿的頂點緩衝區。

</dd> <dt>

*.pdata* \[在\]
</dt> <dd>

類型： **const void \***

要設定的頂點資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
