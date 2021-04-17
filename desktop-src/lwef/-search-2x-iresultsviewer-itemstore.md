---
title: 'IResultsViewer ItemStore 屬性 (WdsView .h) '
description: 這個屬性會設定或傳回用來篩選結果的存放區名稱。
ms.assetid: c2a60485-c8f7-4951-a75e-2e6f6dcc2e4f
keywords:
- ItemStore 屬性舊版 Windows 環境功能
- ItemStore 屬性舊版 Windows 環境功能，IResultsViewer 介面
- IResultsViewer 介面舊版 Windows 環境功能，ItemStore 屬性
topic_type:
- apiref
api_name:
- IResultsViewer.ItemStore
- IResultsViewer.get_ItemStore
- IResultsViewer.put_ItemStore
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99abd4ef7ee36a0c76efa391d98a9fdb1d75f34e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465168"
---
# <a name="iresultsvieweritemstore-property"></a>IResultsViewer：： ItemStore 屬性

> [!NOTE]
> Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。 在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。 

這個屬性會設定或傳回用來篩選結果的存放區名稱。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ItemStore(
  [in]          BSTR name
);

HRESULT get_ItemStore(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>屬性值

設定存放區的名稱。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP2） \[ 桌面應用程式\]<br/>                                 |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]<br/>                        |
| 可轉散發套件<br/>          | Windows 桌面搜尋 (WDS) 2.6。5<br/>                                        |
| 標頭<br/>                   | <dl> <dt>WdsView。h</dt> </dl> |



 

 





