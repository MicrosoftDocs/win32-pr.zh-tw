---
description: 信號格式
ms.assetid: 8684972c-3233-49bf-8c34-ca644aca432a
title: 信號格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6983328729e0dc72d93c0e00a74e7e65a7f237
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846412"
---
# <a name="signal-format"></a><span data-ttu-id="d8d83-103">信號格式</span><span class="sxs-lookup"><span data-stu-id="d8d83-103">Signal Format</span></span>

<span data-ttu-id="d8d83-104">DV 攝像機的信號格式可以是 NTSC、PAL、標準或長時間播放。</span><span class="sxs-lookup"><span data-stu-id="d8d83-104">A DV camcorder's signal format can be NTSC or PAL, standard or long-play.</span></span>

<span data-ttu-id="d8d83-105">**MSDV 驅動程式**</span><span class="sxs-lookup"><span data-stu-id="d8d83-105">**MSDV Driver**</span></span>

<span data-ttu-id="d8d83-106">若要從 MSDV 驅動程式取得輸入信號格式，請呼叫 [**IAMExtTransport：： GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters) 方法並傳入 ED \_ TRANSBASIC \_ 輸入 \_ 信號旗標。</span><span class="sxs-lookup"><span data-stu-id="d8d83-106">To get the input signal format from the MSDV driver, call the [**IAMExtTransport::GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters) method and pass in the ED\_TRANSBASIC\_INPUT\_SIGNAL flag.</span></span> <span data-ttu-id="d8d83-107">方法會傳回定義的常數，表示格式。</span><span class="sxs-lookup"><span data-stu-id="d8d83-107">The method returns a defined constant, indicating the format.</span></span>

<span data-ttu-id="d8d83-108">下列程式碼會檢查信號格式，並使用此值來計算每個畫面格的平均時間。</span><span class="sxs-lookup"><span data-stu-id="d8d83-108">The following code checks the signal format, and uses this value to calculates the average time per frame.</span></span> <span data-ttu-id="d8d83-109">變數模式會接收信號格式常數。</span><span class="sxs-lookup"><span data-stu-id="d8d83-109">The variable Mode receives the signal-format constant.</span></span>


```C++
LONG Mode, AvgTimePerFrame;
hr = MyDevCap.pTransport->GetTransportBasicParameters(
        ED_TRANSBASIC_INPUT_SIGNAL, &Mode, NULL);
if (SUCCEEDED(hr))
{
    switch (Mode)
    {
    case ED_TRANSBASIC_SIGNAL_525_60_SD: // NTSC SD
        AvgTimePerFrame = 33;  // 33 msec (29.97 FPS)
        break;
    case ED_TRANSBASIC_SIGNAL_525_60_SDL: // NTSC SDL
        AvgTimePerFrame = 33;  
        break;
    case ED_TRANSBASIC_SIGNAL_625_50_SD: // PAL SD
        AvgTimePerFrame = 40;  // 40 msec (25 FPS)
        break;
    case ED_TRANSBASIC_SIGNAL_625_50_SDL: // PAL SDL
        AvgTimePerFrame = 40;  
        break;
    default: 
        // Unknown type
        AvgTimePerFrame = 33; // Default
        break;
    }
}
```



<span data-ttu-id="d8d83-110">若要取得輸出信號格式，請使用 ED \_ TRANSBASIC \_ 輸出信號旗標來呼叫相同的方法 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d8d83-110">To get the output signal format, call the same method with the ED\_TRANSBASIC\_OUTPUT\_SIGNAL flag.</span></span>

<span data-ttu-id="d8d83-111">**UVC 驅動程式**</span><span class="sxs-lookup"><span data-stu-id="d8d83-111">**UVC Driver**</span></span>

<span data-ttu-id="d8d83-112">若要從 UVC 驅動程式取得輸入或輸出信號格式，請在 pin 上呼叫 [**IAMStreamConfig：： >iformatprovider.getformat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) ，並檢查影片格式區塊。</span><span class="sxs-lookup"><span data-stu-id="d8d83-112">To get the input or output signal format from the UVC driver, call [**IAMStreamConfig::GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) on the pin and examine the video format block.</span></span> <span data-ttu-id="d8d83-113">針對 UVC 裝置 (，上述範例中所示的程式碼通常會傳回 ED \_ TRANSBASIC \_ 信號 \_ 未知，因此不可靠。 ) </span><span class="sxs-lookup"><span data-stu-id="d8d83-113">(For UVC devices, the code shown in the previous example usually returns ED\_TRANSBASIC\_SIGNAL\_UNKNOWN, so it is not reliable.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8d83-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="d8d83-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8d83-115">控制 DV 攝像機</span><span class="sxs-lookup"><span data-stu-id="d8d83-115">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



