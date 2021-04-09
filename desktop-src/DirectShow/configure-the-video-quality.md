---
description: 本主題說明應用程式如何以程式設計方式變更影片捕獲裝置上的影像和相機設定。
ms.assetid: f789db78-292e-4092-a5dc-1906845fb1dd
title: 設定影片品質
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cb8d2d28e39f0083aac521f1953ebbb1ca8d5b6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687704"
---
# <a name="configure-the-video-quality"></a><span data-ttu-id="fa257-103">設定影片品質</span><span class="sxs-lookup"><span data-stu-id="fa257-103">Configure the Video Quality</span></span>

<span data-ttu-id="fa257-104">本主題說明應用程式如何以程式設計方式變更影片捕獲裝置上的影像和相機設定。</span><span class="sxs-lookup"><span data-stu-id="fa257-104">This topic describes how an application can programmatically change the image and camera settings on a video capture device.</span></span>

-   [<span data-ttu-id="fa257-105">ProcAmp 設定</span><span class="sxs-lookup"><span data-stu-id="fa257-105">ProcAmp Settings</span></span>](#procamp-settings)
-   [<span data-ttu-id="fa257-106">照相機設定</span><span class="sxs-lookup"><span data-stu-id="fa257-106">Camera Settings</span></span>](#camera-settings)
-   [<span data-ttu-id="fa257-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="fa257-107">Related topics</span></span>](#related-topics)

## <a name="procamp-settings"></a><span data-ttu-id="fa257-108">ProcAmp 設定</span><span class="sxs-lookup"><span data-stu-id="fa257-108">ProcAmp Settings</span></span>

<span data-ttu-id="fa257-109">Windows Driver Model (WDM) 視頻攝影機可以支援控制影像品質的屬性：</span><span class="sxs-lookup"><span data-stu-id="fa257-109">Windows Driver Model (WDM) video cameras can support properties that control the quality of the image:</span></span>

-   <span data-ttu-id="fa257-110">背光補償</span><span class="sxs-lookup"><span data-stu-id="fa257-110">Backlight compensation</span></span>
-   <span data-ttu-id="fa257-111">亮度</span><span class="sxs-lookup"><span data-stu-id="fa257-111">Brightness</span></span>
-   <span data-ttu-id="fa257-112">這個</span><span class="sxs-lookup"><span data-stu-id="fa257-112">Contrast</span></span>
-   <span data-ttu-id="fa257-113">獲得</span><span class="sxs-lookup"><span data-stu-id="fa257-113">Gain</span></span>
-   <span data-ttu-id="fa257-114">色差補正</span><span class="sxs-lookup"><span data-stu-id="fa257-114">Gamma</span></span>
-   <span data-ttu-id="fa257-115">色調</span><span class="sxs-lookup"><span data-stu-id="fa257-115">Hue</span></span>
-   <span data-ttu-id="fa257-116">飽和度</span><span class="sxs-lookup"><span data-stu-id="fa257-116">Saturation</span></span>
-   <span data-ttu-id="fa257-117">清晰度</span><span class="sxs-lookup"><span data-stu-id="fa257-117">Sharpness</span></span>
-   <span data-ttu-id="fa257-118">白平衡</span><span class="sxs-lookup"><span data-stu-id="fa257-118">White balance</span></span>

<span data-ttu-id="fa257-119">這些屬性是透過 [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) 介面來控制。</span><span class="sxs-lookup"><span data-stu-id="fa257-119">These properties are controlled through the [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) interface.</span></span> <span data-ttu-id="fa257-120">使用此介面，如下所示：</span><span class="sxs-lookup"><span data-stu-id="fa257-120">Use this interface as follows:</span></span>

1.  <span data-ttu-id="fa257-121">在 [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp)介面的 capture 篩選器上呼叫 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 。</span><span class="sxs-lookup"><span data-stu-id="fa257-121">Call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the capture filter for the [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) interface.</span></span>
2.  <span data-ttu-id="fa257-122">針對您想要設定的每個屬性，呼叫 [**IAMVideoProcAmp：： GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) 方法。</span><span class="sxs-lookup"><span data-stu-id="fa257-122">For each property that you want to set, call the [**IAMVideoProcAmp::GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) method.</span></span> <span data-ttu-id="fa257-123">屬性是由 [**VideoProcAmpProperty**](/windows/win32/api/strmif/ne-strmif-videoprocampproperty) 列舉所指定。</span><span class="sxs-lookup"><span data-stu-id="fa257-123">Properties are specified by the [**VideoProcAmpProperty**](/windows/win32/api/strmif/ne-strmif-videoprocampproperty) enumeration.</span></span> <span data-ttu-id="fa257-124">如果 **GetRange** 方法失敗，則表示相機不支援該特定屬性。</span><span class="sxs-lookup"><span data-stu-id="fa257-124">If the **GetRange** method fails, it means the camera does not support that particular property.</span></span>
3.  <span data-ttu-id="fa257-125">如果 [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) 成功，它會傳回屬性的支援值範圍、預設值，以及最小增量。</span><span class="sxs-lookup"><span data-stu-id="fa257-125">If [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) succeeds, it returns the range of supported values for the property, the default value, and the minimum increment.</span></span>
4.  <span data-ttu-id="fa257-126">若要取得屬性目前的值，請呼叫 [**IAMVideoProcAmp：： get**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-get)。</span><span class="sxs-lookup"><span data-stu-id="fa257-126">To get the current value of a property, call [**IAMVideoProcAmp::Get**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-get).</span></span>
5.  <span data-ttu-id="fa257-127">若要設定屬性，請呼叫 [**IAMVideoProcAmp：： set**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-set) 方法。</span><span class="sxs-lookup"><span data-stu-id="fa257-127">To set a property, call the [**IAMVideoProcAmp::Set**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-set) method.</span></span> <span data-ttu-id="fa257-128">若要將屬性還原為預設值，請呼叫 [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) 來尋找預設值，並將該值傳遞至 **Set** 方法。</span><span class="sxs-lookup"><span data-stu-id="fa257-128">To restore a property to its default value, call [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) to find the default and pass that value to the **Set** method.</span></span>

<span data-ttu-id="fa257-129">當您設定屬性時，不需要停止篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="fa257-129">You do not have to stop the filter graph when you set the properties.</span></span>

<span data-ttu-id="fa257-130">下列程式碼會設定 [程式碼] 控制項，讓它可以用來設定亮度。</span><span class="sxs-lookup"><span data-stu-id="fa257-130">The following code configures a trackbar control so that it can be used to set the brightness.</span></span> <span data-ttu-id="fa257-131">涵蓋範圍的範圍對應至裝置所支援的亮度範圍，而對應項的位置則對應于裝置的初始亮度設定。</span><span class="sxs-lookup"><span data-stu-id="fa257-131">The range of the trackbar corresponds to the brightness range that the device supports, and position of the trackbar corresponds to the device's initial brightness setting.</span></span>


```C++
HWND hTrackbar; // Handle to the trackbar control. 
// Initialize hTrackbar (not shown).

// Query the capture filter for the IAMVideoProcAmp interface.
IAMVideoProcAmp *pProcAmp = 0;
hr = pCap->QueryInterface(IID_IAMVideoProcAmp, (void**)&pProcAmp);
if (FAILED(hr))
{
    // The device does not support IAMVideoProcAmp, so disable the control.
    EnableWindow(hTrackbar, FALSE);
}
else
{
    long Min, Max, Step, Default, Flags, Val;

    // Get the range and default value. 
    hr = m_pProcAmp->GetRange(VideoProcAmp_Brightness, &Min, &Max, &Step,
        &Default, &Flags);
    if (SUCCEEDED(hr))
    {
        // Get the current value.
        hr = m_pProcAmp->Get(VideoProcAmp_Brightness, &Val, &Flags);
    }
    if (SUCCEEDED(hr))
    {
        // Set the trackbar range and position.
        SendMessage(hTrackbar, TBM_SETRANGE, TRUE, MAKELONG(Min, Max));
        SendMessage(hTrackbar, TBM_SETPOS, TRUE, Val);
        EnableWindow(hTrackbar, TRUE);
    }
    else
    {
        // This property is not supported, so disable the control.
        EnableWindow(hTrackbar, FALSE);
    }
}
```



## <a name="camera-settings"></a><span data-ttu-id="fa257-132">照相機設定</span><span class="sxs-lookup"><span data-stu-id="fa257-132">Camera Settings</span></span>

<span data-ttu-id="fa257-133">[**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol)介面類別似于 [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp)，但會控制攝影機本身的各種不同的功能：</span><span class="sxs-lookup"><span data-stu-id="fa257-133">The [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol) interface is similar to [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp), but controls various setttings on the camera itself:</span></span>

-   <span data-ttu-id="fa257-134">曝光</span><span class="sxs-lookup"><span data-stu-id="fa257-134">Exposure</span></span>
-   <span data-ttu-id="fa257-135">焦點</span><span class="sxs-lookup"><span data-stu-id="fa257-135">Focus</span></span>
-   <span data-ttu-id="fa257-136">虹膜</span><span class="sxs-lookup"><span data-stu-id="fa257-136">Iris</span></span>
-   <span data-ttu-id="fa257-137">移動瀏覽</span><span class="sxs-lookup"><span data-stu-id="fa257-137">Pan</span></span>
-   <span data-ttu-id="fa257-138">Roll</span><span class="sxs-lookup"><span data-stu-id="fa257-138">Roll</span></span>
-   <span data-ttu-id="fa257-139">傾斜</span><span class="sxs-lookup"><span data-stu-id="fa257-139">Tilt</span></span>
-   <span data-ttu-id="fa257-140">Zoom</span><span class="sxs-lookup"><span data-stu-id="fa257-140">Zoom</span></span>

<span data-ttu-id="fa257-141">若要使用此介面，請依照用於 [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp)的相同步驟執行：</span><span class="sxs-lookup"><span data-stu-id="fa257-141">To use this interface, follow the same steps used for [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp):</span></span>

1.  <span data-ttu-id="fa257-142">查詢 [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol)的捕獲篩選。</span><span class="sxs-lookup"><span data-stu-id="fa257-142">Query the capture filter for the [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol).</span></span>
2.  <span data-ttu-id="fa257-143">呼叫 [**IAMCameraControl：： GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-getrange) ，尋找支援的設定，以及每個設定的可能範圍。</span><span class="sxs-lookup"><span data-stu-id="fa257-143">Call [**IAMCameraControl::GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-getrange) to find which settings are supported, and the possible range for each settings.</span></span>
3.  <span data-ttu-id="fa257-144">呼叫 [**IAMCameraControl：： get**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-get) 以取得設定的目前值。</span><span class="sxs-lookup"><span data-stu-id="fa257-144">Call [**IAMCameraControl::Get**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-get) to get the current value of a setting.</span></span>
4.  <span data-ttu-id="fa257-145">呼叫 [**IAMCameraControl：： set**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-set) 來設定值。</span><span class="sxs-lookup"><span data-stu-id="fa257-145">Call [**IAMCameraControl::Set**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-set) to set the value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa257-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="fa257-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa257-147">設定影片捕獲裝置</span><span class="sxs-lookup"><span data-stu-id="fa257-147">Configuring a Video Capture Device</span></span>](configuring-a-video-capture-device.md)
</dt> </dl>

 

 
