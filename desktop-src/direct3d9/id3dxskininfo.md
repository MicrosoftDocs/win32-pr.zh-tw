---
description: 應用程式會使用 ID3DXSkinInfo 介面的方法來操作骨骼矩陣，這些矩陣會用來為動畫的外觀頂點資料。 這個介面不再與 ID3DXMesh 緊密系結，而且可以用來對任何一組頂點資料進行外觀。
ms.assetid: 4ccf88b0-2cc7-4e91-a0f2-fb8eea66a3ce
title: 'ID3DXSkinInfo 介面 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0d7bfeddb5cb34bb9b5d0372f424c40248f06e55fa7263e1e884e71fb82dafcb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727758"
---
# <a name="id3dxskininfo-interface"></a>ID3DXSkinInfo 介面

應用程式會使用 ID3DXSkinInfo 介面的方法來操作骨骼矩陣，這些矩陣會用來為動畫的外觀頂點資料。 這個介面不再與 [**ID3DXMesh**](id3dxmesh.md) 緊密系結，而且可以用來對任何一組頂點資料進行外觀。

## <a name="members"></a>成員

**ID3DXSkinInfo** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DXSkinInfo** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXSkinInfo** 介面具有這些方法。



| 方法                                                                              | 描述                                                                                                                                                                                    |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**複製**](id3dxskininfo--clone.md)                                               | 複製面板資訊物件。<br/>                                                                                                                                                          |
| [**ConvertToBlendedMesh**](id3dxskininfo--converttoblendedmesh.md)                 | 使用網格，並傳回具有個別頂點 blend 加權和骨骼組合表的新網格。 此表描述哪些骨骼會影響網格的哪些子集。<br/>                   |
| [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md)   | 使用網格，並傳回具有個別頂點 blend 加權、索引和骨骼組合表的新網格。 表格描述哪些骨骼調色板會影響網格的哪些子集。<br/> |
| [**FindBoneVertexInfluenceIndex**](id3dxskininfo--findbonevertexinfluenceindex.md) | 捕獲影響單一頂點之骨骼影響的索引。<br/>                                                                                                                |
| [**GetBoneInfluence**](id3dxskininfo--getboneinfluence.md)                         | 取得骨骼影響的頂點和加權。<br/>                                                                                                                               |
| [**GetBoneName**](id3dxskininfo--getbonename.md)                                   | 從骨骼索引取得骨骼名稱。<br/>                                                                                                                                            |
| [**GetBoneOffsetMatrix**](id3dxskininfo--getboneoffsetmatrix.md)                   | 取得骨骼位移矩陣。<br/>                                                                                                                                                        |
| [**GetBoneVertexInfluence**](id3dxskininfo--getbonevertexinfluence.md)             | 抓取受指定之骨骼影響影響的 blend 因數和頂點。<br/>                                                                                                       |
| [**GetDeclaration**](id3dxskininfo--getdeclaration.md)                             | 取得頂點宣告。<br/>                                                                                                                                                        |
| [**GetFVF**](id3dxskininfo--getfvf.md)                                             | 取得固定的函式頂點值。<br/>                                                                                                                                               |
| [**GetMaxFaceInfluences**](id3dxskininfo--getmaxfaceinfluences.md)                 | 取得具有指定之索引緩衝區的三角形網格中最大臉部影響。<br/>                                                                                                |
| [**GetMaxVertexInfluences**](id3dxskininfo--getmaxvertexinfluences.md)             | 取得網格中任何頂點的最大影響數目。<br/>                                                                                                                   |
| [**GetMinBoneInfluence**](id3dxskininfo--getminboneinfluence.md)                   | 取得最小的骨骼影響。 影響小於此值的值會被忽略。<br/>                                                                                                    |
| [**GetNumBoneInfluences**](id3dxskininfo--getnumboneinfluences.md)                 | 取得骨骼的影響數目。<br/>                                                                                                                                           |
| [**GetNumBones**](id3dxskininfo--getnumbones.md)                                   | 取得骨骼數目。<br/>                                                                                                                                                           |
| [**重新**](id3dxskininfo--remap.md)                                               | 更新骨骼影響資訊，使其在重新排序之後符合頂點。 如果目標頂點緩衝區已從外部重新排序，則應該呼叫這個方法。<br/>              |
| [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md)                         | 設定骨骼的影響值。<br/>                                                                                                                                                |
| [**SetBoneName**](id3dxskininfo--setbonename.md)                                   | 設定骨骼名稱。<br/>                                                                                                                                                                 |
| [**SetBoneOffsetMatrix**](id3dxskininfo--setboneoffsetmatrix.md)                   | 設定骨骼位移矩陣。<br/>                                                                                                                                                        |
| [**SetBoneVertexInfluence**](id3dxskininfo--setbonevertexinfluence.md)             | 將骨骼的影響值設定在單一頂點上。<br/>                                                                                                                               |
| [**SetDeclaration**](id3dxskininfo--setdeclaration.md)                             | 設定頂點宣告。<br/>                                                                                                                                                        |
| [**SetFVF**](id3dxskininfo--setfvf.md)                                             | 設定 (FVF) 類型的彈性頂點格式。<br/>                                                                                                                                         |
| [**SetMinBoneInfluence**](id3dxskininfo--setminboneinfluence.md)                   | 設定最小的骨骼影響。 影響小於此值的值會被忽略。<br/>                                                                                                    |
| [**UpdateSkinnedMesh**](id3dxskininfo--updateskinnedmesh.md)                       | 根據目前的矩陣，將軟體外觀套用至目標頂點。<br/>                                                                                                     |



 

## <a name="remarks"></a>備註

使用 [**D3DXCreateSkinInfo**](d3dxcreateskininfo.md)、 [**D3DXCreateSkinInfoFromBlendedMesh**](d3dxcreateskininfofromblendedmesh.md)或 [**D3DXCreateSkinInfoFVF**](d3dxcreateskininfofvf.md)建立 **ID3DXSkinInfo** 介面。

LPD3DXSKININFO 型別定義為 **ID3DXSkinInfo** 介面的指標。


```
typedef struct ID3DXSkinInfo *LPD3DXSKININFO;
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

 

 
