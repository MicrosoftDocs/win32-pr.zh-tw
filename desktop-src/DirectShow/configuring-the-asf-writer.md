---
description: 設定 ASF 寫入器
ms.assetid: 5708c4a0-6197-4a42-adfd-01c6dfe86302
title: 設定 ASF 寫入器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62a6dfc1827743dce946188ebf9e050226b5c484
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973138"
---
# <a name="configuring-the-asf-writer"></a><span data-ttu-id="9b42c-103">設定 ASF 寫入器</span><span class="sxs-lookup"><span data-stu-id="9b42c-103">Configuring the ASF Writer</span></span>

<span data-ttu-id="9b42c-104">當您建立了 [WM ASF 寫入](wm-asf-writer-filter.md) 器篩選器時，它會自動使用 \_ WMProfile \_ V80 256Video 設定檔進行設定。</span><span class="sxs-lookup"><span data-stu-id="9b42c-104">When the [WM ASF Writer](wm-asf-writer-filter.md) filter is created, it is configured automatically with the WMProfile\_V80\_256Video profile.</span></span> <span data-ttu-id="9b42c-105">此設定檔會使用 Windows Media 音訊和 Windows Media 視訊第8版編解碼器，而不像 Windows Media 9 系列編解碼器一樣。</span><span class="sxs-lookup"><span data-stu-id="9b42c-105">This profile uses the Windows Media Audio and Windows Media Video version 8 codecs, which are not as recent as the Windows Media 9 Series codecs.</span></span> <span data-ttu-id="9b42c-106">建議您建立自訂設定檔，以使用 Windows Media 9 系列編解碼器，並使用自訂設定檔設定 WM ASF 寫入器，如設定 [設定檔和其他 ASF 檔案屬性](configuring-profiles-and-other-asf-file-properties.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="9b42c-106">It is recommended to create a custom profile that uses the Windows Media 9 Series codecs, and configure the WM ASF Writer with the custom profile, as described in [Configuring Profiles and Other ASF File Properties](configuring-profiles-and-other-asf-file-properties.md).</span></span> <span data-ttu-id="9b42c-107">在設定篩選之前，您必須先將 WM ASF 寫入器篩選器新增至篩選圖形，並先設定篩選器，再將它連接到其他任何篩選器。</span><span class="sxs-lookup"><span data-stu-id="9b42c-107">You must add the WM ASF Writer filter to the filter graph before configuring the filter, and configure the filter before connecting it to any other filters.</span></span>

<span data-ttu-id="9b42c-108">所有輸入的資料都必須加上時間戳記，而且必須先連接所有輸入的 pin，然後才能執行或暫停篩選。</span><span class="sxs-lookup"><span data-stu-id="9b42c-108">All input data must be time-stamped, and all input pins must be connected before the filter can be run or paused.</span></span> <span data-ttu-id="9b42c-109">因此，如果您使用具有音訊串流和影片串流的設定檔來設定篩選準則，則篩選準則會建立音訊和影片輸入的 pin，而且必須先連接這兩個 pin，然後才能執行篩選。</span><span class="sxs-lookup"><span data-stu-id="9b42c-109">Therefore, if you configure the filter with a profile that has an audio stream and a video stream, the filter will create an audio and a video input pin, and both pins must be connected before the filter can be run.</span></span> <span data-ttu-id="9b42c-110">由於 Windows Media Format SDK 需要音訊串流才能運作，因此，即使是針對虛擬資料流程（也就是靜音的低位速率音訊串流），WM ASF 寫入器一律必須有輸入音訊 pin。</span><span class="sxs-lookup"><span data-stu-id="9b42c-110">Because the Windows Media Format SDK requires an audio stream to work, the WM ASF Writer must always have an input audio pin, even if it is for a dummy stream—that is, a muted, low-bit-rate audio stream.</span></span>

<span data-ttu-id="9b42c-111">新增資料單位延伸模組</span><span class="sxs-lookup"><span data-stu-id="9b42c-111">Adding Data Unit Extensions</span></span>

<span data-ttu-id="9b42c-112">您可以設定資料單位延伸模組的設定檔串流，例如在連接篩選器之前或之後的 SMPTE 時間代碼，只要遵循此作業順序：</span><span class="sxs-lookup"><span data-stu-id="9b42c-112">You can configure a profile stream for data unit extensions, such as SMPTE time codes, either before or after the filter is connected, as long as you follow this order of operations:</span></span>

1.  <span data-ttu-id="9b42c-113">使用 **IWMStreamConfig2：： AddDataUnitExtension**，將一個或多個資料單位延伸加入至資料流程。</span><span class="sxs-lookup"><span data-stu-id="9b42c-113">Add one or more data unit extensions to the stream using **IWMStreamConfig2::AddDataUnitExtension**.</span></span>
2.  <span data-ttu-id="9b42c-114">呼叫 **IWMProfile：： ReconfigStream** 來更新設定檔。</span><span class="sxs-lookup"><span data-stu-id="9b42c-114">Call **IWMProfile::ReconfigStream** to update the profile.</span></span>
3.  <span data-ttu-id="9b42c-115">以更新的設定檔物件呼叫 [**IConfigAsfWriter：： ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) 。</span><span class="sxs-lookup"><span data-stu-id="9b42c-115">Call [**IConfigAsfWriter::ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) with the updated profile object.</span></span>
4.  <span data-ttu-id="9b42c-116">尋找影片輸入 pin，並呼叫其 [**IAMWMBufferPass：： SetNotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) 方法來註冊您的應用程式定義 [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) 介面。</span><span class="sxs-lookup"><span data-stu-id="9b42c-116">Find the video input pin, and call its [**IAMWMBufferPass::SetNotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) method to register your application-defined [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) interface.</span></span>

<span data-ttu-id="9b42c-117">當圖形執行時，將會針對每個框架呼叫 [**IAMWMBufferPassCallback：： Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) 方法，而且您將可以使用其 **INSSBuffer3** 介面方法來取得和設定範例上的屬性。</span><span class="sxs-lookup"><span data-stu-id="9b42c-117">When the graph runs, your [**IAMWMBufferPassCallback::Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) method will be called for each frame, and you will be able to get and set properties on the sample using its **INSSBuffer3** interface methods.</span></span>

> [!Note]  
> <span data-ttu-id="9b42c-118">在某些耗用大量處理器的案例中，例如反向電視的情況下，WM ASF 寫入器可能需要的輸出緩衝區比某些下游篩選器可支援的更多。</span><span class="sxs-lookup"><span data-stu-id="9b42c-118">In some processor-intensive scenarios such as inverse telecine, the WM ASF Writer may require more output buffers than some downstream filters can support.</span></span> <span data-ttu-id="9b42c-119">例如，DV 解碼器將不會接受一個以上的緩衝區作為輸出 pin，而且在某些情況下，AVI 解壓縮程式也是如此。</span><span class="sxs-lookup"><span data-stu-id="9b42c-119">The DV Decoder, for example, will not accept more than one buffer for its output pin and the same is true for the AVI Decompressor in certain conditions.</span></span> <span data-ttu-id="9b42c-120">如果您在嘗試連線至這些篩選器時遇到問題，或在執行圖形時遇到問題，可能需要撰寫可接受其輸出 pin 上任意數目緩衝區的中繼篩選。</span><span class="sxs-lookup"><span data-stu-id="9b42c-120">If you encounter problems when attempting to connect to these filters, or possibly when running the graph, it may be necessary to write an intermediary filter that accepts any number of buffers on its output pin.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9b42c-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="9b42c-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b42c-122">在 DirectShow 中建立 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="9b42c-122">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



