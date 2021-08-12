---
description: 取得網狀的點 rep 緩衝區。
ms.assetid: 4be7bee5-15ea-496f-83c2-a3a9bafd97c6
title: 'ID3DX10Mesh：： GetPointRepBuffer 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetPointRepBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4e3c23f4ac4e77d97d290075ba6970062af9ea3a44c608d02e98c05e8f248b07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540234"
---
# <a name="id3dx10meshgetpointrepbuffer-method"></a>ID3DX10Mesh：： GetPointRepBuffer 方法

取得網狀的點 rep 緩衝區。

## <a name="syntax"></a>語法


```C++
HRESULT GetPointRepBuffer(
  [out] ID3DX10MeshBuffer **ppPointReps
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppPointReps* \[擴展\]
</dt> <dd>

類型： **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***

包含網格點代表資料的網狀緩衝區指標。 請參閱 [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)。

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

 

 




