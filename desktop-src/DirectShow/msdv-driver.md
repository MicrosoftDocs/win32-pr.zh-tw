---
description: MSDV 驅動程式
ms.assetid: 146ca753-fe41-49d3-8b1c-077e10a28192
title: MSDV 驅動程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b7c1bda24980abe84a11613126476ccfe35380d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385557"
---
# <a name="msdv-driver"></a><span data-ttu-id="0ef9a-103">MSDV 驅動程式</span><span class="sxs-lookup"><span data-stu-id="0ef9a-103">MSDV Driver</span></span>

<span data-ttu-id="0ef9a-104">MSDV 是適用于 DV 攝影機的 Microsoft Windows Driver Model (WDM) 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-104">MSDV is the Microsoft Windows Driver Model (WDM) driver for DV camcorders.</span></span> <span data-ttu-id="0ef9a-105">當裝置插入電源時，驅動程式會顯示為 DirectShow 篩選。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-105">The driver appears as a DirectShow filter when the device is plugged in.</span></span> <span data-ttu-id="0ef9a-106">它是以兩個篩選準則分類來列舉：</span><span class="sxs-lookup"><span data-stu-id="0ef9a-106">It is enumerated in two filter categories:</span></span>

-   <span data-ttu-id="0ef9a-107">CLSID \_ VideoInputDeviceCategory ( 「影片捕獲來源」 ) </span><span class="sxs-lookup"><span data-stu-id="0ef9a-107">CLSID\_VideoInputDeviceCategory ("Video Capture Sources")</span></span>
-   <span data-ttu-id="0ef9a-108">\_KSCATEGORY 轉譯 \_ ( 「WDM 串流轉譯裝置」 ) </span><span class="sxs-lookup"><span data-stu-id="0ef9a-108">AM\_KSCATEGORY\_RENDER ("WDM Streaming Rendering Devices")</span></span>

<span data-ttu-id="0ef9a-109">篩選的易記名稱是 `Microsoft DV Camera and VCR` 或當地語系化的對等專案。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-109">The filter's friendly name is `Microsoft DV Camera and VCR`, or a localized equivalent.</span></span> <span data-ttu-id="0ef9a-110">在某些裝置中， **description** 屬性包含特定模型的描述，可用來取代一般的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-110">In some devices, the **Description** property contains a description of the specific model, which can be used instead of the generic friendly name.</span></span> <span data-ttu-id="0ef9a-111">如需詳細資訊，請參閱 [選取擷取裝置](selecting-a-capture-device.md)。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-111">For more information, see [Selecting a Capture Device](selecting-a-capture-device.md).</span></span>

<span data-ttu-id="0ef9a-112">MSDV 有兩個輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-112">MSDV has two output pins.</span></span> <span data-ttu-id="0ef9a-113">一個 pin 會提供包含交錯音訊和影片資料的 DV 框架。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-113">One pin delivers DV frames that contain interleaved audio and video data.</span></span> <span data-ttu-id="0ef9a-114">另一個 pin 提供僅限影片的框架，沒有音訊。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-114">The other pin delivers video-only frames with no audio.</span></span> <span data-ttu-id="0ef9a-115">MSDV 無法同時從這兩個 pin 進行串流，所以一次只能連接一個輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-115">MSDV cannot stream from both pins at once, so only one output pin can be connected at a time.</span></span> <span data-ttu-id="0ef9a-116">如需從 DV 裝置捕獲影片的詳細資訊，請參閱 [將 dv 帶到](capture-dv-to-file.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-116">For more information about capturing video from a DV device, see [Capture DV to File](capture-dv-to-file.md).</span></span>

![從裝置捕獲 dv 資料](images/dv-filters4.png)

<span data-ttu-id="0ef9a-118">大部分的 DV 攝影機都有影片磁帶錄製器 (VTR) 的次級，可將資料從磁帶傳輸到電腦。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-118">Most DV camcorders have a video tape recorder (VTR) subunit, which can transmit data from tape to the computer.</span></span> <span data-ttu-id="0ef9a-119">針對應用程式，從磁帶進行捕捉的運作方式與捕捉即時影片相同。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-119">For the application, capturing from tape works the same as capturing live video.</span></span> <span data-ttu-id="0ef9a-120">唯一的差別在於應用程式必須控制外部磁帶傳輸—啟動和停止磁帶、倒轉等等。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-120">The only difference is that the application must control the external tape transport — start and stop the tape, rewind, and so forth.</span></span> <span data-ttu-id="0ef9a-121">基於這個目的，MSDV 會公開 [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice)、 [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)和 [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) 介面。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-121">For this purpose, MSDV exposes the [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice), [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport), and [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) interfaces.</span></span> <span data-ttu-id="0ef9a-122">如需控制 VTR 的詳細資訊，請參閱 [控制 DV 攝像機](controlling-a-dv-camcorder.md)。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-122">For more information about controlling a VTR, see [Controlling a DV Camcorder](controlling-a-dv-camcorder.md).</span></span>

<span data-ttu-id="0ef9a-123">您也可以從電腦傳輸 DV 到攝像機。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-123">You can also transmit DV from the computer to the camcorder.</span></span> <span data-ttu-id="0ef9a-124">然後可以在攝像機的上架畫面中查看影片，或記錄到磁帶上。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-124">The video can then be viewed in the camcorder's onboard screen, or recorded to tape.</span></span> <span data-ttu-id="0ef9a-125">為了支援此功能，MSDV 具有可接收交錯 DV 串流的輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-125">To support this functionality, MSDV has an input pin that can receive an interleaved DV stream.</span></span> <span data-ttu-id="0ef9a-126">當輸入連接連接時，MSDV 會作為轉譯器篩選器，而不是「捕捉」篩選。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-126">When the input pin is connected, MSDV acts as a renderer filter instead of a capture filter.</span></span> <span data-ttu-id="0ef9a-127">MSDV 不支援在此模式中進行搜尋。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-127">MSDV does not support seeking in this mode.</span></span> <span data-ttu-id="0ef9a-128">如需將 DV 傳送至裝置的詳細資訊，請參閱 [從檔案傳輸 dv 至磁帶](transmit-dv-from-file-to-tape.md)。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-128">For more information about sending DV to the device, see [Transmit DV from File to Tape](transmit-dv-from-file-to-tape.md).</span></span>

![將 dv 資料傳輸至裝置](images/dv-filters5.png)

<span data-ttu-id="0ef9a-130">請注意，輸入和輸出 pin 無法同時連線，因為裝置無法同時以雙向方式進行串流。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-130">Note that the input and output pins cannot be connected at the same time, because the device cannot stream in both directions at the same time.</span></span>

<span data-ttu-id="0ef9a-131">在許多攝影機中，在 VTR 模式和攝影機模式之間切換，會導致裝置關閉。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-131">In many camcorders, switching between VTR mode and camera mode causes the device to switch off.</span></span> <span data-ttu-id="0ef9a-132">因此，當使用者切換模式時，DirectShow 可能會遺失裝置。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-132">Therefore, DirectShow may lose the device when the user switches modes.</span></span> <span data-ttu-id="0ef9a-133">如需裝置移除事件的詳細資訊，請參閱 [裝置移除通知](device-removal-notification.md)。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-133">For information about device removal events, see [Device Removal Notification](device-removal-notification.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0ef9a-134">備註</span><span class="sxs-lookup"><span data-stu-id="0ef9a-134">Remarks</span></span>

<span data-ttu-id="0ef9a-135">如需 MSDV 驅動程式所支援之 DV 格式的相關資訊，請參閱 [**DV 影片子類型**](dv-video-subtypes.md)。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-135">For information about which DV formats are supported by the MSDV driver, see [**DV Video Subtypes**](dv-video-subtypes.md).</span></span>

<span data-ttu-id="0ef9a-136">使用 MSDV 建立篩選圖形的一些秘訣：</span><span class="sxs-lookup"><span data-stu-id="0ef9a-136">Some tips on building filter graphs with MSDV:</span></span>

-   <span data-ttu-id="0ef9a-137">您無法使用 [**IGraphBuilder：： render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) 在 MSDV 上轉譯輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-137">You cannot use [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) to render an output pin on MSDV.</span></span> <span data-ttu-id="0ef9a-138"> (篩選圖形管理員嘗試將輸出連接連接到 MSDV 的輸入 pin 失敗。 ) 改為使用 [**IGraphBuilder：： connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) 或 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-138">(The Filter Graph Manager tries to connect the output pin to MSDV's input pin, which fails.) Instead, use [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) or [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream).</span></span>
-   <span data-ttu-id="0ef9a-139">當篩選圖形包含 MSDV 時，MSDV 應該提供圖形的參考時鐘。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-139">When a filter graph contains MSDV, MSDV should supply the reference clock for the graph.</span></span> <span data-ttu-id="0ef9a-140">從 DirectX 8.0，篩選圖形管理員會自動選擇 MSDV 做為參考時鐘。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-140">As of DirectX 8.0, the Filter Graph Manager will automatically choose MSDV as the reference clock.</span></span> <span data-ttu-id="0ef9a-141">使用較舊的版本時，您應該在篩選圖形管理員上呼叫 [**IMediaFilter：： SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) 方法。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-141">With earlier versions, you should call the [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method on the Filter Graph Manager.</span></span> <span data-ttu-id="0ef9a-142">如需時鐘的詳細資訊，請參閱 [DirectShow 中的時間和時鐘](time-and-clocks-in-directshow.md)。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-142">For more information about clocks, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>
-   <span data-ttu-id="0ef9a-143">視裝置而定， **IAMExtDevice**、 **IAMExtTransport** 和 **IAMTimeCodeReader** 中的某些方法可能會傳回 Windows 錯誤碼，而不是 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-143">Depending on the device, some methods in **IAMExtDevice**, **IAMExtTransport**, and **IAMTimeCodeReader** might return Windows error codes instead of **HRESULT** values.</span></span> <span data-ttu-id="0ef9a-144">可能的錯誤代碼包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-144">Possible error codes include the following.</span></span>

    | <span data-ttu-id="0ef9a-145">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="0ef9a-145">Error Code</span></span>              | <span data-ttu-id="0ef9a-146">描述</span><span class="sxs-lookup"><span data-stu-id="0ef9a-146">Description</span></span>                                                                                      |
    |-------------------------|--------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="0ef9a-147">錯誤 \_ 超時</span><span class="sxs-lookup"><span data-stu-id="0ef9a-147">ERROR\_TIMEOUT</span></span>          | <span data-ttu-id="0ef9a-148">外部裝置命令已超時。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-148">An external device command has timed out.</span></span>                                                        |
    | <span data-ttu-id="0ef9a-149">錯誤 \_ 需求 \_ 未 \_ ACCEP</span><span class="sxs-lookup"><span data-stu-id="0ef9a-149">ERROR\_REQ\_NOT\_ACCEP</span></span>  | <span data-ttu-id="0ef9a-150">裝置未接受此外部裝置命令。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-150">The device did not accept this external device command.</span></span>                                          |
    | <span data-ttu-id="0ef9a-151">\_不 \_ 支援的錯誤</span><span class="sxs-lookup"><span data-stu-id="0ef9a-151">ERROR\_NOT\_SUPPORTED</span></span>   | <span data-ttu-id="0ef9a-152">裝置不支援此外部裝置命令。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-152">The device does not support this external device command.</span></span>                                        |
    | <span data-ttu-id="0ef9a-153">錯誤 \_ 要求已 \_ 中止</span><span class="sxs-lookup"><span data-stu-id="0ef9a-153">ERROR\_REQUEST\_ABORTED</span></span> | <span data-ttu-id="0ef9a-154">外部裝置命令已中止。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-154">An external device command was aborted.</span></span> <span data-ttu-id="0ef9a-155">可能是裝置已移除或發生匯流排重設。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-155">Possibly the device was removed or a bus reset occurred.</span></span> |

    

     

### <a name="device-information"></a><span data-ttu-id="0ef9a-156">裝置資訊</span><span class="sxs-lookup"><span data-stu-id="0ef9a-156">Device Information</span></span>

<span data-ttu-id="0ef9a-157">在 Windows Millennium Edition 和 Windows XP 中，DV 篩選器的裝置標記除了 **FriendlyName** 屬性之外，還支援 **Description** 屬性。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-157">In Windows Millennium Edition and Windows XP, the DV filter's device moniker supports a **Description** property in addition to the **FriendlyName** property.</span></span> <span data-ttu-id="0ef9a-158">這個屬性會傳回從 INF 檔案取得之裝置的描述，其中通常包含裝置的品牌名稱。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-158">This property returns a description of the device, taken from the INF file, which usually contains the brand name of the device.</span></span> <span data-ttu-id="0ef9a-159">但是，並非所有裝置型號都支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-159">This property is not supported for all device models, however.</span></span>

<span data-ttu-id="0ef9a-160">如需裝置名字標記的詳細資訊，請參閱 [使用系統裝置枚舉器](using-the-system-device-enumerator.md)。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-160">For more information about device monikers, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

### <a name="clock-times"></a><span data-ttu-id="0ef9a-161">時鐘時間</span><span class="sxs-lookup"><span data-stu-id="0ef9a-161">Clock Times</span></span>

<span data-ttu-id="0ef9a-162">MSDV 驅動程式會使用1394資料封包中包含的1394匯流排時鐘來衍生時鐘。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-162">The MSDV driver uses the 1394 bus clock that is contained in the 1394 data packets to derive the clock.</span></span> <span data-ttu-id="0ef9a-163">它會使用這些值，以時間戳記 DV 媒體範例。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-163">It uses these values to time stamp the DV media samples.</span></span> <span data-ttu-id="0ef9a-164">由於此來源時鐘不是電腦系統時鐘，因此時間最後會與電腦系統時鐘漂移。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-164">Because this source clock is not the computer system clock, the times will eventually drift from the computer system clock.</span></span> <span data-ttu-id="0ef9a-165">不過，如先前所述，篩選圖形管理員預設會選取 [MSDV] 做為圖形參考時鐘。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-165">As noted above, however, by default the Filter Graph Manager will select MSDV as the graph reference clock.</span></span>

<span data-ttu-id="0ef9a-166">[**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes)介面會報告驅動程式目前的已卸載框架量值;在指定的時間內，此值可能不會與實際的已捨棄框架數目完全同步處理。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-166">The [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) interface reports the driver's current measure of dropped frames; this value may not be perfectly synchronized with the actual number of dropped frames at a given time.</span></span> <span data-ttu-id="0ef9a-167">如果已卸載框架，表示系統未平衡 (資料生產量超過) 的資料耗用量。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-167">If frames are dropped, it indicates that the system is not balanced (data production exceeds data consumption).</span></span> <span data-ttu-id="0ef9a-168">例如，使用者的硬碟可能不夠快，無法支援 DV 捕捉率。</span><span class="sxs-lookup"><span data-stu-id="0ef9a-168">For example, the user's hard disk may not be fast enough to support DV capture rates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ef9a-169">相關主題</span><span class="sxs-lookup"><span data-stu-id="0ef9a-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ef9a-170">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="0ef9a-170">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="0ef9a-171">DirectShow 中的數位視訊</span><span class="sxs-lookup"><span data-stu-id="0ef9a-171">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



