---
description: 計算使用 ID3DXPRTEngine：： SetMeshMaterials 所設定的調適型取樣和材質屬性，將來源 radiance 對應至地下散佈所產生之結束 radiance 的傳輸向量。
ms.assetid: 34e42271-703b-4b67-8153-2eca3f8dde92
title: 'ID3DXPRTEngine：： ComputeSSAdaptive 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSSAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 198a597020a0bfcbc789cc741e42048bd89eb95f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993920"
---
# <a name="id3dxprtenginecomputessadaptive-method"></a>ID3DXPRTEngine：： ComputeSSAdaptive 方法

計算使用 [**ID3DXPRTEngine：： SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md)所設定的調適型取樣和材質屬性，將來源 radiance 對應至地下散佈所產生之結束 radiance 的傳輸向量。 方法會在網格上產生新的頂點和臉部，以更精確地近似預先計算 radiance 傳輸 (PRT) 信號。 這個方法僅適用于網格物件中每個頂點定義的材質。

## <a name="syntax"></a>語法


```C++
HRESULT ComputeSSAdaptive(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDataIn* \[在\]
</dt> <dd>

類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

輸入 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標，該物件代表前一個光線彈跳的3d 物件。 此輸入緩衝區必須有配置給模擬的適當顏色通道數目。

</dd> <dt>

*AdaptiveThresh* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

用於細分網格頂點和臉部的 PRT 向量閾值。 如果小於 1e-6f，則會指定值為 1e-6f 的預設值。

</dd> <dt>

*MinEdgeLength* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

自動調整取樣中將產生的最小臉部邊長度。 如果方法判斷該值太小，則會指定模型相依的值。

</dd> <dt>

*MaxSubdiv* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

臉部的最大細分層級，將用於適應性取樣中。 如果為零，則會指定預設值4。

</dd> <dt>

*pDataOut* \[in、out\]
</dt> <dd>

類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

輸出 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標，該物件會為地下分散的光線建立單一彈跳的模型。 此輸出緩衝區必須有配置給模擬的適當顏色通道數目。

</dd> <dt>

*pDataTotal* \[in、out\]
</dt> <dd>

類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

選擇性 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標，該物件為所有先前 pDataOut 輸出的執行總和。 可能是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

若要建立地下散佈的模型，請在呼叫 [**ID3DXPRTEngine：： ComputeDirectLightingSHAdaptive**](id3dxprtengine--computedirectlightingshadaptive.md) 方法之後，針對每個燈光彈跳呼叫這個方法。

此方法的輸出不包含 >albedo，而且模擬器中只會整合連入的光線。 藉由不乘以 >albedo，您可以使用比來源 radiance 更精細的規模來建立 >albedo 變異的模型，進而從壓縮產生更精確的結果。

呼叫 [**ID3DXPRTEngine：： MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) ，以將每個 PRT 向量乘以 >albedo。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeBounce**](id3dxprtengine--computebounce.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeSS**](id3dxprtengine--computess.md)
</dt> </dl>

 

 
