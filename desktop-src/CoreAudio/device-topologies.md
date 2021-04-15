---
description: 裝置拓撲
ms.assetid: 5ac421e5-74a4-40e8-af6f-a99a05ebc3e0
title: 裝置拓撲
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31e0af267bb4a0fa924ee23d36a2a615ac5ae7fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510725"
---
# <a name="device-topologies"></a><span data-ttu-id="22945-103">裝置拓撲</span><span class="sxs-lookup"><span data-stu-id="22945-103">Device Topologies</span></span>

<span data-ttu-id="22945-104">[DEVICETOPOLOGY api](devicetopology-api.md)可讓用戶端控制無法透過[MMDevice api](mmdevice-api.md)、 [WASAPI](wasapi.md)或[EndpointVolume api](endpointvolume-api.md)存取的各種音訊配接器內部功能。</span><span class="sxs-lookup"><span data-stu-id="22945-104">The [DeviceTopology API](devicetopology-api.md) gives clients control over a variety of internal functions of audio adapters that they cannot access through the [MMDevice API](mmdevice-api.md), [WASAPI](wasapi.md), or the [EndpointVolume API](endpointvolume-api.md).</span></span>

<span data-ttu-id="22945-105">如先前所述， [MMDEVICE api](mmdevice-api.md)、 [WASAPI](wasapi.md)和 [EndpointVolume api](endpointvolume-api.md) 會將麥克風、喇叭、耳機和其他音訊輸入和輸出裝置呈現給用戶端作為 [音訊端點裝置](audio-endpoint-devices.md)。</span><span class="sxs-lookup"><span data-stu-id="22945-105">As explained previously, the [MMDevice API](mmdevice-api.md), [WASAPI](wasapi.md), and the [EndpointVolume API](endpointvolume-api.md) present microphones, speakers, headphones, and other audio input and output devices to clients as [audio endpoint devices](audio-endpoint-devices.md).</span></span> <span data-ttu-id="22945-106">端點裝置模型可讓用戶端方便存取音訊裝置中的音量和靜音控制項。</span><span class="sxs-lookup"><span data-stu-id="22945-106">The endpoint device model provides clients with convenient access to volume and mute controls in audio devices.</span></span> <span data-ttu-id="22945-107">只需要這些簡單控制項的用戶端可以避免將硬體裝置的內部拓撲用於音訊介面卡。</span><span class="sxs-lookup"><span data-stu-id="22945-107">Clients that require only these simple controls can avoid traversing the internal topologies of hardware devices in audio adapters.</span></span>

<span data-ttu-id="22945-108">在 Windows Vista 中，音訊引擎會自動設定音訊裝置的拓撲，以供音訊應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="22945-108">In Windows Vista, the audio engine automatically configures the topologies of audio devices for use by audio applications.</span></span> <span data-ttu-id="22945-109">因此，應用程式很少需要使用 DeviceTopology API 來達到此目的。</span><span class="sxs-lookup"><span data-stu-id="22945-109">Thus, applications rarely, if ever, need to use the DeviceTopology API for this purpose.</span></span> <span data-ttu-id="22945-110">例如，假設音訊介面卡包含可從線路輸入或麥克風捕捉串流的輸入多工器，但無法同時從兩個端點裝置捕獲資料流程。</span><span class="sxs-lookup"><span data-stu-id="22945-110">For example, assume that an audio adapter contains an input multiplexer that can capture a stream from either a line input or a microphone, but that cannot capture streams from both endpoint devices at the same time.</span></span> <span data-ttu-id="22945-111">假設使用者已啟用獨佔模式應用程式，以依照共用模式應用程式來搶先使用音訊端點裝置，如 [獨佔模式串流](exclusive-mode-streams.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="22945-111">Assume that the user has enabled exclusive-mode applications to preempt the use of an audio endpoint device by shared-mode applications, as described in [Exclusive-Mode Streams](exclusive-mode-streams.md).</span></span> <span data-ttu-id="22945-112">如果共用模式應用程式在獨佔模式應用程式開始從麥克風錄製串流時，從行輸入記錄資料流程，則音訊引擎會自動將多工器從線路輸入切換至麥克風。</span><span class="sxs-lookup"><span data-stu-id="22945-112">If a shared-mode application is recording a stream from the line input at the time that an exclusive-mode application begins recording a stream from the microphone, the audio engine automatically switches the multiplexer from the line input to the microphone.</span></span> <span data-ttu-id="22945-113">相反地，在舊版 Windows （包括 Windows XP）中，此範例中的獨佔模式應用程式會使用 Windows 多媒體應用程式開發介面中的 **mixerXxx** 函式來跨越介面卡裝置的拓撲、探索多工器，並設定多工器以選取麥克風輸入。</span><span class="sxs-lookup"><span data-stu-id="22945-113">In contrast, in earlier versions of Windows, including Windows XP, the exclusive-mode application in this example would use the **mixerXxx** functions in the Windows multimedia API to traverse the topologies of the adapter devices, discover the multiplexer, and configure the multiplexer to select the microphone input.</span></span> <span data-ttu-id="22945-114">在 Windows Vista 中，不再需要這些步驟。</span><span class="sxs-lookup"><span data-stu-id="22945-114">In Windows Vista, these steps are no longer required.</span></span>

<span data-ttu-id="22945-115">不過，某些用戶端可能需要明確控制無法透過 MMDevice API、WASAPI 或 EndpointVolume API 存取的音訊硬體控制項類型。</span><span class="sxs-lookup"><span data-stu-id="22945-115">However, some clients might require explicit control over types of audio hardware controls that cannot be accessed through the MMDevice API, WASAPI, or the EndpointVolume API.</span></span> <span data-ttu-id="22945-116">針對這些用戶端，DeviceTopology API 可讓您遍歷介面卡裝置的拓撲，以探索及管理裝置中的音訊控制項。</span><span class="sxs-lookup"><span data-stu-id="22945-116">For these clients, the DeviceTopology API provides the ability to traverse the topologies of adapter devices to discover and manage the audio controls in the devices.</span></span> <span data-ttu-id="22945-117">使用 DeviceTopology API 的應用程式必須謹慎設計，以避免干擾 Windows 音訊原則，並干擾與其他應用程式共用之音訊裝置的內部設定。</span><span class="sxs-lookup"><span data-stu-id="22945-117">Applications that use the DeviceTopology API must be designed with care to avoid interfering with Windows audio policy and disturbing the internal configurations of audio devices that are shared with other applications.</span></span> <span data-ttu-id="22945-118">如需 Windows 音訊原則的詳細資訊，請參閱 [使用者模式音訊元件](user-mode-audio-components.md)。</span><span class="sxs-lookup"><span data-stu-id="22945-118">For more information about Windows audio policy, see [User-Mode Audio Components](user-mode-audio-components.md).</span></span>

<span data-ttu-id="22945-119">DeviceTopology API 提供介面來探索和管理裝置拓撲中的下列音訊控制項類型：</span><span class="sxs-lookup"><span data-stu-id="22945-119">The DeviceTopology API provides interfaces for discovering and managing the following types of audio controls in a device topology:</span></span>

-   <span data-ttu-id="22945-120">自動增益控制</span><span class="sxs-lookup"><span data-stu-id="22945-120">Automatic gain control</span></span>
-   <span data-ttu-id="22945-121">低音控制</span><span class="sxs-lookup"><span data-stu-id="22945-121">Bass control</span></span>
-   <span data-ttu-id="22945-122">輸入選取器 (多工器) </span><span class="sxs-lookup"><span data-stu-id="22945-122">Input selector (multiplexer)</span></span>
-   <span data-ttu-id="22945-123">音量控制項</span><span class="sxs-lookup"><span data-stu-id="22945-123">Loudness control</span></span>
-   <span data-ttu-id="22945-124">中型控制項</span><span class="sxs-lookup"><span data-stu-id="22945-124">Midrange control</span></span>
-   <span data-ttu-id="22945-125">靜音控制</span><span class="sxs-lookup"><span data-stu-id="22945-125">Mute control</span></span>
-   <span data-ttu-id="22945-126">輸出選取器 (信號信號) </span><span class="sxs-lookup"><span data-stu-id="22945-126">Output selector (demultiplexer)</span></span>
-   <span data-ttu-id="22945-127">尖峰計量</span><span class="sxs-lookup"><span data-stu-id="22945-127">Peak meter</span></span>
-   <span data-ttu-id="22945-128">高音控制項</span><span class="sxs-lookup"><span data-stu-id="22945-128">Treble control</span></span>
-   <span data-ttu-id="22945-129">音量控制</span><span class="sxs-lookup"><span data-stu-id="22945-129">Volume control</span></span>

<span data-ttu-id="22945-130">此外，DeviceTopology API 可讓用戶端查詢介面卡裝置，以取得其所支援之串流格式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="22945-130">In addition, the DeviceTopology API enables clients to query adapter devices for information about the stream formats that they support.</span></span> <span data-ttu-id="22945-131">標頭檔 Devicetopology 會定義 DeviceTopology API 中的介面。</span><span class="sxs-lookup"><span data-stu-id="22945-131">The header file Devicetopology.h defines the interfaces in the DeviceTopology API.</span></span>

<span data-ttu-id="22945-132">下圖顯示 PCI 介面卡部分的數個連線裝置拓撲範例，可從麥克風、線路輸入和 CD 播放機捕獲音訊。</span><span class="sxs-lookup"><span data-stu-id="22945-132">The following diagram shows an example of several connected device topologies for the portion of a PCI adapter that captures audio from a microphone, line input, and CD player.</span></span>

![四個連線裝置拓撲的範例](images/fig2.jpg)

<span data-ttu-id="22945-134">上圖顯示從類比輸入到系統匯流排的資料路徑。</span><span class="sxs-lookup"><span data-stu-id="22945-134">The preceding diagram shows the data paths that lead from the analog inputs to the system bus.</span></span> <span data-ttu-id="22945-135">下列每個裝置都會以具有 [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) 介面的裝置拓撲物件表示：</span><span class="sxs-lookup"><span data-stu-id="22945-135">Each of the following devices is represented as a device-topology object with an [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) interface:</span></span>

-   <span data-ttu-id="22945-136">Wave capture 裝置</span><span class="sxs-lookup"><span data-stu-id="22945-136">Wave capture device</span></span>
-   <span data-ttu-id="22945-137">輸入多工器裝置</span><span class="sxs-lookup"><span data-stu-id="22945-137">Input multiplexer device</span></span>
-   <span data-ttu-id="22945-138">端點裝置 A</span><span class="sxs-lookup"><span data-stu-id="22945-138">Endpoint device A</span></span>
-   <span data-ttu-id="22945-139">端點裝置 B</span><span class="sxs-lookup"><span data-stu-id="22945-139">Endpoint device B</span></span>

<span data-ttu-id="22945-140">請注意，拓撲圖結合了介面卡裝置 (wave 捕捉和輸入多工器裝置) 與端點裝置。</span><span class="sxs-lookup"><span data-stu-id="22945-140">Note that the topology diagram combines adapter devices (the wave capture and input multiplexer devices) with endpoint devices.</span></span> <span data-ttu-id="22945-141">透過裝置之間的連線，音訊資料會從一部裝置傳遞到下一個裝置。</span><span class="sxs-lookup"><span data-stu-id="22945-141">Through the connections between devices, audio data passes from one device to the next.</span></span> <span data-ttu-id="22945-142">在連線的每一端都是連接器 (在圖表中標示為 Con，) 資料進入或離開裝置的位置。</span><span class="sxs-lookup"><span data-stu-id="22945-142">On each side of a connection is a connector (labeled Con in the diagram) through which data enters or leaves a device.</span></span>

<span data-ttu-id="22945-143">在圖表的左邊緣，線路輸入和麥克風插孔的信號會進入端點裝置。</span><span class="sxs-lookup"><span data-stu-id="22945-143">On the left edge of the diagram, signals from the line-input and microphone jacks enter the endpoint devices.</span></span>

<span data-ttu-id="22945-144">在 wave capture 裝置和輸入多工器裝置中，是串流處理函式，在 DeviceTopology API 的術語中，稱為次單元連接。</span><span class="sxs-lookup"><span data-stu-id="22945-144">Inside the wave capture device and input multiplexer device are stream-processing functions, which, in the terminology of the DeviceTopology API, are called subunits.</span></span> <span data-ttu-id="22945-145">上圖顯示下列類型的次單元連接：</span><span class="sxs-lookup"><span data-stu-id="22945-145">The following types of subunits appear in the preceding diagram:</span></span>

-   <span data-ttu-id="22945-146">磁片區控制 (標示的音量) </span><span class="sxs-lookup"><span data-stu-id="22945-146">Volume control (labeled Vol)</span></span>
-   <span data-ttu-id="22945-147">將控制項靜音 (標示為靜音) </span><span class="sxs-lookup"><span data-stu-id="22945-147">Mute control (labeled Mute)</span></span>
-   <span data-ttu-id="22945-148">多工器 (或輸入選取器;標記的 MUX) </span><span class="sxs-lookup"><span data-stu-id="22945-148">Multiplexer (or input selector; labeled MUX)</span></span>
-   <span data-ttu-id="22945-149">類比轉數位轉換器 (標示的 ADC) </span><span class="sxs-lookup"><span data-stu-id="22945-149">Analog-to-digital converter (labeled ADC)</span></span>

<span data-ttu-id="22945-150">[磁片區]、[靜音] 和 [多工器] 次單元連接中的設定可由用戶端控制，而 DeviceTopology API 則提供控制介面給用戶端來控制這些設定。</span><span class="sxs-lookup"><span data-stu-id="22945-150">The settings in the volume, mute, and multiplexer subunits can be controlled by clients, and the DeviceTopology API provides control interfaces to clients for controlling them.</span></span> <span data-ttu-id="22945-151">在此範例中，ADC 子單位沒有任何控制設定。</span><span class="sxs-lookup"><span data-stu-id="22945-151">In this example, the ADC subunit has no control settings.</span></span> <span data-ttu-id="22945-152">因此，DeviceTopology API 不會提供任何 ADC 的控制介面。</span><span class="sxs-lookup"><span data-stu-id="22945-152">Thus, the DeviceTopology API provides no control interface for the ADC.</span></span>

<span data-ttu-id="22945-153">在 DeviceTopology API 的術語中，連接器和次單元連接屬於相同的一般類別（部分）。</span><span class="sxs-lookup"><span data-stu-id="22945-153">In the terminology of the DeviceTopology API, connectors and subunits belong to the same general category—parts.</span></span> <span data-ttu-id="22945-154">無論是連接器或次單元連接，所有零件都能提供一組通用的函式。</span><span class="sxs-lookup"><span data-stu-id="22945-154">All parts, regardless of whether they are connectors or subunits, provide a common set of functions.</span></span> <span data-ttu-id="22945-155">DeviceTopology API 會執行 [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) 介面，以代表連接器和次單元連接通用的一般函數。</span><span class="sxs-lookup"><span data-stu-id="22945-155">The DeviceTopology API implements an [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) interface to represent the generic functions that are common to connectors and subunits.</span></span> <span data-ttu-id="22945-156">API 會執行 [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector) 和 [**ISubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit) 介面，以代表連接器和次單元連接的特定層面。</span><span class="sxs-lookup"><span data-stu-id="22945-156">The API implements the [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector) and [**ISubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit) interfaces to represent the specific aspects of connectors and subunits.</span></span>

<span data-ttu-id="22945-157">DeviceTopology API 會從核心串流處理 wave capture 裝置和輸入多工器裝置的拓朴 (KS) 篩選器，音訊驅動程式會將這些篩選器公開給作業系統來代表這些裝置。</span><span class="sxs-lookup"><span data-stu-id="22945-157">The DeviceTopology API constructs the topologies of the wave capture device and input multiplexer device from the kernel-streaming (KS) filters that the audio driver exposes to the operating system to represent these devices.</span></span> <span data-ttu-id="22945-158"> (音訊介面卡驅動程式會執行 **IMiniportWaveXxx** 和 **IMiniportTopology** 介面，以代表這些篩選器的硬體相依部分;如需這些介面和有關 KS 篩選器的詳細資訊，請參閱 Windows DDK 檔。 ) </span><span class="sxs-lookup"><span data-stu-id="22945-158">(The audio adapter driver implements **IMiniportWaveXxx** and **IMiniportTopology** interfaces to represent the hardware-dependent portions of these filters; for more information about these interfaces and about KS filters, see the Windows DDK documentation.)</span></span>

<span data-ttu-id="22945-159">DeviceTopology API 會在上圖中，建立代表端點裝置 A 和 B 的簡單拓撲。</span><span class="sxs-lookup"><span data-stu-id="22945-159">The DeviceTopology API constructs trivial topologies to represent endpoint devices A and B in the preceding diagram.</span></span> <span data-ttu-id="22945-160">端點裝置的裝置拓撲是由單一連接器所組成。</span><span class="sxs-lookup"><span data-stu-id="22945-160">The device topology of an endpoint device consists of a single connector.</span></span> <span data-ttu-id="22945-161">此拓撲只是端點裝置的預留位置，不包含處理音訊資料的次單元連接。</span><span class="sxs-lookup"><span data-stu-id="22945-161">This topology is merely a placeholder for the endpoint device and contains no subunits for processing audio data.</span></span> <span data-ttu-id="22945-162">事實上，介面卡裝置包含用戶端應用程式用來控制音訊處理的所有次單元連接。</span><span class="sxs-lookup"><span data-stu-id="22945-162">In fact, adapter devices contain all of the subunits that client applications use to control audio processing.</span></span> <span data-ttu-id="22945-163">端點裝置的裝置拓撲主要做為探索介面卡裝置之裝置拓撲的起點。</span><span class="sxs-lookup"><span data-stu-id="22945-163">The device topology of an endpoint device serves primarily as a starting point for exploring the device topologies of adapter devices.</span></span>

<span data-ttu-id="22945-164">裝置拓撲中兩個元件之間的內部連接稱為連結。</span><span class="sxs-lookup"><span data-stu-id="22945-164">Internal connections between two parts in a device topology are called links.</span></span> <span data-ttu-id="22945-165">DeviceTopology API 提供的方法，可讓您將連結從某個元件的連結到裝置拓撲中的下一個部分。</span><span class="sxs-lookup"><span data-stu-id="22945-165">The DeviceTopology API provides methods for traversing links from one part to the next in a device topology.</span></span> <span data-ttu-id="22945-166">此 API 也會提供方法來進行裝置拓撲之間的連接。</span><span class="sxs-lookup"><span data-stu-id="22945-166">The API also provides methods for traversing the connections between device topologies.</span></span>

<span data-ttu-id="22945-167">為了開始探索一組已連線的裝置拓撲，用戶端應用程式會啟用音訊端點裝置的 **IDeviceTopology** 介面。</span><span class="sxs-lookup"><span data-stu-id="22945-167">To begin exploration of a set of connected device topologies, a client application activates the **IDeviceTopology** interface of an audio endpoint device.</span></span> <span data-ttu-id="22945-168">端點裝置中的連接器會連接到音訊介面卡或網路中的連接器。</span><span class="sxs-lookup"><span data-stu-id="22945-168">The connector in an endpoint device connects either to a connector in an audio adapter or to a network.</span></span> <span data-ttu-id="22945-169">如果端點連線到音訊介面卡上的裝置，則 DeviceTopology API 中的方法會在連線的另一端取得介面卡裝置的 **IDeviceTopology** 介面參考，讓應用程式能夠從端點到介面卡的連線逐步進行。</span><span class="sxs-lookup"><span data-stu-id="22945-169">If the endpoint connects to a device on an audio adapter, then the methods in the DeviceTopology API enable the application to step across the connection from the endpoint to the adapter by obtaining a reference to the **IDeviceTopology** interface of the adapter device on the other side of the connection.</span></span> <span data-ttu-id="22945-170">另一方面，網路沒有裝置拓撲。</span><span class="sxs-lookup"><span data-stu-id="22945-170">A network, on the other hand, has no device topology.</span></span> <span data-ttu-id="22945-171">網路連接會使用管線將音訊串流輸送至遠端存取系統的用戶端。</span><span class="sxs-lookup"><span data-stu-id="22945-171">A network connection pipes an audio stream to a client that is accessing the system remotely.</span></span>

<span data-ttu-id="22945-172">DeviceTopology API 只會提供音訊介面卡中硬體裝置拓撲的存取權。</span><span class="sxs-lookup"><span data-stu-id="22945-172">The DeviceTopology API provides access only to the topologies of the hardware devices in an audio adapter.</span></span> <span data-ttu-id="22945-173">圖表左邊緣的外部裝置和右邊邊緣的軟體元件超出 API 的範圍。</span><span class="sxs-lookup"><span data-stu-id="22945-173">The external devices on the left edge of the diagram and the software components on the right edge are beyond the scope of the API.</span></span> <span data-ttu-id="22945-174">圖表任一側的虛線表示 DeviceTopology API 的限制。</span><span class="sxs-lookup"><span data-stu-id="22945-174">The dashed lines on either side of the diagram represent the limits of the DeviceTopology API.</span></span> <span data-ttu-id="22945-175">用戶端可以使用 API 來探索從輸入插孔延伸至系統匯流排的資料路徑，但是 API 無法滲透于這些界限之外。</span><span class="sxs-lookup"><span data-stu-id="22945-175">The client can use the API to explore a data path that stretches from the input jack to the system bus, but the API cannot penetrate beyond these boundaries.</span></span>

<span data-ttu-id="22945-176">上圖中的每個連接器都有相關聯的連線類型，指出連接器所進行的連線類型。</span><span class="sxs-lookup"><span data-stu-id="22945-176">Each connector in the preceding diagram has an associated connection type that indicates the type of connection that the connector makes.</span></span> <span data-ttu-id="22945-177">因此，連接兩端的連接器一律具有相同的連線類型。</span><span class="sxs-lookup"><span data-stu-id="22945-177">Thus, the connectors on the two sides of a connection always have identical connection types.</span></span> <span data-ttu-id="22945-178">連線類型是由 [**ConnectorType**](/windows/win32/api/devicetopology/ne-devicetopology-connectortype) 列舉值（實體 \_ 外部、實體 \_ 內部、軟體 \_ 固定、軟體 \_ IO 或網路）所表示。</span><span class="sxs-lookup"><span data-stu-id="22945-178">The connection type is indicated by a [**ConnectorType**](/windows/win32/api/devicetopology/ne-devicetopology-connectortype) enumeration value—Physical\_External, Physical\_Internal, Software\_Fixed, Software\_IO, or Network.</span></span> <span data-ttu-id="22945-179">輸入多工器裝置與端點裝置 A 和 B 之間的連線是實體 \_ 外部類型，也就是說，連線代表外部裝置的實體連線 (換句話說，就是使用者可存取的音訊插孔) 。</span><span class="sxs-lookup"><span data-stu-id="22945-179">The connections between the input multiplexer device and endpoint devices A and B are of type Physical\_External, which means that the connection represents a physical connection to an external device (in other words, a user-accessible audio jack).</span></span> <span data-ttu-id="22945-180">從內部 CD 播放機到類比信號的連接是實體 \_ 內部類型，表示安裝在系統底座內的輔助裝置實體連接。</span><span class="sxs-lookup"><span data-stu-id="22945-180">The connection to the analog signal from the internal CD player is of type Physical\_Internal, which indicates a physical connection to an auxiliary device that is installed inside the system chassis.</span></span> <span data-ttu-id="22945-181">Wave capture 裝置和輸入多工器裝置之間的連線類型為「軟體 \_ 固定」，這表示永久連線是固定的，且無法在軟體控制下設定。</span><span class="sxs-lookup"><span data-stu-id="22945-181">The connection between the wave capture device and input multiplexer device is of type Software\_Fixed, which indicates a permanent connection that is fixed and cannot be configured under software control.</span></span> <span data-ttu-id="22945-182">最後，連接到圖表右側的系統匯流排類型為「軟體 \_ IO」，這表示連線的資料 i/o 是由軟體控制下的 DMA 引擎所執行。</span><span class="sxs-lookup"><span data-stu-id="22945-182">Finally, the connection to the system bus on the right side of the diagram is of type Software\_IO, which indicates that the data I/O for the connection is implemented by a DMA engine under software control.</span></span> <span data-ttu-id="22945-183"> (圖表不包含網路連接類型的範例。 ) </span><span class="sxs-lookup"><span data-stu-id="22945-183">(The diagram does not include an example of a Network connection type.)</span></span>

<span data-ttu-id="22945-184">用戶端會開始遍歷端點裝置上的資料路徑。</span><span class="sxs-lookup"><span data-stu-id="22945-184">The client begins traversing a data path at the endpoint device.</span></span> <span data-ttu-id="22945-185">首先，用戶端會取得代表端點裝置的 [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) 介面，如 [列舉音訊裝置](enumerating-audio-devices.md)所述。</span><span class="sxs-lookup"><span data-stu-id="22945-185">First, the client obtains an [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface that represents the endpoint device, as explained in [Enumerating Audio Devices](enumerating-audio-devices.md).</span></span> <span data-ttu-id="22945-186">為了取得端點裝置的 **IDeviceTopology** 介面，用戶端會呼叫 [**IMMDevice：： Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) 方法，並將參數 *iid* 設定為 REFIID iid \_ IDeviceTopology。</span><span class="sxs-lookup"><span data-stu-id="22945-186">To obtain the **IDeviceTopology** interface for the endpoint device, the client calls the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method with parameter *iid* set to REFIID IID\_IDeviceTopology.</span></span>

<span data-ttu-id="22945-187">在上圖的範例中，輸入多工器裝置包含的所有硬體控制項都 (磁片區、靜音和多工器，) 適用于來自線路輸入和麥克風插孔的捕獲資料流程。</span><span class="sxs-lookup"><span data-stu-id="22945-187">In the example in the preceding diagram, the input multiplexer device contains all the hardware controls (volume, mute, and multiplexer) for the capture streams from the line-input and microphone jacks.</span></span> <span data-ttu-id="22945-188">下列程式碼範例示範如何從線路輸入或麥克風的端點裝置的 **IMMDevice** 介面取得輸入多工器裝置的 **IDeviceTopology** 介面：</span><span class="sxs-lookup"><span data-stu-id="22945-188">The following code example shows how to obtain the **IDeviceTopology** interface for the input multiplexer device from the **IMMDevice** interface for the endpoint device for the line input or microphone:</span></span>


```C++
//-----------------------------------------------------------
// The input argument to this function is a pointer to the
// IMMDevice interface of an endpoint device. The function
// outputs a pointer (counted reference) to the
// IDeviceTopology interface of the adapter device that
// connects to the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const IID IID_IDeviceTopology = __uuidof(IDeviceTopology);
const IID IID_IPart = __uuidof(IPart);

HRESULT GetHardwareDeviceTopology(
            IMMDevice *pEndptDev,
            IDeviceTopology **ppDevTopo)
{
    HRESULT hr = S_OK;
    IDeviceTopology *pDevTopoEndpt = NULL;
    IConnector *pConnEndpt = NULL;
    IConnector *pConnHWDev = NULL;
    IPart *pPartConn = NULL;

    // Get the endpoint device's IDeviceTopology interface.

    hr = pEndptDev->Activate(
                      IID_IDeviceTopology, CLSCTX_ALL,
                      NULL, (void**)&pDevTopoEndpt);
    EXIT_ON_ERROR(hr)

    // The device topology for an endpoint device always
    // contains just one connector (connector number 0).

    hr = pDevTopoEndpt->GetConnector(0, &pConnEndpt);
    EXIT_ON_ERROR(hr)

    // Use the connector in the endpoint device to get the
    // connector in the adapter device.

    hr = pConnEndpt->GetConnectedTo(&pConnHWDev);
    EXIT_ON_ERROR(hr)

    // Query the connector in the adapter device for
    // its IPart interface.

    hr = pConnHWDev->QueryInterface(
                         IID_IPart, (void**)&pPartConn);
    EXIT_ON_ERROR(hr)

    // Use the connector's IPart interface to get the
    // IDeviceTopology interface for the adapter device.

    hr = pPartConn->GetTopologyObject(ppDevTopo);

Exit:
    SAFE_RELEASE(pDevTopoEndpt)
    SAFE_RELEASE(pConnEndpt)
    SAFE_RELEASE(pConnHWDev)
    SAFE_RELEASE(pPartConn)

    return hr;
}
```



<span data-ttu-id="22945-189">上述程式碼範例中的 GetHardwareDeviceTopology 函式會執行下列步驟，以取得輸入多工器裝置的 **IDeviceTopology** 介面：</span><span class="sxs-lookup"><span data-stu-id="22945-189">The GetHardwareDeviceTopology function in the previous code example performs the following steps to obtain the **IDeviceTopology** interface for the input multiplexer device:</span></span>

1.  <span data-ttu-id="22945-190">呼叫 **IMMDevice：： Activate** 方法以取得端點裝置的 **IDeviceTopology** 介面。</span><span class="sxs-lookup"><span data-stu-id="22945-190">Call the **IMMDevice::Activate** method to get the **IDeviceTopology** interface for the endpoint device.</span></span>
2.  <span data-ttu-id="22945-191">使用上一個步驟取得的 **IDeviceTopology** 介面，呼叫 [**IDeviceTopology：： GetConnector**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getconnector) 方法，以取得端點裝置中單一連接器 (連接器編號 0) 的 **IConnector** 介面。</span><span class="sxs-lookup"><span data-stu-id="22945-191">With the **IDeviceTopology** interface obtained in the preceding step, call the [**IDeviceTopology::GetConnector**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getconnector) method to get the **IConnector** interface of the single connector (connector number 0) in the endpoint device.</span></span>
3.  <span data-ttu-id="22945-192">使用上一個步驟取得的 **IConnector** 介面，呼叫 [**IConnector：： GetConnectedTo**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getconnectedto) 方法，以取得輸入多工器裝置中連接器的 **IConnector** 介面。</span><span class="sxs-lookup"><span data-stu-id="22945-192">With the **IConnector** interface obtained in the preceding step, call the [**IConnector::GetConnectedTo**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getconnectedto) method to get the **IConnector** interface of the connector in the input multiplexer device.</span></span>
4.  <span data-ttu-id="22945-193">查詢在上一個步驟中取得的 **IConnector** 介面，以取得其 **IPart** 介面。</span><span class="sxs-lookup"><span data-stu-id="22945-193">Query the **IConnector** interface obtained in the preceding step for its **IPart** interface.</span></span>
5.  <span data-ttu-id="22945-194">使用上一個步驟中取得的 **IPart** 介面，呼叫 [**IPart：： GetTopologyObject**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) 方法以取得輸入多工器裝置的 **IDeviceTopology** 介面。</span><span class="sxs-lookup"><span data-stu-id="22945-194">With the **IPart** interface obtained in the preceding step, call the [**IPart::GetTopologyObject**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) method to get the **IDeviceTopology** interface for the input multiplexer device.</span></span>

<span data-ttu-id="22945-195">在使用者可以從上圖中的麥克風錄製之前，用戶端應用程式必須確定多工器選取麥克風輸入。</span><span class="sxs-lookup"><span data-stu-id="22945-195">Before the user can record from the microphone in the preceding diagram, the client application must make certain that the multiplexer selects the microphone input.</span></span> <span data-ttu-id="22945-196">下列程式碼範例會示範用戶端如何從麥克風中找出資料路徑，直到找到多工器為止，然後程式會選取麥克風輸入：</span><span class="sxs-lookup"><span data-stu-id="22945-196">The following code example shows how a client can traverse the data path from the microphone until it finds the multiplexer, which it then programs to select the microphone input:</span></span>


```C++
//-----------------------------------------------------------
// The input argument to this function is a pointer to the
// IMMDevice interface for a capture endpoint device. The
// function traverses the data path that extends from the
// endpoint device to the system bus (for example, PCI)
// or external bus (USB). If the function discovers a MUX
// (input selector) in the path, it selects the MUX input
// that connects to the stream from the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const IID IID_IDeviceTopology = __uuidof(IDeviceTopology);
const IID IID_IPart = __uuidof(IPart);
const IID IID_IConnector = __uuidof(IConnector);
const IID IID_IAudioInputSelector = __uuidof(IAudioInputSelector);

HRESULT SelectCaptureDevice(IMMDevice *pEndptDev)
{
    HRESULT hr = S_OK;
    DataFlow flow;
    IDeviceTopology *pDeviceTopology = NULL;
    IConnector *pConnFrom = NULL;
    IConnector *pConnTo = NULL;
    IPart *pPartPrev = NULL;
    IPart *pPartNext = NULL;
    IAudioInputSelector *pSelector = NULL;

    if (pEndptDev == NULL)
    {
        EXIT_ON_ERROR(hr = E_POINTER)
    }

    // Get the endpoint device's IDeviceTopology interface.
    hr = pEndptDev->Activate(
                      IID_IDeviceTopology, CLSCTX_ALL, NULL,
                      (void**)&pDeviceTopology);
    EXIT_ON_ERROR(hr)

    // The device topology for an endpoint device always
    // contains just one connector (connector number 0).
    hr = pDeviceTopology->GetConnector(0, &pConnFrom);
    SAFE_RELEASE(pDeviceTopology)
    EXIT_ON_ERROR(hr)

    // Make sure that this is a capture device.
    hr = pConnFrom->GetDataFlow(&flow);
    EXIT_ON_ERROR(hr)

    if (flow != Out)
    {
        // Error -- this is a rendering device.
        EXIT_ON_ERROR(hr = AUDCLNT_E_WRONG_ENDPOINT_TYPE)
    }

    // Outer loop: Each iteration traverses the data path
    // through a device topology starting at the input
    // connector and ending at the output connector.
    while (TRUE)
    {
        BOOL bConnected;
        hr = pConnFrom->IsConnected(&bConnected);
        EXIT_ON_ERROR(hr)

        // Does this connector connect to another device?
        if (bConnected == FALSE)
        {
            // This is the end of the data path that
            // stretches from the endpoint device to the
            // system bus or external bus. Verify that
            // the connection type is Software_IO.
            ConnectorType  connType;
            hr = pConnFrom->GetType(&connType);
            EXIT_ON_ERROR(hr)

            if (connType == Software_IO)
            {
                break;  // finished
            }
            EXIT_ON_ERROR(hr = E_FAIL)
        }

        // Get the connector in the next device topology,
        // which lies on the other side of the connection.
        hr = pConnFrom->GetConnectedTo(&pConnTo);
        EXIT_ON_ERROR(hr)
        SAFE_RELEASE(pConnFrom)

        // Get the connector's IPart interface.
        hr = pConnTo->QueryInterface(
                        IID_IPart, (void**)&pPartPrev);
        EXIT_ON_ERROR(hr)
        SAFE_RELEASE(pConnTo)

        // Inner loop: Each iteration traverses one link in a
        // device topology and looks for input multiplexers.
        while (TRUE)
        {
            PartType parttype;
            UINT localId;
            IPartsList *pParts;

            // Follow downstream link to next part.
            hr = pPartPrev->EnumPartsOutgoing(&pParts);
            EXIT_ON_ERROR(hr)

            hr = pParts->GetPart(0, &pPartNext);
            pParts->Release();
            EXIT_ON_ERROR(hr)

            hr = pPartNext->GetPartType(&parttype);
            EXIT_ON_ERROR(hr)

            if (parttype == Connector)
            {
                // We've reached the output connector that
                // lies at the end of this device topology.
                hr = pPartNext->QueryInterface(
                                  IID_IConnector,
                                  (void**)&pConnFrom);
                EXIT_ON_ERROR(hr)

                SAFE_RELEASE(pPartPrev)
                SAFE_RELEASE(pPartNext)
                break;
            }

            // Failure of the following call means only that
            // the part is not a MUX (input selector).
            hr = pPartNext->Activate(
                              CLSCTX_ALL,
                              IID_IAudioInputSelector,
                              (void**)&pSelector);
            if (hr == S_OK)
            {
                // We found a MUX (input selector), so select
                // the input from our endpoint device.
                hr = pPartPrev->GetLocalId(&localId);
                EXIT_ON_ERROR(hr)

                hr = pSelector->SetSelection(localId, NULL);
                EXIT_ON_ERROR(hr)

                SAFE_RELEASE(pSelector)
            }

            SAFE_RELEASE(pPartPrev)
            pPartPrev = pPartNext;
            pPartNext = NULL;
        }
    }

Exit:
    SAFE_RELEASE(pConnFrom)
    SAFE_RELEASE(pConnTo)
    SAFE_RELEASE(pPartPrev)
    SAFE_RELEASE(pPartNext)
    SAFE_RELEASE(pSelector)
    return hr;
}
```



<span data-ttu-id="22945-197">DeviceTopology API 會實 [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector) 介面來封裝多工器，例如上圖中的多工器。</span><span class="sxs-lookup"><span data-stu-id="22945-197">The DeviceTopology API implements an [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector) interface to encapsulate a multiplexer, such as the one in the preceding diagram.</span></span> <span data-ttu-id="22945-198"> ([**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector) 介面會封裝一個信號。 ) 在上述程式碼範例中，SelectCaptureDevice 函式的內部迴圈會查詢它找到的每個子單位，以探索子單位是否為多工器。</span><span class="sxs-lookup"><span data-stu-id="22945-198">(An [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector) interface encapsulates a demultiplexer.) In the preceding code example, the inner loop of the SelectCaptureDevice function queries each subunit that it finds to discover whether the subunit is a multiplexer.</span></span> <span data-ttu-id="22945-199">如果子單位為多工器，則函式會呼叫 [**IAudioInputSelector：： SetSelection**](/windows/desktop/api/Devicetopology/nf-devicetopology-iaudioinputselector-setselection) 方法，以選取從端點裝置連接到資料流程的輸入。</span><span class="sxs-lookup"><span data-stu-id="22945-199">If the subunit is a multiplexer, then the function calls the [**IAudioInputSelector::SetSelection**](/windows/desktop/api/Devicetopology/nf-devicetopology-iaudioinputselector-setselection) method to select the input that connects to the stream from the endpoint device.</span></span>

<span data-ttu-id="22945-200">在上述程式碼範例中，外部迴圈的每個反復專案都會流經一個裝置拓撲。</span><span class="sxs-lookup"><span data-stu-id="22945-200">In the preceding code example, each iteration of the outer loop traverses one device topology.</span></span> <span data-ttu-id="22945-201">當您在上圖中遍歷裝置拓撲時，第一次反覆運算會流經輸入多工器裝置，而第二個反復專案則會流經 wave capture 裝置。</span><span class="sxs-lookup"><span data-stu-id="22945-201">When traversing the device topologies in the preceding diagram, the first iteration traverses the input multiplexer device and the second iteration traverses the wave capture device.</span></span> <span data-ttu-id="22945-202">函式會在到達圖表右邊緣的接點時終止。</span><span class="sxs-lookup"><span data-stu-id="22945-202">The function will terminate when it reaches the connector at the right edge of the diagram.</span></span> <span data-ttu-id="22945-203">當函數偵測到具有軟體 IO 連線類型的連接器時，就會發生終止 \_ 。</span><span class="sxs-lookup"><span data-stu-id="22945-203">Termination occurs when the function detects a connector with a Software\_IO connection type.</span></span> <span data-ttu-id="22945-204">此連線類型會識別介面卡裝置連接到系統匯流排的點。</span><span class="sxs-lookup"><span data-stu-id="22945-204">This connection type identifies the point at which the adapter device connects to the system bus.</span></span>

<span data-ttu-id="22945-205">在上述程式碼範例中，呼叫 [**IPart：： GetPartType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype) 方法會取得 **IPartType** 列舉值，這個值表示目前的元件是連接器或音訊處理子單位。</span><span class="sxs-lookup"><span data-stu-id="22945-205">The call to the [**IPart::GetPartType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype) method in the preceding code example obtains an **IPartType** enumeration value that indicates whether the current part is a connector or an audio-processing subunit.</span></span>

<span data-ttu-id="22945-206">上述程式碼範例中的內部迴圈會透過呼叫 [**IPart：： EnumPartsOutgoing**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsoutgoing) 方法，從某個部分到下一個部分的連結逐步執行。</span><span class="sxs-lookup"><span data-stu-id="22945-206">The inner loop in the preceding code example steps across the link from one part to the next by calling the [**IPart::EnumPartsOutgoing**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsoutgoing) method.</span></span> <span data-ttu-id="22945-207"> (也會有 [**IPart：： EnumPartsIncoming**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsincoming) 方法，以相反的方向逐步執行。 ) 這個方法會抓取 [**IPartsList**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist) 物件，其中包含所有傳出部分的清單。</span><span class="sxs-lookup"><span data-stu-id="22945-207">(There's also an [**IPart::EnumPartsIncoming**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsincoming) method for stepping in the opposite direction.) This method retrieves an [**IPartsList**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist) object that contains a list of all the outgoing parts.</span></span> <span data-ttu-id="22945-208">不過，SelectCaptureDevice 函式預期在捕獲裝置中遇到的任何部分，一律會有一個外寄部分。</span><span class="sxs-lookup"><span data-stu-id="22945-208">However, any part that the SelectCaptureDevice function expects to encounter in a capture device will always have exactly one outgoing part.</span></span> <span data-ttu-id="22945-209">因此，後續對 [**IPartsList：： GetPart**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getpart) 的呼叫一律會要求清單中的第一個部分（元件編號0），因為此函式會假設這是清單中的唯一部分。</span><span class="sxs-lookup"><span data-stu-id="22945-209">Thus, the subsequent call to [**IPartsList::GetPart**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getpart) always requests the first part in the list, part number 0, because the function assumes that this is the only part in the list.</span></span>

<span data-ttu-id="22945-210">如果 SelectCaptureDevice 函式遇到該假設不正確拓撲，此函式可能無法正確設定裝置。</span><span class="sxs-lookup"><span data-stu-id="22945-210">If the SelectCaptureDevice function encounters a topology for which that assumption is not valid, the function might fail to configure the device correctly.</span></span> <span data-ttu-id="22945-211">若要避免這類失敗，更一般用途的函式版本可能會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="22945-211">To avoid such a failure, a more general-purpose version of the function might do the following:</span></span>

-   <span data-ttu-id="22945-212">呼叫 [**IPartsList：： GetCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getcount) 方法，以判斷外寄部分的數目。</span><span class="sxs-lookup"><span data-stu-id="22945-212">Call the [**IPartsList::GetCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getcount) method to determine the number of outgoing parts.</span></span>
-   <span data-ttu-id="22945-213">針對每個外寄部分，呼叫 **IPartsList：： GetPart** 來開始遍歷元件的資料路徑。</span><span class="sxs-lookup"><span data-stu-id="22945-213">For each outgoing part, call **IPartsList::GetPart** to begin to traverse the data path that leads from the part.</span></span>

<span data-ttu-id="22945-214">部分（但不一定全部）部分都有用戶端可以設定或取得的相關硬體控制項。</span><span class="sxs-lookup"><span data-stu-id="22945-214">Some, but not necessarily all, parts have associated hardware controls that clients can set or get.</span></span> <span data-ttu-id="22945-215">特定元件可能會有零個、一個或多個硬體控制項。</span><span class="sxs-lookup"><span data-stu-id="22945-215">A particular part might have zero, one, or more hardware controls.</span></span> <span data-ttu-id="22945-216">硬體控制項是由下列成對的介面所代表：</span><span class="sxs-lookup"><span data-stu-id="22945-216">A hardware control is represented by the following pair of interfaces:</span></span>

-   <span data-ttu-id="22945-217">泛型控制項介面 [**IControlInterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface)，其具有所有硬體控制項通用的方法。</span><span class="sxs-lookup"><span data-stu-id="22945-217">A generic control interface, [**IControlInterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface), which has methods that are common to all hardware controls.</span></span>
-   <span data-ttu-id="22945-218"> (的函式特定介面，例如，會公開特定硬體控制項類型之控制項參數的 [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel))  (例如，磁片區控制項) 。</span><span class="sxs-lookup"><span data-stu-id="22945-218">A function-specific interface (for example, [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)) that exposes the control parameters for a particular type of hardware control (for example, a volume control).</span></span>

<span data-ttu-id="22945-219">為了列舉元件的硬體控制項，用戶端會先呼叫 [**IPart：： GetControlInterfaceCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterfacecount) 方法，以判斷與元件相關聯的硬體控制項數目。</span><span class="sxs-lookup"><span data-stu-id="22945-219">To enumerate the hardware controls for a part, the client first calls the [**IPart::GetControlInterfaceCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterfacecount) method to determine the number of hardware controls that are associated with the part.</span></span> <span data-ttu-id="22945-220">接下來，用戶端會對 [**IPart：： GetControlInterface**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterface) 方法進行一連串的呼叫，以取得每個硬體控制項的 **IControlInterface** 介面。</span><span class="sxs-lookup"><span data-stu-id="22945-220">Next, the client makes a series of calls to the [**IPart::GetControlInterface**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterface) method to obtain the **IControlInterface** interface for each hardware control.</span></span> <span data-ttu-id="22945-221">最後，用戶端會呼叫 [**IControlInterface：： GetIID**](/windows/desktop/api/Devicetopology/nf-devicetopology-icontrolinterface-getiid) 方法取得介面識別碼，以取得每個硬體控制項的函式特定介面。</span><span class="sxs-lookup"><span data-stu-id="22945-221">Finally, the client obtains the function-specific interface for each hardware control by calling the [**IControlInterface::GetIID**](/windows/desktop/api/Devicetopology/nf-devicetopology-icontrolinterface-getiid) method to obtain the interface ID.</span></span> <span data-ttu-id="22945-222">用戶端會使用這個識別碼呼叫 [**IPart：： Activate**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-activate) 方法來取得函式特定的介面。</span><span class="sxs-lookup"><span data-stu-id="22945-222">The client calls the [**IPart::Activate**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-activate) method with this ID to obtain the function-specific interface.</span></span>

<span data-ttu-id="22945-223">屬於連接器的元件可能會支援下列其中一個函式特定的控制項介面：</span><span class="sxs-lookup"><span data-stu-id="22945-223">A part that is a connector might support one of the following function-specific control interfaces:</span></span>

-   [<span data-ttu-id="22945-224">**IKsFormatSupport**</span><span class="sxs-lookup"><span data-stu-id="22945-224">**IKsFormatSupport**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)
-   [<span data-ttu-id="22945-225">**IKsJackDescription**</span><span class="sxs-lookup"><span data-stu-id="22945-225">**IKsJackDescription**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)

<span data-ttu-id="22945-226">屬於子單位的部分可能會支援下列一或多個特定的函式控制項介面：</span><span class="sxs-lookup"><span data-stu-id="22945-226">A part that is a subunit might support one or more of the following function-specific control interfaces:</span></span>

-   [<span data-ttu-id="22945-227">**IAudioAutoGainControl**</span><span class="sxs-lookup"><span data-stu-id="22945-227">**IAudioAutoGainControl**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)
-   [<span data-ttu-id="22945-228">**IAudioBass**</span><span class="sxs-lookup"><span data-stu-id="22945-228">**IAudioBass**</span></span>](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)
-   [<span data-ttu-id="22945-229">**IAudioChannelConfig**</span><span class="sxs-lookup"><span data-stu-id="22945-229">**IAudioChannelConfig**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)
-   [<span data-ttu-id="22945-230">**IAudioInputSelector**</span><span class="sxs-lookup"><span data-stu-id="22945-230">**IAudioInputSelector**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)
-   [<span data-ttu-id="22945-231">**IAudioLoudness**</span><span class="sxs-lookup"><span data-stu-id="22945-231">**IAudioLoudness**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)
-   [<span data-ttu-id="22945-232">**IAudioMidrange**</span><span class="sxs-lookup"><span data-stu-id="22945-232">**IAudioMidrange**</span></span>](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)
-   [<span data-ttu-id="22945-233">**IAudioMute**</span><span class="sxs-lookup"><span data-stu-id="22945-233">**IAudioMute**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)
-   [<span data-ttu-id="22945-234">**IAudioOutputSelector**</span><span class="sxs-lookup"><span data-stu-id="22945-234">**IAudioOutputSelector**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)
-   [<span data-ttu-id="22945-235">**IAudioPeakMeter**</span><span class="sxs-lookup"><span data-stu-id="22945-235">**IAudioPeakMeter**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)
-   [<span data-ttu-id="22945-236">**IAudioTreble**</span><span class="sxs-lookup"><span data-stu-id="22945-236">**IAudioTreble**</span></span>](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)
-   [<span data-ttu-id="22945-237">**IAudioVolumeLevel**</span><span class="sxs-lookup"><span data-stu-id="22945-237">**IAudioVolumeLevel**</span></span>](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)
-   [<span data-ttu-id="22945-238">**IDeviceSpecificProperty**</span><span class="sxs-lookup"><span data-stu-id="22945-238">**IDeviceSpecificProperty**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty)

<span data-ttu-id="22945-239">只有當基礎硬體控制項有裝置特定的控制值，且控制項無法由上述清單中的任何其他函式特定介面明確表示時，元件才支援 **IDeviceSpecificProperty** 介面。</span><span class="sxs-lookup"><span data-stu-id="22945-239">A part supports the **IDeviceSpecificProperty** interface only if the underlying hardware control has a device-specific control value and the control cannot be adequately represented by any other function-specific interface in the preceding list.</span></span> <span data-ttu-id="22945-240">通常，裝置專屬屬性只適用于可從元件類型、元件子類型和部分名稱等資訊推斷屬性值意義的用戶端。</span><span class="sxs-lookup"><span data-stu-id="22945-240">Typically, a device-specific property is useful only to a client that can infer the meaning of the property value from information such as the part type, part subtype, and part name.</span></span> <span data-ttu-id="22945-241">用戶端可以藉由呼叫 [**IPart：： GetPartType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype)、 [**IPart：： GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype)和 [**IPart：： GetName**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getname) 方法來取得此資訊。</span><span class="sxs-lookup"><span data-stu-id="22945-241">The client can obtain this information by calling the [**IPart::GetPartType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype), [**IPart::GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype), and [**IPart::GetName**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getname) methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22945-242">相關主題</span><span class="sxs-lookup"><span data-stu-id="22945-242">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22945-243">程式設計指南</span><span class="sxs-lookup"><span data-stu-id="22945-243">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
