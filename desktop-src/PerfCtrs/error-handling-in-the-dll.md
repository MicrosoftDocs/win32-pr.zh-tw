---
description: 使用事件記錄來記錄效能 DLL 中發生的錯誤。
ms.assetid: 61bc4fa1-8185-4e07-a3b5-4bd357f0f75a
title: DLL 中的錯誤處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd21f0b9338600012d65aa19801ee57794fac294
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944260"
---
# <a name="error-handling-in-the-dll"></a><span data-ttu-id="9566f-103">DLL 中的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="9566f-103">Error Handling in the DLL</span></span>

<span data-ttu-id="9566f-104">使用事件記錄來記錄效能 DLL 中發生的錯誤。</span><span class="sxs-lookup"><span data-stu-id="9566f-104">Use event logging to record errors that occur in the performance DLL.</span></span> <span data-ttu-id="9566f-105">記錄錯誤事件有助於針對在開發期間和安裝之後提供效能資料的應用程式進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="9566f-105">Logging error events aids in troubleshooting applications that provide performance data during development and after installation.</span></span> <span data-ttu-id="9566f-106">您應該限制 [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) 函式中發生的錯誤記錄量，因為資料收集可能很頻繁。</span><span class="sxs-lookup"><span data-stu-id="9566f-106">You should limit the amount of error logging that occurs in the [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) function because data collection can be frequent.</span></span>

<span data-ttu-id="9566f-107">如果 [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) 函數發生問題，系統會將下列錯誤記錄到事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="9566f-107">The system logs the following errors to the event log if there are problems with the [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) function.</span></span> <span data-ttu-id="9566f-108">如果發生下列其中一個錯誤，系統就不會再次呼叫效能 DLL。</span><span class="sxs-lookup"><span data-stu-id="9566f-108">If one of the following errors occurs, the system does not call the performance DLL again.</span></span> <span data-ttu-id="9566f-109">相反地，DLL 已卸載。</span><span class="sxs-lookup"><span data-stu-id="9566f-109">Instead, the DLL is unloaded.</span></span>

-   <span data-ttu-id="9566f-110">**PERFLIB \_找 \_ \_ 不 \_ 到開啟** 的程式—當 DLL 中定義的程式名稱在 DLL 中找不到匯出的函式時，就會進行記錄。</span><span class="sxs-lookup"><span data-stu-id="9566f-110">**PERFLIB\_OPEN\_PROC\_NOT\_FOUND**—Logged when the procedure name defined in the registry could not be found in the DLL as an exported function.</span></span> <span data-ttu-id="9566f-111">當 DLL 或服務未正確安裝，或函式名稱已重新命名而未更新安裝程式時，通常就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="9566f-111">This usually occurs when the DLL or the service is not installed correctly or the function name has been renamed without updating the installation procedure.</span></span>
-   <span data-ttu-id="9566f-112">**PERFLIB \_開啟 \_ 程式 \_ 失敗**：當 OPEN 程式傳回錯誤狀態，而不是錯誤成功時所記錄 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9566f-112">**PERFLIB\_OPEN\_PROC\_FAILURE**—Logged when the open procedure returned an error status other than ERROR\_SUCCESS.</span></span> <span data-ttu-id="9566f-113">如果發生這種情況，DLL 應該也輸入一個事件記錄檔專案，以描述造成失敗的狀況。</span><span class="sxs-lookup"><span data-stu-id="9566f-113">Should this happen, the DLL should have also entered an event log entry describing the conditions that caused the failure.</span></span>
-   <span data-ttu-id="9566f-114">**PERFLIB \_OPEN \_ procedure \_ 例外** 狀況—在 open 程式遇到未處理的例外狀況時記錄。</span><span class="sxs-lookup"><span data-stu-id="9566f-114">**PERFLIB\_OPEN\_PROC\_EXCEPTION**—Logged when the open procedure encounters an unhandled exception.</span></span> <span data-ttu-id="9566f-115">這通常是因為 open 程式發生非預期的錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="9566f-115">This is usually due to an unexpected error condition encountered by the open procedure.</span></span>

 

 
