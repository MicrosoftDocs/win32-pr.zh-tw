---
description: 適用于通訊端關閉操作的 Winsock 網路追蹤事件。
ms.assetid: C59B2B51-288A-46C9-B390-26A18DB0C2FB
title: AFD_EVENT_CLOSE 事件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AFD_EVENT_CLOSE
api_type:
- NA
api_location: ''
ms.openlocfilehash: fbc6c63a3084db6a9be0a4b4ea7672d84881a29a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690420"
---
# <a name="afd_event_close-event"></a><span data-ttu-id="917f7-103">AFD \_ 事件 \_ 關閉事件</span><span class="sxs-lookup"><span data-stu-id="917f7-103">AFD\_EVENT\_CLOSE event</span></span>

<span data-ttu-id="917f7-104">**AFD \_ 事件 \_ CLOSE** 事件是通訊端關閉作業的 Winsock 網路追蹤事件。</span><span class="sxs-lookup"><span data-stu-id="917f7-104">The **AFD\_EVENT\_CLOSE** event is a Winsock network tracing event for socket close operation.</span></span>


```C++
const EVENT_DESCRIPTOR AFD_EVENT_CLOSE = {0x3e9, 0x0, 0x10, 0x4, 0xf, 0x3e9, 0x8000000000000004};
```



## <a name="parameters"></a><span data-ttu-id="917f7-105">參數</span><span class="sxs-lookup"><span data-stu-id="917f7-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="917f7-106">*EnterExit*</span><span class="sxs-lookup"><span data-stu-id="917f7-106">*EnterExit*</span></span> 
</dt> <dd>

<span data-ttu-id="917f7-107">此事件的資訊。</span><span class="sxs-lookup"><span data-stu-id="917f7-107">Information on this event.</span></span>

<span data-ttu-id="917f7-108">下表列出 *EnterExit* 參數的可能值：</span><span class="sxs-lookup"><span data-stu-id="917f7-108">The following table lists the possible values for the *EnterExit* parameter:</span></span>



| <span data-ttu-id="917f7-109">值</span><span class="sxs-lookup"><span data-stu-id="917f7-109">Value</span></span>                                                                        | <span data-ttu-id="917f7-110">意義</span><span class="sxs-lookup"><span data-stu-id="917f7-110">Meaning</span></span>                                                                                              |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="917f7-111"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="917f7-111"><dt>0</dt></span></span> </dl> | <span data-ttu-id="917f7-112">Winsock 要求的開始。</span><span class="sxs-lookup"><span data-stu-id="917f7-112">The start of a Winsock request.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="917f7-113"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="917f7-113"><dt>1</dt></span></span> </dl> | <span data-ttu-id="917f7-114">Winsock 要求已完成。</span><span class="sxs-lookup"><span data-stu-id="917f7-114">The Winsock request completed.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="917f7-115"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="917f7-115"><dt>2</dt></span></span> </dl> | <span data-ttu-id="917f7-116">Winsock AFD 驅動程式採取內部動作 (中止連線，例如) 。</span><span class="sxs-lookup"><span data-stu-id="917f7-116">The Winsock AFD driver took an internal action (aborting a connection, for example).</span></span><br/>      |
| <dl> <span data-ttu-id="917f7-117"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="917f7-117"><dt>3</dt></span></span> </dl> | <span data-ttu-id="917f7-118">TCP/IP 驅動程式導致此事件發生。</span><span class="sxs-lookup"><span data-stu-id="917f7-118">The TCP/IP driver caused this event to occur.</span></span> <span data-ttu-id="917f7-119">這通常表示資料通知。</span><span class="sxs-lookup"><span data-stu-id="917f7-119">This usually indicates a data notification.</span></span><br/> |
| <dl> <span data-ttu-id="917f7-120"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="917f7-120"><dt>4</dt></span></span> </dl> | <span data-ttu-id="917f7-121">Winsock AFD 驅動程式會導致此事件發生 (設定 socket 選項，例如) 。</span><span class="sxs-lookup"><span data-stu-id="917f7-121">The Winsock AFD driver caused this event to occur (setting a socket option, for example).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="917f7-122">*位置*</span><span class="sxs-lookup"><span data-stu-id="917f7-122">*Location*</span></span> 
</dt> <dd>

<span data-ttu-id="917f7-123">內部使用的私用欄位。</span><span class="sxs-lookup"><span data-stu-id="917f7-123">A private field used internally.</span></span>

</dd> <dt>

<span data-ttu-id="917f7-124">*處理*</span><span class="sxs-lookup"><span data-stu-id="917f7-124">*Process*</span></span> 
</dt> <dd>

<span data-ttu-id="917f7-125">擁有相關通訊端之進程的 [EPROCESS](/windows-hardware/drivers/kernel/eprocess) 位址。</span><span class="sxs-lookup"><span data-stu-id="917f7-125">The [EPROCESS](/windows-hardware/drivers/kernel/eprocess) address of the process that owns the related socket.</span></span> <span data-ttu-id="917f7-126">這是一個不透明的結構，可作為進程的處理常式物件。</span><span class="sxs-lookup"><span data-stu-id="917f7-126">This is an opaque structure that serves as the process object for a process.</span></span> <span data-ttu-id="917f7-127">如需詳細資訊，請參閱 [EPROCESS](/windows-hardware/drivers/kernel/eprocess) 結構的 Windows 驅動程式套件檔。</span><span class="sxs-lookup"><span data-stu-id="917f7-127">For more information, see the Windows Driver Kit documentation for the [EPROCESS](/windows-hardware/drivers/kernel/eprocess) structure.</span></span>

</dd> <dt>

<span data-ttu-id="917f7-128">*端點*</span><span class="sxs-lookup"><span data-stu-id="917f7-128">*Endpoint*</span></span> 
</dt> <dd>

<span data-ttu-id="917f7-129">\_通訊端的 AFD 端點位址。</span><span class="sxs-lookup"><span data-stu-id="917f7-129">The AFD\_ENDPOINT address of the socket.</span></span>

</dd> <dt>

<span data-ttu-id="917f7-130">*狀態*</span><span class="sxs-lookup"><span data-stu-id="917f7-130">*Status*</span></span> 
</dt> <dd>

<span data-ttu-id="917f7-131">運算的 NTSTATUS 程式碼。</span><span class="sxs-lookup"><span data-stu-id="917f7-131">The NTSTATUS code for the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="917f7-132">備註</span><span class="sxs-lookup"><span data-stu-id="917f7-132">Remarks</span></span>

<span data-ttu-id="917f7-133">**AFD \_ 事件 \_ 關閉** 事件是針對 Winsock 網路作業追蹤，以關閉通訊端。</span><span class="sxs-lookup"><span data-stu-id="917f7-133">The **AFD\_EVENT\_CLOSE** event is traced for a Winsock network operation to close a socket.</span></span> <span data-ttu-id="917f7-134">此事件的通道是 Winsock-AFD。</span><span class="sxs-lookup"><span data-stu-id="917f7-134">The channel for this event is Winsock-AFD.</span></span> <span data-ttu-id="917f7-135">此事件的層級為資訊。</span><span class="sxs-lookup"><span data-stu-id="917f7-135">The level for this event is informational.</span></span>

## <a name="requirements"></a><span data-ttu-id="917f7-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="917f7-136">Requirements</span></span>



| <span data-ttu-id="917f7-137">需求</span><span class="sxs-lookup"><span data-stu-id="917f7-137">Requirement</span></span> | <span data-ttu-id="917f7-138">值</span><span class="sxs-lookup"><span data-stu-id="917f7-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="917f7-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="917f7-139">Minimum supported client</span></span><br/> | <span data-ttu-id="917f7-140">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="917f7-140">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="917f7-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="917f7-141">Minimum supported server</span></span><br/> | <span data-ttu-id="917f7-142">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="917f7-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="917f7-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="917f7-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="917f7-144">Winsock 追蹤的控制權</span><span class="sxs-lookup"><span data-stu-id="917f7-144">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="917f7-145">**事件 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="917f7-145">**EVENT\_DESCRIPTOR**</span></span>](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
</dt> <dt>

[<span data-ttu-id="917f7-146">Winsock 追蹤</span><span class="sxs-lookup"><span data-stu-id="917f7-146">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="917f7-147">Winsock 追蹤層級</span><span class="sxs-lookup"><span data-stu-id="917f7-147">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="917f7-148">Winsock 目錄變更追蹤詳細資料</span><span class="sxs-lookup"><span data-stu-id="917f7-148">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

