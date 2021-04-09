---
description: 顯示 VFW 捕捉對話方塊
ms.assetid: 708212ca-d148-4079-8052-3bf6696a33ab
title: 顯示 VFW 捕捉對話方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45b8b51b164630a8fa6e91b2e68ca8a9a3a875b6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687503"
---
# <a name="display-vfw-capture-dialog-boxes"></a><span data-ttu-id="91557-103">顯示 VFW 捕捉對話方塊</span><span class="sxs-lookup"><span data-stu-id="91557-103">Display VFW Capture Dialog Boxes</span></span>

<span data-ttu-id="91557-104">仍使用 Windows (VFW) 驅動程式影片的捕獲裝置可支援下列任何三個對話方塊，可用來設定裝置。</span><span class="sxs-lookup"><span data-stu-id="91557-104">A capture device that still uses a Video for Windows (VFW) driver can support any of the following three dialog boxes, which are used to configure the device.</span></span>



| <span data-ttu-id="91557-105">對話方塊</span><span class="sxs-lookup"><span data-stu-id="91557-105">Dialog box</span></span>    | <span data-ttu-id="91557-106">描述</span><span class="sxs-lookup"><span data-stu-id="91557-106">Description</span></span>                                                                                           |
|---------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91557-107">影片來源</span><span class="sxs-lookup"><span data-stu-id="91557-107">Video Source</span></span>  | <span data-ttu-id="91557-108">用來選取影片輸入，以及調整裝置設定，例如圖片亮度或對比。</span><span class="sxs-lookup"><span data-stu-id="91557-108">Used to select the video input and to adjust device settings, such as picture brightness or contrast.</span></span> |
| <span data-ttu-id="91557-109">影片格式</span><span class="sxs-lookup"><span data-stu-id="91557-109">Video Format</span></span>  | <span data-ttu-id="91557-110">用來選取影像維度和位深度。</span><span class="sxs-lookup"><span data-stu-id="91557-110">Used to select the image dimensions and bit depth.</span></span>                                                    |
| <span data-ttu-id="91557-111">影片顯示</span><span class="sxs-lookup"><span data-stu-id="91557-111">Video Display</span></span> | <span data-ttu-id="91557-112">用來控制呈現影片的外觀。</span><span class="sxs-lookup"><span data-stu-id="91557-112">Used to control the appearance of the rendered video.</span></span>                                                 |



 

<span data-ttu-id="91557-113">若要顯示這些對話方塊的其中一個，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="91557-113">To show one of these dialog boxes, do the following:</span></span>

1.  <span data-ttu-id="91557-114">停止篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="91557-114">Stop the filter graph.</span></span>
2.  <span data-ttu-id="91557-115">查詢 [**IAMVfwCaptureDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs) 介面的 capture 篩選器。</span><span class="sxs-lookup"><span data-stu-id="91557-115">Query the capture filter for the [**IAMVfwCaptureDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs) interface.</span></span> <span data-ttu-id="91557-116">如果 **QueryInterface** 成功，則表示 capture 裝置為 VFW 裝置。</span><span class="sxs-lookup"><span data-stu-id="91557-116">If **QueryInterface** succeeds, it means the capture device is a VFW device.</span></span>
3.  <span data-ttu-id="91557-117">呼叫 [**IAMVfwCaptureDialogs：： HasDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-hasdialog) ，以檢查驅動程式是否支援您想要顯示的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="91557-117">Call [**IAMVfwCaptureDialogs::HasDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-hasdialog) to check if the driver supports the dialog box that you wish to display.</span></span> <span data-ttu-id="91557-118">[**VfwCaptureDialogs**](/windows/desktop/api/strmif/ne-strmif-vfwcapturedialogs)列舉會定義每個 VFW 對話方塊的旗標。</span><span class="sxs-lookup"><span data-stu-id="91557-118">The [**VfwCaptureDialogs**](/windows/desktop/api/strmif/ne-strmif-vfwcapturedialogs) enumeration defines flags for each of the VFW dialog boxes.</span></span> <span data-ttu-id="91557-119">如果支援此對話方塊， **HasDialog** 會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="91557-119">**HasDialog** returns S\_OK if the dialog box is supported.</span></span> <span data-ttu-id="91557-120">否則，它會傳回 \_ FALSE，因此請直接檢查值 s \_ OK，而不是使用 **SUCCEEDED** 宏。</span><span class="sxs-lookup"><span data-stu-id="91557-120">It returns S\_FALSE otherwise, so check for the value S\_OK directly, rather than using the **SUCCEEDED** macro.</span></span>
4.  <span data-ttu-id="91557-121">如果支援對話方塊，請呼叫 [**IAMVfwCaptureDialogs：： ShowDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-showdialog) 來顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="91557-121">If the dialog box is supported, call [**IAMVfwCaptureDialogs::ShowDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-showdialog) to display the dialog box.</span></span>
5.  <span data-ttu-id="91557-122">重新開機圖形。</span><span class="sxs-lookup"><span data-stu-id="91557-122">Restart the graph.</span></span>

<span data-ttu-id="91557-123">下列程式碼顯示 [影片來源] 對話方塊的下列步驟：</span><span class="sxs-lookup"><span data-stu-id="91557-123">The following code shows these steps for the Video Source dialog box:</span></span>


```C++
pControl->Stop(); // Stop the graph.

// Query the capture filter for the IAMVfwCaptureDialogs interface.
IAMVfwCaptureDialogs *pVfw = 0;
hr = pCap->QueryInterface(IID_IAMVfwCaptureDialogs, (void**)&pVfw);
if (SUCCEEDED(hr))
{
    // Check if the device supports this dialog box.
    if (S_OK == pVfw->HasDialog(VfwCaptureDialog_Source))
    {
        // Show the dialog box.
        hr = pVfw->ShowDialog(VfwCaptureDialog_Source, hwndParent);
    }
}
pControl->Run();
```



## <a name="related-topics"></a><span data-ttu-id="91557-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="91557-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91557-125">設定影片捕獲裝置</span><span class="sxs-lookup"><span data-stu-id="91557-125">Configuring a Video Capture Device</span></span>](configuring-a-video-capture-device.md)
</dt> </dl>

 

 



