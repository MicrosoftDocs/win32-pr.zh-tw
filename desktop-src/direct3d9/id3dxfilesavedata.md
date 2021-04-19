---
description: 應用程式會使用 ID3DXFileSaveData 介面的方法，將資料物件新增為. x 檔案資料節點的子系。
ms.assetid: ab5bdd9a-496a-4ae1-b93a-fe5856bd97d4
title: 'ID3DXFileSaveData 介面 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d42f431dbb2f9108c5e503aea07ba6b11915f0ac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988589"
---
# <a name="id3dxfilesavedata-interface"></a>ID3DXFileSaveData 介面

應用程式會使用 ID3DXFileSaveData 介面的方法，將資料物件新增為. x 檔案資料節點的子系。

## <a name="members"></a>成員

**ID3DXFileSaveData** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DXFileSaveData** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXFileSaveData** 介面具有這些方法。



| 方法                                                          | 描述                                                                                                                                |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddDataObject**](id3dxfilesavedata--adddataobject.md)       | 將資料物件新增為 **ID3DXFileSaveData** 檔資料節點的子系。<br/>                                                      |
| [**AddDataReference**](id3dxfilesavedata--adddatareference.md) | 將資料參考加入為這個 **ID3DXFileSaveData** 檔資料節點的子系。 資料參考會指向檔案資料物件。<br/> |
| [**GetId**](id3dxfilesavedata--getid.md)                       | 抓取這個 **ID3DXFileSaveData** 檔資料節點的 GUID。<br/>                                                                |
| [**GetName**](id3dxfilesavedata--getname.md)                   | 抓取這個 **ID3DXFileSaveData** 檔資料節點的名稱。<br/>                                                                |
| [**GetSave**](id3dxfilesavedata--getsave.md)                   | 抓取這個 [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) 檔資料節點的指標。<br/>                                  |
| [**GetType**](id3dxfilesavedata--gettype.md)                   | 抓取此檔案資料節點的範本識別碼。<br/>                                                                               |



 

## <a name="remarks"></a>備註

ID3DXFileSaveObject 介面的 GUID 是 IID \_ ID3DXFileSaveObject。

LPD3DXFileSaveData 型別定義為這個介面的指標。


```
typedef interface ID3DXFileSaveData *LPD3DXFILESAVEDATA;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Xof。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX X 檔案介面](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
