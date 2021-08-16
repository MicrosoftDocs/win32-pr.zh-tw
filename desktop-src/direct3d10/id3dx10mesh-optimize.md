---
description: ID3DX10Mesh：： Optimize 方法-產生具有重新排列臉部和頂點的新網格，以將繪製效能優化。
ms.assetid: c03e112a-7c9b-4082-9afe-42e1c20b5f4d
title: 'ID3DX10Mesh：： Optimize 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Optimize
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 41bc7b4ac7fb263073a88cd998190b0fa6e044d528f9d3f4613c3284f28c0f47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118302573"
---
# <a name="id3dx10meshoptimize-method"></a>ID3DX10Mesh：： Optimize 方法

產生具有重新排序臉部和頂點的新網格，以將繪製效能優化。

## <a name="syntax"></a>語法


```C++
HRESULT Optimize(
  [in]  UINT        Flags,
  [in]  UINT        *pFaceRemap,
  [out] LPD3D10BLOB *ppVertexRemap
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*旗標* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

指定要執行的優化類型。 這個參數可以設定為 D3DXMESHOPT 和 D3DXMESH (的一或多個旗標的組合，除了 D3DXMESH \_ 32 位、D3DXMESH \_ IB \_ WRITEONLY 和 D3DXMESH \_ WRITEONLY) 之外。

</dd> <dt>

*pFaceRemap* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

UINTs 的陣列，每個臉部各一個，用來識別對應至優化網格中各臉部的原始網格臉部。 如果提供給此引數的值為 **Null**，則不會傳回臉部重新對應資料。

</dd> <dt>

*ppVertexRemap* \[擴展\]
</dt> <dd>

類型： **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***

[**ID3D10Blob 介面**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)指標的位址，其中包含每個頂點的 DWORD，以指定新頂點如何對應至舊頂點。 如果您需要根據新的頂點對應來改變外部資料，這個重新對應會很有用。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="remarks"></a>備註

這個方法會產生新的網格。 執行 Optimize 之前，應用程式必須藉由呼叫 [**ID3DX10Mesh：： GenerateAdjacencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md)來產生連續的緩衝區。 鄰接緩衝區包含連續的資料，例如邊緣清單和彼此連續的臉部。

這個方法與 [**ID3DX10Mesh：： CloneMesh**](id3dx10mesh-clonemesh.md) 方法非常類似，不同之處在于它可以在產生新的網格複製時執行優化。 輸出網格會繼承輸入網格的所有建立參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
