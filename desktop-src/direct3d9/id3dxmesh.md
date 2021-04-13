---
description: 應用程式會使用 ID3DXMesh 介面的方法來操作網格物件。
ms.assetid: f571fe0b-3f0c-43c9-809c-d1e14f85b720
title: 'ID3DXMesh 介面 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9c2a677edba4bad5e908b6dd69aa21a467b2a245
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323263"
---
# <a name="id3dxmesh-interface"></a>ID3DXMesh 介面

應用程式會使用 ID3DXMesh 介面的方法來操作網格物件。

## <a name="members"></a>成員

**ID3DXMesh** 介面繼承自 [**ID3DXBaseMesh**](id3dxbasemesh.md)。 **ID3DXMesh** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXMesh** 介面具有這些方法。



| 方法                                                            | 描述                                                                                                                            |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**LockAttributeBuffer**](id3dxmesh--lockattributebuffer.md)     | 鎖定包含網格屬性資料的網狀緩衝區，並傳回其指標。<br/>                                   |
| [**優化**](id3dxmesh--optimize.md)                           | 產生具有重新排序臉部和頂點的新網格，以將繪製效能優化。<br/>                                     |
| [**OptimizeInplace**](id3dxmesh--optimizeinplace.md)             | 產生具有重新排序臉部和頂點的網格，以將繪製效能優化。 這個方法會重新排序現有的網格。<br/> |
| [**SetAttributeTable**](id3dxmesh--setattributetable.md)         | 設定網格的屬性工作表和儲存在資料表中的專案數目。<br/>                                          |
| [**UnlockAttributeBuffer**](id3dxmesh--unlockattributebuffer.md) | 解除鎖定屬性緩衝區。<br/>                                                                                                |



 

## <a name="remarks"></a>備註

若要取得 **ID3DXMesh** 介面，請呼叫 [**D3DXCreateMesh**](d3dxcreatemesh.md) 或 [**D3DXCreateMeshFVF**](d3dxcreatemeshfvf.md) 函數。

這個介面會從 [**ID3DXBaseMesh**](id3dxbasemesh.md) 介面繼承其他功能。

LPD3DXMESH 型別定義為 **ID3DXMesh** 介面的指標。


```
typedef struct ID3DXMesh *LPD3DXMESH;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ID3DXBaseMesh**](id3dxbasemesh.md)
</dt> <dt>

[D3DX 介面](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[網格函數](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




