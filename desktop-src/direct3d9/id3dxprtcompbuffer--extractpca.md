---
description: 從 ID3DXPRTCompBuffer 壓縮的資料緩衝區，將每個樣本的主體元件分析 (PCA) 投影係數。
ms.assetid: 149098c2-35ca-46e9-a13a-94906c95cfd9
title: 'ID3DXPRTCompBuffer：： ExtractPCA 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractPCA
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6ef949e9f88a843f4636643dadd7d00ffd94d98b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000575"
---
# <a name="id3dxprtcompbufferextractpca-method"></a>ID3DXPRTCompBuffer：： ExtractPCA 方法

從 [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) 壓縮的資料緩衝區，將每個樣本的主體元件分析 (PCA) 投影係數。

## <a name="syntax"></a>語法


```C++
HRESULT ExtractPCA(
  [in] UINT  StartPCA,
  [in] UINT  NumExtract,
  [in] FLOAT *pPCACoefficients
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*StartPCA* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

開始從緩衝區解壓縮的 PCA 投射係數索引。

</dd> <dt>

*NumExtract* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要從緩衝區中解壓縮的 PCA 投射係數數目。

</dd> <dt>

*pPCACoefficients* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

寫入叢集主體元件分析 (CPCA) 係數之位置的指標。 寫入的資料大小是 (數目的樣本數目) \* (的 PCA 係數數) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則會傳回下列值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
