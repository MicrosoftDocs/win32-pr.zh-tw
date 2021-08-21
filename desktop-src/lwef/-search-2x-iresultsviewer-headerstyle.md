---
title: 'IResultsViewer HeaderStyle 屬性 (WdsView .h) '
description: 顯示在視圖中的標頭樣式。
ms.assetid: 092a2ff2-eb88-4347-a81c-6a8005971ca9
keywords:
- HeaderStyle 屬性舊版 Windows 環境功能
- HeaderStyle 屬性舊版 Windows 環境功能，IResultsViewer 介面
- IResultsViewer 介面舊版 Windows 環境功能，HeaderStyle 屬性
topic_type:
- apiref
api_name:
- IResultsViewer.HeaderStyle
- IResultsViewer.get_HeaderStyle
- IResultsViewer.put_HeaderStyle
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c7c60687c3d306c3f9c3fcbb551f2d746723c7223b1964d42386464729b4069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753889"
---
# <a name="iresultsviewerheaderstyle-property"></a>IResultsViewer：： HeaderStyle 屬性

> [!NOTE]
> WindowsDesktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集的形式提供。 在更新版本中，請改用[Windows Search API](../search/-search-reference-entry-page.md) 。 

顯示在視圖中的標頭樣式。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_HeaderStyle(
  [in]          HeaderDisplayStyle style
);

HRESULT get_HeaderStyle(
  [out, retval] HeaderDisplayStyle *style
);
```



## <a name="property-value"></a>屬性值

設定顯示的標頭樣式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows只有 XP （含 SP2） \[ 桌面應用程式\]<br/>                                 |
| 最低支援的伺服器<br/> | Windows只有 Server 2003 （含 SP1） \[ 桌面應用程式\]<br/>                        |
| 可轉散發套件<br/>          | Windows (WDS 的桌面搜尋) 2.6。5<br/>                                        |
| 標頭<br/>                   | <dl> <dt>WdsView。h</dt> </dl> |



 

 





