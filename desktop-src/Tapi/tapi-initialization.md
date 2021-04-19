---
description: TAPI 元件的正常運作需要在電腦上設定通訊環境。
ms.assetid: 3df3d974-629e-4d78-b97d-b8121b185309
title: TAPI 初始化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 973d67931fb9f33751fedc638ab77021d3d3d34c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979323"
---
# <a name="tapi-initialization"></a><span data-ttu-id="d5a85-103">TAPI 初始化</span><span class="sxs-lookup"><span data-stu-id="d5a85-103">TAPI Initialization</span></span>

<span data-ttu-id="d5a85-104">TAPI 元件的正常運作需要在電腦上設定通訊環境，如下所示：</span><span class="sxs-lookup"><span data-stu-id="d5a85-104">Proper functioning of TAPI components requires setting up the communications environment on a computer as follows:</span></span>

-   <span data-ttu-id="d5a85-105">第一次將軟體或硬體新增至電腦時，會執行[安裝](installation.md)。</span><span class="sxs-lookup"><span data-stu-id="d5a85-105">[Installation](installation.md) is performed when software or hardware is first added to the computer.</span></span> <span data-ttu-id="d5a85-106">詳細的程式取決於作業系統和軟體本身。</span><span class="sxs-lookup"><span data-stu-id="d5a85-106">Detailed procedures depend on the operating system and the software itself.</span></span>
-   <span data-ttu-id="d5a85-107">[主要初始化](primary-initialization.md) 會建立物件和通訊路徑。</span><span class="sxs-lookup"><span data-stu-id="d5a85-107">[Primary initialization](primary-initialization.md) creates the objects and communication paths.</span></span>
-   <span data-ttu-id="d5a85-108">[版本協商](version-negotiation.md) 可確保 TAPI 元件可以交換資料。</span><span class="sxs-lookup"><span data-stu-id="d5a85-108">[Version negotiation](version-negotiation.md) ensures that TAPI components will be able to exchange data.</span></span>
-   <span data-ttu-id="d5a85-109">[資源清查](resource-inventory.md) 會抓取可供 TAPI 應用程式使用之裝置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d5a85-109">[Resource inventory](resource-inventory.md) retrieves information concerning devices available for use by a TAPI application.</span></span>
-   <span data-ttu-id="d5a85-110">[事件通知](event-notification.md) 會指定 TAPI 和服務提供者如何將非同步作業結果和狀態變更資訊傳遞給應用程式。</span><span class="sxs-lookup"><span data-stu-id="d5a85-110">[Event notification](event-notification.md) specifies how TAPI and the service providers pass asynchronous operation results and state change information to the application.</span></span>

## <a name="summary-of-related-reference-pages"></a><span data-ttu-id="d5a85-111">相關參考頁面的摘要</span><span class="sxs-lookup"><span data-stu-id="d5a85-111">Summary of Related Reference Pages</span></span>



| <span data-ttu-id="d5a85-112">TAPI 2.x 函數</span><span class="sxs-lookup"><span data-stu-id="d5a85-112">TAPI 2.x functions</span></span>                                        | <span data-ttu-id="d5a85-113">Description</span><span class="sxs-lookup"><span data-stu-id="d5a85-113">Description</span></span>                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5a85-114">**lineInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="d5a85-114">**lineInitializeEx**</span></span>](/windows/win32/api/tapi/nf-tapi-lineinitializeexa)     | <span data-ttu-id="d5a85-115">設定電話語音環境，傳回應用程式控制碼和裝置計數。</span><span class="sxs-lookup"><span data-stu-id="d5a85-115">Sets up the telephony environment, returns application handle and device count.</span></span>                                                   |
| [<span data-ttu-id="d5a85-116">**lineGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="d5a85-116">**lineGetDevCaps**</span></span>](/windows/win32/api/tapi/nf-tapi-linegetdevcaps)         | <span data-ttu-id="d5a85-117">取得支援的裝置功能，例如 TAPI 版本或媒體類型。</span><span class="sxs-lookup"><span data-stu-id="d5a85-117">Gets device capabilities, such as TAPI version or media types supported.</span></span>                                                          |
| [<span data-ttu-id="d5a85-118">**lineGetAddressCaps**</span><span class="sxs-lookup"><span data-stu-id="d5a85-118">**lineGetAddressCaps**</span></span>](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) | <span data-ttu-id="d5a85-119">取得位址功能，例如是否支援呼叫公園。</span><span class="sxs-lookup"><span data-stu-id="d5a85-119">Gets address capabilities, such as whether call park is supported.</span></span>                                                                |
| [<span data-ttu-id="d5a85-120">**lineOpen**</span><span class="sxs-lookup"><span data-stu-id="d5a85-120">**lineOpen**</span></span>](/windows/win32/api/tapi/nf-tapi-lineopen)                     | <span data-ttu-id="d5a85-121">通知 TAPI 應用程式將會使用這一行，並以何種方式使用。</span><span class="sxs-lookup"><span data-stu-id="d5a85-121">Notifies TAPI that the application will be using the line, and in what way.</span></span>                                                       |
| [<span data-ttu-id="d5a85-122">**lineGetMessage**</span><span class="sxs-lookup"><span data-stu-id="d5a85-122">**lineGetMessage**</span></span>](/windows/win32/api/tapi/nf-tapi-linegetmessage)         | <span data-ttu-id="d5a85-123">傳回已排入佇列的下一個 TAPI 訊息，以傳遞至使用事件處理常式通知機制的應用程式</span><span class="sxs-lookup"><span data-stu-id="d5a85-123">Returns the next TAPI message that is queued for delivery to an application that is using the Event Handle notification mechanism</span></span> |



 



| <span data-ttu-id="d5a85-124">TAPI 3.x 介面或方法</span><span class="sxs-lookup"><span data-stu-id="d5a85-124">TAPI 3.x interfaces or methods</span></span>                                                | <span data-ttu-id="d5a85-125">Description</span><span class="sxs-lookup"><span data-stu-id="d5a85-125">Description</span></span>                                                                                                                                |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5a85-126">**ITTAPI：： Initialize**</span><span class="sxs-lookup"><span data-stu-id="d5a85-126">**ITTAPI::Initialize**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize)                               | <span data-ttu-id="d5a85-127">設定電話語音環境。</span><span class="sxs-lookup"><span data-stu-id="d5a85-127">Sets up telephony environment.</span></span>                                                                                                             |
| [<span data-ttu-id="d5a85-128">**ITTAPI::EnumerateAddresses**</span><span class="sxs-lookup"><span data-stu-id="d5a85-128">**ITTAPI::EnumerateAddresses**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses)               | <span data-ttu-id="d5a85-129">列舉目前可用的位址。</span><span class="sxs-lookup"><span data-stu-id="d5a85-129">Enumerates addresses currently available.</span></span>                                                                                                  |
| [<span data-ttu-id="d5a85-130">**ITTAPI：： get \_ 位址**</span><span class="sxs-lookup"><span data-stu-id="d5a85-130">**ITTAPI::get\_Addresses**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses)                        | <span data-ttu-id="d5a85-131">建立目前可用的位址集合。</span><span class="sxs-lookup"><span data-stu-id="d5a85-131">Creates a collection of addresses currently available.</span></span> <span data-ttu-id="d5a85-132">提供給 Automation 用戶端應用程式，例如以 Visual Basic 撰寫的應用程式。</span><span class="sxs-lookup"><span data-stu-id="d5a85-132">Provided for Automation client applications, such as those written in Visual Basic.</span></span> |
| [<span data-ttu-id="d5a85-133">**ITTAPIEventNotification：： Event**</span><span class="sxs-lookup"><span data-stu-id="d5a85-133">**ITTAPIEventNotification::Event**</span></span>](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)       | <span data-ttu-id="d5a85-134">判斷非同步事件通知的回應。</span><span class="sxs-lookup"><span data-stu-id="d5a85-134">Determines response to an asynchronous event notification.</span></span> <span data-ttu-id="d5a85-135">由 TAPI 叫用的應用程式所執行。</span><span class="sxs-lookup"><span data-stu-id="d5a85-135">Implemented by the application, invoked by TAPI.</span></span>                                |
| [<span data-ttu-id="d5a85-136">**ITTAPI：:p 的 \_ >eventfilter**</span><span class="sxs-lookup"><span data-stu-id="d5a85-136">**ITTAPI::put\_EventFilter**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter)                    | <span data-ttu-id="d5a85-137">設定事件篩選器遮罩，以通知 TAPI 應用程式所需的事件。</span><span class="sxs-lookup"><span data-stu-id="d5a85-137">Sets the event filter mask, which notifies TAPI which events the application requires.</span></span>                                                     |
| [<span data-ttu-id="d5a85-138">**ITTAPI::RegisterCallNotifications**</span><span class="sxs-lookup"><span data-stu-id="d5a85-138">**ITTAPI::RegisterCallNotifications**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) | <span data-ttu-id="d5a85-139">指示 TAPI 針對指定的位址和一組媒體類型傳遞應用程式傳入會話。</span><span class="sxs-lookup"><span data-stu-id="d5a85-139">Instructs TAPI to pass the application incoming sessions for a specified address and set of media types.</span></span>                                   |
| [<span data-ttu-id="d5a85-140">**ITMediaSupport**</span><span class="sxs-lookup"><span data-stu-id="d5a85-140">**ITMediaSupport**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)                                      | <span data-ttu-id="d5a85-141">允許應用程式探索位址的媒體支援功能。</span><span class="sxs-lookup"><span data-stu-id="d5a85-141">Allows an application to discover the media support capabilities for an address.</span></span>                                                           |



 

 

 
