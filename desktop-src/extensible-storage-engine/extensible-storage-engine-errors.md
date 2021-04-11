---
description: 深入瞭解：可擴充儲存引擎錯誤
title: 可擴充儲存引擎錯誤
TOCTitle: Extensible Storage Engine Errors
ms:assetid: 0c071ed6-0ea2-448b-9f9f-e606c5abf3db
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269184(v=EXCHG.10)
ms:contentKeyID: 32765487
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 55c86d51f44414688897d6450adf214a0478f7d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852851"
---
# <a name="extensible-storage-engine-errors"></a><span data-ttu-id="0c019-103">可擴充儲存引擎錯誤</span><span class="sxs-lookup"><span data-stu-id="0c019-103">Extensible Storage Engine Errors</span></span>


<span data-ttu-id="0c019-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0c019-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="extensible-storage-engine-errors"></a><span data-ttu-id="0c019-105">可擴充儲存引擎錯誤</span><span class="sxs-lookup"><span data-stu-id="0c019-105">Extensible Storage Engine Errors</span></span>

<span data-ttu-id="0c019-106">可延伸儲存引擎所傳回的所有可能錯誤 (ESE) API 都是由 [JET_ERR](./jet-err.md) 資料類型所定義。</span><span class="sxs-lookup"><span data-stu-id="0c019-106">All possible errors returned by the Extensible Storage Engine (ESE) API are defined by the [JET_ERR](./jet-err.md) data type.</span></span> <span data-ttu-id="0c019-107">如需為此 API 定義的錯誤旗標清單，請參閱可延伸 [儲存引擎錯誤碼](./extensible-storage-engine-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="0c019-107">For a list of the error flags that are defined for this API, see [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).</span></span>

<span data-ttu-id="0c019-108">在整個 ESE API 檔中，只會記錄最重要的錯誤。</span><span class="sxs-lookup"><span data-stu-id="0c019-108">Throughout the ESE API documentation, only the most important errors are documented.</span></span> <span data-ttu-id="0c019-109">這些錯誤通常代表 API 使用錯誤或非常重要的錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="0c019-109">These errors typically represent API usage errors or very important error conditions.</span></span> <span data-ttu-id="0c019-110">請注意，這些 ESE Api 中的任何一項也可能會傳回未針對每個 API 記載的其他錯誤。</span><span class="sxs-lookup"><span data-stu-id="0c019-110">Be aware that any of these ESE APIs can also return other errors that are not documented for each API.</span></span> <span data-ttu-id="0c019-111">在這些情況下，呼叫端應該直接處理錯誤，就像 API 所傳回的任何其他錯誤一樣。</span><span class="sxs-lookup"><span data-stu-id="0c019-111">In these cases, the caller should simply handle the error as they would any other error that is returned by the API.</span></span> <span data-ttu-id="0c019-112">特定的錯誤值接著可以用於診斷用途，例如追蹤。</span><span class="sxs-lookup"><span data-stu-id="0c019-112">The specific error value may then be used for diagnostic purposes such as tracing.</span></span>

<span data-ttu-id="0c019-113">一般情況下，大於零的值應解釋為警告、值為零應解讀為成功，而小於零的值則應視為錯誤。</span><span class="sxs-lookup"><span data-stu-id="0c019-113">In general, a value that is greater than zero should be interpreted as a warning, a value of zero should be interpreted as success, and a value that is less than zero should be interpreted as an error.</span></span> <span data-ttu-id="0c019-114">這些值中沒有其他模式 (例如，) 的值範圍應該依賴應用程式。</span><span class="sxs-lookup"><span data-stu-id="0c019-114">No other patterns in these values (for example, ranges of values) should be relied upon by an application.</span></span>

<span data-ttu-id="0c019-115">當 ESE 遇到一些較嚴重的錯誤時，它會建立一個事件記錄檔專案，其中包含錯誤的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0c019-115">When ESE encounters some of the more serious errors, it creates an event log entry that contains details about the errors.</span></span> <span data-ttu-id="0c019-116">記錄層級可由 [事件記錄參數](./event-log-parameters.md)控制。</span><span class="sxs-lookup"><span data-stu-id="0c019-116">The level of logging can be controlled by [Event Log Parameters](./event-log-parameters.md).</span></span>

<span data-ttu-id="0c019-117">某些應用程式需要能夠以 Hresult 的方式傳回 [JET_ERR](./jet-err.md)s。</span><span class="sxs-lookup"><span data-stu-id="0c019-117">Some applications require the ability to return [JET_ERR](./jet-err.md)s as HRESULTs.</span></span> <span data-ttu-id="0c019-118">下列 c + + 範例顯示如何進行轉換：</span><span class="sxs-lookup"><span data-stu-id="0c019-118">The following C++ example shows how to make that conversion:</span></span>

```cpp
    #ifndef FACILITY_JET_ERR
    #define FACILITY_JET_ERR 0xE5E
    #endif
    #ifndef HRESULT_FROM_JET_ERR
    #define HRESULT_FROM_JET_ERR( __err )
    (
      ( __err ) == JET_errSuccess ?
      S_OK :
      (
        ( __err ) == JET_errOutOfMemory ?
        E_OUTOFMEMORY :
        MAKE_HRESULT
        (
          (
            ( __err ) < 0 ?
            SEVERITY_ERROR :
            SEVERITY_SUCCESS
          ),
          FACILITY_JET_ERR,
          (
            ( __err ) < 0 ?
            -( __err ) :
            ( __err )
          )
          & 0xFFFF
        )
      )
    )
    
    #endif
```

<span data-ttu-id="0c019-119">如需設定系統參數進行錯誤處理的詳細資訊，請參閱 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="0c019-119">For information about configuring system parameters for error handling, see [Error Handling Parameters](./error-handling-parameters.md).</span></span>

### <a name="see-also"></a><span data-ttu-id="0c019-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c019-120">See Also</span></span>

[<span data-ttu-id="0c019-121">錯誤處理參數</span><span class="sxs-lookup"><span data-stu-id="0c019-121">Error Handling Parameters</span></span>](./error-handling-parameters.md)

[<span data-ttu-id="0c019-122">可擴充儲存引擎錯誤碼</span><span class="sxs-lookup"><span data-stu-id="0c019-122">Extensible Storage Engine Error Codes</span></span>](./extensible-storage-engine-error-codes.md)

[<span data-ttu-id="0c019-123">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="0c019-123">JET_ERR</span></span>](./jet-err.md)
