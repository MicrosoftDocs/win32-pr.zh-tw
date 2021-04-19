---
description: 從 ID3DXPRTCompBuffer 壓縮的資料緩衝區中，針對指定的叢集，將 mean 和主體元件分析 (PCA) 基礎向量。
ms.assetid: dcb1372f-2c8f-4d18-9840-5982b2ed0d6e
title: 'ID3DXPRTCompBuffer：： ExtractBasis 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractBasis
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ebedef91c9f3d1e277a099ffd295903e9ba77ba8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106998586"
---
# <a name="id3dxprtcompbufferextractbasis-method"></a>ID3DXPRTCompBuffer：： ExtractBasis 方法

從 [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) 壓縮的資料緩衝區中，針對指定的叢集，將 mean 和主體元件分析 (PCA) 基礎向量。

## <a name="syntax"></a>語法


```C++
HRESULT ExtractBasis(
  [in]      UINT  Cluster,
  [in, out] FLOAT *pClusterBasis
);
```



## <a name="parameters"></a>參數

<dl> <dt>

叢集 \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

將解壓縮其基礎的叢集。

</dd> <dt>

*pClusterBasis* \[in、out\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

叢集之基礎向量資料陣列的指標。 儲存的 FLOAT 資料大小將會是： (1 + 每個叢集的 PCA 向量數目) \* (係數數目) \* (色頻數目) 

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

 

 
