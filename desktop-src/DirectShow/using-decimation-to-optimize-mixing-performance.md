---
description: 使用減去優化混合效能
ms.assetid: 94d4ce86-9d60-4fd4-ab01-851dc073680b
title: 使用減去優化混合效能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e9e4ddfe3bbba3eb5eeab91b7cf0e8b9cbfa03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850343"
---
# <a name="using-decimation-to-optimize-mixing-performance"></a><span data-ttu-id="5fc7a-103">使用減去優化混合效能</span><span class="sxs-lookup"><span data-stu-id="5fc7a-103">Using Decimation to Optimize Mixing Performance</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5fc7a-104">本節所述的優化高度取決於基礎硬體。</span><span class="sxs-lookup"><span data-stu-id="5fc7a-104">The optimization described in this section is highly dependent on the underlying hardware.</span></span> <span data-ttu-id="5fc7a-105">除非您可以保證應用程式會使用何種類型的圖形硬體，否則可能會嚴重降低影片影像的外觀。</span><span class="sxs-lookup"><span data-stu-id="5fc7a-105">Unless you can guarantee what type of graphics hardware will be used with the application, it may seriously degrade the appearance of the video image.</span></span>

 

<span data-ttu-id="5fc7a-106">HDTV 需要大量的處理能力，但在較新的系統上，大部分都是由圖形配接器來提供。</span><span class="sxs-lookup"><span data-stu-id="5fc7a-106">HDTV requires a lot of processing power, which on newer systems is provided mostly by the graphics card.</span></span> <span data-ttu-id="5fc7a-107">但是，即使圖形配接器和解碼器可支援1920x1080 的解析度，使用者也不一定會將其監視設定為此解決方案。</span><span class="sxs-lookup"><span data-stu-id="5fc7a-107">But even if the graphics card and the decoder can support resolutions of 1920x1080, the user may not always have their monitor set to this resolution.</span></span> <span data-ttu-id="5fc7a-108">在此情況下，需要圖形晶片才能建立 1920 x 1080 映射，然後在將其傳送至框架緩衝區之前，先減少解析度。</span><span class="sxs-lookup"><span data-stu-id="5fc7a-108">In this case, the graphics chip is required to create a 1920 x 1080 image, and then reduce the resolution before sending it to the frame buffer.</span></span>

<span data-ttu-id="5fc7a-109">因為這會浪費處理能力，所以 VMR 會提供一種方法來刪減 (在轉譯至 DirectDraw 表面時，減少影像) 。</span><span class="sxs-lookup"><span data-stu-id="5fc7a-109">Since this is a waste of processing power, the VMR provides a way to decimate (reduce) the image at the time it is being rendered onto the DirectDraw surface.</span></span> <span data-ttu-id="5fc7a-110">如果映射必須在轉譯後調整大小，就不需要額外的記憶體複製。</span><span class="sxs-lookup"><span data-stu-id="5fc7a-110">This eliminates the extra memory copy required if the image has to be resized after it has been rendered.</span></span>

<span data-ttu-id="5fc7a-111">**VMR-7：** 若要啟用減去，請使用 MixerPref DecimateOutput 旗標來呼叫 [**IVMRMixerControl：： SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) \_ 。</span><span class="sxs-lookup"><span data-stu-id="5fc7a-111">**VMR-7:** To enable decimation, call [**IVMRMixerControl::SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) with the MixerPref\_DecimateOutput flag.</span></span>

<span data-ttu-id="5fc7a-112">**VMR-9：** 若要啟用減去，請使用 MixerPref9 DecimateOutput 旗標來呼叫 [**IVMRMixerControl9：： SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) \_ 。</span><span class="sxs-lookup"><span data-stu-id="5fc7a-112">**VMR-9:** To enable decimation, call [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) with the MixerPref9\_DecimateOutput flag.</span></span>

<span data-ttu-id="5fc7a-113">您必須在 VMR 連接之前呼叫 **SetMixingPrefs** 方法。</span><span class="sxs-lookup"><span data-stu-id="5fc7a-113">The **SetMixingPrefs** method must be called before the VMR is connected.</span></span> <span data-ttu-id="5fc7a-114">當圖形正在執行時，不能變更混合喜好設定旗標。</span><span class="sxs-lookup"><span data-stu-id="5fc7a-114">The mixing preference flags cannot be changed once the graph is running.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5fc7a-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="5fc7a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5fc7a-116">使用 VMR 混合模式</span><span class="sxs-lookup"><span data-stu-id="5fc7a-116">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



