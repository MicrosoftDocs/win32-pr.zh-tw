---
description: ITParticipantSubStreamControl 介面是由 IPConf MSP 所執行。
ms.assetid: d5af0fb1-af18-4efb-9b68-1fa60c1272f6
title: 'ITParticipantSubStreamControl 介面 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 799b1a85c6619e1175e620f2c5c5ef851005ba50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980238"
---
# <a name="itparticipantsubstreamcontrol-interface"></a><span data-ttu-id="86a85-103">ITParticipantSubStreamControl 介面</span><span class="sxs-lookup"><span data-stu-id="86a85-103">ITParticipantSubStreamControl interface</span></span>

<span data-ttu-id="86a85-104">\[**ITParticipantSubStreamControl** 無法在 windows Vista、windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="86a85-104">\[**ITParticipantSubStreamControl** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="86a85-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="86a85-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="86a85-106">**ITParticipantSubStreamControl** 介面是由 IPConf MSP 所執行。</span><span class="sxs-lookup"><span data-stu-id="86a85-106">The **ITParticipantSubStreamControl** interface is implemented by the IPConf MSP.</span></span> <span data-ttu-id="86a85-107">此介面會在呼叫物件上公開。</span><span class="sxs-lookup"><span data-stu-id="86a85-107">This interface is exposed on the call object.</span></span> <span data-ttu-id="86a85-108">這個介面會提供方法，讓應用程式能夠探索或控制與參與者的子串流相符。</span><span class="sxs-lookup"><span data-stu-id="86a85-108">This interface provides methods that allow an application to either discover or control the matching of substream to participant.</span></span> <span data-ttu-id="86a85-109">**ITParticipantSubStreamControl** 介面是藉由在 [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)上呼叫 **QueryInterface** 來建立。</span><span class="sxs-lookup"><span data-stu-id="86a85-109">The **ITParticipantSubStreamControl** interface is created by calling **QueryInterface** on [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).</span></span>

## <a name="members"></a><span data-ttu-id="86a85-110">成員</span><span class="sxs-lookup"><span data-stu-id="86a85-110">Members</span></span>

<span data-ttu-id="86a85-111">**ITParticipantSubStreamControl** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="86a85-111">The **ITParticipantSubStreamControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="86a85-112">**ITParticipantSubStreamControl** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="86a85-112">**ITParticipantSubStreamControl** also has these types of members:</span></span>

-   [<span data-ttu-id="86a85-113">方法</span><span class="sxs-lookup"><span data-stu-id="86a85-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="86a85-114">方法</span><span class="sxs-lookup"><span data-stu-id="86a85-114">Methods</span></span>

<span data-ttu-id="86a85-115">**ITParticipantSubStreamControl** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="86a85-115">The **ITParticipantSubStreamControl** interface has these methods.</span></span>



| <span data-ttu-id="86a85-116">方法</span><span class="sxs-lookup"><span data-stu-id="86a85-116">Method</span></span>                                                                                              | <span data-ttu-id="86a85-117">描述</span><span class="sxs-lookup"><span data-stu-id="86a85-117">Description</span></span>                                                     |
|:----------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| [<span data-ttu-id="86a85-118">**取得 \_ ParticipantFromSubStream**</span><span class="sxs-lookup"><span data-stu-id="86a85-118">**get\_ParticipantFromSubStream**</span></span>](itparticipantsubstreamcontrol-get-participantfromsubstream.md) | <span data-ttu-id="86a85-119">取得與指定子流相關聯的參與者。</span><span class="sxs-lookup"><span data-stu-id="86a85-119">Gets participants associated with a given substream.</span></span><br/> |
| [<span data-ttu-id="86a85-120">**取得 \_ SubStreamFromParticipant**</span><span class="sxs-lookup"><span data-stu-id="86a85-120">**get\_SubStreamFromParticipant**</span></span>](itparticipantsubstreamcontrol-get-substreamfromparticipant.md) | <span data-ttu-id="86a85-121">取得與指定參與者相關聯的子串流。</span><span class="sxs-lookup"><span data-stu-id="86a85-121">Gets substreams associated with a given participant.</span></span><br/> |
| [<span data-ttu-id="86a85-122">**SwitchTerminalToSubStream**</span><span class="sxs-lookup"><span data-stu-id="86a85-122">**SwitchTerminalToSubStream**</span></span>](itparticipantsubstreamcontrol-switchterminaltosubstream.md)        | <span data-ttu-id="86a85-123">設定子流上的參與者。</span><span class="sxs-lookup"><span data-stu-id="86a85-123">Sets a participant on a substream.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="86a85-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="86a85-124">Requirements</span></span>



| <span data-ttu-id="86a85-125">需求</span><span class="sxs-lookup"><span data-stu-id="86a85-125">Requirement</span></span> | <span data-ttu-id="86a85-126">值</span><span class="sxs-lookup"><span data-stu-id="86a85-126">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86a85-127">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="86a85-127">TAPI version</span></span><br/> | <span data-ttu-id="86a85-128">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="86a85-128">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="86a85-129">標頭</span><span class="sxs-lookup"><span data-stu-id="86a85-129">Header</span></span><br/>       | <dl> <span data-ttu-id="86a85-130"><dt>Confpriv。h</dt></span><span class="sxs-lookup"><span data-stu-id="86a85-130"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="86a85-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="86a85-131">Library</span></span><br/>      | <dl> <span data-ttu-id="86a85-132"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="86a85-132"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="86a85-133">DLL</span><span class="sxs-lookup"><span data-stu-id="86a85-133">DLL</span></span><br/>          | <dl> <span data-ttu-id="86a85-134"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86a85-134"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="86a85-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86a85-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86a85-136">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="86a85-136">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="86a85-137">**ITSubStream**</span><span class="sxs-lookup"><span data-stu-id="86a85-137">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

