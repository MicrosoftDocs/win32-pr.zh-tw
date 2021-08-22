---
description: ID3DX10Mesh：:D rawSubset 方法-繪製網格的子集。
ms.assetid: e785949e-fcda-4ef9-b50a-193cd954e97d
title: 'ID3DX10Mesh：:D rawSubset 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.DrawSubset
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 75723819ab7a4f82f25a68dfc2f0017e8b871130a8e0fbe70c939a95de221426
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753098"
---
# <a name="id3dx10meshdrawsubset-method"></a>ID3DX10Mesh：:D rawSubset 方法

繪製網格的子集。

## <a name="syntax"></a>語法


```C++
HRESULT DrawSubset(
  [in] UINT AttribId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*AttribId* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

指定要繪製的網格子集。 此值可用來區分網格中的臉部，以屬於一或多個屬性群組。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="remarks"></a>備註

屬性工作表用來識別需要以不同紋理、轉譯狀態、材質等等繪製的網格區域。 此外，應用程式也可以使用屬性工作表來隱藏部分網格，而不是在繪製框架時 (AttribId) 繪製指定的屬性識別碼。

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

 

 
