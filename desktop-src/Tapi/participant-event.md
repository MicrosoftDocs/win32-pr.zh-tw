---
description: 參與者 \_ 事件列舉描述參與者事件。
ms.assetid: 678165f2-ad0b-415f-86bf-8c4e3bd8d793
title: 'PARTICIPANT_EVENT 列舉 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 225b1b9901efa5648dfaa326c53ed69cff2c4295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990195"
---
# <a name="participant_event-enumeration"></a><span data-ttu-id="fea34-103">參與者 \_ 事件列舉</span><span class="sxs-lookup"><span data-stu-id="fea34-103">PARTICIPANT\_EVENT enumeration</span></span>

<span data-ttu-id="fea34-104">\[ 此列舉無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="fea34-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fea34-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="fea34-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="fea34-106">**參與者 \_ 事件** 列舉描述參與者事件。</span><span class="sxs-lookup"><span data-stu-id="fea34-106">The **PARTICIPANT\_EVENT** enum describes participant events.</span></span> <span data-ttu-id="fea34-107">[**ITParticipantEvent：： get \_ 事件**](itparticipantevent-get-event.md)方法會傳回這個列舉的成員，以表示發生的會議參與者事件種類。</span><span class="sxs-lookup"><span data-stu-id="fea34-107">The [**ITParticipantEvent::get\_Event**](itparticipantevent-get-event.md) method returns a member of this enum to indicate the type of conference participant event that occurred.</span></span> <span data-ttu-id="fea34-108">存取 [IPCONF MSP](ipconf-msp.md)的應用程式會使用這個列舉。</span><span class="sxs-lookup"><span data-stu-id="fea34-108">This enum is used by applications that access the [IPConf MSP](ipconf-msp.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fea34-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="fea34-109">Syntax</span></span>


```C++
} PARTICIPANT_EVENT;
```



## <a name="constants"></a><span data-ttu-id="fea34-110">常數</span><span class="sxs-lookup"><span data-stu-id="fea34-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fea34-111"><span id="PE_NEW_PARTICIPANT"></span><span id="pe_new_participant"></span>**PE \_ 新 \_ 參與者**</span><span class="sxs-lookup"><span data-stu-id="fea34-111"><span id="PE_NEW_PARTICIPANT"></span><span id="pe_new_participant"></span>**PE\_NEW\_PARTICIPANT**</span></span>
</dt> <dd>

<span data-ttu-id="fea34-112">會議已加入新的參與者。</span><span class="sxs-lookup"><span data-stu-id="fea34-112">A new participant has been added to the conference.</span></span>

</dd> <dt>

<span data-ttu-id="fea34-113"><span id="PE_INFO_CHANGE"></span><span id="pe_info_change"></span>**PE \_ 資訊 \_ 變更**</span><span class="sxs-lookup"><span data-stu-id="fea34-113"><span id="PE_INFO_CHANGE"></span><span id="pe_info_change"></span>**PE\_INFO\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="fea34-114">參與者的資訊已變更。</span><span class="sxs-lookup"><span data-stu-id="fea34-114">Information on a participant has changed.</span></span>

</dd> <dt>

<span data-ttu-id="fea34-115"><span id="PE_PARTICIPANT_LEAVE"></span><span id="pe_participant_leave"></span>**PE \_ 參與者 \_ 離開**</span><span class="sxs-lookup"><span data-stu-id="fea34-115"><span id="PE_PARTICIPANT_LEAVE"></span><span id="pe_participant_leave"></span>**PE\_PARTICIPANT\_LEAVE**</span></span>
</dt> <dd>

<span data-ttu-id="fea34-116">參與者已離開會議。</span><span class="sxs-lookup"><span data-stu-id="fea34-116">A participant has left the conference.</span></span>

</dd> <dt>

<span data-ttu-id="fea34-117"><span id="PE_NEW_SUBSTREAM"></span><span id="pe_new_substream"></span>**PE \_ 新的子 \_ 流**</span><span class="sxs-lookup"><span data-stu-id="fea34-117"><span id="PE_NEW_SUBSTREAM"></span><span id="pe_new_substream"></span>**PE\_NEW\_SUBSTREAM**</span></span>
</dt> <dd>

<span data-ttu-id="fea34-118">參與者已加入新的子流。</span><span class="sxs-lookup"><span data-stu-id="fea34-118">A new substream has been added to the participant.</span></span>

</dd> <dt>

<span data-ttu-id="fea34-119"><span id="PE_SUBSTREAM_REMOVED"></span><span id="pe_substream_removed"></span>**\_ \_ 已移除 PE 子流**</span><span class="sxs-lookup"><span data-stu-id="fea34-119"><span id="PE_SUBSTREAM_REMOVED"></span><span id="pe_substream_removed"></span>**PE\_SUBSTREAM\_REMOVED**</span></span>
</dt> <dd>

<span data-ttu-id="fea34-120">已從參與者移除新的子流。</span><span class="sxs-lookup"><span data-stu-id="fea34-120">A new substream has been removed from the participant.</span></span>

</dd> <dt>

<span data-ttu-id="fea34-121"><span id="PE_SUBSTREAM_MAPPED"></span><span id="pe_substream_mapped"></span>**PE 子 \_ 流 \_ 對應**</span><span class="sxs-lookup"><span data-stu-id="fea34-121"><span id="PE_SUBSTREAM_MAPPED"></span><span id="pe_substream_mapped"></span>**PE\_SUBSTREAM\_MAPPED**</span></span>
</dt> <dd>

<span data-ttu-id="fea34-122">參與者已對應到子流。</span><span class="sxs-lookup"><span data-stu-id="fea34-122">A participant has been mapped to a substream.</span></span>

</dd> <dt>

<span data-ttu-id="fea34-123"><span id="PE_SUBSTREAM_UNMAPPED"></span><span id="pe_substream_unmapped"></span>**PE 子流未對應 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fea34-123"><span id="PE_SUBSTREAM_UNMAPPED"></span><span id="pe_substream_unmapped"></span>**PE\_SUBSTREAM\_UNMAPPED**</span></span>
</dt> <dd>

<span data-ttu-id="fea34-124">已從子流取消對應參與者。</span><span class="sxs-lookup"><span data-stu-id="fea34-124">A participant has been unmapped from a substream.</span></span>

</dd> <dt>

<span data-ttu-id="fea34-125"><span id="PE_PARTICIPANT_TIMEOUT"></span><span id="pe_participant_timeout"></span>**PE \_ 參與者 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="fea34-125"><span id="PE_PARTICIPANT_TIMEOUT"></span><span id="pe_participant_timeout"></span>**PE\_PARTICIPANT\_TIMEOUT**</span></span>
</dt> <dd>

<span data-ttu-id="fea34-126">因為有超時時間，所以已從會議中移除參與者。</span><span class="sxs-lookup"><span data-stu-id="fea34-126">A participant has been removed from the conference due to a timeout.</span></span>

</dd> <dt>

<span data-ttu-id="fea34-127"><span id="PE_PARTICIPANT_RECOVERED"></span><span id="pe_participant_recovered"></span>**已 \_ 復原 PE 參與者 \_**</span><span class="sxs-lookup"><span data-stu-id="fea34-127"><span id="PE_PARTICIPANT_RECOVERED"></span><span id="pe_participant_recovered"></span>**PE\_PARTICIPANT\_RECOVERED**</span></span>
</dt> <dd>

<span data-ttu-id="fea34-128">已移除的參與者也會再次顯示。</span><span class="sxs-lookup"><span data-stu-id="fea34-128">A removed participant is again visible.</span></span> <span data-ttu-id="fea34-129">通常，這是已超時但現在收到信號的參與者。</span><span class="sxs-lookup"><span data-stu-id="fea34-129">Usually, this is a participant who timed out but signals are now being received.</span></span>

</dd> <dt>

<span data-ttu-id="fea34-130"><span id="PE_PARTICIPANT_ACTIVE"></span><span id="pe_participant_active"></span>**使用中的 PE \_ 參與者 \_**</span><span class="sxs-lookup"><span data-stu-id="fea34-130"><span id="PE_PARTICIPANT_ACTIVE"></span><span id="pe_participant_active"></span>**PE\_PARTICIPANT\_ACTIVE**</span></span>
</dt> <dd>

<span data-ttu-id="fea34-131">參與者已在會議中生效。</span><span class="sxs-lookup"><span data-stu-id="fea34-131">The participant has become active in the conference.</span></span>

</dd> <dt>

<span data-ttu-id="fea34-132"><span id="PE_PARTICIPANT_INACTIVE"></span><span id="pe_participant_inactive"></span>**PE \_ 參與者 \_ 非使用中**</span><span class="sxs-lookup"><span data-stu-id="fea34-132"><span id="PE_PARTICIPANT_INACTIVE"></span><span id="pe_participant_inactive"></span>**PE\_PARTICIPANT\_INACTIVE**</span></span>
</dt> <dd>

<span data-ttu-id="fea34-133">參與者在會議中已變成非使用中。</span><span class="sxs-lookup"><span data-stu-id="fea34-133">The participant has become inactive in the conference.</span></span>

</dd> <dt>

<span data-ttu-id="fea34-134"><span id="PE_LOCAL_TALKING"></span><span id="pe_local_talking"></span>**PE \_ 本機 \_ 交談**</span><span class="sxs-lookup"><span data-stu-id="fea34-134"><span id="PE_LOCAL_TALKING"></span><span id="pe_local_talking"></span>**PE\_LOCAL\_TALKING**</span></span>
</dt> <dd>

<span data-ttu-id="fea34-135">本機參與者已開始交談。</span><span class="sxs-lookup"><span data-stu-id="fea34-135">The local participant has started to talk.</span></span>

</dd> <dt>

<span data-ttu-id="fea34-136"><span id="PE_LOCAL_SILENT"></span><span id="pe_local_silent"></span>**PE \_ 本機 \_ 無訊息**</span><span class="sxs-lookup"><span data-stu-id="fea34-136"><span id="PE_LOCAL_SILENT"></span><span id="pe_local_silent"></span>**PE\_LOCAL\_SILENT**</span></span>
</dt> <dd>

<span data-ttu-id="fea34-137">本機參與者在會議中已變成無訊息。</span><span class="sxs-lookup"><span data-stu-id="fea34-137">The local participant has become silent in the conference.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fea34-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="fea34-138">Requirements</span></span>



| <span data-ttu-id="fea34-139">需求</span><span class="sxs-lookup"><span data-stu-id="fea34-139">Requirement</span></span> | <span data-ttu-id="fea34-140">值</span><span class="sxs-lookup"><span data-stu-id="fea34-140">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fea34-141">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="fea34-141">TAPI version</span></span><br/> | <span data-ttu-id="fea34-142">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="fea34-142">Requires TAPI 3.0 or later</span></span><br/>                                              |
| <span data-ttu-id="fea34-143">標頭</span><span class="sxs-lookup"><span data-stu-id="fea34-143">Header</span></span><br/>       | <dl> <span data-ttu-id="fea34-144"><dt>Ipmsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="fea34-144"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fea34-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fea34-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fea34-146">**ITParticipantEvent：： get \_ 事件**</span><span class="sxs-lookup"><span data-stu-id="fea34-146">**ITParticipantEvent::get\_Event**</span></span>](itparticipantevent-get-event.md)
</dt> <dt>

[<span data-ttu-id="fea34-147">IPConf MSP</span><span class="sxs-lookup"><span data-stu-id="fea34-147">IPConf MSP</span></span>](ipconf-msp.md)
</dt> <dt>

[<span data-ttu-id="fea34-148">IPConf MSP 介面</span><span class="sxs-lookup"><span data-stu-id="fea34-148">IPConf MSP Interfaces</span></span>](ipconf-msp-interfaces.md)
</dt> </dl>

 

 




