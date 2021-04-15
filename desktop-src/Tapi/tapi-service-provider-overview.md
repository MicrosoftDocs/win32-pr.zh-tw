---
description: TAPI 應用程式位於自己的進程空間中。
ms.assetid: 57dedad1-7264-48fc-9ac2-c6c72f7fee27
title: TAPI 服務提供者總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e847ed49879e9ff55662477a762fa7297443d12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104554298"
---
# <a name="tapi-service-provider-overview"></a><span data-ttu-id="89ec0-103">TAPI 服務提供者總覽</span><span class="sxs-lookup"><span data-stu-id="89ec0-103">TAPI Service Provider Overview</span></span>

<span data-ttu-id="89ec0-104">TAPI 應用程式位於自己的進程空間中。</span><span class="sxs-lookup"><span data-stu-id="89ec0-104">TAPI applications reside in their own process space.</span></span> <span data-ttu-id="89ec0-105">TAPI 應用程式會載入 Tapi32.dll 或 Tapi3.dll 至其進程，而 TAPI 會透過私用 RPC 介面與 TAPISRV 通訊。</span><span class="sxs-lookup"><span data-stu-id="89ec0-105">TAPI applications load the Tapi32.dll or Tapi3.dll into their process, and TAPI communicates with TAPISRV through a private RPC interface.</span></span> <span data-ttu-id="89ec0-106">TSP 會在 TAPISRV 的內容中執行。</span><span class="sxs-lookup"><span data-stu-id="89ec0-106">A TSP runs in the context of TAPISRV.</span></span> <span data-ttu-id="89ec0-107">給定的 TSP 可能位於使用者電腦以外的電腦上，並使用遠端 TSP 存取。</span><span class="sxs-lookup"><span data-stu-id="89ec0-107">A given TSP may reside on a machine other than the user's machine and is accessed using a remote TSP.</span></span> <span data-ttu-id="89ec0-108">TAPISRV 會實作為 SVCHOST 內的服務進程。</span><span class="sxs-lookup"><span data-stu-id="89ec0-108">TAPISRV is implemented as a service process within SVCHOST.</span></span> <span data-ttu-id="89ec0-109">MSP 存在於應用程式的進程空間內，一律為本機。</span><span class="sxs-lookup"><span data-stu-id="89ec0-109">An MSP lives within the process space of the application and is always local.</span></span>

<span data-ttu-id="89ec0-110">TSP/MSP 組可以視為具有虛擬私人通訊路徑。</span><span class="sxs-lookup"><span data-stu-id="89ec0-110">A TSP/MSP pair can be regarded as having a virtual private communication path.</span></span> <span data-ttu-id="89ec0-111">您可以使用不透明的緩衝區（不是由 TAPISRV 或 TAPI DLL 來解讀），在這兩者之間傳送資訊。</span><span class="sxs-lookup"><span data-stu-id="89ec0-111">Information can be sent between the two using opaque buffers that are not interpreted by either TAPISRV or the TAPI DLL.</span></span>

<span data-ttu-id="89ec0-112">某些服務提供者會執行涉及硬體的特定作業。</span><span class="sxs-lookup"><span data-stu-id="89ec0-112">Some service providers implement operations specific to the hardware involved.</span></span> <span data-ttu-id="89ec0-113">TAPI 2.x 提供透過 [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific) 或 [**phoneDevSpecific**](/windows/win32/api/tapi/nf-tapi-phonedevspecific) 函式存取這類作業的功能。</span><span class="sxs-lookup"><span data-stu-id="89ec0-113">TAPI 2.x provides access to such operations through the [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific) or [**phoneDevSpecific**](/windows/win32/api/tapi/nf-tapi-phonedevspecific) function.</span></span> <span data-ttu-id="89ec0-114">TAPI 3.x 會公開 [提供者特定的介面](./provider-specific-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="89ec0-114">TAPI 3.x exposes [provider-specific Interfaces](./provider-specific-interfaces.md).</span></span>

<span data-ttu-id="89ec0-115">下圖說明控制項和資訊的流程，其中顯示一部獨立的 TSP (Unimodem) 和一組 TSP/MSP 組 (h.) 。</span><span class="sxs-lookup"><span data-stu-id="89ec0-115">The following diagram illustrates the flow of controls and information, showing one stand-alone TSP (Unimodem) and one TSP/MSP pair (H.323).</span></span>

![獨立的 tsp 和成對的 tsp/msp 控制與資訊的流程](images/tsp-msp1.png)

<span data-ttu-id="89ec0-117">下圖說明包含 TSP 和 MSP 之來電的進度。</span><span class="sxs-lookup"><span data-stu-id="89ec0-117">The following diagram illustrates the progress of an incoming call that involves both a TSP and an MSP.</span></span>

![具有 tsp 和 msp 的撥入電話](images/tspmspin.png)

## <a name="incoming-call-setup"></a><span data-ttu-id="89ec0-119">撥入電話設定</span><span class="sxs-lookup"><span data-stu-id="89ec0-119">Incoming Call Setup</span></span>

-   <span data-ttu-id="89ec0-120">TSP 會將 [**一行 \_ NEWCALL**](line-newcall.md) 訊息傳送至 TAPISRV。</span><span class="sxs-lookup"><span data-stu-id="89ec0-120">The TSP sends a [**LINE\_NEWCALL**](line-newcall.md) message to TAPISRV.</span></span> <span data-ttu-id="89ec0-121">[**通話狀態**](./linecallstate--constants.md)為 LINECALLSTATE 供應專案 \_ 。</span><span class="sxs-lookup"><span data-stu-id="89ec0-121">The [**call state**](./linecallstate--constants.md) is LINECALLSTATE\_OFFERING.</span></span>
-   <span data-ttu-id="89ec0-122">TAPISRV 會通知用戶端呼叫。</span><span class="sxs-lookup"><span data-stu-id="89ec0-122">TAPISRV notifies clients of the call.</span></span>
-   <span data-ttu-id="89ec0-123">TAPI3 會建立 TAPI Call 物件，然後呼叫由 MSP 所執行的 [**ITMSPAddress：： CreateMSPCall**](/windows/win32/api/tapi3/nf-tapi3-itmspaddress-createmspcall)。</span><span class="sxs-lookup"><span data-stu-id="89ec0-123">TAPI3 creates the TAPI Call object, then calls [**ITMSPAddress::CreateMSPCall**](/windows/win32/api/tapi3/nf-tapi3-itmspaddress-createmspcall), which is implemented by the MSP.</span></span>
-   <span data-ttu-id="89ec0-124">MSP 會根據呼叫所需的 [**媒體類型**](./tapimediatype--constants.md) ，建立 msp 呼叫物件和預設串流。</span><span class="sxs-lookup"><span data-stu-id="89ec0-124">The MSP creates an MSP Call object and default streams based on the [**media types**](./tapimediatype--constants.md) required for the call.</span></span> <span data-ttu-id="89ec0-125">它會傳回 MSP 呼叫物件的 IUnknown 指標。</span><span class="sxs-lookup"><span data-stu-id="89ec0-125">It returns an IUnknown pointer to the MSP call object.</span></span>
-   <span data-ttu-id="89ec0-126">TAPI3 會將 MSP 呼叫物件匯總至 TAPI 呼叫物件，讓應用程式可以使用 [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) 等介面。</span><span class="sxs-lookup"><span data-stu-id="89ec0-126">TAPI3 aggregates the MSP Call object into the TAPI Call object, making interfaces such as [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) available to the application.</span></span> <span data-ttu-id="89ec0-127">然後，它會通知應用程式有新的呼叫。</span><span class="sxs-lookup"><span data-stu-id="89ec0-127">It then notifies the application of the new call.</span></span>

<span data-ttu-id="89ec0-128">然後，應用程式可以使用 [**ITStream：： SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) 等方法來完成通話完成的準備工作。</span><span class="sxs-lookup"><span data-stu-id="89ec0-128">The application may then use methods such as [**ITStream::SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) to complete preparations for call completion.</span></span>

## <a name="incoming-call-completion"></a><span data-ttu-id="89ec0-129">撥入電話完成</span><span class="sxs-lookup"><span data-stu-id="89ec0-129">Incoming Call Completion</span></span>

-   <span data-ttu-id="89ec0-130">應用程式會呼叫 [**ITBasicCallControl：：解答**](/windows/win32/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer)。</span><span class="sxs-lookup"><span data-stu-id="89ec0-130">The application calls [**ITBasicCallControl::Answer**](/windows/win32/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer).</span></span>
-   <span data-ttu-id="89ec0-131">TAPI3 呼叫 [**lineAnswer**](/windows/win32/api/tapi/nf-tapi-lineanswer)。</span><span class="sxs-lookup"><span data-stu-id="89ec0-131">TAPI3 calls [**lineAnswer**](/windows/win32/api/tapi/nf-tapi-lineanswer).</span></span>
-   <span data-ttu-id="89ec0-132">TAPISERV 會呼叫 [**TSPI \_ lineAnswer**](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer)。</span><span class="sxs-lookup"><span data-stu-id="89ec0-132">TAPISERV calls [**TSPI\_lineAnswer**](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer).</span></span>
-   <span data-ttu-id="89ec0-133">TSP 起始通話串流。</span><span class="sxs-lookup"><span data-stu-id="89ec0-133">The TSP initiates call streaming.</span></span> <span data-ttu-id="89ec0-134">通常，TSP 會將訊息傳送至對應的 MSP，而 MSP 會啟動串流。</span><span class="sxs-lookup"><span data-stu-id="89ec0-134">Usually, the TSP sends a message to the corresponding MSP, and the MSP starts the streams.</span></span> <span data-ttu-id="89ec0-135">在某些 TSP/MSP 實施中，TSP 會啟動串流。</span><span class="sxs-lookup"><span data-stu-id="89ec0-135">In some TSP/MSP implementations, the TSP starts the streams.</span></span>

## <a name="tspmsp-communication-during-call-progress"></a><span data-ttu-id="89ec0-136">通話過程中的 TSP/MSP 通訊</span><span class="sxs-lookup"><span data-stu-id="89ec0-136">TSP/MSP Communication During Call Progress</span></span>

<span data-ttu-id="89ec0-137">進行呼叫之後，TSP 和 MSP 會透過 TAPISRV 和 TAPI3 傳遞不透明的緩衝區來進行通訊。</span><span class="sxs-lookup"><span data-stu-id="89ec0-137">After the call is in progress, the TSP and the MSP communicate by passing opaque buffers through TAPISRV and TAPI3.</span></span>

-   <span data-ttu-id="89ec0-138">TSP 將 [**\_ SENDMSPDATA**](line-sendmspdata.md) 訊息傳送至 TAPISRV，以將資訊傳送至 MSP。</span><span class="sxs-lookup"><span data-stu-id="89ec0-138">The TSP sends information to the MSP by sending the [**LINE\_SENDMSPDATA**](line-sendmspdata.md) message to TAPISRV.</span></span>
-   <span data-ttu-id="89ec0-139">MSP 會透過 [**ITMSPAddress：： ReceiveTSPData**](/windows/win32/api/tapi3/nf-tapi3-itmspaddress-receivetspdata) 方法接收來自 TSP 的資訊。</span><span class="sxs-lookup"><span data-stu-id="89ec0-139">The MSP receives information from the TSP through the [**ITMSPAddress::ReceiveTSPData**](/windows/win32/api/tapi3/nf-tapi3-itmspaddress-receivetspdata) method.</span></span> <span data-ttu-id="89ec0-140">如果資料與 MSP 呼叫物件相關，則會以該方法的參數形式提供 MSP 呼叫物件的介面指標。</span><span class="sxs-lookup"><span data-stu-id="89ec0-140">If the data is related to a MSP call object, an interface pointer to the MSP call object is provided as a parameter of that method.</span></span>
-   <span data-ttu-id="89ec0-141">MSP 會將 MSP \_ TSP \_ 資料事件傳送到 TAPI 3，以將資訊傳送至 TSP。</span><span class="sxs-lookup"><span data-stu-id="89ec0-141">The MSP sends information to the TSP by sending a MSP\_TSP\_DATA event to TAPI 3.</span></span>
-   <span data-ttu-id="89ec0-142">TSP 會透過 [**TSPI \_ lineReceiveMSPData**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata) 函式接收來自 MSP 的資訊。</span><span class="sxs-lookup"><span data-stu-id="89ec0-142">The TSP receives information from the MSP through the [**TSPI\_lineReceiveMSPData**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata) function.</span></span>

<span data-ttu-id="89ec0-143">服務提供者之間的確切程式和通訊內容，是指定的 TSP/MSP 集合專屬的。</span><span class="sxs-lookup"><span data-stu-id="89ec0-143">The exact process and content of communication between service providers is specific to a given TSP/MSP set.</span></span>

> [!Note]  
> <span data-ttu-id="89ec0-144">對於外寄呼叫，MSP 通常會知道 TSP 之前的呼叫。</span><span class="sxs-lookup"><span data-stu-id="89ec0-144">For outgoing calls, the MSP typically knows about the call before the TSP.</span></span> <span data-ttu-id="89ec0-145">如果 MSP 嘗試在 TSP 告知來電之前與 TSP 進行通訊，則通訊會失敗。</span><span class="sxs-lookup"><span data-stu-id="89ec0-145">If the MSP tries to communicate with the TSP before the TSP is informed about a call, the communication will fail.</span></span> <span data-ttu-id="89ec0-146">當 MSP 和 TSP 需要交換有關特定通話的資訊時，TSP 應該起始通訊。</span><span class="sxs-lookup"><span data-stu-id="89ec0-146">When the MSP and the TSP need to exchange information concerning a specific call, the TSP should initiate communication.</span></span>

 

 

 
