---
description: 抓取網格頂點的 >albedo 值。
ms.assetid: 12b8d6d1-c806-4dcd-80ac-f3963215dcf4
title: 'ID3DXPRTEngine：： GetVertexAlbedo 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.GetVertexAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7926f6393221552107667c9209ef2b4c51945ab8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986542"
---
# <a name="id3dxprtenginegetvertexalbedo-method"></a>ID3DXPRTEngine：： GetVertexAlbedo 方法

抓取網格頂點的 >albedo 值。

## <a name="syntax"></a>語法


```C++
HRESULT GetVertexAlbedo(
  [in, out] D3DXCOLOR *pVertColors,
  [in]      UINT      NumVerts
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVertColors* \[in、out\]
</dt> <dd>

類型： **[ **D3DXCOLOR**](d3dxcolor.md)\***

網格頂點的 >albedo 值之目的地陣列的指標。 請參閱 [**D3DXCOLOR**](d3dxcolor.md)。

</dd> <dt>

*NumVerts* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

網格中的頂點數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
