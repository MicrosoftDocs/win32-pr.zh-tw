---
description: 這四個 NPP 介面的捕獲程式都相同。
ms.assetid: f778aba5-8f66-4fc9-830b-f830c364da56
title: 捕獲進程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0ca1987266b7e042713f1d1c292cf63d5e3ccf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570988"
---
# <a name="the-capture-process"></a><span data-ttu-id="9788b-103">捕獲進程</span><span class="sxs-lookup"><span data-stu-id="9788b-103">The Capture Process</span></span>

<span data-ttu-id="9788b-104">這四個 NPP 介面的捕獲程式都相同。</span><span class="sxs-lookup"><span data-stu-id="9788b-104">The capture process is the same for each of the four NPP interfaces.</span></span> <span data-ttu-id="9788b-105">在每個案例中，處理常式包括：</span><span class="sxs-lookup"><span data-stu-id="9788b-105">In each case, the process includes:</span></span>

-   <span data-ttu-id="9788b-106">取得要使用的 NPP 介面物件</span><span class="sxs-lookup"><span data-stu-id="9788b-106">Obtaining the NPP interface object to use</span></span>
-   <span data-ttu-id="9788b-107">連接到網路</span><span class="sxs-lookup"><span data-stu-id="9788b-107">Connecting to the network</span></span>
-   <span data-ttu-id="9788b-108">啟動並停止 [*捕獲*](c.md)</span><span class="sxs-lookup"><span data-stu-id="9788b-108">Starting and then stopping the [*capture*](c.md)</span></span>
-   <span data-ttu-id="9788b-109">中斷與網路的連線</span><span class="sxs-lookup"><span data-stu-id="9788b-109">Disconnecting from the network</span></span>

> [!Note]  
> <span data-ttu-id="9788b-110">當您取得所需的介面物件時，請確定您只呼叫該介面中包含的方法。</span><span class="sxs-lookup"><span data-stu-id="9788b-110">When you obtain the interface object that you want, ensure you call only the methods included in that interface.</span></span> <span data-ttu-id="9788b-111">下圖顯示每個介面都提供類似的方法來捕捉網路資料。</span><span class="sxs-lookup"><span data-stu-id="9788b-111">The following illustration shows each interface provides similar methods for capturing network data.</span></span> <span data-ttu-id="9788b-112">如果您使用一個介面連接到網路，然後嘗試使用其他介面中的方法來執行捕捉，則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="9788b-112">An error is returned if you connect to the network with one interface and then try to run a capture using the methods from another interface.</span></span>

 

<span data-ttu-id="9788b-113">下圖顯示兩個您可以執行捕捉的不同方式。</span><span class="sxs-lookup"><span data-stu-id="9788b-113">The following illustrations show two different ways you could run a capture.</span></span> <span data-ttu-id="9788b-114">第一個圖例顯示如何執行一或多個連續的捕獲，讓您可以建立任意數目的獨立捕獲。</span><span class="sxs-lookup"><span data-stu-id="9788b-114">The first illustration shows how to run one or more sequential captures, allowing you to create any number of independent captures.</span></span>

![連續捕捉](images/capt1.png)

<span data-ttu-id="9788b-116">如上所示，在連線到網路之後，您可以視需要多次啟動和停止 capture，啟動新的捕獲，並在每次重新開機捕獲時產生新的統計資料。</span><span class="sxs-lookup"><span data-stu-id="9788b-116">As shown above, after you connect to the network you can start and stop a capture as many times as you wish, starting a new capture and generating new statistics every time you restart the capture.</span></span> <span data-ttu-id="9788b-117">例如，針對使用 [**IDelaydC**](idelaydc.md) 介面的延遲捕捉，每次您重新開機捕獲時，就會建立新的 [*capture*](c.md) 檔。</span><span class="sxs-lookup"><span data-stu-id="9788b-117">For example, for a delayed capture using the [**IDelaydC**](idelaydc.md) interface, a new [*capture file*](c.md) would be created each time you restarted the capture.</span></span>

<span data-ttu-id="9788b-118">不過，也請注意，每次您重新開機 capture 程式時，都必須呼叫適當的 configure 方法來重新設定連接。</span><span class="sxs-lookup"><span data-stu-id="9788b-118">However, also be aware that every time you restart the capture process you must call the appropriate configure method to reconfigure the connection.</span></span> <span data-ttu-id="9788b-119">針對開始捕獲的初始呼叫，連接是透過連接到網路的呼叫來設定。</span><span class="sxs-lookup"><span data-stu-id="9788b-119">For the initial call to start the capture, the connection is configured by the call to connect to the network.</span></span>

<span data-ttu-id="9788b-120">第二個圖例顯示如何藉由暫停和重新開機來執行單一捕獲。</span><span class="sxs-lookup"><span data-stu-id="9788b-120">The second illustration shows how you could run a single capture by pausing and restarting.</span></span>

![藉由暫停和重新開機來進行單一捕獲](images/capt2.png)

<span data-ttu-id="9788b-122">在此情況下，您可以依需要暫停和重新開機 capture。</span><span class="sxs-lookup"><span data-stu-id="9788b-122">In this case, you can pause and restart a capture as many times as you want.</span></span> <span data-ttu-id="9788b-123">使用這個方法時，您可以執行資料 (的捕獲，並將其相關的統計資料) 記錄為單一捕獲。</span><span class="sxs-lookup"><span data-stu-id="9788b-123">With this approach, you can run a capture whose data (and its related statistics) are recorded as a single capture.</span></span> <span data-ttu-id="9788b-124">例如，若要使用 [**IDelaydC**](idelaydc.md) 介面執行延遲的捕獲，所有捕獲的網路資訊都會儲存在單一的 [*捕獲*](c.md)檔案中。</span><span class="sxs-lookup"><span data-stu-id="9788b-124">For example, to perform a delayed capture using the [**IDelaydC**](idelaydc.md) interface, all the captured network information would be saved in a single [*capture file*](c.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9788b-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="9788b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9788b-126">**CreateNPPInterface**</span><span class="sxs-lookup"><span data-stu-id="9788b-126">**CreateNPPInterface**</span></span>](createnppinterface.md)
</dt> <dt>

[<span data-ttu-id="9788b-127">**IDelaydC：： Configure**</span><span class="sxs-lookup"><span data-stu-id="9788b-127">**IDelaydC::Configure**</span></span>](idelaydc-configure.md)
</dt> <dt>

[<span data-ttu-id="9788b-128">**IDelaydC：： Connect**</span><span class="sxs-lookup"><span data-stu-id="9788b-128">**IDelaydC::Connect**</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="9788b-129">**IDelaydC：:D isconnect**</span><span class="sxs-lookup"><span data-stu-id="9788b-129">**IDelaydC::Disconnect**</span></span>](idelaydc-disconnect.md)
</dt> <dt>

[<span data-ttu-id="9788b-130">**IDelaydC：:P ause**</span><span class="sxs-lookup"><span data-stu-id="9788b-130">**IDelaydC::Pause**</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="9788b-131">**IDelaydC：： Resume**</span><span class="sxs-lookup"><span data-stu-id="9788b-131">**IDelaydC::Resume**</span></span>](idelaydc-resume.md)
</dt> <dt>

[<span data-ttu-id="9788b-132">**IDelaydC：： Start**</span><span class="sxs-lookup"><span data-stu-id="9788b-132">**IDelaydC::Start**</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="9788b-133">**IDelaydC：： Stop**</span><span class="sxs-lookup"><span data-stu-id="9788b-133">**IDelaydC::Stop**</span></span>](idelaydc-stop.md)
</dt> <dt>

[<span data-ttu-id="9788b-134">**IESP：： Configure**</span><span class="sxs-lookup"><span data-stu-id="9788b-134">**IESP::Configure**</span></span>](iesp-configure.md)
</dt> <dt>

[<span data-ttu-id="9788b-135">**IESP：： Connect**</span><span class="sxs-lookup"><span data-stu-id="9788b-135">**IESP::Connect**</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="9788b-136">**IESP：:D isconnect**</span><span class="sxs-lookup"><span data-stu-id="9788b-136">**IESP::Disconnect**</span></span>](iesp-disconnect.md)
</dt> <dt>

[<span data-ttu-id="9788b-137">**IESP：:P ause**</span><span class="sxs-lookup"><span data-stu-id="9788b-137">**IESP::Pause**</span></span>](iesp-pause.md)
</dt> <dt>

[<span data-ttu-id="9788b-138">**IESP：： Resume**</span><span class="sxs-lookup"><span data-stu-id="9788b-138">**IESP::Resume**</span></span>](iesp-resume.md)
</dt> <dt>

[<span data-ttu-id="9788b-139">**IESP：： Start**</span><span class="sxs-lookup"><span data-stu-id="9788b-139">**IESP::Start**</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="9788b-140">**IESP：： Stop**</span><span class="sxs-lookup"><span data-stu-id="9788b-140">**IESP::Stop**</span></span>](iesp-stop.md)
</dt> <dt>

[<span data-ttu-id="9788b-141">**IRTC：： Configure**</span><span class="sxs-lookup"><span data-stu-id="9788b-141">**IRTC::Configure**</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="9788b-142">**IRTC：： Connect**</span><span class="sxs-lookup"><span data-stu-id="9788b-142">**IRTC::Connect**</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="9788b-143">**IRTC：:D isconnect**</span><span class="sxs-lookup"><span data-stu-id="9788b-143">**IRTC::Disconnect**</span></span>](irtc-disconnect.md)
</dt> <dt>

[<span data-ttu-id="9788b-144">**IRTC：:P ause**</span><span class="sxs-lookup"><span data-stu-id="9788b-144">**IRTC::Pause**</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="9788b-145">**IRTC：： Resume**</span><span class="sxs-lookup"><span data-stu-id="9788b-145">**IRTC::Resume**</span></span>](irtc-resume.md)
</dt> <dt>

[<span data-ttu-id="9788b-146">**IRTC：： Start**</span><span class="sxs-lookup"><span data-stu-id="9788b-146">**IRTC::Start**</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="9788b-147">**IRTC：： Stop**</span><span class="sxs-lookup"><span data-stu-id="9788b-147">**IRTC::Stop**</span></span>](irtc-stop.md)
</dt> <dt>

[<span data-ttu-id="9788b-148">**IStats：： Configure**</span><span class="sxs-lookup"><span data-stu-id="9788b-148">**IStats::Configure**</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="9788b-149">**IStats：： Connect**</span><span class="sxs-lookup"><span data-stu-id="9788b-149">**IStats::Connect**</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="9788b-150">**IStats：:D isconnect**</span><span class="sxs-lookup"><span data-stu-id="9788b-150">**IStats::Disconnect**</span></span>](istats-disconnect.md)
</dt> <dt>

[<span data-ttu-id="9788b-151">**IStats：:P ause**</span><span class="sxs-lookup"><span data-stu-id="9788b-151">**IStats::Pause**</span></span>](istats-pause.md)
</dt> <dt>

[<span data-ttu-id="9788b-152">**IStats：： Resume**</span><span class="sxs-lookup"><span data-stu-id="9788b-152">**IStats::Resume**</span></span>](istats-resume.md)
</dt> <dt>

[<span data-ttu-id="9788b-153">**IStats：： Start**</span><span class="sxs-lookup"><span data-stu-id="9788b-153">**IStats::Start**</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="9788b-154">**IStats：： Stop**</span><span class="sxs-lookup"><span data-stu-id="9788b-154">**IStats::Stop**</span></span>](istats-stop.md)
</dt> </dl>

 

 



