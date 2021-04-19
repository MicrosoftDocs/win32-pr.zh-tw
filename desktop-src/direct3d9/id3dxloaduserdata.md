---
description: 此介面是由應用程式所執行，用以儲存任何其他內嵌在. x 檔案中的使用者資料。
ms.assetid: 0d656f99-c24c-4326-bc6f-c0e7874c0fb2
title: 'ID3DXLoadUserData 介面 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fcb07ba9351e5f6c23dd86c8147151932b3972ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999969"
---
# <a name="id3dxloaduserdata-interface"></a>ID3DXLoadUserData 介面

此介面是由應用程式所執行，用以儲存任何其他內嵌在. x 檔案中的使用者資料。 這個介面的實例會傳遞至 [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md)，而 D3DX 會在每次遇到適當的資料時，在此介面上呼叫適當的方法。 例如，針對. x 檔案中的每個框架物件，會呼叫 [**ID3DXLoadUserData：： LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) ，並傳遞子資料。

## <a name="members"></a>成員

**ID3DXLoadUserData** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DXLoadUserData** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXLoadUserData** 介面具有這些方法。



| 方法                                                              | 描述                                      |
|:--------------------------------------------------------------------|:-------------------------------------------------|
| [**LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) | 從. x 檔案載入框架子資料。<br/> |
| [**LoadMeshChildData**](id3dxloaduserdata--loadmeshchilddata.md)   | 從. x 檔案載入網格子資料。<br/>  |
| [**LoadTopLevelData**](id3dxloaduserdata--loadtopleveldata.md)     | 從. x 檔案載入最上層資料。<br/>   |



 

## <a name="remarks"></a>備註

LPD3DXLOADUSERDATA 型別定義為這個介面的指標。


```
typedef interface ID3DXLoadUserData ID3DXLoadUserData;
typedef interface ID3DXLoadUserData *LPD3DXLOADUSERDATA;
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

 

 
