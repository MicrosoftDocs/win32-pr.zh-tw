---
description: 網狀緩衝區是包含網格相關資料的緩衝區。
ms.assetid: a9fdfa22-531d-4da0-89f0-8766c2635e20
title: 'ID3DX10MeshBuffer 介面 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 42076393c3be5443688ec4db954131935b62f696
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991464"
---
# <a name="id3dx10meshbuffer-interface"></a>ID3DX10MeshBuffer 介面

網狀緩衝區是包含網格相關資料的緩衝區。 它可以包含五種不同類型的資料之一：頂點資料、索引資料、相鄰資料、屬性資料或點代表資料。 結構是用來透過下列五個 Api 來存取這五個數據片段： [**ID3DX10Mesh：： GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md)、 [**ID3DX10Mesh：： GetIndexBuffer**](id3dx10mesh-getindexbuffer.md)、 [**ID3DX10Mesh：： GetAdjacencyBuffer**](id3dx10mesh-getadjacencybuffer.md)、 [**ID3DX10Mesh：： GetAttributeBuffer**](id3dx10mesh-getattributebuffer.md)或 [**ID3DX10Mesh：： GetPointRepBuffer**](id3dx10mesh-getpointrepbuffer.md)。

## <a name="members"></a>成員

**ID3DX10MeshBuffer** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DX10MeshBuffer** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DX10MeshBuffer** 介面具有這些方法。



| 方法                                       | 描述                                                                |
|:---------------------------------------------|:---------------------------------------------------------------------------|
| [**GetSize**](id3dx10meshbuffer-getsize.md) | 取得網狀緩衝區的大小（以位元組為單位）。<br/>                      |
| [**對應**](id3dx10meshbuffer-map.md)         | 取得網狀緩衝區記憶體的指標，以修改其內容。<br/> |
| [**Unmap**](id3dx10meshbuffer-unmap.md)     | 取消對應緩衝區。<br/>                                                 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
