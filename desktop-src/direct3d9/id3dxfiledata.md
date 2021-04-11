---
description: 應用程式會使用 ID3DXFileData 介面的方法來建立或存取資料物件的直屬階層。 範本限制會決定階層。
ms.assetid: ce291e2b-b926-4502-8bee-55fe6d6d3267
title: 'ID3DXFileData 介面 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1764787864c059e9c7417525a1a5ab5ff862f7d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196340"
---
# <a name="id3dxfiledata-interface"></a>ID3DXFileData 介面

應用程式會使用 ID3DXFileData 介面的方法來建立或存取資料物件的直屬階層。 範本限制會決定階層。

## <a name="members"></a>成員

**ID3DXFileData** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DXFileData** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXFileData** 介面具有這些方法。



| 方法                                            | 描述                                                                                                          |
|:--------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**System.windows.media.visualtreehelper.getchild**](id3dxfiledata--getchild.md)       | 抓取這個檔案資料物件中的子物件。<br/>                                                        |
| [**GetChildren**](id3dxfiledata--getchildren.md) | 捕獲此檔案資料物件中的子係數目。<br/>                                                |
| [**GetEnum**](id3dxfiledata--getenum.md)         | 抓取這個檔案資料物件中的列舉物件。<br/>                                                |
| [**GetId**](id3dxfiledata--getid.md)             | 抓取此檔案資料物件的 GUID。<br/>                                                              |
| [**GetName**](id3dxfiledata--getname.md)         | 抓取這個檔案資料物件的名稱。<br/>                                                              |
| [**GetType**](id3dxfiledata--gettype.md)         | 抓取此檔案資料物件中的範本識別碼。<br/>                                                       |
| [**IsReference**](id3dxfiledata--isreference.md) | 指出此檔案資料物件是否為指向另一個子資料物件的參考物件。<br/>   |
| [**鎖定**](id3dxfiledata--lock.md)               | 存取. x 檔案資料。<br/>                                                                                |
| [**Unlock**](id3dxfiledata--unlock.md)           | 結束 [**ID3DXFileData：： Lock**](id3dxfiledata--lock.md)所傳回之 *ppData* 指標的存留期。<br/> |



 

## <a name="remarks"></a>備註

範本所允許的資料類型稱為選擇性成員。 選用的成員並不是必要的，但物件可能會遺失重要資訊。 這些選用的成員會儲存為數據物件的子系。 子系可以是其他資料物件或較早資料物件的參考。

ID3DXFileData 介面的 GUID 是 IID \_ ID3DXFileData。

LPD3DXFILEDATA 型別定義為這個介面的指標。


```
typedef interface ID3DXFileData *LPD3DXFILEDATA;
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

 

 
