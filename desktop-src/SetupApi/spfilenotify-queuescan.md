---
description: 針對檔案 \_ 佇列的複製子佇列中的每個節點 SetupScanFileQueue，會將 SPFILENOTIFY QUEUESCAN 通知傳送至回呼常式。 只有在呼叫 SetupScanFileQueue 函式來指定旗標 SPQ \_ SCAN 使用回呼時，才會發生這種情況 \_ \_ 。
ms.assetid: 8aacc6c0-b6fe-4b4a-bbe4-a0351baf1f30
title: 'SPFILENOTIFY_QUEUESCAN 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66202a398f7e3f4e1121782f9469d2d6f299452c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988351"
---
# <a name="spfilenotify_queuescan-message"></a><span data-ttu-id="197a2-104">SPFILENOTIFY \_ QUEUESCAN 訊息</span><span class="sxs-lookup"><span data-stu-id="197a2-104">SPFILENOTIFY\_QUEUESCAN message</span></span>

<span data-ttu-id="197a2-105">針對檔案佇列的複製子佇列中的每個節點 [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) ，會將 **SPFILENOTIFY \_ QUEUESCAN** 通知傳送至回呼常式。</span><span class="sxs-lookup"><span data-stu-id="197a2-105">The **SPFILENOTIFY\_QUEUESCAN** notification is sent to a callback routine by [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) for each node in the copy subqueue of the file queue.</span></span> <span data-ttu-id="197a2-106">只有在呼叫 **SetupScanFileQueue** 函式來指定旗標 SPQ \_ SCAN \_ 使用回呼時，才會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="197a2-106">This only occurs if the **SetupScanFileQueue** function was called specifying the flag SPQ\_SCAN\_USE\_CALLBACK.</span></span>


```C++
SPFILENOTIFY_QUEUESCAN
  Param1 = (UINT) TargetPath;
  Param2 = (UINT) DelayFlag;
            
```



## <a name="parameters"></a><span data-ttu-id="197a2-107">參數</span><span class="sxs-lookup"><span data-stu-id="197a2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="197a2-108">*Param1*</span><span class="sxs-lookup"><span data-stu-id="197a2-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="197a2-109">以 Null 終止的字串，指定目前節點中佇列之檔案的目標路徑資訊。</span><span class="sxs-lookup"><span data-stu-id="197a2-109">Null-terminated string that specifies the target path information for the file queued in the current node.</span></span>

</dd> <dt>

<span data-ttu-id="197a2-110">*Param2*</span><span class="sxs-lookup"><span data-stu-id="197a2-110">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="197a2-111">如果佇列目前節點中的檔案正在使用中， *Param2* 會將值 SPQ \_ 延遲 \_ 複製。</span><span class="sxs-lookup"><span data-stu-id="197a2-111">If the file in the current node of the queue is in use, *Param2* takes the value SPQ\_DELAYED\_COPY.</span></span> <span data-ttu-id="197a2-112">如果檔案不在使用中，此值為零。</span><span class="sxs-lookup"><span data-stu-id="197a2-112">If the file is not in use, the value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="197a2-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="197a2-113">Return value</span></span>

<span data-ttu-id="197a2-114">回呼常式應該會傳回 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="197a2-114">The callback routine should return a [system error code](/windows/desktop/Debug/system-error-codes).</span></span>

<span data-ttu-id="197a2-115">如果回呼常式未傳回 \_ 錯誤，則會繼續執行佇列掃描。</span><span class="sxs-lookup"><span data-stu-id="197a2-115">If the callback routine returns NO\_ERROR, the queue scan continues.</span></span> <span data-ttu-id="197a2-116">如果常式傳回任何其他錯誤碼，則佇列掃描會中止，且 [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="197a2-116">If the routine returns any other error code, the queue scan aborts and [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) returns **FALSE**.</span></span>

> [!Note]  
> <span data-ttu-id="197a2-117">[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)函數不會處理這項通知。</span><span class="sxs-lookup"><span data-stu-id="197a2-117">This notification is not handled by the [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) function.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="197a2-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="197a2-118">Requirements</span></span>



| <span data-ttu-id="197a2-119">需求</span><span class="sxs-lookup"><span data-stu-id="197a2-119">Requirement</span></span> | <span data-ttu-id="197a2-120">值</span><span class="sxs-lookup"><span data-stu-id="197a2-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="197a2-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="197a2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="197a2-122">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="197a2-122">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="197a2-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="197a2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="197a2-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="197a2-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="197a2-125">標頭</span><span class="sxs-lookup"><span data-stu-id="197a2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="197a2-126"><dt>Setupapi.log。h</dt></span><span class="sxs-lookup"><span data-stu-id="197a2-126"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="197a2-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="197a2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="197a2-128">概觀</span><span class="sxs-lookup"><span data-stu-id="197a2-128">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="197a2-129">通知</span><span class="sxs-lookup"><span data-stu-id="197a2-129">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="197a2-130">**SetupScanFileQueue**</span><span class="sxs-lookup"><span data-stu-id="197a2-130">**SetupScanFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

