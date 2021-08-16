---
title: 透過使用者介面傳達的訊息
description: 本主題列出目錄服務可從使用者介面傳送的訊息。
ms.assetid: c81a3c44-c01d-4029-8a7d-6e0911d4f5ab
ms.tgt_platform: multiple
keywords:
- 透過使用者介面傳達的訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b20b2706ae9f03109064c459ce494fb38da3f4579ca8f5b03ade970fcb0391f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186570"
---
# <a name="messages-communicated-through-user-interfaces"></a>透過使用者介面傳達的訊息

本主題列出目錄服務可從使用者介面傳送的訊息。

## <a name="common-query-page-messages"></a>一般查詢頁面訊息

下列訊息會傳送至 [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) 回呼函數中的目錄服務查詢表單延伸頁面：

-   [**CQPM \_ CLEARFORM**](cqpm-clearform.md)
-   [**CQPM \_ 啟用**](cqpm-enable.md)
-   [**CQPM \_ GETPARAMETERS**](cqpm-getparameters.md)
-   [**CQPM \_ HANDLERSPECIFIC**](cqpm-handlerspecific.md)
-   [**CQPM \_ 說明**](cqpm-help.md)
-   [**CQPM \_ INITIALIZE**](cqpm-initialize.md)
-   [**CQPM \_ 保存**](cqpm-persist.md)
-   [**CQPM \_ 版本**](cqpm-release.md)
-   [**CQPM \_ SETDEFAULTPARAMETERS**](cqpm-setdefaultparameters.md)

## <a name="miscellaneous-messages"></a>其他訊息

下表列出目錄服務可傳送的訊息。



| 訊息                  | 值                     | 描述                                                                                                                                                                                                                                   |
|--------------------------|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DSPROP \_ ATTRCHANGED \_ MSG | "DsPropAttrChanged"       | 針對同步處理屬性頁和目錄服務管理工具所傳送的訊息，在 Dsclient 中宣告。                                                                                                                       |
| DSQPM \_ GETCLASSLIST      | CQPM \_ HANDLERSPECIFIC + 0   | 傳送至表單頁面的頁面訊息，可供您用來取得查詢類別清單，供欄位選取器和屬性妥善建立，以建立其顯示類別清單。 wParam = flags 和 lParam = LPLPDSQUERYCLASSLIST，在 Dsquery. h 中宣告。 |
| DSQPM \_ HELPTOPICS        |  (CQPM \_ HANDLERSPECIFIC + 1)  | 傳送至表單頁面的頁面訊息，用來處理「說明主題」要求。 wParam = 0，lParam = hWndParent，在 Dsquery. h 中宣告。                                                                                                         |



 

 

 




