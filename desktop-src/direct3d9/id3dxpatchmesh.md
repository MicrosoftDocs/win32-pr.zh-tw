---
description: 此介面會封裝修補程式網格功能。
ms.assetid: c70c0fe0-b695-4ad9-b0c6-7854cf8f7593
title: 'ID3DXPatchMesh 介面 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f1f13e6abe3a164e8027ddcb6bb33e9f0ca618fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323060"
---
# <a name="id3dxpatchmesh-interface"></a>ID3DXPatchMesh 介面

此介面會封裝修補程式網格功能。

## <a name="members"></a>成員

**ID3DXPatchMesh** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DXPatchMesh** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXPatchMesh** 介面具有這些方法。



| 方法                                                                           | 描述                                                                                     |
|:---------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**CloneMesh**](id3dxpatchmesh--clonemesh.md)                                   | 使用指定的頂點宣告來建立新的 patch 網狀。<br/>                      |
| [**GenerateAdjacency**](id3dxpatchmesh--generateadjacency.md)                   | 產生網格邊緣清單以及共用每個邊緣的修補程式。<br/>                  |
| [**GetControlVerticesPerPatch**](id3dxpatchmesh--getcontrolverticesperpatch.md) | 取得每個修補程式的控制頂點數目。<br/>                                       |
| [**GetDeclaration**](id3dxpatchmesh--getdeclaration.md)                         | 取得頂點宣告。<br/>                                                         |
| [**GetDevice**](id3dxpatchmesh--getdevice.md)                                   | 取得建立網格的裝置。<br/>                                               |
| [**GetDisplaceParam**](id3dxpatchmesh--getdisplaceparam.md)                     | 取得網狀幾何置換參數。<br/>                                          |
| [**GetIndexBuffer**](id3dxpatchmesh--getindexbuffer.md)                         | 取得網狀索引緩衝區。<br/>                                                          |
| [**GetNumPatches**](id3dxpatchmesh--getnumpatches.md)                           | 取得網格中的修補程式數目。<br/>                                              |
| [**GetNumVertices**](id3dxpatchmesh--getnumvertices.md)                         | 取得網格中的頂點數目。<br/>                                             |
| [**GetOptions**](id3dxpatchmesh--getoptions.md)                                 | 取得修補程式的類型。<br/>                                                              |
| [**GetPatchInfo**](id3dxpatchmesh--getpatchinfo.md)                             | 取得修補程式的屬性。<br/>                                                    |
| [**GetTessSize**](id3dxpatchmesh--gettesssize.md)                               | 取得鑲嵌層級的鑲嵌網格大小。<br/>                   |
| [**GetVertexBuffer**](id3dxpatchmesh--getvertexbuffer.md)                       | 取得網格頂點緩衝區。<br/>                                                         |
| [**LockAttributeBuffer**](id3dxpatchmesh--lockattributebuffer.md)               | 鎖定屬性緩衝區。<br/>                                                          |
| [**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md)                       | 鎖定索引緩衝區。<br/>                                                               |
| [**LockVertexBuffer**](id3dxpatchmesh--lockvertexbuffer.md)                     | 鎖定頂點緩衝區。<br/>                                                              |
| [**優化**](id3dxpatchmesh--optimize.md)                                     | 將修補程式網格優化以進行有效率的鑲嵌。<br/>                                 |
| [**SetDisplaceParam**](id3dxpatchmesh--setdisplaceparam.md)                     | 設定網狀幾何置換參數。<br/>                                          |
| [**Tessellate**](id3dxpatchmesh--tessellate.md)                                 | 根據鑲嵌式層級執行統一鑲嵌。<br/>                       |
| [**TessellateAdaptive**](id3dxpatchmesh--tessellateadaptive.md)                 | 根據以 z 為基礎的調適型鑲嵌準則，執行適應性鑲嵌。<br/> |
| [**UnlockAttributeBuffer**](id3dxpatchmesh--unlockattributebuffer.md)           | 解除鎖定屬性緩衝區。<br/>                                                         |
| [**UnlockIndexBuffer**](id3dxpatchmesh--unlockindexbuffer.md)                   | 解除鎖定索引緩衝區。<br/>                                                             |
| [**UnlockVertexBuffer**](id3dxpatchmesh--unlockvertexbuffer.md)                 | 解除鎖定頂點緩衝區。<br/>                                                            |



 

## <a name="remarks"></a>備註

Patch 網格是由一連串修補程式所組成的網格。

若要取得 **ID3DXPatchMesh** 介面，請呼叫 [**D3DXCreatePatchMesh**](d3dxcreatepatchmesh.md) 函數。

LPD3DXPATCHMESH 型別定義為 **ID3DXPatchMesh** 介面的指標，如下所示：


```
typedef struct ID3DXPatchMesh *LPD3DXPATCHMESH;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 介面](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[網格函數](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
