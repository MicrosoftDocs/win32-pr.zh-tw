---
description: 下列函數用於結構化例外狀況處理。
ms.assetid: 61cf055b-eb9a-4e56-9d36-21fc95adea77
title: 結構化例外狀況處理函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70b431be2961a55bba28bdfe07723e93b95ac69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972334"
---
# <a name="structured-exception-handling-functions"></a>結構化例外狀況處理函式

下列函數用於結構化例外狀況處理。

-   [**AbnormalTermination**](abnormaltermination.md)

    指出終止處理常式的 **\_ \_ try** 區塊是否正常終止。

-   [**AddVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler)

    註冊向量 continue 處理常式。

-   [**AddVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler)

    註冊向量式例外狀況處理常式。

-   [**GetExceptionCode**](getexceptioncode.md)

    抓取可識別發生之例外狀況類型的程式碼。

-   [**GetExceptionInformation**](getexceptioninformation.md)

    抓取與電腦無關的例外狀況描述，以及發生例外狀況時，針對執行緒所存在之電腦狀態的相關資訊。

-   [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception)

    在呼叫執行緒中引發例外狀況。

-   [**RemoveVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler)

    取消註冊向量 continue 處理常式。

-   [**RemoveVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler)

    取消註冊向量例外狀況處理常式。

-   [**RtlAddGrowableFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtladdgrowablefunctiontable)

    通知系統有動態函式資料表，代表包含程式碼的記憶體區域。

-   [**RtlDeleteGrowableFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtldeletegrowablefunctiontable)

    通知系統，先前報告的動態函式資料表已不再使用中。

-   [**RtlGrowFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtlgrowfunctiontable)

    動態函式資料表大小已增加的報告。

-   [**SetUnhandledExceptionFilter**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setunhandledexceptionfilter)

    讓應用程式取代每個執行緒和進程的最上層例外狀況處理常式。

-   [**UnhandledExceptionFilter**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter)

    如果正在調試進程，則將未處理的例外狀況傳遞至偵錯工具。

-   [**VectoredHandler**](/windows/desktop/api/WinNT/nc-winnt-pvectored_exception_handler)

    應用程式定義的函數，做為向量例外狀況處理常式。

下列函式僅適用于64位 Windows。

-   [**RtlAddFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtladdfunctiontable)

    將動態函數資料表加入至動態函數資料表清單。

-   [**RtlCaptureCoNtext**](/windows/desktop/api/WinNT/nf-winnt-rtlcapturecontext)

    在呼叫端的內容中捕獲內容記錄。

-   [**RtlDeleteFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtldeletefunctiontable)

    從動態函數資料表清單中移除動態函式資料表。

-   [**RtlInstallFunctionTableCallback**](/windows/desktop/api/WinNT/nf-winnt-rtlinstallfunctiontablecallback)

    將動態函數資料表加入至動態函數資料表清單。

-   [**RtlRestoreCoNtext**](/windows/desktop/api/WinNT/nf-winnt-rtlrestorecontext)

    將呼叫端的內容還原至指定的內容記錄。

 

 
