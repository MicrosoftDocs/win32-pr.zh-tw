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
# <a name="developing-ime-aware-multiple-thread-applications"></a><span data-ttu-id="921d7-103">開發 IME-Aware 多執行緒應用程式</span><span class="sxs-lookup"><span data-stu-id="921d7-103">Developing IME-Aware Multiple-thread Applications</span></span>

<span data-ttu-id="921d7-104">IMM 包含執行緒識別檢查，可判斷呼叫執行緒是否為指定之輸入方法內容控制碼的建立者 (HIMC 類型) 或視窗控制碼 (HWND 類型) 。</span><span class="sxs-lookup"><span data-stu-id="921d7-104">The IMM includes thread identification checking that determines if a calling thread is the creator of a specified input method context handle (HIMC type) or window handle (HWND type).</span></span> <span data-ttu-id="921d7-105">如果執行緒不是控制碼的建立者，則呼叫的 IMM 函式會失敗，而且後續的 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 呼叫會傳回錯誤 \_ 不正確 \_ 存取權。</span><span class="sxs-lookup"><span data-stu-id="921d7-105">If the thread is not the creator of the handle, the called IMM function fails and a subsequent call to [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INVALID\_ACCESS.</span></span>

> [!Note]  
> <span data-ttu-id="921d7-106">目前的 IMM 架構未提供可存取 IMM 控制碼的同步處理功能。</span><span class="sxs-lookup"><span data-stu-id="921d7-106">The current IMM architecture does not provide a synchronization facility for access to IMM handles.</span></span>

 

<span data-ttu-id="921d7-107">若要使用執行緒識別檢查，您的應用程式必須遵守下列指導方針：</span><span class="sxs-lookup"><span data-stu-id="921d7-107">To use thread identification checking, your applications must adhere to the following guidelines:</span></span>

-   <span data-ttu-id="921d7-108">執行緒不應存取另一個執行緒所建立的輸入內容。</span><span class="sxs-lookup"><span data-stu-id="921d7-108">A thread should not access the input context created by another thread.</span></span>
-   <span data-ttu-id="921d7-109">執行緒不應將輸入內容與另一個執行緒所建立的視窗產生關聯，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="921d7-109">A thread should not associate an input context with a window created by another thread, and vice versa.</span></span>

## <a name="related-topics"></a><span data-ttu-id="921d7-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="921d7-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="921d7-111">使用輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="921d7-111">Using Input Method Manager</span></span>](using-input-method-manager.md)
</dt> </dl>

 

 
