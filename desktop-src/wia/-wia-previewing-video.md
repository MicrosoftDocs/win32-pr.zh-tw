---
description: IWiaVideo 介面可讓應用程式觀看影片，並從它中捕捉影像。
ms.assetid: 59eddbdc-4957-44be-a602-0763f3385e89
title: '預覽影片 (WIA) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 935625c1c16ceea66326963185dd75d96d98ed02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511613"
---
# <a name="previewing-video-wia"></a><span data-ttu-id="ada73-103">預覽影片 (WIA) </span><span class="sxs-lookup"><span data-stu-id="ada73-103">Previewing Video (WIA)</span></span>

<span data-ttu-id="ada73-104">[**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo)介面可讓應用程式觀看影片，並從它中捕捉影像。</span><span class="sxs-lookup"><span data-stu-id="ada73-104">The [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) interface enables an application to view video and capture still images from it.</span></span> <span data-ttu-id="ada73-105">請執行下列步驟來選取串流影片裝置，並在視窗中顯示影片串流。</span><span class="sxs-lookup"><span data-stu-id="ada73-105">Perform the following steps to select the streaming video device and display a video stream in a window.</span></span>

-   <span data-ttu-id="ada73-106">呼叫 [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 以取得 [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="ada73-106">Call [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to retrieve a pointer to the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) interface.</span></span>
-   <span data-ttu-id="ada73-107">使用 [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr)介面的 [**IWiaDevMgr：： EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo)方法，取得 [**IEnumWIA \_ 開發人員 \_ 資訊**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="ada73-107">Use the [**IWiaDevMgr::EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) method of the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) interface to obtain a pointer to the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) interface.</span></span> <span data-ttu-id="ada73-108">如需有關如何列舉裝置的指示，請參閱列舉系統裝置。</span><span class="sxs-lookup"><span data-stu-id="ada73-108">For instructions on how to enumerate devices, see Enumerating System Devices.</span></span>
-   <span data-ttu-id="ada73-109">使用 [**IEnumWIA \_ DEV \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) 介面取得找到的每個 WINDOWS 映射取得 (WIA) 裝置的 [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="ada73-109">Use the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) interface to obtain an [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface pointer for each Windows Image Acquisition (WIA) device found.</span></span>
-   <span data-ttu-id="ada73-110">使用 [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) 介面取得所需裝置的 DeviceID 屬性。</span><span class="sxs-lookup"><span data-stu-id="ada73-110">Use the [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface to get the DeviceID property of the desired device.</span></span> <span data-ttu-id="ada73-111">串流影片裝置具有 [WIA \_ DIP \_ 開發 \_ 類型] 屬性集的 StiDeviceTypeStreamingVideo 旗標。</span><span class="sxs-lookup"><span data-stu-id="ada73-111">A streaming video device has the StiDeviceTypeStreamingVideo flag of the WIA\_DIP\_DEV\_TYPE property set.</span></span>
-   <span data-ttu-id="ada73-112">使用 [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) 介面取得 [WIA \_ DPV IMAGES] \_ \_ 目錄屬性值。</span><span class="sxs-lookup"><span data-stu-id="ada73-112">Use the [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface to get the WIA\_DPV\_IMAGES\_DIRECTORY property value.</span></span>
-   <span data-ttu-id="ada73-113">呼叫 [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 以取得 [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="ada73-113">Call [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to retrieve a pointer to the [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) interface.</span></span>
-   <span data-ttu-id="ada73-114">將 [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo)介面的 [**IWiaVideo：： ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory)屬性設定為從 WIA \_ DPV \_ IMAGES \_ 目錄屬性值收到的值。</span><span class="sxs-lookup"><span data-stu-id="ada73-114">Set the [**IWiaVideo::ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) property of the [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) interface to the value received from the WIA\_DPV\_IMAGES\_DIRECTORY property value.</span></span>
-   <span data-ttu-id="ada73-115">在 [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo)介面上呼叫 [**IWiaVideo：： CreateVideoByWiaDevID**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-createvideobywiadevid) ，並傳遞串流映射裝置的裝置識別碼，以及要顯示影片的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="ada73-115">Call [**IWiaVideo::CreateVideoByWiaDevID**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-createvideobywiadevid) on the [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) interface, passing the device ID of the streaming image device and the handle of the window in which the video is to be displayed.</span></span>

> [!Note]  
> <span data-ttu-id="ada73-116">WIA 不支援 Windows Server 2003、Windows Vista 或更新版本中的影片裝置。</span><span class="sxs-lookup"><span data-stu-id="ada73-116">WIA does not support video devices in Windows Server 2003, Windows Vista, or later.</span></span> <span data-ttu-id="ada73-117">針對這些版本的 Windows，請使用 [DirectShow](/previous-versions//ms783323(v=vs.85)) 從影片取得影像。</span><span class="sxs-lookup"><span data-stu-id="ada73-117">For those versions of the Windows, use [DirectShow](/previous-versions//ms783323(v=vs.85)) to acquire images from video.</span></span>

 

 

 
