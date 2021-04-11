---
description: 捕獲呈現介面的參數。
ms.assetid: 4f46a4c6-7c50-479c-b2f5-24edff590c57
title: 'ID3DXRenderToSurface：： GetDesc 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 00824c6b418a3e6707ebfd588d8d32d4e38f173d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196432"
---
# <a name="id3dxrendertosurfacegetdesc-method"></a>ID3DXRenderToSurface：： GetDesc 方法

捕獲呈現介面的參數。

## <a name="syntax"></a>語法


```C++
HRESULT GetDesc(
  [out] D3DXRTS_DESC *pParameters
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pParameters* \[擴展\]
</dt> <dd>

類型： **[ **D3DXRTS \_ DESC**](d3dxrts-desc.md)\***

[**D3DXRTS \_ DESC**](d3dxrts-desc.md)結構的指標，描述呈現介面的參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXRenderToSurface](id3dxrendertosurface.md)
</dt> </dl>

 

 




