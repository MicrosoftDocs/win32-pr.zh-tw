---
description: IP 會議 MSP 會為參與者控制項實作為提供者專用的數個介面。 如果此 MSP 與呼叫相關聯，則會在呼叫物件上公開這些介面。
ms.assetid: 01af2452-de2d-42ce-970d-82a83ae0b428
title: IPConf MSP 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edb3c04a93909d237ae25e06c3ed2e0fcc5db9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114928"
---
# <a name="ipconf-msp-interfaces"></a><span data-ttu-id="dcd8b-104">IPConf MSP 介面</span><span class="sxs-lookup"><span data-stu-id="dcd8b-104">IPConf MSP Interfaces</span></span>

<span data-ttu-id="dcd8b-105">\[ IPConf MSP 介面無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="dcd8b-105">\[ The IPConf MSP Interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="dcd8b-106">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="dcd8b-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="dcd8b-107">IP 會議 MSP 會為參與者控制項實作為提供者專用的數個介面。</span><span class="sxs-lookup"><span data-stu-id="dcd8b-107">The IP conferencing MSP implements several provider-specific interfaces for participant control.</span></span> <span data-ttu-id="dcd8b-108">如果此 MSP 與呼叫相關聯，則會在呼叫物件上公開這些介面。</span><span class="sxs-lookup"><span data-stu-id="dcd8b-108">These interfaces are exposed on the call object, if this MSP is associated with the call.</span></span>

<span data-ttu-id="dcd8b-109">[**ITParticipantEvent**](itparticipantevent.md)和 [**IEnumParticipant**](ienumparticipant.md)介面是獨立的物件，此處會列出以供參考之用。</span><span class="sxs-lookup"><span data-stu-id="dcd8b-109">The [**ITParticipantEvent**](itparticipantevent.md) and [**IEnumParticipant**](ienumparticipant.md) interfaces are stand-alone objects, and are listed here for reference convenience.</span></span>



| <span data-ttu-id="dcd8b-110">介面</span><span class="sxs-lookup"><span data-stu-id="dcd8b-110">Interface</span></span>                                            | <span data-ttu-id="dcd8b-111">描述</span><span class="sxs-lookup"><span data-stu-id="dcd8b-111">Description</span></span>                                                                                                                                               |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dcd8b-112">**IMulticastControl**</span><span class="sxs-lookup"><span data-stu-id="dcd8b-112">**IMulticastControl**</span></span>](imulticastcontrol.md)       | <span data-ttu-id="dcd8b-113">允許應用程式為多播會議物件設定和取得 ( [**多播 \_ 回送 \_ 模式**](multicast-loopback-mode.md)) 的回送模式。</span><span class="sxs-lookup"><span data-stu-id="dcd8b-113">Allows an application to set and get the loopback mode ( [**MULTICAST\_LOOPBACK\_MODE**](multicast-loopback-mode.md)) for a multicast conference object.</span></span> |
| [<span data-ttu-id="dcd8b-114">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="dcd8b-114">**ITParticipant**</span></span>](itparticipant.md)               | <span data-ttu-id="dcd8b-115">允許應用程式抓取會議參與者的資訊，以及取得與這些參與者相關聯之資料流程的指標。</span><span class="sxs-lookup"><span data-stu-id="dcd8b-115">Allows an application to retrieve information on conference participants, and get pointers to the streams associated with those participants.</span></span>             |
| [<span data-ttu-id="dcd8b-116">**ITParticipantControl**</span><span class="sxs-lookup"><span data-stu-id="dcd8b-116">**ITParticipantControl**</span></span>](itparticipantcontrol.md) | <span data-ttu-id="dcd8b-117">允許應用程式取得會議中參與者的指標。</span><span class="sxs-lookup"><span data-stu-id="dcd8b-117">Allows an application to retrieve pointers to the participants in a conference.</span></span>                                                                           |
| [<span data-ttu-id="dcd8b-118">**ITParticipantEvent**</span><span class="sxs-lookup"><span data-stu-id="dcd8b-118">**ITParticipantEvent**</span></span>](itparticipantevent.md)     | <span data-ttu-id="dcd8b-119">允許應用程式抓取有關會議參與者的事件資訊。</span><span class="sxs-lookup"><span data-stu-id="dcd8b-119">Allows an application to retrieve event information concerning a conference participant.</span></span>                                                                  |
| [<span data-ttu-id="dcd8b-120">**IEnumParticipant**</span><span class="sxs-lookup"><span data-stu-id="dcd8b-120">**IEnumParticipant**</span></span>](ienumparticipant.md)         | <span data-ttu-id="dcd8b-121">列舉 [**ITParticipant**](itparticipant.md)。</span><span class="sxs-lookup"><span data-stu-id="dcd8b-121">Enumerates [**ITParticipant**](itparticipant.md).</span></span>                                                                                                        |



 

 

 



