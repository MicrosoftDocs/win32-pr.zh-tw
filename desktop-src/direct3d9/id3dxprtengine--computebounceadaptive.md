---
description: 使用調適型取樣來計算由單一 interreflected 燈彈跳產生的來源 radiance。
ms.assetid: 61f8cecd-d95a-4f02-929e-02f2bce5bde9
title: 'ID3DXPRTEngine：： ComputeBounceAdaptive 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeBounceAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: efe983a0160d46910e7b8d1e29d0042d801275ef70aef30f6050e0538b6f9927
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729747"
---
# <a name="id3dxprtenginecomputebounceadaptive-method"></a>ID3DXPRTEngine：： ComputeBounceAdaptive 方法

使用調適型取樣來計算由單一 interreflected 燈彈跳產生的來源 radiance。 這個方法會在網格上產生新的頂點和臉部，以更精確地近似預先計算 radiance 傳輸 (PRT) 信號。 此方法可用於任何照明的場景，包括球形調和 (SH) 為基礎的 PRT 模型。

## <a name="syntax"></a>語法


```C++
HRESULT ComputeBounceAdaptive(
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

輸出 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標。 此輸出緩衝區必須有配置給模擬的適當顏色通道數目。

</dd> <dt>

*pDataTotal* \[in、out\]
</dt> <dd>

類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

選擇性 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標，此物件會保持 pDataOut 的執行總和與每個輕量彈跳計算。 可能是 **Null**。

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

 

 
