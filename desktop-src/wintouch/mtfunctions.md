---
title: '函數 (Windows Touch 輸入) '
description: 本節包含 Windows Touch 輸入的功能。
ms.assetid: 6c64ed75-37ac-47ae-b39e-bdf10d2b5211
keywords:
- Windows觸控功能，函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af2aae5f0e355a6fdb809b70c2d5fad629434b62c802f6ff0f5ad180facba82d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118435324"
---
# <a name="functions-windows-touch-input"></a>函數 (Windows Touch 輸入) 

本節包含 Windows Touch 輸入的功能。

下列函式用於 Windows Touch 輸入。



| 函式                                                                                               | 描述                                                                                                                             |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**CloseTouchInputHandle**](/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle)                                                 | 關閉觸控輸入控點、釋放與其相關聯的進程記憶體，並使控制碼失效。                                       |
| [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo)                                                         | 抓取與特定觸控輸入控點相關聯之觸控輸入的詳細資訊。                                        |
| [**IsTouchWindow**](/windows/desktop/api/winuser/nf-winuser-istouchwindow)                                                                 | 檢查指定的視窗是否具備觸控功能，並選擇性地抓取為視窗觸控功能設定的修飾詞旗標。 |
| [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)                                                     | 將視窗註冊為具備觸控功能。                                                                                              |
| [**UnregisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-unregistertouchwindow)                                                 | 註冊不再具備觸控功能的視窗。                                                                                    |
| [SendMessage、PostMessage 和相關函數](sendmessage--postmessage--and-related-functions.md) | 包含轉送訊息的考慮。                                                                                      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows觸控輸入](multi-touch-input.md)
</dt> <dt>

[Windows觸控輸入程式設計指南](guide-multi-touch-input.md)
</dt> </dl>

 

 




