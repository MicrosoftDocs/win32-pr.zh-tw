---
description: 設定錯誤記錄檔
ms.assetid: 2e3124e3-32d0-4eb6-9c1d-91b625018ac4
title: 設定錯誤記錄檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac96fb90570408ca41be06656f7cf1704e9f48dc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106991582"
---
# <a name="setting-the-error-log"></a><span data-ttu-id="0a508-103">設定錯誤記錄檔</span><span class="sxs-lookup"><span data-stu-id="0a508-103">Setting the Error Log</span></span>

<span data-ttu-id="0a508-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="0a508-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="0a508-105">在您執行錯誤記錄類別之後，請建立類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="0a508-105">After you implement the error logging class, create a new instance of the class.</span></span> <span data-ttu-id="0a508-106">然後，藉由在時間軸上呼叫 [**IAMSetErrorLog：:p \_ 錯誤**](iamseterrorlog-put-errorlog.md)記錄檔方法，為 [DirectShow 編輯服務](directshow-editing-services.md)提供指標。</span><span class="sxs-lookup"><span data-stu-id="0a508-106">Then, give [DirectShow Editing Services](directshow-editing-services.md) a pointer to it by calling the [**IAMSetErrorLog::put\_ErrorLog**](iamseterrorlog-put-errorlog.md) method on the timeline.</span></span> <span data-ttu-id="0a508-107">查詢 **IAMSetErrorLog** 介面的時間軸。</span><span class="sxs-lookup"><span data-stu-id="0a508-107">Query the timeline for the **IAMSetErrorLog** interface.</span></span> <span data-ttu-id="0a508-108">為確保記錄所有錯誤，您應該先呼叫這個方法，然後再載入、儲存或轉譯時間軸。</span><span class="sxs-lookup"><span data-stu-id="0a508-108">To ensure that all errors are logged, you should call this method before you load, save, or render the timeline.</span></span>


```C++
IAMSetErrorLog  *pSetLog = NULL;
IAMErrorLog     *pLog = new CErrReporter();

pTL->QueryInterface(IID_IAMSetErrorLog, (void **)&pSetLog);
pSetLog->put_ErrorLog(pLog);
pSetLog->Release();
```



<span data-ttu-id="0a508-109">當您在應用程式中呼叫方法時，錯誤記錄不會影響您所收到的傳回值。</span><span class="sxs-lookup"><span data-stu-id="0a508-109">Error logging has no effect on the return values that you receive when you call methods in your application.</span></span> <span data-ttu-id="0a508-110">錯誤記錄會補充，但不會取代一般的錯誤處理技巧。</span><span class="sxs-lookup"><span data-stu-id="0a508-110">Error logging complements but does not replace the usual error handling techniques.</span></span> <span data-ttu-id="0a508-111">若要建立健全的應用程式，請一律檢查 HRESULT 值。</span><span class="sxs-lookup"><span data-stu-id="0a508-111">To create a robust application, always check HRESULT values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a508-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="0a508-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a508-113">記錄錯誤</span><span class="sxs-lookup"><span data-stu-id="0a508-113">Logging Errors</span></span>](logging-errors.md)
</dt> </dl>

 

 



