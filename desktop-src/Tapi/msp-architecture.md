---
description: 在 TAPI 架構中，所有 Tsp 都是在 TAPISRV 的內容中執行，這會在 SVCHOST 中實作為服務進程。
ms.assetid: f47662f9-2fca-4044-ab26-617e5b1f9eae
title: MSP 架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8c1229ddce90f79c122c47572b4567d230b0b4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386062"
---
# <a name="msp-architecture"></a><span data-ttu-id="6b608-103">MSP 架構</span><span class="sxs-lookup"><span data-stu-id="6b608-103">MSP Architecture</span></span>

<span data-ttu-id="6b608-104">在 TAPI 架構中，所有 Tsp 都是在 TAPISRV 的內容中執行，這會在 SVCHOST 中實作為服務進程。</span><span class="sxs-lookup"><span data-stu-id="6b608-104">In TAPI architecture, all TSPs are run in the context of TAPISRV, which is implemented as a service process within SVCHOST.</span></span> <span data-ttu-id="6b608-105">TAPI 應用程式會在自己的進程中存留。</span><span class="sxs-lookup"><span data-stu-id="6b608-105">TAPI applications live in their own process.</span></span> <span data-ttu-id="6b608-106">TAPI 應用程式會將 Tapi3.dll 以及任何所需的 Msp 載入其本身的進程，而 TAPI DLL 會透過私用 RPC 介面與 TAPISRV 通訊。</span><span class="sxs-lookup"><span data-stu-id="6b608-106">TAPI applications load Tapi3.dll and any needed MSPs into their own process, and the TAPI DLL communicates with TAPISRV through a private RPC interface.</span></span> <span data-ttu-id="6b608-107">下圖說明這些元件的互動。</span><span class="sxs-lookup"><span data-stu-id="6b608-107">The following diagram illustrates the interaction of these components.</span></span>

![tapisrv、tapi 應用程式與 msp 之間的互動](images/tsp-msp1.png)

<span data-ttu-id="6b608-109"> (MSP 的媒體服務提供者) 使用終端機、串流和子串流的抽象概念來提供媒體串流處理。</span><span class="sxs-lookup"><span data-stu-id="6b608-109">A media service provider (MSP) provides media streaming using the abstractions of Terminals, Streams, and SubStreams.</span></span>

<span data-ttu-id="6b608-110">終端機是媒體串流的接收或來源。</span><span class="sxs-lookup"><span data-stu-id="6b608-110">A Terminal is a sink or source for a media stream.</span></span> <span data-ttu-id="6b608-111">它可能是實體物件，例如喇叭或麥克風，也可能是裝置的抽象類別，例如影片視窗。</span><span class="sxs-lookup"><span data-stu-id="6b608-111">It may be a physical object, such as a speaker or a microphone, or it may be an abstraction of a device, such as a video window.</span></span> <span data-ttu-id="6b608-112">[Terminal 物件](terminal-object.md)會公開 [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)介面。</span><span class="sxs-lookup"><span data-stu-id="6b608-112">The [Terminal Object](terminal-object.md) exposes the [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface.</span></span> <span data-ttu-id="6b608-113">終端機 [**類別**](terminal-class.md) GUID 描述終端機類別。</span><span class="sxs-lookup"><span data-stu-id="6b608-113">The class of terminal is described by the [**Terminal Class**](terminal-class.md) GUID.</span></span> <span data-ttu-id="6b608-114">MSP 可能會定義自己的終端機類別。</span><span class="sxs-lookup"><span data-stu-id="6b608-114">An MSP may define its own terminal classes.</span></span>

<span data-ttu-id="6b608-115">資料流程會根據媒體 [**類型**](tapimediatype--constants.md) 或類型、資料流程的 [**方向**](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction)和媒體的目的地位址來分割通話的媒體。</span><span class="sxs-lookup"><span data-stu-id="6b608-115">Streams divide the media of a call based on the [**media type**](tapimediatype--constants.md) or type, the stream's [**direction**](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction), and the destination address of the media.</span></span> <span data-ttu-id="6b608-116">例如，來自數據機的連入音訊串流是串流物件、連至 IP 位址的輸出影片串流，以及埠是資料流程物件，來自 IP 多播群組的影片串流也會被視為一個資料流程物件。</span><span class="sxs-lookup"><span data-stu-id="6b608-116">For example, an incoming audio stream from a modem is a stream object, an outgoing video stream to an IP address and port is a stream object, the video streams coming from a IP multicast group are also considered as one stream object.</span></span> <span data-ttu-id="6b608-117">資料流程物件是以 [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) 介面表示。</span><span class="sxs-lookup"><span data-stu-id="6b608-117">The Stream object is represented by the [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) interface.</span></span>

<span data-ttu-id="6b608-118">子串流可讓您更精確地控制媒體。</span><span class="sxs-lookup"><span data-stu-id="6b608-118">SubStreams allow finer control over the media.</span></span> <span data-ttu-id="6b608-119">例如，在 IP 多播案例中，內送的影片資料流程物件可能代表數個人員。</span><span class="sxs-lookup"><span data-stu-id="6b608-119">For example, in the IP multicast case, the incoming video stream object might represent several people.</span></span> <span data-ttu-id="6b608-120">應用程式很可能會希望每個參與者都有個別的轉譯器。</span><span class="sxs-lookup"><span data-stu-id="6b608-120">The application will most likely want each participant to have a separate renderer.</span></span> <span data-ttu-id="6b608-121">傳入的影片串流可以分成數個子串流，每個人一個。</span><span class="sxs-lookup"><span data-stu-id="6b608-121">The incoming video stream can be divided into several substreams, one for each person.</span></span> <span data-ttu-id="6b608-122">一個子串流會對應到一個人，並且可以個別設定和控制。</span><span class="sxs-lookup"><span data-stu-id="6b608-122">One substream would correspond to one person, and can be configured and controlled separately.</span></span> <span data-ttu-id="6b608-123">子流物件是以 [**ITSubStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstreamcontrol) 介面表示。</span><span class="sxs-lookup"><span data-stu-id="6b608-123">The SubStream object is represented by the [**ITSubStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstreamcontrol) interface.</span></span>

<span data-ttu-id="6b608-124">當應用程式呼叫 [**ITAddress：： CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall) 來設定呼叫時，必須指定所需的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6b608-124">When an application calls [**ITAddress::CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall) to set up a call, it must specify the type of media required.</span></span> <span data-ttu-id="6b608-125">在撥打電話時，它只會在呼叫建立時告訴 TAPI。</span><span class="sxs-lookup"><span data-stu-id="6b608-125">On an outgoing call, it simply tells TAPI when the call is created.</span></span> <span data-ttu-id="6b608-126">例如：</span><span class="sxs-lookup"><span data-stu-id="6b608-126">For example:</span></span>

``` syntax
HRESULT hr = pAddress->CreateCall( 
       pszDestAddress, 
       lAddressType, 
       TAPIMEDIATYPE_AUDIO | TAPIMEDIATYPE_VIDEO, 
       &pCall 
       ); 
// If (hr != S_OK ) process the error here
```

<span data-ttu-id="6b608-127">在此情況下，應用程式會建立外寄音訊視頻通話。</span><span class="sxs-lookup"><span data-stu-id="6b608-127">In this case, the application is creating an outgoing audio-video call.</span></span>

<span data-ttu-id="6b608-128">傳入的媒體類型表示應用程式在呼叫的存留期內有興趣的媒體。</span><span class="sxs-lookup"><span data-stu-id="6b608-128">The media types passed in indicate the media that the application is interested in over the lifetime of the call.</span></span> <span data-ttu-id="6b608-129">例如，應用程式可能會在建立通話時指定音訊和影片，但一開始只選取音訊端子。</span><span class="sxs-lookup"><span data-stu-id="6b608-129">For example, the application may specify audio and video when creating the call, but select only audio terminals at the beginning.</span></span> <span data-ttu-id="6b608-130">MSP 只會開始串流音訊，但不會拒絕稍後在呼叫的存留期內進行的本機或遠端影片要求。</span><span class="sxs-lookup"><span data-stu-id="6b608-130">The MSP will start streaming only audio, but will not reject a local or remote video request made later in the lifetime of the call.</span></span>

<span data-ttu-id="6b608-131">當應用程式接著呼叫 [**ITBasicCallControl：： Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect)時，TAPI 3 會呼叫 TSP 中的 [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) 。</span><span class="sxs-lookup"><span data-stu-id="6b608-131">When the application then calls [**ITBasicCallControl::Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect), TAPI 3 calls [**TSPI\_lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) in the TSP.</span></span> <span data-ttu-id="6b608-132">在建立通話之後，MSP 和 TSP 可以視需要進行通訊。</span><span class="sxs-lookup"><span data-stu-id="6b608-132">After a call is established, the MSP and TSP can communicate as necessary.</span></span>

<span data-ttu-id="6b608-133">當通話中斷時，就會由 MSP 和 TSP 來傳達中斷通話的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6b608-133">When a call is disconnecting, it is up to the MSP and TSP to communicate about tearing down the call.</span></span> <span data-ttu-id="6b608-134">如果應用程式呼叫 [**中斷連接**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect)，Tapi3.dll 會呼叫 [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) 。</span><span class="sxs-lookup"><span data-stu-id="6b608-134">Tapi3.dll will call [**TSPI\_lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) if the application calls [**Disconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).</span></span>

 

 
