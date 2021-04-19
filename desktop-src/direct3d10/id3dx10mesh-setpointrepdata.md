---
description: 設定網格的點代表資料。
ms.assetid: 451a1ff0-68fa-48c4-b3f1-d41d7583cb3f
title: 'ID3DX10Mesh：： SetPointRepData 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetPointRepData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 65114c5411de7932e9cb71166fcf8554fa0bf7b6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989210"
---
# <a name="id3dx10meshsetpointrepdata-method"></a>ID3DX10Mesh：： SetPointRepData 方法

設定網格的點代表資料。

## <a name="syntax"></a>語法


```C++
HRESULT SetPointRepData(
  [in] const UINT *pPointReps
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pPointReps* \[在\]
</dt> <dd>

類型： **Const [**UINT**](../winprog/windows-data-types.md) \***

要設定的點代表資料。

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

 

 
