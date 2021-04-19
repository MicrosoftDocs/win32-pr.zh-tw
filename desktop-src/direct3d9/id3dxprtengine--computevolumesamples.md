---
description: 計算上一個光源的投射投射到球面調和 (SH) 基礎向量（代表指定位置的事件 radiance）。
ms.assetid: ccde7c59-cb82-4d61-822a-e1e9ecea0a28
title: 'ID3DXPRTEngine：： ComputeVolumeSamples 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeVolumeSamples
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bd77fff723f0cf7e3dc2a52be6a40ff6f0d71fe1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982044"
---
# <a name="id3dxprtenginecomputevolumesamples-method"></a>ID3DXPRTEngine：： ComputeVolumeSamples 方法

計算上一個光源的投射投射到球面調和 (SH) 基礎向量（代表指定位置的事件 radiance）。

## <a name="syntax"></a>語法


```C++
HRESULT ComputeVolumeSamples(
  [in]            LPD3DXPRTBUFFER pSurfDataIn,
  [in]            UINT            Order,
  [in]            UINT            NumVolSamples.xml,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSurfDataIn* \[在\]
</dt> <dd>

類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

輸入 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標，該物件代表前一個光線彈跳的3d 物件。

</dd> <dt>

*訂單* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

SH 評估的順序。 必須在 [D3DXSH \_ MINORDER](other-d3dx-constants.md) 到 D3DXSH \_ MAXORDER （含）的範圍內。 評估會產生順序²係數。 評估的程度是順序-1。

</dd> <dt>

*NumVolSamples.xml* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

範例位置的數目。

</dd> <dt>

*pSampleLocs* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***

每個範例的位置。 如果 pSampleLocs 為 **Null**，則 ComputeVolumeSamples 會在每個網格頂點計算傳輸矩陣。 但是，如果 pSampleLocs 不是 **Null**，您就必須在球體 (set UseSphere = **TRUE** and UseCosine = **FALSE** 的 [**ID3DXPRTEngine：： SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md)) ;否則，ComputeVolumeSamples 會傳回 D3DERR \_ INVALIDCALL。

</dd> <dt>

*pDataOut* \[in、out\]
</dt> <dd>

類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

輸出 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標，該物件會投射上一個光源的直接光源，以 SH 為單位的向量。 這個緩衝區必須有配置給模擬的適當顏色通道數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

這個方法會計算來源 radiance 函式中的光線如何反映出表示場景 (pSurfDataIn) ，然後抵達 pSampleLocs 所指定空間中每個點的介面。 SH 係數代表來源 radiance 到傳輸事件 radiance 的每個 pSampleLocs 點的對應。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeVolumeSamplesDirectSH**](id3dxprtengine--computevolumesamplesdirectsh.md)
</dt> </dl>

 

 
