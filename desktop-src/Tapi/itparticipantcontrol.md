---
description: ITParticipantControl 介面是由 IPConf MSP 所執行。
ms.assetid: e617f2a4-6be8-4cb1-9f03-470c5100b834
title: 'ITParticipantControl 介面 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96075748f0c35cbc5af3c6cd07277d15222e0658
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998408"
---
# <a name="itparticipantcontrol-interface"></a><span data-ttu-id="6a957-103">ITParticipantControl 介面</span><span class="sxs-lookup"><span data-stu-id="6a957-103">ITParticipantControl interface</span></span>

<span data-ttu-id="6a957-104">\[**ITParticipantControl** 無法在 windows Vista、windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="6a957-104">\[**ITParticipantControl** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6a957-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="6a957-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="6a957-106">**ITParticipantControl** 介面是由 IPConf MSP 所執行。</span><span class="sxs-lookup"><span data-stu-id="6a957-106">The **ITParticipantControl** interface is implemented by the IPConf MSP.</span></span> <span data-ttu-id="6a957-107">此介面會在呼叫物件上公開。</span><span class="sxs-lookup"><span data-stu-id="6a957-107">This interface is exposed on the call object.</span></span> <span data-ttu-id="6a957-108">這個介面可讓應用程式取得會議中參與者的指標。</span><span class="sxs-lookup"><span data-stu-id="6a957-108">This interface allows an application to retrieve pointers to the participants in a conference.</span></span> <span data-ttu-id="6a957-109">**ITParticipantControl** 介面是藉由在 [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)上呼叫 **QueryInterface** 來建立。</span><span class="sxs-lookup"><span data-stu-id="6a957-109">The **ITParticipantControl** interface is created by calling **QueryInterface** on [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).</span></span>

## <a name="members"></a><span data-ttu-id="6a957-110">成員</span><span class="sxs-lookup"><span data-stu-id="6a957-110">Members</span></span>

<span data-ttu-id="6a957-111">**ITParticipantControl** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="6a957-111">The **ITParticipantControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6a957-112">**ITParticipantControl** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6a957-112">**ITParticipantControl** also has these types of members:</span></span>

-   [<span data-ttu-id="6a957-113">方法</span><span class="sxs-lookup"><span data-stu-id="6a957-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6a957-114">方法</span><span class="sxs-lookup"><span data-stu-id="6a957-114">Methods</span></span>

<span data-ttu-id="6a957-115">**ITParticipantControl** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="6a957-115">The **ITParticipantControl** interface has these methods.</span></span>



| <span data-ttu-id="6a957-116">方法</span><span class="sxs-lookup"><span data-stu-id="6a957-116">Method</span></span>                                                                      | <span data-ttu-id="6a957-117">描述</span><span class="sxs-lookup"><span data-stu-id="6a957-117">Description</span></span>                                                                                                                                                                 |
|:----------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6a957-118">**EnumerateParticipants**</span><span class="sxs-lookup"><span data-stu-id="6a957-118">**EnumerateParticipants**</span></span>](itparticipantcontrol-enumerateparticipants.md) | <span data-ttu-id="6a957-119">列舉目前參與會議的參與者。</span><span class="sxs-lookup"><span data-stu-id="6a957-119">Enumerates participants currently involved in the conference.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="6a957-120">**取得 \_ 參與者**</span><span class="sxs-lookup"><span data-stu-id="6a957-120">**get\_Participants**</span></span>](itparticipantcontrol-get-participants.md)          | <span data-ttu-id="6a957-121">建立與目前會議相關聯的參與者集合。</span><span class="sxs-lookup"><span data-stu-id="6a957-121">Creates a collection of participants associated with the current conference.</span></span> <span data-ttu-id="6a957-122">提供給 Automation 用戶端應用程式，例如以 Visual Basic 撰寫的應用程式。</span><span class="sxs-lookup"><span data-stu-id="6a957-122">Provided for Automation client applications, such as those written in Visual Basic.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6a957-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a957-123">Requirements</span></span>



| <span data-ttu-id="6a957-124">需求</span><span class="sxs-lookup"><span data-stu-id="6a957-124">Requirement</span></span> | <span data-ttu-id="6a957-125">值</span><span class="sxs-lookup"><span data-stu-id="6a957-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6a957-126">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="6a957-126">TAPI version</span></span><br/> | <span data-ttu-id="6a957-127">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="6a957-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="6a957-128">標頭</span><span class="sxs-lookup"><span data-stu-id="6a957-128">Header</span></span><br/>       | <dl> <span data-ttu-id="6a957-129"><dt>Confpriv。h</dt></span><span class="sxs-lookup"><span data-stu-id="6a957-129"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="6a957-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="6a957-130">Library</span></span><br/>      | <dl> <span data-ttu-id="6a957-131"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="6a957-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="6a957-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6a957-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="6a957-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a957-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



 

