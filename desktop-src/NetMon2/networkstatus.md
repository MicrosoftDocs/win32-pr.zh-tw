---
description: '>NETWORKSTATUS 結構描述 NPP 的目前狀態。'
ms.assetid: e5e07480-cfc3-408f-9ca2-48a697e4b875
title: '>NETWORKSTATUS 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NETWORKSTATUS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 067a57dabfb5222deb27de44c60c6eb121cd8c36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514145"
---
# <a name="networkstatus-structure"></a><span data-ttu-id="04691-103">>NETWORKSTATUS 結構</span><span class="sxs-lookup"><span data-stu-id="04691-103">NETWORKSTATUS structure</span></span>

<span data-ttu-id="04691-104">**>networkstatus** 結構描述 NPP 的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="04691-104">The **NETWORKSTATUS** structure describes the current status of the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="04691-105">語法</span><span class="sxs-lookup"><span data-stu-id="04691-105">Syntax</span></span>


```C++
typedef struct _NETWORKSTATUS {
  DWORD State;
  DWORD Flags;
} NETWORKSTATUS, *LPNETWORKSTATUS;
```



## <a name="members"></a><span data-ttu-id="04691-106">成員</span><span class="sxs-lookup"><span data-stu-id="04691-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="04691-107">**State**</span><span class="sxs-lookup"><span data-stu-id="04691-107">**State**</span></span>
</dt> <dd>

<span data-ttu-id="04691-108">表示 NPP 的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="04691-108">Indicates the current state of the NPP.</span></span>



| <span data-ttu-id="04691-109">值</span><span class="sxs-lookup"><span data-stu-id="04691-109">Value</span></span>                                                                                                                                                                                                          | <span data-ttu-id="04691-110">意義</span><span class="sxs-lookup"><span data-stu-id="04691-110">Meaning</span></span>                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="NETWORKSTATUS_STATE_VOID"></span><span id="networkstatus_state_void"></span><dl> <span data-ttu-id="04691-111"><dt>**>NETWORKSTATUS \_ 狀態 \_ VOID**</dt></span><span class="sxs-lookup"><span data-stu-id="04691-111"><dt>**NETWORKSTATUS\_STATE\_VOID**</dt></span></span> </dl>                | <span data-ttu-id="04691-112">NPP 未連接或已連線，且未啟動 capture。</span><span class="sxs-lookup"><span data-stu-id="04691-112">The NPP is not connected, or it is connected and the capture is not started.</span></span><br/> |
| <span id="NETWORKSTATUS_STATE_CAPTURING"></span><span id="networkstatus_state_capturing"></span><dl> <span data-ttu-id="04691-113"><dt>**>NETWORKSTATUS \_ 狀態 \_ 捕獲**</dt></span><span class="sxs-lookup"><span data-stu-id="04691-113"><dt>**NETWORKSTATUS\_STATE\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="04691-114">NPP 正在捕獲資料。</span><span class="sxs-lookup"><span data-stu-id="04691-114">The NPP is capturing data.</span></span><br/>                                                   |
| <span id="NETWORKSTATUS_STATE_PAUSED"></span><span id="networkstatus_state_paused"></span><dl> <span data-ttu-id="04691-115"><dt>**>NETWORKSTATUS \_ 狀態已 \_ 暫停**</dt></span><span class="sxs-lookup"><span data-stu-id="04691-115"><dt>**NETWORKSTATUS\_STATE\_PAUSED**</dt></span></span> </dl>          | <span data-ttu-id="04691-116">NPP 已在捕獲資料時暫停。</span><span class="sxs-lookup"><span data-stu-id="04691-116">The NPP has paused while capturing data.</span></span><br/>                                     |



 

</dd> <dt>

<span data-ttu-id="04691-117">**旗標**</span><span class="sxs-lookup"><span data-stu-id="04691-117">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="04691-118">描述 NPP 目前狀態的旗標。</span><span class="sxs-lookup"><span data-stu-id="04691-118">Flags that describe the current state of the NPP.</span></span>



| <span data-ttu-id="04691-119">值</span><span class="sxs-lookup"><span data-stu-id="04691-119">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="04691-120">意義</span><span class="sxs-lookup"><span data-stu-id="04691-120">Meaning</span></span>                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="NETWORKSTATUS_FLAGS_TRIGGER_PENDING"></span><span id="networkstatus_flags_trigger_pending"></span><dl> <span data-ttu-id="04691-121"><dt>**>NETWORKSTATUS \_ 旗標 \_ 觸發程式 \_ 暫止**</dt></span><span class="sxs-lookup"><span data-stu-id="04691-121"><dt>**NETWORKSTATUS\_FLAGS\_TRIGGER\_PENDING**</dt></span></span> </dl> | <span data-ttu-id="04691-122">NPP 有暫止的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="04691-122">There is a trigger pending for the NPP.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="04691-123">備註</span><span class="sxs-lookup"><span data-stu-id="04691-123">Remarks</span></span>

<span data-ttu-id="04691-124">使用這個結構時，您必須先配置結構的記憶體，才能使用它，並在不再需要結構時釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="04691-124">When using this structure, you must allocate the memory for the structure before it can be used and free the memory when the structure is no longer needed.</span></span>

<span data-ttu-id="04691-125">本主題底部的 [另請參閱] 清單會列出使用此結構的所有方法。</span><span class="sxs-lookup"><span data-stu-id="04691-125">The See Also list at the bottom of this topic lists all the methods that use this structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="04691-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="04691-126">Requirements</span></span>



| <span data-ttu-id="04691-127">需求</span><span class="sxs-lookup"><span data-stu-id="04691-127">Requirement</span></span> | <span data-ttu-id="04691-128">值</span><span class="sxs-lookup"><span data-stu-id="04691-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="04691-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="04691-129">Minimum supported client</span></span><br/> | <span data-ttu-id="04691-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04691-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="04691-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="04691-131">Minimum supported server</span></span><br/> | <span data-ttu-id="04691-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04691-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="04691-133">標頭</span><span class="sxs-lookup"><span data-stu-id="04691-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="04691-134"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="04691-134"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04691-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04691-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04691-136">IDelaydC：： QueryStatus</span><span class="sxs-lookup"><span data-stu-id="04691-136">IDelaydC::QueryStatus</span></span>](idelaydc-querystatus.md)
</dt> <dt>

[<span data-ttu-id="04691-137">IESP：： QueryStatus</span><span class="sxs-lookup"><span data-stu-id="04691-137">IESP::QueryStatus</span></span>](iesp-querystatus.md)
</dt> <dt>

[<span data-ttu-id="04691-138">IRTC：： QueryStatus</span><span class="sxs-lookup"><span data-stu-id="04691-138">IRTC::QueryStatus</span></span>](irtc-querystatus.md)
</dt> <dt>

[<span data-ttu-id="04691-139">IStats：： QueryStatus</span><span class="sxs-lookup"><span data-stu-id="04691-139">IStats::QueryStatus</span></span>](istats-querystatus.md)
</dt> </dl>

 

 




