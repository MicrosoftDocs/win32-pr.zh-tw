---
description: 計算3D 物件的直接光源比重，其中來源 radiance 是以球面調和 (SH) 近似值表示。
ms.assetid: 52d614cc-578a-4f2b-ba91-70d0c4371042
title: 'ID3DXPRTEngine：： ComputeDirectLightingSH 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 01b6c3cff082c40c4df5d9bee1d997599a41965b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986552"
---
# <a name="id3dxprtenginecomputedirectlightingsh-method"></a>ID3DXPRTEngine：： ComputeDirectLightingSH 方法

計算3D 物件的直接光源比重，其中來源 radiance 是以球面調和 (SH) 近似值表示。

## <a name="syntax"></a>語法


```C++
HRESULT ComputeDirectLightingSH(
  [in]      UINT            Order,
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

*pDataOut* \[in、out\]
</dt> <dd>

類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

輸出 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標，該物件會以 SH 近似值來將直接光源比重模型。 這個緩衝區必須有配置給模擬的適當顏色通道數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

輸出不會包含 >albedo，而且模擬器中只會整合連入的光線。 藉由不乘以 >albedo，您可以使用比來源 radiance 更精細的規模來建立 >albedo 變異的模型，進而從壓縮產生更精確的結果。

呼叫 [**ID3DXPRTEngine：： MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) ，以將每個預先計算 radiance 傳輸 (PRT) vector 乘以 >albedo。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
