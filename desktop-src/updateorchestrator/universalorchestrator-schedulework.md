---
title: IUniversalOrchestrator::ScheduleWork
description: 呼叫通用協調器來排程工作
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 456df8f975114f7bdf750a0449f3bd98efcc3b2e
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/21/2021
ms.locfileid: "107000500"
---
# <a name="iuniversalorchestratorschedulework-method"></a><span data-ttu-id="a4c0a-103">IUniversalOrchestrator：： ScheduleWork 方法</span><span class="sxs-lookup"><span data-stu-id="a4c0a-103">IUniversalOrchestrator::ScheduleWork method</span></span>

> [!NOTE] 
> <span data-ttu-id="a4c0a-104">此 API 屬於通用 Orchestrator API。</span><span class="sxs-lookup"><span data-stu-id="a4c0a-104">This API belongs to the Universal Orchestrator API.</span></span>

<span data-ttu-id="a4c0a-105">允許用戶端通知通用協調器，其工作已暫止，並提供可供通用協調器呼叫的二進位檔，以在稍後執行更新工作。</span><span class="sxs-lookup"><span data-stu-id="a4c0a-105">Allows clients to inform Universal Orchestrator that work is pending and provide a binary that will be called by Universal Orchestrator to perform the update work at a later time.</span></span>

<span data-ttu-id="a4c0a-106">回呼二進位檔必須使用有效的 Microsoft 憑證進行簽署，而且呼叫端必須從系統內容叫用 ScheduleWork 呼叫。</span><span class="sxs-lookup"><span data-stu-id="a4c0a-106">The callback binary must be signed with a valid Microsoft certificate, and the caller must be invoking the ScheduleWork call from SYSTEM context.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4c0a-107">語法</span><span class="sxs-lookup"><span data-stu-id="a4c0a-107">Syntax</span></span>

```C++
HRESULT ScheduleWork(
  LPCWSTR callerIdentifier,
  LPCWSTR cmdLine
  LPCWSTR startArg,
  LPCWSTR pauseArg);
```

## <a name="parameters"></a><span data-ttu-id="a4c0a-108">參數</span><span class="sxs-lookup"><span data-stu-id="a4c0a-108">Parameters</span></span>

`callerIdentifier`

<span data-ttu-id="a4c0a-109">識別此特定用戶端所有呼叫的唯一字串。</span><span class="sxs-lookup"><span data-stu-id="a4c0a-109">A unique string that identifies all calls from this specific client.</span></span>

`cmdLine`

<span data-ttu-id="a4c0a-110">將由通用協調器叫用來執行工作的回呼二進位檔的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="a4c0a-110">The full path to the callback binary that will be invoked by Universal Orchestrator to perform work.</span></span>

`startArg`

<span data-ttu-id="a4c0a-111">要求傳遞至回呼二進位檔的參數，以表示要求啟動。</span><span class="sxs-lookup"><span data-stu-id="a4c0a-111">Parameters to pass to the callback binary to indicate Start is requested.</span></span>

`pauseArg`

<span data-ttu-id="a4c0a-112">*(選擇性)* 要傳遞至回呼二進位檔以表示已要求暫停的參數。</span><span class="sxs-lookup"><span data-stu-id="a4c0a-112">*(optional)* Parameters to pass to the callback binary to indicate Pause is requested.</span></span>

## <a name="return-value"></a><span data-ttu-id="a4c0a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a4c0a-113">Return value</span></span>
<span data-ttu-id="a4c0a-114">如果這個方法成功，它會傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="a4c0a-114">If this method succeeds, it returns **S_OK**.</span></span>  <span data-ttu-id="a4c0a-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a4c0a-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4c0a-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4c0a-116">Requirements</span></span>

| <span data-ttu-id="a4c0a-117">需求</span><span class="sxs-lookup"><span data-stu-id="a4c0a-117">Requirement</span></span> | <span data-ttu-id="a4c0a-118">版本</span><span class="sxs-lookup"><span data-stu-id="a4c0a-118">Version</span></span> |
|---|---|
| <span data-ttu-id="a4c0a-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a4c0a-119">Minimum supported client</span></span> | <span data-ttu-id="a4c0a-120">Windows 10 1903</span><span class="sxs-lookup"><span data-stu-id="a4c0a-120">Windows 10 1903</span></span> |
|   |   |



 

 



