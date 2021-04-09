---
description: EVRPresenter 範例
ms.assetid: 791a9816-4c40-4683-8b32-22f73d7fe84d
title: EVRPresenter 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bde85de152c41f348b1aae74a8c0d67ca746cab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111773"
---
# <a name="evrpresenter-sample"></a><span data-ttu-id="1b9f4-103">EVRPresenter 範例</span><span class="sxs-lookup"><span data-stu-id="1b9f4-103">EVRPresenter Sample</span></span>

<span data-ttu-id="1b9f4-104">示範如何將 [增強型影片](enhanced-video-renderer.md) 轉譯器的自訂展示者 (EVR) 。</span><span class="sxs-lookup"><span data-stu-id="1b9f4-104">Shows how to implement a custom presenter for the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span> <span data-ttu-id="1b9f4-105">自訂展示者可以與 DirectShow EVR 濾波器或 Microsoft 媒體基礎 EVR 接收器搭配使用。</span><span class="sxs-lookup"><span data-stu-id="1b9f4-105">The custom presenter can be used with either the DirectShow EVR filter or the Microsoft Media Foundation EVR sink.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="1b9f4-106">示範的 Api</span><span class="sxs-lookup"><span data-stu-id="1b9f4-106">APIs Demonstrated</span></span>

<span data-ttu-id="1b9f4-107">這個範例會示範下列媒體基礎介面：</span><span class="sxs-lookup"><span data-stu-id="1b9f4-107">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="1b9f4-108">**IMFClockStateSink**</span><span class="sxs-lookup"><span data-stu-id="1b9f4-108">**IMFClockStateSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [<span data-ttu-id="1b9f4-109">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="1b9f4-109">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [<span data-ttu-id="1b9f4-110">**IMFTopologyServiceLookupClient**</span><span class="sxs-lookup"><span data-stu-id="1b9f4-110">**IMFTopologyServiceLookupClient**</span></span>](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient)
-   [<span data-ttu-id="1b9f4-111">**IMFVideoDeviceID**</span><span class="sxs-lookup"><span data-stu-id="1b9f4-111">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)
-   [<span data-ttu-id="1b9f4-112">**IMFVideoDisplayControl**</span><span class="sxs-lookup"><span data-stu-id="1b9f4-112">**IMFVideoDisplayControl**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)
-   [<span data-ttu-id="1b9f4-113">**IMFVideoPresenter**</span><span class="sxs-lookup"><span data-stu-id="1b9f4-113">**IMFVideoPresenter**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopresenter)

## <a name="usage"></a><span data-ttu-id="1b9f4-114">使用方式</span><span class="sxs-lookup"><span data-stu-id="1b9f4-114">Usage</span></span>

<span data-ttu-id="1b9f4-115">EVRPresenter 範例會建立一個 DLL，它是展示者的 COM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="1b9f4-115">The EVRPresenter sample builds a DLL that is a COM server for the presenter.</span></span> <span data-ttu-id="1b9f4-116">使用自訂展示者之前，您必須先註冊 DLL。</span><span class="sxs-lookup"><span data-stu-id="1b9f4-116">Before using the custom presenter, you must register the DLL.</span></span>

<span data-ttu-id="1b9f4-117">若要在媒體基礎中使用此範例：</span><span class="sxs-lookup"><span data-stu-id="1b9f4-117">To use this sample in Media Foundation:</span></span>

1.  <span data-ttu-id="1b9f4-118">建置範例。</span><span class="sxs-lookup"><span data-stu-id="1b9f4-118">Build the sample.</span></span>
2.  <span data-ttu-id="1b9f4-119">Regsvr32 EvrPresenter.dll。</span><span class="sxs-lookup"><span data-stu-id="1b9f4-119">Regsvr32 EvrPresenter.dll.</span></span>
3.  <span data-ttu-id="1b9f4-120">建立並執行 [MFPlayer 範例](/previous-versions//bb970516(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1b9f4-120">Build and run the [MFPlayer Sample](/previous-versions//bb970516(v=vs.85)).</span></span>
4.  <span data-ttu-id="1b9f4-121">從 [ **檔案** ] 功能表選取 [ **開啟** 檔案]。</span><span class="sxs-lookup"><span data-stu-id="1b9f4-121">From the **File** menu, select **Open** File.</span></span>
5.  <span data-ttu-id="1b9f4-122">在 [ **開啟** 檔案] 對話方塊中，選取 [ **自訂 EVR 展示者]。**</span><span class="sxs-lookup"><span data-stu-id="1b9f4-122">In the **Open File** dialog box, select **Custom EVR Presenter.**</span></span>
6.  <span data-ttu-id="1b9f4-123">選取要播放的檔案。</span><span class="sxs-lookup"><span data-stu-id="1b9f4-123">Select a file for playback.</span></span>

<span data-ttu-id="1b9f4-124">若要在 DirectShow 中使用此範例：</span><span class="sxs-lookup"><span data-stu-id="1b9f4-124">To use this sample in DirectShow:</span></span>

1.  <span data-ttu-id="1b9f4-125">建置範例。</span><span class="sxs-lookup"><span data-stu-id="1b9f4-125">Build the sample.</span></span>
2.  <span data-ttu-id="1b9f4-126">註冊 EvrPresenter.dll。</span><span class="sxs-lookup"><span data-stu-id="1b9f4-126">Register EvrPresenter.dll.</span></span>
3.  <span data-ttu-id="1b9f4-127">建立並執行 EVRPlayer 範例。</span><span class="sxs-lookup"><span data-stu-id="1b9f4-127">Build and run the EVRPlayer sample.</span></span> <span data-ttu-id="1b9f4-128">此範例隨附于 Windows SDK 中的 DirectShow 範例。</span><span class="sxs-lookup"><span data-stu-id="1b9f4-128">This sample is included with the DirectShow samples in the Windows SDK.</span></span>
4.  <span data-ttu-id="1b9f4-129">**在 [檔案**] 功能表中，選取 [EVR 展示 **者**]。</span><span class="sxs-lookup"><span data-stu-id="1b9f4-129">From the **File** menu, select **EVR Presenter**.</span></span>
5.  <span data-ttu-id="1b9f4-130">選取要播放的檔案。</span><span class="sxs-lookup"><span data-stu-id="1b9f4-130">Select a file for playback.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b9f4-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="1b9f4-131">Requirements</span></span>



| <span data-ttu-id="1b9f4-132">產品</span><span class="sxs-lookup"><span data-stu-id="1b9f4-132">Product</span></span>                                                        | <span data-ttu-id="1b9f4-133">版本</span><span class="sxs-lookup"><span data-stu-id="1b9f4-133">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="1b9f4-134">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="1b9f4-134">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="1b9f4-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1b9f4-135">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="1b9f4-136">下載範例</span><span class="sxs-lookup"><span data-stu-id="1b9f4-136">Downloading the Sample</span></span>

<span data-ttu-id="1b9f4-137">此範例可在 [Windows 傳統範例 github 存放庫](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip)中取得。</span><span class="sxs-lookup"><span data-stu-id="1b9f4-137">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b9f4-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="1b9f4-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b9f4-139">增強的影片轉譯器</span><span class="sxs-lookup"><span data-stu-id="1b9f4-139">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> <dt>

[<span data-ttu-id="1b9f4-140">如何撰寫 EVR 展示者</span><span class="sxs-lookup"><span data-stu-id="1b9f4-140">How to Write an EVR Presenter</span></span>](how-to-write-an-evr-presenter.md)
</dt> <dt>

[<span data-ttu-id="1b9f4-141">媒體基礎 SDK 範例</span><span class="sxs-lookup"><span data-stu-id="1b9f4-141">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> </dl>

 

 
