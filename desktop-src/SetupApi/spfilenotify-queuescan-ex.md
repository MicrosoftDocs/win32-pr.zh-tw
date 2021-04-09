---
description: 針對檔案 \_ \_ 佇列的複製子佇列中的每個節點，SetupScanFileQueue 會將 SPFILENOTIFY QUEUESCAN EX 通知傳送至回呼常式。
ms.assetid: 293e63f9-9567-4ea7-b7e5-e5046c8a704b
title: 'SPFILENOTIFY_QUEUESCAN_EX 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0e18cf1cdb1cd007dcf46793d2d018dedd80037
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848827"
---
# <a name="spfilenotify_queuescan_ex-message"></a><span data-ttu-id="762d2-103">SPFILENOTIFY \_ QUEUESCAN \_ EX 訊息</span><span class="sxs-lookup"><span data-stu-id="762d2-103">SPFILENOTIFY\_QUEUESCAN\_EX message</span></span>

<span data-ttu-id="762d2-104">針對檔案佇列的複製子佇列中的每個節點， [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)會將 **SPFILENOTIFY \_ QUEUESCAN \_ EX** 通知傳送至回呼常式。</span><span class="sxs-lookup"><span data-stu-id="762d2-104">The **SPFILENOTIFY\_QUEUESCAN\_EX** notification is sent to a callback routine by [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) for each node in the copy subqueue of the file queue.</span></span> <span data-ttu-id="762d2-105">只有在呼叫 **SetupScanFileQueue** 函式來指定旗標 SPQ \_ SCAN \_ USE CALLBACKEX 時，才會發生這種情況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="762d2-105">This only occurs if the **SetupScanFileQueue** function was called specifying the flag SPQ\_SCAN\_USE\_CALLBACKEX.</span></span>


```C++
SPFILENOTIFY_QUEUESCAN_EX
  Param1 = (PFILEPATHS) Filepaths;
            
```



## <a name="parameters"></a><span data-ttu-id="762d2-106">參數</span><span class="sxs-lookup"><span data-stu-id="762d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="762d2-107">*Param1*</span><span class="sxs-lookup"><span data-stu-id="762d2-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="762d2-108">[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="762d2-108">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span> <span data-ttu-id="762d2-109">**目標** 成員是系統上目標檔案的檔案名。</span><span class="sxs-lookup"><span data-stu-id="762d2-109">The **Target** member is the filename of the target file on the system.</span></span> <span data-ttu-id="762d2-110">**來源** 成員是原始程式檔的預期路徑。</span><span class="sxs-lookup"><span data-stu-id="762d2-110">The **Source** member is the expected path of the source file.</span></span> <span data-ttu-id="762d2-111">**Win32Error** 成員是簽署錯誤。</span><span class="sxs-lookup"><span data-stu-id="762d2-111">The **Win32Error** member is the signing error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="762d2-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="762d2-112">Return value</span></span>

<span data-ttu-id="762d2-113">回呼常式應該會傳回 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="762d2-113">The callback routine should return a [system error code](/windows/desktop/Debug/system-error-codes).</span></span>

<span data-ttu-id="762d2-114">如果回呼常式未傳回 \_ 錯誤，則會繼續執行佇列掃描。</span><span class="sxs-lookup"><span data-stu-id="762d2-114">If the callback routine returns NO\_ERROR, the queue scan continues.</span></span> <span data-ttu-id="762d2-115">如果常式傳回任何其他錯誤碼，則佇列掃描會中止，且 [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) 會傳回 FALSE。</span><span class="sxs-lookup"><span data-stu-id="762d2-115">If the routine returns any other error code, the queue scan aborts and [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) returns FALSE.</span></span>

> [!Note]  
> <span data-ttu-id="762d2-116">[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)函數不會處理這項通知。</span><span class="sxs-lookup"><span data-stu-id="762d2-116">This notification is not handled by the [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) function.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="762d2-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="762d2-117">Requirements</span></span>



| <span data-ttu-id="762d2-118">需求</span><span class="sxs-lookup"><span data-stu-id="762d2-118">Requirement</span></span> | <span data-ttu-id="762d2-119">值</span><span class="sxs-lookup"><span data-stu-id="762d2-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="762d2-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="762d2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="762d2-121">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="762d2-121">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="762d2-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="762d2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="762d2-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="762d2-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="762d2-124">標頭</span><span class="sxs-lookup"><span data-stu-id="762d2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="762d2-125"><dt>Setupapi.log。h</dt></span><span class="sxs-lookup"><span data-stu-id="762d2-125"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="762d2-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="762d2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="762d2-127">概觀</span><span class="sxs-lookup"><span data-stu-id="762d2-127">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="762d2-128">通知</span><span class="sxs-lookup"><span data-stu-id="762d2-128">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="762d2-129">**SetupScanFileQueue**</span><span class="sxs-lookup"><span data-stu-id="762d2-129">**SetupScanFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

