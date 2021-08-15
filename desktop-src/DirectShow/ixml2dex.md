---
description: IXml2Dex 介面會在可延伸標記語言 (XML)  (XML) 中，儲存並載入 DirectShow 編輯服務 (DES) 專案檔。 這個介面也提供讀取和寫入 DirectShow graph ( grf) 檔案的方法。
ms.assetid: a07b0cbe-1f1d-4ccd-a994-9bb1a49c78d8
title: 'IXml2Dex 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3bc12c2305a8b92110d4aa17522184e9a3c5ee83b60ccd5a989468fa0a8c6e7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952387"
---
# <a name="ixml2dex-interface"></a>IXml2Dex 介面

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`IXml2Dex`介面會在可延伸標記語言 (XML)  (XML) 中儲存和載入[DirectShow 編輯服務](directshow-editing-services.md) (DES) 專案檔。 這個介面也提供讀取和寫入 DirectShow graph ( grf) 檔案的方法。

## <a name="members"></a>成員

**IXml2Dex** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IXml2Dex** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IXml2Dex** 介面具有這些方法。



| 方法                                                      | 描述                                                                |
|:------------------------------------------------------------|:---------------------------------------------------------------------------|
| [**CopyXML**](ixml2dex-copyxml.md)                         | 未實作。<br/>                                                |
| [**CreateGraphFromFile**](ixml2dex-creategraphfromfile.md) | 未實作。<br/>                                                |
| [**刪除**](ixml2dex-delete.md)                           | 未實作。<br/>                                                |
| [**PasteXML**](ixml2dex-pastexml.md)                       | 未實作。<br/>                                                |
| [**PasteXMLFile**](ixml2dex-pastexmlfile.md)               | 未實作。<br/>                                                |
| [**ReadXML**](ixml2dex-readxml.md)                         | 未實作。<br/>                                                |
| [**ReadXMLFile**](ixml2dex-readxmlfile.md)                 | 載入 XML 專案檔。<br/>                                      |
| [**重設**](ixml2dex-reset.md)                             | 未實作。<br/>                                                |
| [**WriteGrfFile**](ixml2dex-writegrffile.md)               | 將篩選圖形寫入 grf 格式的檔案。<br/>                 |
| [**WriteXML**](ixml2dex-writexml.md)                       | 將時間軸轉譯為 XML 字串。<br/>                         |
| [**WriteXMLFile**](ixml2dex-writexmlfile.md)               | 將時間軸轉譯成 XML，並將 XML 資料寫入檔案。<br/> |
| [**WriteXMLPart**](ixml2dex-writexmlpart.md)               | 未實作。<br/>                                                |



 

## <a name="remarks"></a>備註

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載[Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | Internet Explorer 4.0 或更新版本<br/>                                               |
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



 

 
