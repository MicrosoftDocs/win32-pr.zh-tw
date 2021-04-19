---
title: IUniversalOrchestrator::HasMoratoriumPassed
description: 查詢通用協調器，以判斷是否已超過過了時間（OOBE）。
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 2ed354d365b795a0c959396e6b26d6bc73baad97
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/21/2021
ms.locfileid: "106974734"
---
# <a name="iuniversalorchestratorhasmoratoriumpassed-method"></a><span data-ttu-id="f1e41-103">IUniversalOrchestrator：： HasMoratoriumPassed 方法</span><span class="sxs-lookup"><span data-stu-id="f1e41-103">IUniversalOrchestrator::HasMoratoriumPassed method</span></span>

> [!NOTE] 
> <span data-ttu-id="f1e41-104">此 API 屬於通用 Orchestrator API。</span><span class="sxs-lookup"><span data-stu-id="f1e41-104">This API belongs to the Universal Orchestrator API.</span></span>

<span data-ttu-id="f1e41-105">可讓用戶端判斷通用協調器是否在新的裝置現成體驗之後立即運作，這會限制工作嘗試將使用者中斷降至最低。</span><span class="sxs-lookup"><span data-stu-id="f1e41-105">Allows clients to determine if Universal Orchestrator is operating immediately after the new device Out of Box Experience, which limits work attempts to minimize user interruption.</span></span> 

## <a name="syntax"></a><span data-ttu-id="f1e41-106">語法</span><span class="sxs-lookup"><span data-stu-id="f1e41-106">Syntax</span></span>

```C++
HRESULT HasMoratoriumPassed(
  LPCWSTR callerIdentifier,
  BOOL*   moratoriumPassed);
```

## <a name="parameters"></a><span data-ttu-id="f1e41-107">參數</span><span class="sxs-lookup"><span data-stu-id="f1e41-107">Parameters</span></span>

`callerIdentifier`

<span data-ttu-id="f1e41-108">識別此特定用戶端所有呼叫的唯一字串。</span><span class="sxs-lookup"><span data-stu-id="f1e41-108">A unique string that identifies all calls from this specific client.</span></span>

`hasMoratoriumPassed`

<span data-ttu-id="f1e41-109">輸出參數，可儲存查詢的結果。</span><span class="sxs-lookup"><span data-stu-id="f1e41-109">Output parameter that stores the result of the query.</span></span>

## <a name="return-value"></a><span data-ttu-id="f1e41-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="f1e41-110">Return value</span></span>
<span data-ttu-id="f1e41-111">如果這個方法成功，它會傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="f1e41-111">If this method succeeds, it returns **S_OK**.</span></span>  <span data-ttu-id="f1e41-112">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f1e41-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1e41-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1e41-113">Requirements</span></span>

| <span data-ttu-id="f1e41-114">需求</span><span class="sxs-lookup"><span data-stu-id="f1e41-114">Requirement</span></span> | <span data-ttu-id="f1e41-115">版本</span><span class="sxs-lookup"><span data-stu-id="f1e41-115">Version</span></span> |
|---|---|
| <span data-ttu-id="f1e41-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1e41-116">Minimum supported client</span></span> | <span data-ttu-id="f1e41-117">Windows 10 1903</span><span class="sxs-lookup"><span data-stu-id="f1e41-117">Windows 10 1903</span></span> |
|   |   |



 

 



