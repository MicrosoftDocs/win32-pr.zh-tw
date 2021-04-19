---
description: OnStop 方法必須由監視器所執行。 MSCVC 會呼叫這個方法，以通知監視器將會停止該捕獲。
ms.assetid: 5988bfb8-2068-42a1-a774-6f6be9828568
title: 'IMonitor：： OnStop 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStop
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: a737aa5bede443b63f2074239eec17ea8a205cc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972594"
---
# <a name="imonitoronstop-method"></a><span data-ttu-id="95e2d-104">IMonitor：： OnStop 方法</span><span class="sxs-lookup"><span data-stu-id="95e2d-104">IMonitor::OnStop method</span></span>

<span data-ttu-id="95e2d-105">**OnStop** 方法必須由監視器所執行。</span><span class="sxs-lookup"><span data-stu-id="95e2d-105">The **OnStop** method must be implemented by the monitor.</span></span> <span data-ttu-id="95e2d-106">MSCVC 會呼叫這個方法，以通知監視器將會停止該捕獲。</span><span class="sxs-lookup"><span data-stu-id="95e2d-106">The MSCVC calls this method to notify the monitor that the capture will be stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="95e2d-107">語法</span><span class="sxs-lookup"><span data-stu-id="95e2d-107">Syntax</span></span>


```C++
HRESULT OnStop();
```



## <a name="parameters"></a><span data-ttu-id="95e2d-108">參數</span><span class="sxs-lookup"><span data-stu-id="95e2d-108">Parameters</span></span>

<span data-ttu-id="95e2d-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="95e2d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="95e2d-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="95e2d-110">Return value</span></span>

<span data-ttu-id="95e2d-111">如果方法成功，則傳回值為 S \_ OK (與 >aad-userreadusingalternativesecurityid-noerror) 相同。</span><span class="sxs-lookup"><span data-stu-id="95e2d-111">If the method is successful, the return value is S\_OK (which is the same as NOERROR).</span></span>

<span data-ttu-id="95e2d-112">如果此方法不成功，則傳回值會是錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="95e2d-112">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="95e2d-113">傳回錯誤碼時，無法重新開機監視。</span><span class="sxs-lookup"><span data-stu-id="95e2d-113">When an error code is returned, the monitor cannot be restarted.</span></span>

## <a name="remarks"></a><span data-ttu-id="95e2d-114">備註</span><span class="sxs-lookup"><span data-stu-id="95e2d-114">Remarks</span></span>

<span data-ttu-id="95e2d-115">MCSVC 會在呼叫 [IRTC：： Stop](irtc-stop.md) 之後呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="95e2d-115">The MCSVC calls this method after [IRTC::Stop](irtc-stop.md) is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="95e2d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="95e2d-116">Requirements</span></span>



| <span data-ttu-id="95e2d-117">需求</span><span class="sxs-lookup"><span data-stu-id="95e2d-117">Requirement</span></span> | <span data-ttu-id="95e2d-118">值</span><span class="sxs-lookup"><span data-stu-id="95e2d-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="95e2d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="95e2d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="95e2d-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95e2d-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="95e2d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="95e2d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="95e2d-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95e2d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="95e2d-123">標頭</span><span class="sxs-lookup"><span data-stu-id="95e2d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="95e2d-124"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="95e2d-124"><dt>Netmon.h</dt></span></span> </dl> |



 

 




