---
title: IUniversalOrchestrator::WorkCompleted
description: 呼叫通用協調器以表示工作已完成
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 8d4a08e7f021811e59a182a8b726397476b78433
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/21/2021
ms.locfileid: "106974735"
---
# <a name="iuniversalorchestratorworkcompleted-method"></a><span data-ttu-id="632df-103">IUniversalOrchestrator：： WorkCompleted 方法</span><span class="sxs-lookup"><span data-stu-id="632df-103">IUniversalOrchestrator::WorkCompleted method</span></span>

> [!NOTE] 
> <span data-ttu-id="632df-104">此 API 屬於通用 Orchestrator API。</span><span class="sxs-lookup"><span data-stu-id="632df-104">This API belongs to the Universal Orchestrator API.</span></span>

<span data-ttu-id="632df-105">允許用戶端通知通用協調器，先前已排程的工作已完成，並停止回呼來執行工作，直到下一次成功的 ScheduleWork 呼叫為止。</span><span class="sxs-lookup"><span data-stu-id="632df-105">Allows clients to inform Universal Orchestrator that the previously scheduled work has been completed and stop callbacks to perform work until the next successful ScheduleWork call.</span></span>

## <a name="syntax"></a><span data-ttu-id="632df-106">語法</span><span class="sxs-lookup"><span data-stu-id="632df-106">Syntax</span></span>

```C++
HRESULT WorkCompleted(
  LPCWSTR callerIdentifier,
  BOOL    workCompleted);
```

## <a name="parameters"></a><span data-ttu-id="632df-107">參數</span><span class="sxs-lookup"><span data-stu-id="632df-107">Parameters</span></span>

`callerIdentifier`

<span data-ttu-id="632df-108">識別此特定用戶端所有呼叫的唯一字串。</span><span class="sxs-lookup"><span data-stu-id="632df-108">A unique string that identifies all calls from this specific client.</span></span>

`workCompleted`

<span data-ttu-id="632df-109">如果工作已順利完成，**則為 TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="632df-109">**TRUE** if the work successfully completed.</span></span> <span data-ttu-id="632df-110">否則，如果工作嘗試失敗，而且未來應該重試，則 **為 FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="632df-110">Otherwise, **FALSE** if the work attempt failed and should be retried in the future.</span></span> 

## <a name="return-value"></a><span data-ttu-id="632df-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="632df-111">Return value</span></span>
<span data-ttu-id="632df-112">如果這個方法成功，它會傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="632df-112">If this method succeeds, it returns **S_OK**.</span></span>  <span data-ttu-id="632df-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="632df-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="632df-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="632df-114">Requirements</span></span>

| <span data-ttu-id="632df-115">需求</span><span class="sxs-lookup"><span data-stu-id="632df-115">Requirement</span></span> | <span data-ttu-id="632df-116">版本</span><span class="sxs-lookup"><span data-stu-id="632df-116">Version</span></span> |
|---|---|
| <span data-ttu-id="632df-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="632df-117">Minimum supported client</span></span> | <span data-ttu-id="632df-118">Windows 10 1903</span><span class="sxs-lookup"><span data-stu-id="632df-118">Windows 10 1903</span></span> |
|   |   |



 

 



