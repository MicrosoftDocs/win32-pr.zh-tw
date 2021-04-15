---
description: COM + CRM 中的錯誤處理
ms.assetid: 9de31fb5-31e9-494a-b61f-87bcff0d5085
title: COM + CRM 中的錯誤處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aba2b5c4541485433a85fe01fee7870c2e43f62
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468312"
---
# <a name="error-handling-in-the-com-crm"></a><span data-ttu-id="63a10-103">COM + CRM 中的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="63a10-103">Error Handling in the COM+ CRM</span></span>

<span data-ttu-id="63a10-104">COM + 伺服器應用程式會執行 failfast 原則。</span><span class="sxs-lookup"><span data-stu-id="63a10-104">COM+ server applications implement a failfast policy.</span></span> <span data-ttu-id="63a10-105">如果偵測到嚴重的內部錯誤，伺服器應用程式進程會結束，並將錯誤訊息寫入 Windows 事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="63a10-105">If a serious internal error is detected, the server application process exits and writes an error message to the Windows event log.</span></span> <span data-ttu-id="63a10-106">這可讓您快速偵測問題，而且可能是因為交易處理的應用程式資料受到保護。</span><span class="sxs-lookup"><span data-stu-id="63a10-106">This allows quick detection of problems and is possible due to the protection of application data by transaction processing.</span></span> <span data-ttu-id="63a10-107">請一律檢查 Windows 事件記錄檔中是否有任何來自 CRM 的錯誤，無論是在開發期間或在最終部署期間。</span><span class="sxs-lookup"><span data-stu-id="63a10-107">Always check the Windows event log for any errors from the CRM, either during development or during final deployment.</span></span>

<span data-ttu-id="63a10-108">使用 CRM 介面的基本錯誤，例如不正確引數或順序錯誤 (例如，嘗試在註冊 CRM 補償器) 之前寫入記錄檔記錄、傳回錯誤碼，且不應觸發 failfast。</span><span class="sxs-lookup"><span data-stu-id="63a10-108">Basic errors in using the CRM interfaces, such as invalid arguments or sequence errors (for example, trying to write a log record before registering the CRM Compensator), return error codes and should not trigger failfast.</span></span> <span data-ttu-id="63a10-109">針對 CRM 開發，您可以選擇設定 VTRACE1 登錄機碼 (請參閱 [Com + CRM 登錄設定](com--crm-registry-settings.md)) ，這會導致訊息出現在每個錯誤的偵錯工具輸出視窗中。</span><span class="sxs-lookup"><span data-stu-id="63a10-109">For CRM development, you may choose to set the VTRACE1 registry key (see [COM+ CRM Registry Settings](com--crm-registry-settings.md)), which causes a message to appear in the debugger output window for each error.</span></span>

<span data-ttu-id="63a10-110">也可能發生暫時性錯誤。</span><span class="sxs-lookup"><span data-stu-id="63a10-110">Transient errors can also occur.</span></span> <span data-ttu-id="63a10-111">這些錯誤通常是由計時條件所造成，而且會導致傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="63a10-111">These errors are typically caused by timing conditions and result in an error code being returned.</span></span> <span data-ttu-id="63a10-112">CRM 開發人員應該確保這些錯誤狀況都已處理。</span><span class="sxs-lookup"><span data-stu-id="63a10-112">The CRM developer should ensure that these error conditions are handled.</span></span> <span data-ttu-id="63a10-113">例如，寫入記錄檔記錄時，交易可能會因為超時而中止。方法接著會傳回錯誤，呼叫端應該檢查並適當地處理。</span><span class="sxs-lookup"><span data-stu-id="63a10-113">For example, while writing a log record, the transaction could abort due to a time-out. The method then returns an error, which the caller should check for and handle appropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="63a10-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="63a10-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63a10-115">COM + 補償 Resource Manager 概念</span><span class="sxs-lookup"><span data-stu-id="63a10-115">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



