---
description: DV 攝影機的外部裝置介面
ms.assetid: 001321c5-70c7-4baa-ba5a-1e424ca0d647
title: DV 攝影機的外部裝置介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e52b6d0fe00ff91ff87e9c810bbe7ecc319e9bfd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846880"
---
# <a name="external-device-interfaces-for-dv-camcorders"></a><span data-ttu-id="dd3a0-103">DV 攝影機的外部裝置介面</span><span class="sxs-lookup"><span data-stu-id="dd3a0-103">External Device Interfaces for DV Camcorders</span></span>

<span data-ttu-id="dd3a0-104">[WDM 影片捕獲](wdm-video-capture-filter.md)篩選器會公開三個介面來控制攝影機。</span><span class="sxs-lookup"><span data-stu-id="dd3a0-104">The [WDM Video Capture](wdm-video-capture-filter.md) filter exposes three interfaces for controlling a camcorder.</span></span>



|                                                |                                                 |
|------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="dd3a0-105">**IAMExtDevice**</span><span class="sxs-lookup"><span data-stu-id="dd3a0-105">**IAMExtDevice**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamextdevice)           | <span data-ttu-id="dd3a0-106">外部裝置控制的基底介面。</span><span class="sxs-lookup"><span data-stu-id="dd3a0-106">The base interface for external device control.</span></span> |
| [<span data-ttu-id="dd3a0-107">**IAMExtTransport**</span><span class="sxs-lookup"><span data-stu-id="dd3a0-107">**IAMExtTransport**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)     | <span data-ttu-id="dd3a0-108">控制 VCR 函數。</span><span class="sxs-lookup"><span data-stu-id="dd3a0-108">Controls the VCR functions.</span></span>                     |
| [<span data-ttu-id="dd3a0-109">**IAMTimecodeReader**</span><span class="sxs-lookup"><span data-stu-id="dd3a0-109">**IAMTimecodeReader**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) | <span data-ttu-id="dd3a0-110">從裝置讀取時間碼。</span><span class="sxs-lookup"><span data-stu-id="dd3a0-110">Reads timecode from the device.</span></span>                 |



 

> [!Note]  
> <span data-ttu-id="dd3a0-111">若要搭配使用這些介面與 MSDV 攝影機驅動程式，請在您的專案中包含標頭檔 XPrtDefs。</span><span class="sxs-lookup"><span data-stu-id="dd3a0-111">To use these interfaces with the MSDV camcorder driver, include the header file XPrtDefs.h in your project.</span></span>

 

<span data-ttu-id="dd3a0-112">在您選取 capture 裝置並建立 capture 篩選器的實例之後，請查詢這些介面的篩選。</span><span class="sxs-lookup"><span data-stu-id="dd3a0-112">After you select a capture device and create an instance of the capture filter, query the filter for these interfaces.</span></span> <span data-ttu-id="dd3a0-113">下列範例會宣告保存介面指標的自訂結構，以及指定每個介面可用性的布林值：</span><span class="sxs-lookup"><span data-stu-id="dd3a0-113">The following example declares a custom structure that holds the interface pointers, along with Boolean values that specify the availability of each interface:</span></span>


```C++
struct _MyDevCap
{
    IAMExtDevice       *pDevice;
    IAMExtTransport    *pTransport;
    IAMTimecodeReader  *pTimecode;
    BOOL                bHasDevice;
    BOOL                bHasTransport;
    BOOL                bHasTimecode;
} MyDevCap;

HRESULT hr;
IBaseFilter *pDVCam;  // Pointer to the capture filter.

// Create an instance of the capture filter (not shown).

hr = pDVCam->QueryInterface(IID_IAMExtDevice, (void **)&MyDevCap.pDevice);
MyDevCap.bHasDevice = (SUCCEEDED(hr));

hr = pDVCam->QueryInterface(IID_IAMExtTransport, (void **)&MyDevCap.pTransport);
MyDevCap.bHasTransport = (SUCCEEDED(hr));

hr = pDVCam->QueryInterface(IID_IAMTimecodeReader, (void **)&MyDevCap.pTimecode);
MyDevCap.bHasTimecode = (SUCCEEDED(hr));
```



## <a name="related-topics"></a><span data-ttu-id="dd3a0-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="dd3a0-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd3a0-115">控制 DV 攝像機</span><span class="sxs-lookup"><span data-stu-id="dd3a0-115">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



