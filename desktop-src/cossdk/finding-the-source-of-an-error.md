---
description: 找出錯誤的來源
ms.assetid: d7287cf1-9501-4d37-b022-b56c8008220c
title: 找出錯誤的來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b505981f12a6f8b23adc22e92cfc7b7c4b77b7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025991"
---
# <a name="finding-the-source-of-an-error"></a><span data-ttu-id="0f1cc-103">找出錯誤的來源</span><span class="sxs-lookup"><span data-stu-id="0f1cc-103">Finding the Source of an Error</span></span>

<span data-ttu-id="0f1cc-104">您可以使用 COM + 和其他工具來診斷來源，並取得應用程式錯誤的描述。</span><span class="sxs-lookup"><span data-stu-id="0f1cc-104">You can diagnose the source and obtain a description of application errors by using COM+ and other tools.</span></span> <span data-ttu-id="0f1cc-105">如果您發現應用程式錯誤是由 COM + 所造成，您可以解讀 Winerror.h .h 檔案的錯誤訊息，或使用 Microsoft Visual C++ 錯誤公用程式。</span><span class="sxs-lookup"><span data-stu-id="0f1cc-105">If you discover that the application error is caused by COM+, you can interpret the error message viewing the Winerror.h file or by using the Microsoft Visual C++ error utility.</span></span>

<span data-ttu-id="0f1cc-106">如果您的伺服器應用程式失敗或造成非預期的行為，您必須先判斷發生錯誤的位置。</span><span class="sxs-lookup"><span data-stu-id="0f1cc-106">If your server application is failing or causing unexpected behavior, you must first determine where the error occurred.</span></span> <span data-ttu-id="0f1cc-107">系統事件檢視器會追蹤應用程式、安全性和系統事件。</span><span class="sxs-lookup"><span data-stu-id="0f1cc-107">The system Event Viewer tracks application, security, and system events.</span></span> <span data-ttu-id="0f1cc-108">這裡會記錄許多「無訊息」錯誤。</span><span class="sxs-lookup"><span data-stu-id="0f1cc-108">Many "silent" errors are recorded here.</span></span> <span data-ttu-id="0f1cc-109">不過，並非所有錯誤都會顯示在事件檢視器中。</span><span class="sxs-lookup"><span data-stu-id="0f1cc-109">However, not all errors are shown in the Event Viewer.</span></span>

<span data-ttu-id="0f1cc-110">您應該先參考事件檢視器中的應用程式記錄檔，檢查與事件訊息相關聯的應用程式。</span><span class="sxs-lookup"><span data-stu-id="0f1cc-110">You should first refer to the application log in the Event Viewer to check the application associated with the event message.</span></span> <span data-ttu-id="0f1cc-111"> (，因為您也可以封存事件記錄檔，所以您可以追蹤錯誤的事件歷程記錄。 ) 按兩下記錄檔中的專案，就會啟動 [ **事件** 內容] 頁面，以提供有關系統事件的進一步資訊。</span><span class="sxs-lookup"><span data-stu-id="0f1cc-111">(Because you can also archive event logs, you can track an event history of the error.) Double-clicking an entry in your log activates an **Event Properties** page, which provides further information about the system event.</span></span>

<span data-ttu-id="0f1cc-112">For more information on debugging a COM+ application, see [Debugging COM+ Applications](debugging-com--applications.md).</span><span class="sxs-lookup"><span data-stu-id="0f1cc-112">For more information on debugging a COM+ application, see [Debugging COM+ Applications](debugging-com--applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f1cc-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="0f1cc-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f1cc-114">錯誤隔離和 Failfast 原則</span><span class="sxs-lookup"><span data-stu-id="0f1cc-114">Fault Isolation and Failfast Policy</span></span>](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[<span data-ttu-id="0f1cc-115">COM + 如何修改傳回值</span><span class="sxs-lookup"><span data-stu-id="0f1cc-115">How COM+ Modifies Return Values</span></span>](how-com--modifies-return-values.md)
</dt> <dt>

[<span data-ttu-id="0f1cc-116">解讀錯誤碼</span><span class="sxs-lookup"><span data-stu-id="0f1cc-116">Interpreting Error Codes</span></span>](interpreting-error-codes.md)
</dt> <dt>

[<span data-ttu-id="0f1cc-117">在 COM + 中處理錯誤的策略</span><span class="sxs-lookup"><span data-stu-id="0f1cc-117">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[<span data-ttu-id="0f1cc-118">疑難排解</span><span class="sxs-lookup"><span data-stu-id="0f1cc-118">Troubleshooting</span></span>](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



