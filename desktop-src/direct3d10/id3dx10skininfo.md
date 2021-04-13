---
description: ID3DX10SkinInfo 可讓您優化、處理及手動設定網格中的骨骼與頂點之間的關聯性 (請參閱維琪百科) 上的框架動畫。
ms.assetid: bea0fe71-c201-45c6-8036-d0d76d5851fd
title: 'ID3DX10SkinInfo 介面 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3216765ab9ef2ba9f2b0883c31a878a7eae6861f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322948"
---
# <a name="id3dx10skininfo-interface"></a>ID3DX10SkinInfo 介面

ID3DX10SkinInfo 可讓您優化、處理及手動設定網格中的骨骼與頂點之間的關聯性 (請參閱 [維琪百科) 上的框架動畫](https://en.wikipedia.org/wiki/Skeletal_animation) 。 它最適合用來製作 DCC Apps 所匯出的. x 檔案 (例如 3DS Max 和 Maya) 更容易使用硬體，以及改善 skinned 網格在軟體轉譯模式中的呈現速度。

## <a name="members"></a>成員

**ID3DX10SkinInfo** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DX10SkinInfo** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DX10SkinInfo** 介面具有這些方法。



| 方法                                                                   | 描述                                                                                                                        |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**AddBoneInfluences**](id3dx10skininfo-addboneinfluences.md)           | 啟用現有的骨骼來影響一組頂點，並定義骨骼對每個頂點的影響程度。<br/>     |
| [**AddBones**](id3dx10skininfo-addbones.md)                             | 配置更多骨骼的空間。<br/>                                                                                          |
| [**AddVertices**](id3dx10skininfo-addvertices.md)                       | 配置其他頂點的空間。<br/>                                                                                 |
| [**ClearBoneInfluences**](id3dx10skininfo-clearboneinfluences.md)       | 清除其所影響之骨骼的頂點清單。<br/>                                                                     |
| [**精簡**](id3dx10skininfo-compact.md)                               | 限制可能影響頂點的骨骼數目，以及/或限制骨骼在頂點上可以有的影響數量。<br/> |
| [**DoSoftwareSkinning**](id3dx10skininfo-dosoftwareskinning.md)         | 在頂點的陣列上進行軟體外觀。<br/>                                                                           |
| [**FindBoneInfluenceIndex**](id3dx10skininfo-findboneinfluenceindex.md) | 找出表示指定頂點在受影響頂點的指定清單中之位置的索引。<br/>                    |
| [**GetBoneInfluence**](id3dx10skininfo-getboneinfluence.md)             | 取得指定之骨骼對指定頂點的影響量。<br/>                                                       |
| [**GetBoneInfluenceCount**](id3dx10skininfo-getboneinfluencecount.md)   | 取得指定之骨骼影響的頂點數目。<br/>                                                                |
| [**GetBoneInfluences**](id3dx10skininfo-getboneinfluences.md)           | 取得指定之骨骼影響的頂點清單，以及骨骼對每個頂點的影響數量清單。<br/> |
| [**GetMaxBoneInfluences**](id3dx10skininfo-getmaxboneinfluences.md)     | 取得骨骼可充分影響的頂點數目。<br/>                                                              |
| [**GetNumBones**](id3dx10skininfo-getnumbones.md)                       | 取得 ID3DX10SkinInfo 中的骨骼數目。<br/>                                                                             |
| [**GetNumVertices**](id3dx10skininfo-getnumvertices.md)                 | 取得 ID3DX10SkinInfo 中的頂點數目。<br/>                                                                          |
| [**RemapBones**](id3dx10skininfo-remapbones.md)                         | 變更哪些骨骼會影響哪些頂點。<br/>                                                                            |
| [**RemapVertices**](id3dx10skininfo-remapvertices.md)                   | 變更哪些頂點受哪些骨骼影響。<br/>                                                                    |
| [**RemoveBone**](id3dx10skininfo-removebone.md)                         | 移除骨骼。<br/>                                                                                                          |
| [**SetBoneInfluence**](id3dx10skininfo-setboneinfluence.md)             | 設定指定之骨骼對指定頂點的影響量。<br/>                                                       |



 

## <a name="remarks"></a>備註

使用 [**D3DX10CreateSkinInfo**](d3d10-d3dx10createskininfo.md)、 **D3DX10CreateSkinInfoFromBlendedMesh** 或 **D3DX10CreateSkinInfoFVF** 建立 ID3DX10SkinInfo 介面。

LPD3DX10SKININFO 型別定義為 **ID3DX10SkinInfo** 介面的指標。


```
typedef struct ID3DX10SkinInfo *LPD3DX10SKININFO;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
