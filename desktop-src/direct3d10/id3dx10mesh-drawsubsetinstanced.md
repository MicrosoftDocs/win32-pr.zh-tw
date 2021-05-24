---
description: 繪製相同網格子集的數個實例。
ms.assetid: 2a17ecdb-c6f3-401c-b7ed-8a42fe159de0
title: 'ID3DX10Mesh：:D rawSubsetInstanced 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.DrawSubsetInstanced
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2e28d7a7d2c1d743090832d68793ec3743662308
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335632"
---
# <a name="id3dx10meshdrawsubsetinstanced-method"></a>ID3DX10Mesh：:D rawSubsetInstanced 方法

繪製相同網格子集的數個實例。

## <a name="syntax"></a>語法


```C++
HRESULT DrawSubsetInstanced(
  [in] UINT AttribId,
  [in] UINT InstanceCount,
  [in] UINT StartInstanceLocation
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*AttribId* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

指定要繪製的網格子集。 此值可用來區分網格中的臉部，以屬於一或多個屬性群組。 請參閱＜備註＞。

</dd> <dt>

*InstanceCount* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要呈現的實例數目。

</dd> <dt>

*StartInstanceLocation* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要在每個標記為實例資料的緩衝區中開始提取的實例。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="remarks"></a>備註

網格包含屬性工作表。 屬性資料表可將網格分割成子集，其中每個子集都以屬性識別碼來識別。 例如，具有200臉部的網格（分成三個子集）可能會有如下所示的屬性工作表：



| Subset     | 笑臉           |
|------------|-----------------|
| AttribID 0 | 臉部 0 ~ 50    |
| AttribID 1 | 臉部 51 ~ 125  |
| AttribID 2 | 臉部 126 ~ 200 |



 

實例可能會藉由重複使用相同幾何來在場景中繪製多個物件，來擴充效能。 實例的其中一個範例，就是使用不同的位置和色彩繪製相同的物件。 索引編制需要多個頂點緩衝區：每個頂點的資料至少有一個，以及針對每個實例資料使用第二個緩衝區。

使用 DrawSubsetInstanced 的繪圖實例非常類似于 [實例範例](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)中所述的 [**ID3D10Device：:D rawindexedinstanced**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-drawindexedinstanced)所使用的進程。 使用 DrawSubsetInstanced 時的主要差異在於，您必須先從 [**ID3DX10Mesh 介面**](id3dx10mesh.md) 物件解壓縮頂點和索引緩衝區，然後才能合併實例資料。

下列程式碼說明如何從網格物件中解壓縮頂點和索引緩衝區。


```
      ID3D10Buffer* vertexBuffer;
      pDeviceObj->pMesh->GetDeviceVertexBuffer(0, &vertexBuffer);
      ID3D10Buffer* indexBuffer;
      pDeviceObj->pMesh->GetDeviceIndexBuffer(&indexBuffer);
      
```



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

 

 
