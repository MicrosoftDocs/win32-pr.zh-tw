---
description: 計算目前的光源投射到球面調和 (SH) 基礎向量（代表指定位置的事件 radiance）。
ms.assetid: 4d07b288-aec1-48eb-8d27-f3d7d8cfb69e
title: 'ID3DXPRTEngine：： ComputeVolumeSamplesDirectSH 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeVolumeSamplesDirectSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 757e227907eab73848f43b2b8e2f40f9b4b1071b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991492"
---
# <a name="id3dxprtenginecomputevolumesamplesdirectsh-method"></a>ID3DXPRTEngine：： ComputeVolumeSamplesDirectSH 方法

計算目前的光源投射到球面調和 (SH) 基礎向量（代表指定位置的事件 radiance）。

## <a name="syntax"></a>語法


```C++
HRESULT ComputeVolumeSamplesDirectSH(
  [in]            UINT            OrderIn,
  [in]            UINT            OrderOut,
  [in]            UINT            NumVolSamples.xml,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*訂單* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

距離光線的 SH 標記法的順序。 必須在 [D3DXSH \_ MINORDER](other-d3dx-constants.md) 到 D3DXSH \_ MAXORDER （含）的範圍內。 評估的程度是訂單-1。

</dd> <dt>

*OrderOut* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

區域光源的 SH 標記法的順序。 必須在 [D3DXSH \_ MINORDER](other-d3dx-constants.md) 到 D3DXSH \_ MAXORDER （含）的範圍內。 評估的程度是 OrderOut-1。

</dd> <dt>

*NumVolSamples.xml* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

範例位置的數目。

</dd> <dt>

*pSampleLocs* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***

每個範例的位置。

</dd> <dt>

*pDataOut* \[in、out\]
</dt> <dd>

類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

輸出 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標，此物件會將最遠的光源投射到 SH 基礎向量中。 這個緩衝區必須有配置給模擬的適當顏色通道數目。 這個方法會 \* 在每個範例位置的每個通道產生訂單² OrderOut "²純量。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

這個方法會計算距離來源的光線如何抵達 pSampleLocs 所指定空間中的每個點。 SH 係數代表來源 radiance 到傳輸事件 radiance 的每個 pSampleLocs 點的對應。

若要成功使用此方法，您必須在 [**ID3DXPRTEngine：： SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md); 中以 UseSphere = **TRUE** 和 UseCosine = **FALSE** 的球體設定取樣否則，這個方法會傳回 D3DERR INVALIDCALL 的錯誤 \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeVolumeSamples**](id3dxprtengine--computevolumesamples.md)
</dt> </dl>

 

 
