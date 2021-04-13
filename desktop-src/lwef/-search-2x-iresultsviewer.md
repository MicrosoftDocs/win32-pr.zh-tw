---
title: 'IResultsViewer 介面 (WdsSharedIDL .h) '
description: 公開結果檢視的方法和屬性。
ms.assetid: 4d476511-d65c-4417-8073-337cfbae621d
keywords:
- IResultsViewer 介面舊版 Windows 環境功能
- IResultsViewer 介面舊版 Windows 環境功能，說明
topic_type:
- apiref
api_name:
- IResultsViewer
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18702812394f6e7fedd626062aa8c0116cab8427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508807"
---
# <a name="iresultsviewer-interface"></a>IResultsViewer 介面

> [!NOTE]
> Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。 在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。 

公開結果檢視的方法和屬性。

## <a name="members"></a>成員

**IResultsViewer** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IResultsViewer** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IResultsViewer** 介面具有這些方法。



| 方法                                                   | 描述                                                                            |
|:---------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**GoBack**](-search-2x-iresultsviewer-goback.md)       | 未實作。<br/>                                                            |
| [**GoForward**](-search-2x-iresultsviewer-goforward.md) | 未實作。<br/>                                                            |
| [**重新整理**](-search-2x-iresultsviewer-refresh.md)     | 未實作。<br/>                                                            |
| [**停止**](-search-2x-iresultsviewer-stop.md)           | 未實作。<br/>                                                            |
| [**更新**](-search-2x-iresultsviewer-update.md)       | 套用任何查詢變更，並將視圖導覽至新的結果集。<br/> |



 

### <a name="properties"></a>屬性

**IResultsViewer** 介面具有這些屬性。



| 屬性                                                                            | 存取類型           | Description                                                                                      |
|:------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [**目錄**](-search-2x-iresultsviewer-contents.md)<br/>                   | 唯寫<br/> | 這個屬性會追蹤顯示在結果檢視中的內容類型。 <br/>    |
| [**DisplayName**](-search-2x-iresultsviewer-displayname.md)<br/>             | 唯讀<br/>  | 類型的當地語系化顯示名稱。<br/>                                                   |
| [**EnumSelectedItems**](-search-2x-iresultsviewer-enumselecteditems.md)<br/> | 唯寫<br/> | 未實作。<br/>                                                                      |
| [**FilterType**](-search-2x-iresultsviewer-filtertype.md)<br/>               | 讀取/寫入<br/> | 這個屬性會設定或傳回用來篩選結果的 preceived 類型名稱。<br/> |
| [**HeaderStyle**](-search-2x-iresultsviewer-headerstyle.md)<br/>             | 讀取/寫入<br/> | 顯示在視圖中的標頭樣式。<br/>                                            |
| [**IsUpdateNeeded**](-search-2x-iresultsviewer-isupdateneeded.md)<br/>       | 唯寫<br/> | 如果 views 查詢已修改且需要更新，則會傳回 TRUE。 <br/>           |
| [**ItemStore**](-search-2x-iresultsviewer-itemstore.md)<br/>                 | 讀取/寫入<br/> | 這個屬性會設定或傳回用來篩選結果的存放區名稱。<br/>          |
| [**PreviewStyle**](-search-2x-iresultsviewer-previewstyle.md)<br/>           | 讀取/寫入<br/> | 控制預覽窗格的顯示模式。<br/>                                             |
| [**PropertyFilters**](-search-2x-iresultsviewer-propertyfilters.md)<br/>     | 唯寫<br/> | 呼叫屬性篩選集合時，會傳回下列內容：<br/>             |
| [**QueryText**](-search-2x-iresultsviewer-querytext.md)<br/>                 | 讀取/寫入<br/> | 取得或設定目前的查詢文字。<br/>                                                  |
| [**ResultsStyle**](-search-2x-iresultsviewer-resultsstyle.md)<br/>           | 唯寫<br/> | 未實作。<br/>                                                                      |
| [**SortOrderProperty**](-search-2x-iresultsviewer-sortorderproperty.md)<br/> | 讀取/寫入<br/> | 這個屬性會設定或傳回排序結果所依據的資料行順序。 <br/>            |
| [**SortProperty**](-search-2x-iresultsviewer-sortproperty.md)<br/>           | 讀取/寫入<br/> | 這個屬性會設定或傳回用來排序結果的屬性（property）（IndexColumn）。 <br/> |



 

## <a name="remarks"></a>備註

這些方法和屬性會用來操作所查看的資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP2） \[ 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]<br/>                             |
| 可轉散發套件<br/>          | Windows 桌面搜尋 (WDS) 3。0<br/>                                               |
| 標頭<br/>                   | <dl> <dt>WdsSharedIDL。h</dt> </dl> |



 

