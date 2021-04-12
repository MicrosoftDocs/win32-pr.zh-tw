---
title: ActivationFailureLoggingLevel
description: 針對元件啟動和啟用的失敗要求，設定事件記錄檔專案的詳細資訊。
ms.assetid: c3981621-5826-405c-8962-edfa9c783c2d
keywords:
- ActivationFailureLoggingLevel 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfdd834be35a59dd5d8e207cd679dae68043d70c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372633"
---
# <a name="activationfailurelogginglevel"></a><span data-ttu-id="5ce9e-104">ActivationFailureLoggingLevel</span><span class="sxs-lookup"><span data-stu-id="5ce9e-104">ActivationFailureLoggingLevel</span></span>

<span data-ttu-id="5ce9e-105">針對元件啟動和啟用的失敗要求，設定事件記錄檔專案的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="5ce9e-105">Sets the verbosity of event log entries about failed requests for component launch and activation.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="5ce9e-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="5ce9e-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   ActivationFailureLoggingLevel = value
```

## <a name="remarks"></a><span data-ttu-id="5ce9e-107">備註</span><span class="sxs-lookup"><span data-stu-id="5ce9e-107">Remarks</span></span>

<span data-ttu-id="5ce9e-108">這是 **REG \_ DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="5ce9e-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="5ce9e-109">值</span><span class="sxs-lookup"><span data-stu-id="5ce9e-109">Value</span></span> | <span data-ttu-id="5ce9e-110">描述</span><span class="sxs-lookup"><span data-stu-id="5ce9e-110">Description</span></span>                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ce9e-111">0</span><span class="sxs-lookup"><span data-stu-id="5ce9e-111">0</span></span>     | <span data-ttu-id="5ce9e-112">使用任意記錄。</span><span class="sxs-lookup"><span data-stu-id="5ce9e-112">Use discretionary logging.</span></span> <span data-ttu-id="5ce9e-113">預設會記錄失敗，但用戶端可以 \_ 在 CoCreateInstanceEx 中指定 CLSCTX NO \_ \_ [\*\*\*\*](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)，來覆寫此行為。</span><span class="sxs-lookup"><span data-stu-id="5ce9e-113">Log failures by default, but clients can override this behavior by specifying CLSCTX\_NO\_FAILURE\_LOG in [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex).</span></span> <span data-ttu-id="5ce9e-114">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="5ce9e-114">This is the default value.</span></span> |
| <span data-ttu-id="5ce9e-115">1</span><span class="sxs-lookup"><span data-stu-id="5ce9e-115">1</span></span>     | <span data-ttu-id="5ce9e-116">無論用戶端指定什麼，一律記錄所有失敗。</span><span class="sxs-lookup"><span data-stu-id="5ce9e-116">Always log all failures no matter what the client specified.</span></span>                                                                                                                                                      |
| <span data-ttu-id="5ce9e-117">2</span><span class="sxs-lookup"><span data-stu-id="5ce9e-117">2</span></span>     | <span data-ttu-id="5ce9e-118">請勿記錄任何失敗，不論用戶端是否已指定。</span><span class="sxs-lookup"><span data-stu-id="5ce9e-118">Never log any failures no matter what the client specified.</span></span>                                                                                                                                                       |



 

<span data-ttu-id="5ce9e-119">如果您需要應用程式來控制事件記錄，建議您將此值設為0，並在需要時撰寫用戶端程式代碼加以覆寫。</span><span class="sxs-lookup"><span data-stu-id="5ce9e-119">If you need an application to control event logging, it is recommended that you set this value to 0 and write the client code to override it when needed.</span></span> <span data-ttu-id="5ce9e-120">強烈建議您不要將值設定為2。</span><span class="sxs-lookup"><span data-stu-id="5ce9e-120">It is strongly recommended that you do not set the value to 2.</span></span> <span data-ttu-id="5ce9e-121">如果事件記錄已停用，則更難診斷問題。</span><span class="sxs-lookup"><span data-stu-id="5ce9e-121">If event logging is disabled, it is more difficult to diagnose problems.</span></span> <span data-ttu-id="5ce9e-122">對於電腦限制許可權失敗，其中 COM 沒有 CLSCTX 位，COM 會將0的值視為1。</span><span class="sxs-lookup"><span data-stu-id="5ce9e-122">For machine restrictions permission failures, where COM does not have the CLSCTX bits, COM will treat a value of 0 as 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ce9e-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="5ce9e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ce9e-124">設定 COM 應用程式的安全性</span><span class="sxs-lookup"><span data-stu-id="5ce9e-124">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




