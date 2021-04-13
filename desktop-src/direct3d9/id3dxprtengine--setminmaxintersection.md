---
description: 設定3D 物件之間交集的最小和最大距離。
ms.assetid: da825c70-0c55-4303-b78a-a761ba037182
title: 'ID3DXPRTEngine：： SetMinMaxIntersection 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetMinMaxIntersection
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 68845f713289c524afc844037ca305909e5b89b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323036"
---
# <a name="id3dxprtenginesetminmaxintersection-method"></a>ID3DXPRTEngine：： SetMinMaxIntersection 方法

設定3D 物件之間交集的最小和最大距離。 這些距離值可以用來控制物件可以陰影或反映光線的最小或最大距離。 例如，方法可以用來限制3D 模型的鄰近功能遮蔽。

## <a name="syntax"></a>語法


```C++
HRESULT SetMinMaxIntersection(
  [in] FLOAT fMin ,
  [in] FLOAT fMax
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*fMin* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

最小交集距離。 必須是正數且小於 fMax。

</dd> <dt>

*fMax* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

最大交集距離。 如果是 0.0 f，將會使用先前的值;否則，必須大於 fMin。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

此方法不能用於預先計算 radiance 傳輸 (在 GPU 中執行的 PRT) 模擬。 請參閱 [**ID3DXPRTEngine：： ComputeDirectLightingSHGPU**](id3dxprtengine--computedirectlightingshgpu.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
