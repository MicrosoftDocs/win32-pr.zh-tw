---
description: 使用 GPU 來計算3D 物件的直接光源比重，其中來源 radiance 是以球面調和 (SH) 近似值表示。 計算 GPU 的照明通常會比 CPU 更快。
ms.assetid: ccea5a5e-23f1-4fdf-bce8-9bfc35d45257
title: 'ID3DXPRTEngine：： ComputeDirectLightingSHGPU 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSHGPU
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e56dd807d28ba6952cd20c971b675b83687a3015
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974898"
---
# <a name="id3dxprtenginecomputedirectlightingshgpu-method"></a>ID3DXPRTEngine：： ComputeDirectLightingSHGPU 方法

使用 GPU 來計算3D 物件的直接光源比重，其中來源 radiance 是以球面調和 (SH) 近似值表示。 計算 GPU 的照明通常會比 CPU 更快。

## <a name="syntax"></a>語法


```C++
HRESULT ComputeDirectLightingSHGPU(
  [in]      LPDIRECT3DDEVICE9 pDevice,
  [in]      UINT              Flags,
  [in]      UINT              Order,
  [in]      FLOAT             ZBias,
  [in]      FLOAT             ZAngleBias,
  [in, out] LPD3DXPRTBUFFER   pDataOut
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

用來在 GPU 上執行模擬之 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) 裝置物件的指標。 裝置必須支援 [ps \_ 2 \_ 0](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-0.md) 圖元著色器。

> [!Note]  
> 回呼函式不應使用 GPU 模擬器所使用的 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) 裝置物件。

 

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

定義陰影 z 緩衝區解析度的 GPU 模擬參數。 應設定為 [**D3DXSHGPUSIMOPT**](./d3dxshgpusimopt.md)中的其中一個常數值。 若要指定更高的精確度模擬，D3DXSHGPUSIMOPT \_ HIGHQUALITY 值可以與其中一個 D3DXSHGPUSIMOPT \_ SHADOWRESxxx 值結合。

</dd> <dt>

*訂單* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

SH 評估的順序。 必須在 [D3DXSH \_ MINORDER](other-d3dx-constants.md) 到 D3DXSH \_ MAXORDER （含）的範圍內。 評估會產生順序²係數。 評估的程度是順序-1。

</dd> <dt>

*ZBias* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

正常方向的偏差。

</dd> <dt>

*ZAngleBias* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

一般方向的偏差，以淺光線乘以角度的余弦值減一。

</dd> <dt>

*pDataOut* \[in、out\]
</dt> <dd>

類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

[**ID3DXPRTBuffer**](id3dxprtbuffer.md)物件的指標。 這個緩衝區必須有配置給模擬的適當顏色通道數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

在這個方法中，>albedo 不會乘以淺信號，而且模擬器中只會整合連入的光線。 藉由不乘以 >albedo，您可以使用比來源 radiance 更精細的規模來建立 >albedo 變異的模型，進而從壓縮產生更精確的結果。

呼叫 [**MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) ，以將每個預先計算 radiance 傳輸 (PRT) 向量乘以 >albedo。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
