---
description: 應用程式會使用 ID3DX10Mesh 介面的方法來操作網格物件。
ms.assetid: 1734b8fd-e1a6-4aa4-96a0-8693019a9dac
title: 'ID3DX10Mesh 介面 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2506191db941eee0a046d52f64aaeeb0f642f11dd35e42d6b49c4b5f5f457d79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096648"
---
# <a name="id3dx10mesh-interface"></a>ID3DX10Mesh 介面

應用程式會使用 ID3DX10Mesh 介面的方法來操作網格物件。

## <a name="members"></a>成員

**ID3DX10Mesh** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DX10Mesh** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DX10Mesh** 介面具有這些方法。



| 方法                                                                                   | 描述                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CloneMesh**](id3dx10mesh-clonemesh.md)                                               | 建立新的網格，並將其填入先前載入之網格的資料。<br/>                                                                                                                                                                                                                                                |
| [**CommitToDevice**](id3dx10mesh-committodevice.md)                                     | 將對網格所做的任何變更認可到裝置，以便轉譯變更。 這應該在網格的資料改變之後，以及轉譯之前呼叫。 除非已對裝置認可網狀，否則無法轉譯。 請參閱＜備註＞。<br/>                                                                         |
| [**丟棄**](id3dx10mesh-discard.md)                                                   | 使用 [**ID3DX10Mesh：： CommitToDevice**](id3dx10mesh-committodevice.md)) ，從已認可至裝置 (的裝置移除網格資料。<br/>                                                                                                                                                                         |
| [**DrawSubset**](id3dx10mesh-drawsubset.md)                                             | 繪製網格的子集。<br/>                                                                                                                                                                                                                                                                                                 |
| [**DrawSubsetInstanced**](id3dx10mesh-drawsubsetinstanced.md)                           | 繪製相同網格子集的數個實例。<br/>                                                                                                                                                                                                                                                                      |
| [**GenerateAdjacencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md)       | 產生網格邊緣清單以及共用每個邊緣的臉部清單。<br/>                                                                                                                                                                                                                                           |
| [**GenerateAttributeBufferFromTable**](id3dx10mesh-generateattributebufferfromtable.md) | 從網格的屬性工作表中的資料產生屬性緩衝區。 屬性緩衝區是另一種將資料儲存在屬性工作表中的格式。 屬性緩衝區和屬性資料表都是網格中的內部資料結構。<br/>                                                                  |
| [**GenerateGSAdjacency**](id3dx10mesh-generategsadjacency.md)                           | 將相鄰資料新增至網格的索引緩衝區。 當網格要傳送至採用相鄰資料的幾何著色器時，網格的索引緩衝區必須包含相鄰資料。<br/>                                                                                                                       |
| [**GetAdjacencyBuffer**](id3dx10mesh-getadjacencybuffer.md)                             | 存取網格的相鄰緩衝區。<br/>                                                                                                                                                                                                                                                                                       |
| [**GetAttributeBuffer**](id3dx10mesh-getattributebuffer.md)                             | 存取網格的屬性緩衝區。<br/>                                                                                                                                                                                                                                                                                       |
| [**GetAttributeTable**](id3dx10mesh-getattributetable.md)                               | 抓取網格的屬性工作表，或網格的屬性資料表中儲存的專案數。<br/>                                                                                                                                                                                                         |
| [**GetDeviceIndexBuffer**](id3dx10mesh-getdeviceindexbuffer.md)                         | 在使用 [**ID3DX10Mesh：： CommitToDevice**](id3dx10mesh-committodevice.md)認可至裝置之後，存取網格的索引緩衝區。 這與 [**ID3DX10Mesh：： GetIndexBuffer**](id3dx10mesh-getindexbuffer.md)不同，它會在認可至裝置之前，傳回索引緩衝區。<br/>     |
| [**GetDeviceVertexBuffer**](id3dx10mesh-getdevicevertexbuffer.md)                       | 在使用 [**ID3DX10Mesh：： CommitToDevice**](id3dx10mesh-committodevice.md)認可至裝置之後，存取網格的頂點緩衝區。 這與 [**ID3DX10Mesh：： GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md)不同，它會在認可至裝置之前傳回頂點緩衝區。<br/> |
| [**GetFaceCount**](id3dx10mesh-getfacecount.md)                                         | 抓取網格中的臉部數目。<br/>                                                                                                                                                                                                                                                                                |
| [**GetFlags**](id3dx10mesh-getflags.md)                                                 | 存取網格的建立旗標。<br/>                                                                                                                                                                                                                                                                                         |
| [**GetIndexBuffer**](id3dx10mesh-getindexbuffer.md)                                     | 抓取索引緩衝區中的資料。<br/>                                                                                                                                                                                                                                                                                    |
| [**GetPointRepBuffer**](id3dx10mesh-getpointrepbuffer.md)                               | 取得網狀的點 rep 緩衝區。<br/>                                                                                                                                                                                                                                                                                          |
| [**GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md)                                   | 抓取與網格相關聯的頂點緩衝區。<br/>                                                                                                                                                                                                                                                                     |
| [**GetVertexBufferCount**](id3dx10mesh-getvertexbuffercount.md)                         | 取得網格中的頂點緩衝區數目。<br/>                                                                                                                                                                                                                                                                             |
| [**GetVertexCount**](id3dx10mesh-getvertexcount.md)                                     | 取得網格中的頂點數目。 網格可能包含多個頂點緩衝區 (也就是一個頂點緩衝區可能包含所有位置資料、另一個可能包含所有紋理座標資料等 ) ，不過每個頂點緩衝區都包含相同數目的元素。<br/>                                                   |
| [**GetVertexDescription**](id3dx10mesh-getvertexdescription.md)                         | 存取傳遞至 [**D3DX10CreateMesh**](d3d10-d3dx10createmesh.md)的頂點描述。 頂點描述描述網格頂點緩衝區的版面配置。<br/>                                                                                                                                                   |
| [**相交**](id3dx10mesh-intersect.md)                                               | 判斷光線是否與此網格交集。<br/>                                                                                                                                                                                                                                                                            |
| [**IntersectSubset**](id3dx10mesh-intersectsubset.md)                                   | 判斷光線是否與這個網格的子集相交。<br/>                                                                                                                                                                                                                                                                |
| [**最佳化**](id3dx10mesh-optimize.md)                                                 | 產生具有重新排序臉部和頂點的新網格，以將繪製效能優化。<br/>                                                                                                                                                                                                                                   |
| [**SetAdjacencyData**](id3dx10mesh-setadjacencydata.md)                                 | 設定網狀網格的相鄰資料。<br/>                                                                                                                                                                                                                                                                                            |
| [**SetAttributeData**](id3dx10mesh-setattributedata.md)                                 | 設定網狀的屬性資料。<br/>                                                                                                                                                                                                                                                                                            |
| [**SetAttributeTable**](id3dx10mesh-setattributetable.md)                               | 設定網格的屬性工作表和儲存在資料表中的專案數目。<br/>                                                                                                                                                                                                                                        |
| [**SetIndexData**](id3dx10mesh-setindexdata.md)                                         | 設定網格的索引資料。<br/>                                                                                                                                                                                                                                                                                                |
| [**SetPointRepData**](id3dx10mesh-setpointrepdata.md)                                   | 設定網格的點代表資料。<br/>                                                                                                                                                                                                                                                                                      |
| [**SetVertexData**](id3dx10mesh-setvertexdata.md)                                       | 將頂點資料設定為其中一個網格的頂點緩衝區。<br/>                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>備註

若要取得 ID3DX10Mesh 介面，請呼叫 [**D3DX10CreateMesh**](d3d10-d3dx10createmesh.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
