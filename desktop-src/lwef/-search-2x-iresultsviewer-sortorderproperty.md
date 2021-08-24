---
title: IResultsViewer SortOrderProperty 屬性 (WdsView.h)
description: 這個屬性會設定或傳回排序結果所依據的資料行順序。
ms.assetid: ea05f4df-4caf-404f-8890-a109ca88555c
keywords:
- SortOrderProperty 屬性舊版 Windows 環境功能
- SortOrderProperty 屬性舊版 Windows 環境功能，IResultsViewer 介面
- IResultsViewer 介面舊版 Windows 環境功能，SortOrderProperty 屬性
topic_type:
- apiref
api_name:
- IResultsViewer.SortOrderProperty
- IResultsViewer.get_SortOrderProperty
- IResultsViewer.put_SortOrderProperty
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01680ac46592887cf4f321b771ff0e46039c775c4e9e9d8ed1edbc893ab45977
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829168"
---
# <a name="iresultsviewersortorderproperty-property"></a>IResultsViewer：： SortOrderProperty 屬性

> [!NOTE]
> WindowsDesktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集的形式提供。 在更新版本中，請改用[Windows Search API](../search/-search-reference-entry-page.md) 。 

這個屬性會設定或傳回排序結果所依據的資料行順序。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_SortOrderProperty(
  [in]          ColumnSortOrder order
);

HRESULT get_SortOrderProperty(
  [out, retval] ColumnSortOrder *order
);
```



## <a name="property-value"></a>屬性值

設定 [**ColumnSortOrder**](/windows/win32/api/mmcobj/ne-mmcobj-_columnsortorder) 屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows只有 XP （含 SP2） \[ 桌面應用程式\]<br/>                                 |
| 最低支援的伺服器<br/> | Windows只有 Server 2003 （含 SP1） \[ 桌面應用程式\]<br/>                        |
| 可轉散發套件<br/>          | Windows (WDS 的桌面搜尋) 2.6。5<br/>                                        |
| 標頭<br/>                   | <dl> <dt>WdsView。h</dt> </dl> |



 

 





