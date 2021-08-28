---
description: 應用程式會使用 ID3DXBaseMesh 介面的方法來操作和查詢網格和漸進式網格物件。
ms.assetid: ec4ccd77-e370-470c-9325-3d794a8f7f16
title: 'ID3DXBaseMesh 介面 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b6f437ac6a67f684bd114ebba6aab1fcf8d828c680de88c338ab10ff39672e5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121740"
---
# <a name="id3dxbasemesh-interface"></a>ID3DXBaseMesh 介面

應用程式會使用 **ID3DXBaseMesh** 介面的方法來操作和查詢網格和漸進式網格物件。

## <a name="members"></a>成員

**ID3DXBaseMesh** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DXBaseMesh** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXBaseMesh** 介面具有這些方法。



| 方法                                                                            | 描述                                                                                                                                                                                                           |
|:----------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CloneMesh**](id3dxbasemesh--clonemesh.md)                                     | 使用宣告子複製網格。<br/>                                                                                                                                                                          |
| [**CloneMeshFVF**](id3dxbasemesh--clonemeshfvf.md)                               | 使用彈性頂點格式來複製網格 (FVF) 程式碼。<br/>                                                                                                                                                   |
| [**ConvertAdjacencyToPointReps**](id3dxbasemesh--convertadjacencytopointreps.md) | 將網格相鄰資訊轉換成點代表的陣列。<br/>                                                                                                                                  |
| [**ConvertPointRepsToAdjacency**](id3dxbasemesh--convertpointrepstoadjacency.md) | 將點代表資料轉換為網格相鄰資訊。<br/>                                                                                                                                          |
| [**DrawSubset**](id3dxbasemesh--drawsubset.md)                                   | 繪製網格的子集。<br/>                                                                                                                                                                                  |
| [**GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)                     | 產生網格邊緣清單以及共用每個邊緣的臉部清單。<br/>                                                                                                                            |
| [**GetAttributeTable**](id3dxbasemesh--getattributetable.md)                     | 抓取網格的屬性工作表，或網格的屬性資料表中儲存的專案數。<br/>                                                                                          |
| [**GetDeclaration**](id3dxbasemesh--getdeclaration.md)                           | 捕獲描述網格中頂點的宣告。<br/>                                                                                                                                               |
| [**GetDevice**](id3dxbasemesh--getdevice.md)                                     | 捕獲與網格相關聯的裝置。<br/>                                                                                                                                                             |
| [**GetFVF**](id3dxbasemesh--getfvf.md)                                           | 取得固定的函式頂點值。<br/>                                                                                                                                                                      |
| [**GetIndexBuffer**](id3dxbasemesh--getindexbuffer.md)                           | 抓取索引緩衝區中的資料。<br/>                                                                                                                                                                     |
| [**GetNumBytesPerVertex**](id3dxbasemesh--getnumbytespervertex.md)               | 取得每個頂點的位元組數目。<br/>                                                                                                                                                                       |
| [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)                                 | 抓取網格中的臉部數目。<br/>                                                                                                                                                                 |
| [**GetNumVertices**](id3dxbasemesh--getnumvertices.md)                           | 抓取網格中的頂點數目。<br/>                                                                                                                                                              |
| [**GetOptions**](id3dxbasemesh--getoptions.md)                                   | 抓取在建立時為此網格啟用的網格選項。<br/>                                                                                                                                         |
| [**GetVertexBuffer**](id3dxbasemesh--getvertexbuffer.md)                         | 抓取與網格相關聯的頂點緩衝區。<br/>                                                                                                                                                      |
| [**LockIndexBuffer**](id3dxbasemesh--lockindexbuffer.md)                         | 鎖定索引緩衝區，並取得索引緩衝區記憶體的指標。<br/>                                                                                                                                    |
| [**LockVertexBuffer**](id3dxbasemesh--lockvertexbuffer.md)                       | 鎖定頂點緩衝區，並取得頂點緩衝區記憶體的指標。<br/>                                                                                                                                   |
| [**UnlockIndexBuffer**](id3dxbasemesh--unlockindexbuffer.md)                     | 解除鎖定索引緩衝區。<br/>                                                                                                                                                                                   |
| [**UnlockVertexBuffer**](id3dxbasemesh--unlockvertexbuffer.md)                   | 解除鎖定頂點緩衝區。<br/>                                                                                                                                                                                   |
| [**UpdateSemantics**](id3dxbasemesh--updatesemantics.md)                         | 這種方法可讓使用者變更網格宣告，而不需要變更頂點緩衝區的資料版面配置。 只有當舊的和新的宣告格式具有相同的頂點大小時，呼叫才會有效。<br/> |



 

## <a name="remarks"></a>備註

網格是由一組多邊形臉部所組成的物件。 網格會定義一組頂點和一組臉部 (臉部是根據網格) 的頂點和法線來定義。

LPD3DXBASEMESH 型別定義為 **ID3DXBaseMesh** 介面的指標。


```
typedef struct ID3DXBaseMesh *LPD3DXBASEMESH;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 介面](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
