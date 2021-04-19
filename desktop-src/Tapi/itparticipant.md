---
description: ITParticipant 介面是由 IPConf MSP 所執行。 它可讓應用程式取得會議參與者的相關資訊，並取得與這些參與者相關聯之資料流程的指標。
ms.assetid: 8c3edfc1-3165-48b7-9d83-8892c192498b
title: 'ITParticipant 介面 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8b7aa9d845d8d2489be0850bcc3fcf3f93ccdac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991149"
---
# <a name="itparticipant-interface"></a><span data-ttu-id="194ae-104">ITParticipant 介面</span><span class="sxs-lookup"><span data-stu-id="194ae-104">ITParticipant interface</span></span>

<span data-ttu-id="194ae-105">\[**ITParticipant** 無法在 windows Vista、windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="194ae-105">\[**ITParticipant** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="194ae-106">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="194ae-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="194ae-107">**ITParticipant** 介面是由 [IPConf MSP](ipconf-msp.md)所執行。</span><span class="sxs-lookup"><span data-stu-id="194ae-107">The **ITParticipant** interface is implemented by the [IPConf MSP](ipconf-msp.md).</span></span> <span data-ttu-id="194ae-108">它可讓應用程式取得會議參與者的相關資訊，並取得與這些參與者相關聯之資料流程的指標。</span><span class="sxs-lookup"><span data-stu-id="194ae-108">It allows an application to retrieve information on conference participants, and get pointers to the streams associated with those participants.</span></span>

<span data-ttu-id="194ae-109">當呼叫使用 IP 會議時，會在呼叫物件上公開這個介面。</span><span class="sxs-lookup"><span data-stu-id="194ae-109">This interface is exposed on the call object when a call uses the IP Conferencing.</span></span> <span data-ttu-id="194ae-110">您可以使用 [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)指標呼叫 **QueryInterface** 來取得指標。</span><span class="sxs-lookup"><span data-stu-id="194ae-110">A pointer can be obtained by calling **QueryInterface** using an [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) pointer.</span></span>

## <a name="members"></a><span data-ttu-id="194ae-111">成員</span><span class="sxs-lookup"><span data-stu-id="194ae-111">Members</span></span>

<span data-ttu-id="194ae-112">**ITParticipant** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="194ae-112">The **ITParticipant** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="194ae-113">**ITParticipant** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="194ae-113">**ITParticipant** also has these types of members:</span></span>

-   [<span data-ttu-id="194ae-114">方法</span><span class="sxs-lookup"><span data-stu-id="194ae-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="194ae-115">方法</span><span class="sxs-lookup"><span data-stu-id="194ae-115">Methods</span></span>

<span data-ttu-id="194ae-116">**ITParticipant** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="194ae-116">The **ITParticipant** interface has these methods.</span></span>



| <span data-ttu-id="194ae-117">方法</span><span class="sxs-lookup"><span data-stu-id="194ae-117">Method</span></span>                                                                      | <span data-ttu-id="194ae-118">描述</span><span class="sxs-lookup"><span data-stu-id="194ae-118">Description</span></span>                                                                                                                                                             |
|:----------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="194ae-119">**EnumerateStreams**</span><span class="sxs-lookup"><span data-stu-id="194ae-119">**EnumerateStreams**</span></span>](itparticipant-enumeratestreams.md)                  | <span data-ttu-id="194ae-120">列舉與目前參與者相關聯的資料流程。</span><span class="sxs-lookup"><span data-stu-id="194ae-120">Enumerates streams associated with the current participant.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="194ae-121">**取得 \_ MediaTypes**</span><span class="sxs-lookup"><span data-stu-id="194ae-121">**get\_MediaTypes**</span></span>](itparticipant-get-mediatypes.md)                     | <span data-ttu-id="194ae-122">取得與參與者相關聯的 [**媒體類型**](tapimediatype--constants.md) 。</span><span class="sxs-lookup"><span data-stu-id="194ae-122">Gets the [**media types**](tapimediatype--constants.md) associated with a participant.</span></span><br/>                                                                      |
| [<span data-ttu-id="194ae-123">**取得 \_ ParticipantTypedInfo**</span><span class="sxs-lookup"><span data-stu-id="194ae-123">**get\_ParticipantTypedInfo**</span></span>](itparticipant-get-participanttypedinfo.md) | <span data-ttu-id="194ae-124">取得所需資訊類型的 BSTR 標記法，例如 PTI \_ EMAILADDRESS。</span><span class="sxs-lookup"><span data-stu-id="194ae-124">Gets a BSTR representation of the needed type of information, such as PTI\_EMAILADDRESS.</span></span><br/>                                                                     |
| [<span data-ttu-id="194ae-125">**取得 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="194ae-125">**get\_Status**</span></span>](itparticipant-get-status.md)                             | <span data-ttu-id="194ae-126">取得參與者的狀態。</span><span class="sxs-lookup"><span data-stu-id="194ae-126">Gets the status of the participant.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="194ae-127">**取得 \_ 資料流程**</span><span class="sxs-lookup"><span data-stu-id="194ae-127">**get\_Streams**</span></span>](itparticipant-get-streams.md)                           | <span data-ttu-id="194ae-128">建立與目前參與者相關聯的資料流程集合。</span><span class="sxs-lookup"><span data-stu-id="194ae-128">Creates a collection of streams associated with the current participant.</span></span> <span data-ttu-id="194ae-129">提供給 Automation 用戶端應用程式，例如以 Visual Basic 撰寫的應用程式。</span><span class="sxs-lookup"><span data-stu-id="194ae-129">Provided for Automation client applications, such as those written in Visual Basic.</span></span><br/> |
| [<span data-ttu-id="194ae-130">**put \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="194ae-130">**put\_Status**</span></span>](itparticipant-put-status.md)                             | <span data-ttu-id="194ae-131">設定是否啟用與參與者相關聯的資料流程。</span><span class="sxs-lookup"><span data-stu-id="194ae-131">Sets whether a stream associated with the participant is enabled.</span></span><br/>                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="194ae-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="194ae-132">Requirements</span></span>



| <span data-ttu-id="194ae-133">需求</span><span class="sxs-lookup"><span data-stu-id="194ae-133">Requirement</span></span> | <span data-ttu-id="194ae-134">值</span><span class="sxs-lookup"><span data-stu-id="194ae-134">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="194ae-135">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="194ae-135">TAPI version</span></span><br/> | <span data-ttu-id="194ae-136">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="194ae-136">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="194ae-137">標頭</span><span class="sxs-lookup"><span data-stu-id="194ae-137">Header</span></span><br/>       | <dl> <span data-ttu-id="194ae-138"><dt>Ipmsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="194ae-138"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="194ae-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="194ae-139">Library</span></span><br/>      | <dl> <span data-ttu-id="194ae-140"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="194ae-140"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="194ae-141">DLL</span><span class="sxs-lookup"><span data-stu-id="194ae-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="194ae-142"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="194ae-142"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="194ae-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="194ae-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="194ae-144">IPConf MSP</span><span class="sxs-lookup"><span data-stu-id="194ae-144">IPConf MSP</span></span>](ipconf-msp.md)
</dt> <dt>

[<span data-ttu-id="194ae-145">IPConf MSP 介面</span><span class="sxs-lookup"><span data-stu-id="194ae-145">IPConf MSP Interfaces</span></span>](ipconf-msp-interfaces.md)
</dt> <dt>

[<span data-ttu-id="194ae-146">**ITCallInfo**</span><span class="sxs-lookup"><span data-stu-id="194ae-146">**ITCallInfo**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> </dl>

 

