---
title: 'IResultsViewer PreviewStyle 屬性 (WdsView .h) '
description: 控制預覽窗格的顯示模式。
ms.assetid: 750664ea-506a-4219-ade5-1c7f1ffbd0d7
keywords:
- PreviewStyle 屬性舊版 Windows 環境功能
- PreviewStyle 屬性舊版 Windows 環境功能，IResultsViewer 介面
- IResultsViewer 介面舊版 Windows 環境功能，PreviewStyle 屬性
topic_type:
- apiref
api_name:
- IResultsViewer.PreviewStyle
- IResultsViewer.get_PreviewStyle
- IResultsViewer.put_PreviewStyle
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b412c92ca82263481b83ce739d44f21c2d15d99e9e6e7c74502480e0d8fad1b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753780"
---
# <a name="iresultsviewerpreviewstyle-property"></a>IResultsViewer：:P reviewStyle 屬性

> [!NOTE]
> WindowsDesktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集的形式提供。 在更新版本中，請改用[Windows Search API](../search/-search-reference-entry-page.md) 。 

控制預覽窗格的顯示模式。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_PreviewStyle(
  [in]          PreviewDisplayStyle style
);

HRESULT get_PreviewStyle(
  [out, retval] PreviewDisplayStyle *style
);
```



## <a name="property-value"></a>屬性值

設定預覽窗格的目前樣式屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows只有 XP （含 SP2） \[ 桌面應用程式\]<br/>                                 |
| 最低支援的伺服器<br/> | Windows只有 Server 2003 （含 SP1） \[ 桌面應用程式\]<br/>                        |
| 可轉散發套件<br/>          | Windows (WDS 的桌面搜尋) 2.6。5<br/>                                        |
| 標頭<br/>                   | <dl> <dt>WdsView。h</dt> </dl> |



 

 





