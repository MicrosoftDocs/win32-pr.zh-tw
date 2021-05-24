---
description: 取得網狀緩衝區記憶體的指標，以修改其內容。
ms.assetid: d15ed47a-450e-404a-bcc2-a641abc2d02e
title: 'ID3DX10MeshBuffer：： Map 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer.Map
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c4a71aaaffe7ed11429efa67b6065f94ecd154d0
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335352"
---
# <a name="id3dx10meshbuffermap-method"></a>ID3DX10MeshBuffer：： Map 方法

取得網狀緩衝區記憶體的指標，以修改其內容。

## <a name="syntax"></a>語法


```C++
HRESULT Map(
  [out] void   **ppData,
  [out] SIZE_T *pSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppData* \[擴展\]
</dt> <dd>

類型： **void \* \***

緩衝區資料的指標。

</dd> <dt>

*pSize* \[擴展\]
</dt> <dd>

類型： **[**大小 \_ T**](../winprog/windows-data-types.md)\***

以位元組為單位的緩衝區大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="remarks"></a>備註



 Direct3D 9 與 Direct3D 10 之間的差異：

- Direct3D 10 中的 map () 類似于 Direct3D 9 中的資源對應 () 。



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX10MeshBuffer](id3dx10meshbuffer.md)
</dt> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
