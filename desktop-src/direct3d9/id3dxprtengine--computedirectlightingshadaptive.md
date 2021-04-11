---
description: 使用調適型取樣，計算以球面調和 (SH) 近似值表示之3D 物件的直接光源比重。
ms.assetid: 792d8460-d608-4384-ac1c-556435074580
title: 'ID3DXPRTEngine：： ComputeDirectLightingSHAdaptive 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSHAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8abbcfd955fa909166b53f6e050b9aff5837508d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696860"
---
# <a name="id3dxprtenginecomputedirectlightingshadaptive-method"></a>ID3DXPRTEngine：： ComputeDirectLightingSHAdaptive 方法

使用調適型取樣，計算以球面調和 (SH) 近似值表示之3D 物件的直接光源比重。 這個方法會在網格上產生新的頂點和臉部，以更精確地近似預先計算 radiance 傳輸 (PRT) 信號。

## <a name="syntax"></a>語法


```C++
HRESULT ComputeDirectLightingSHAdaptive(
  [in]      UINT            Order,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*訂單* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

SH 評估的順序。 必須在 [D3DXSH \_ MINORDER](other-d3dx-constants.md) 到 D3DXSH \_ MAXORDER （含）的範圍內。 評估會產生順序²係數。 評估的程度是順序-1。

</dd> <dt>

*AdaptiveThresh* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

用於細分網格頂點和臉部的 PRT 向量閾值。 如果小於 1e-6f，則會指定值為 1e-6f 的預設值。

</dd> <dt>

*MinEdgeLength* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

自動調整取樣中將產生的最小臉部邊長度。 如果方法判斷該值太小，則會指定模型相依的值。 如果為零，則會指定預設值4。

</dd> <dt>

*MaxSubdiv* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

臉部的最大細分層級，將用於適應性取樣中。

</dd> <dt>

*pDataOut* \[in、out\]
</dt> <dd>

類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

輸出 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標。 這個緩衝區必須有配置給模擬的適當顏色通道數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::RobustMeshRefine**](id3dxprtengine--robustmeshrefine.md)
</dt> </dl>

 

 
