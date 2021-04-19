---
description: IMM 包含執行緒識別檢查，可判斷呼叫執行緒是否為指定之輸入方法內容控制碼的建立者 (HIMC 類型) 或視窗控制碼 (HWND 類型) 。
ms.assetid: da55d6fe-a620-4ea7-9055-91bcd3233267
title: 開發 IME-Aware 多執行緒應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e5730fc72ef41a84e01655116f94fc274f60548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980634"
---
# <a name="developing-ime-aware-multiple-thread-applications"></a>開發 IME-Aware 多執行緒應用程式

IMM 包含執行緒識別檢查，可判斷呼叫執行緒是否為指定之輸入方法內容控制碼的建立者 (HIMC 類型) 或視窗控制碼 (HWND 類型) 。 如果執行緒不是控制碼的建立者，則呼叫的 IMM 函式會失敗，而且後續的 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 呼叫會傳回錯誤 \_ 不正確 \_ 存取權。

> [!Note]  
> 目前的 IMM 架構未提供可存取 IMM 控制碼的同步處理功能。

 

若要使用執行緒識別檢查，您的應用程式必須遵守下列指導方針：

-   執行緒不應存取另一個執行緒所建立的輸入內容。
-   執行緒不應將輸入內容與另一個執行緒所建立的視窗產生關聯，反之亦然。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用輸入方法管理員](using-input-method-manager.md)
</dt> </dl>

 

 
