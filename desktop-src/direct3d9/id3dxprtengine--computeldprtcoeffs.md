---
description: 計算本地 deformable 預先計算 radiance 傳輸 (LDPRT 相對於每個樣本一般向量的) 係數，以將輸入 ID3DXPRTBuffer 資料的最小平方誤差降至最低。
ms.assetid: 302c20cd-d495-4a23-9692-7456355471eb
title: 'ID3DXPRTEngine：： ComputeLDPRTCoeffs 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeLDPRTCoeffs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 351ecb8022e06b1a5a24abad8fa8541798d13ba0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988221"
---
# <a name="id3dxprtenginecomputeldprtcoeffs-method"></a>ID3DXPRTEngine：： ComputeLDPRTCoeffs 方法

計算本地 deformable 預先計算 radiance 傳輸 (LDPRT 相對於每個樣本一般向量的) 係數，以將輸入 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 資料的最小平方誤差降至最低。 這些係數可搭配 skinned 或轉換的一般向量使用，以在動態物件上建立全域效果的模型。

## <a name="syntax"></a>語法


```C++
HRESULT ComputeLDPRTCoeffs(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      UINT            Order,
  [in, out] D3DXVECTOR3     *pNormOut,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDataIn* \[在\]
</dt> <dd>

類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

輸入的指標 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 球面調和 (SH) 預先計算 radiance 傳輸 (PRT) 資料物件。

</dd> <dt>

*訂單* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

SH 評估的順序。 必須在 [D3DXSH \_ MINORDER](other-d3dx-constants.md) 到 D3DXSH \_ MAXORDER （含）的範圍內。 評估會產生順序²係數。 評估的程度是順序-1。

</dd> <dt>

*pNormOut* \[in、out\]
</dt> <dd>

類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***

選用的向量陣列，要以最適合已優化 LDPRT 係數的著色器最佳標準向量來填滿。 這個陣列的大小必須與 pDataIn 中的樣本數相同。 如果是 **Null**，則會使用介面法線向量。

</dd> <dt>

*pDataOut* \[in、out\]
</dt> <dd>

類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

輸出 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標，該物件包含每個色彩通道每個樣本的順序區域調和係數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

您可以選擇性地使用這個方法來取得陰影一般向量的解決方案。 這些一般向量以及 LDPRT 係數可以更精確地呈現 PRT 信號。 在此情況下，係數代表一般方向的區域性諧波導向。

這個方法無法搭配 [**ID3DXPRTEngine：： ComputeSurfSamplesBounce**](id3dxprtengine--computesurfsamplesbounce.md) 或 [**ID3DXPRTEngine：： ComputeSurfSamplesDirectSH**](id3dxprtengine--computesurfsamplesdirectsh.md)的結果使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
