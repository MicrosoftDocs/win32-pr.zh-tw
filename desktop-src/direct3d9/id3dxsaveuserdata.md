---
description: 此介面是由應用程式所執行，用以儲存任何其他內嵌在. x 檔案中的使用者資料。
ms.assetid: 6294f942-9c14-4eed-92a8-af2821fd7e13
title: 'ID3DXSaveUserData 介面 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 77529a5a7b260dd27dc4af1752c88f55117bc974
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976701"
---
# <a name="id3dxsaveuserdata-interface"></a>ID3DXSaveUserData 介面

此介面是由應用程式所執行，用以儲存任何其他內嵌在. x 檔案中的使用者資料。 這個介面的實例會傳遞至 [**D3DXSaveMeshHierarchyToFile**](d3dxsavemeshhierarchytofile.md)，而 D3DX 會在每次遇到適當的資料時，在此介面上呼叫適當的方法。 例如，針對. x 檔案中的每個框架物件，會呼叫 [**ID3DXSaveUserData：： AddFrameChildData**](id3dxsaveuserdata--addframechilddata.md) ，並傳遞子資料。

## <a name="members"></a>成員

**ID3DXSaveUserData** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DXSaveUserData** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXSaveUserData** 介面具有這些方法。



| 方法                                                                              | 描述                                                        |
|:------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [**AddFrameChildData**](id3dxsaveuserdata--addframechilddata.md)                   | 將子資料新增至框架。<br/>                            |
| [**AddMeshChildData**](id3dxsaveuserdata--addmeshchilddata.md)                     | 將子資料新增至網格。<br/>                             |
| [**AddTopLevelDataObjectsPost**](id3dxsaveuserdata--addtopleveldataobjectspost.md) | 在框架階層之後加入最上層物件。<br/>       |
| [**AddTopLevelDataObjectsPre**](id3dxsaveuserdata--addtopleveldataobjectspre.md)   | 在框架階層之前加入最上層物件。<br/>      |
| [**RegisterTemplates**](id3dxsaveuserdata--registertemplates.md)                   | 用來註冊. x 檔案範本的使用者回呼。<br/> |
| [**SaveTemplates**](id3dxsaveuserdata--savetemplates.md)                           | 使用者用來儲存. x 檔案範本的回呼。<br/>     |



 

## <a name="remarks"></a>備註

LPD3DXSAVEUSERDATA 型別定義為這個介面的指標。


```
typedef interface ID3DXSaveUserData ID3DXSaveUserData;
typedef interface ID3DXSaveUserData *LPD3DXSAVEUSERDATA;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 介面](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
