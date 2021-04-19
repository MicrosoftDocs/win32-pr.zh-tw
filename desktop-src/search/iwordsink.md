---
description: 處理斷詞在索引時間和查詢期間所識別的文字。
ms.assetid: 220FCAE5-D22D-45ED-9689-E78C0D8E0BB3
title: 'IWordSink 介面 (搜尋 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 2eab8eee4f7b07b0f712e68d7ad05b970506b00b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106984164"
---
# <a name="iwordsink-interface"></a>IWordSink 介面

處理斷詞在索引時間和查詢期間所識別的文字。

## <a name="members"></a>成員

**IWordSink** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IWordSink** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWordSink** 介面具有這些方法。



| 方法                                             | 描述                                                                                                                             |
|:---------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**EndAltPhrase**](iwordsink-endaltphrase.md)     | 以斷詞工具在索引時間產生的替代片語順序表示最後一個片語的結尾。<br/>  |
| [**PutAltWord**](iwordsink-putaltword.md)         | 在 **IWordSink** 物件中放置替代單字和其位置。<br/>                                                       |
| [**PutBreak**](iwordsink-putbreak.md)             | 將中斷點放在前面的單字後面。<br/>                                                                                       |
| [**PutWord**](iwordsink-putword.md)               | 在 **IWordSink** 物件中放置單字和其位置。<br/>                                                                    |
| [**StartAltPhrase**](iwordsink-startaltphrase.md) | 表示在索引時間于斷詞工具產生的替代片語序列中，片語之間的界限。<br/> |



 

## <a name="remarks"></a>備註

Windows Search 會建立並初始化 **IWordSink** 物件的實例。 **IWordSink** 物件會在初始化期間接收 *fQuery* 參數，並使用此參數來決定使用物件的斷詞內容。

[**IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker)執行會在 [**IWordBreaker：： BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)方法中收到 **IWordSink** 物件的指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>搜尋。h</dt> </dl> |



 

 
