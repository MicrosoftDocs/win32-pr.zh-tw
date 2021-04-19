---
description: 在網格上細分臉部，以提供不會消除網格上功能的保守調適型取樣。
ms.assetid: 0d74a01a-de67-4607-99eb-ed98e239f199
title: 'ID3DXPRTEngine：： RobustMeshRefine 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.RobustMeshRefine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 65d49fcec3072956365ce1ed8dc5d7a11ce6c826
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991977"
---
# <a name="id3dxprtenginerobustmeshrefine-method"></a>ID3DXPRTEngine：： RobustMeshRefine 方法

在網格上細分臉部，以提供不會消除網格上功能的保守調適型取樣。

## <a name="syntax"></a>語法


```C++
HRESULT RobustMeshRefine(
  [in] FLOAT MinEdgeLength,
  [in] UINT  MaxSubdiv
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*MinEdgeLength* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

自動調整取樣中將產生的最小臉部邊長度。 如果為零，將會取代合理的預設值。

</dd> <dt>

*MaxSubdiv* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

臉部的最大細分層級，將用於適應性取樣中。 如果為零，則會替代預設值5。

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
</dt> <dt>

[**ID3DXPRTEngine::ComputeBounceAdaptive**](id3dxprtengine--computebounceadaptive.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeDirectLightingSHAdaptive**](id3dxprtengine--computedirectlightingshadaptive.md)
</dt> </dl>

 

 
