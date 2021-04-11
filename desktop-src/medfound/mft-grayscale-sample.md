---
description: 說明如何將影片效果實作為媒體基礎轉換 (MFT) 。
ms.assetid: ad7d20bc-5eab-4390-a48b-5ea8e97ead7d
title: MFT_Grayscale 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 273c562eb5985d0a329c434a8e4aa44119744496
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114393"
---
# <a name="mft_grayscale-sample"></a><span data-ttu-id="a12b5-103">MFT \_ 灰階範例</span><span class="sxs-lookup"><span data-stu-id="a12b5-103">MFT\_Grayscale Sample</span></span>

<span data-ttu-id="a12b5-104">說明如何將影片效果實作為媒體基礎轉換 (MFT) 。</span><span class="sxs-lookup"><span data-stu-id="a12b5-104">Shows how to implement a video effect as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="a12b5-105">灰階 MFT 可將影片中的色度值設定為中性，以將 YUV 影片轉換成灰階。</span><span class="sxs-lookup"><span data-stu-id="a12b5-105">The grayscale MFT converts YUV video to grayscale by setting the chroma values in the video to neutral.</span></span> <span data-ttu-id="a12b5-106">MFT 以 UYVY、YUY2 或 NV12 格式接受未壓縮的影片。</span><span class="sxs-lookup"><span data-stu-id="a12b5-106">The MFT accepts uncompressed video in UYVY, YUY2, or NV12 formats.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="a12b5-107">示範的 Api</span><span class="sxs-lookup"><span data-stu-id="a12b5-107">APIs Demonstrated</span></span>

<span data-ttu-id="a12b5-108">這個範例會示範下列 Microsoft 媒體基礎介面：</span><span class="sxs-lookup"><span data-stu-id="a12b5-108">This sample demonstrates the following Microsoft Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="a12b5-109">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="a12b5-109">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="usage"></a><span data-ttu-id="a12b5-110">使用方式</span><span class="sxs-lookup"><span data-stu-id="a12b5-110">Usage</span></span>

<span data-ttu-id="a12b5-111">MFT \_ 灰階範例會建立一個 DLL，它是 MFT 的 COM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="a12b5-111">The MFT\_GrayScale sample builds a DLL that is a COM server for the MFT.</span></span> <span data-ttu-id="a12b5-112">使用 MFT 之前，您必須先註冊 DLL。</span><span class="sxs-lookup"><span data-stu-id="a12b5-112">Before using the MFT, you must register the DLL.</span></span>

<span data-ttu-id="a12b5-113">若要查看使用中的灰階 MFT，請執行 [PlaybackFX 範例](/previous-versions//bb970336(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="a12b5-113">To see the grayscale MFT in use, run the [PlaybackFX Sample](/previous-versions//bb970336(v=vs.85)).</span></span> <span data-ttu-id="a12b5-114">您也可以使用 TopoEdit 工具來建立包含灰階 MFT 的拓撲。</span><span class="sxs-lookup"><span data-stu-id="a12b5-114">You can also use the TopoEdit tool to build a topology that includes the grayscale MFT.</span></span> <span data-ttu-id="a12b5-115">如需 TopoEdit 的詳細資訊，請參閱 [TopoEdit](topoedit.md)。</span><span class="sxs-lookup"><span data-stu-id="a12b5-115">For more information about TopoEdit, see [TopoEdit](topoedit.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a12b5-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="a12b5-116">Requirements</span></span>



| <span data-ttu-id="a12b5-117">產品</span><span class="sxs-lookup"><span data-stu-id="a12b5-117">Product</span></span>                                                        | <span data-ttu-id="a12b5-118">版本</span><span class="sxs-lookup"><span data-stu-id="a12b5-118">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="a12b5-119">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="a12b5-119">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="a12b5-120">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a12b5-120">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="a12b5-121">下載範例</span><span class="sxs-lookup"><span data-stu-id="a12b5-121">Downloading the Sample</span></span>

<span data-ttu-id="a12b5-122">此範例可在 [Windows 傳統範例 github 存放庫](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_grayscale)中取得。</span><span class="sxs-lookup"><span data-stu-id="a12b5-122">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_grayscale).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a12b5-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="a12b5-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a12b5-124">關於 YUV 影片</span><span class="sxs-lookup"><span data-stu-id="a12b5-124">About YUV Video</span></span>](about-yuv-video.md)
</dt> <dt>

[<span data-ttu-id="a12b5-125">媒體基礎 SDK 範例</span><span class="sxs-lookup"><span data-stu-id="a12b5-125">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="a12b5-126">媒體基礎轉換</span><span class="sxs-lookup"><span data-stu-id="a12b5-126">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="a12b5-127">MFT \_ AudioDelay 範例</span><span class="sxs-lookup"><span data-stu-id="a12b5-127">MFT\_AudioDelay Sample</span></span>](mft-audiodelay-sample.md)
</dt> <dt>

[<span data-ttu-id="a12b5-128">撰寫自訂的 MFT</span><span class="sxs-lookup"><span data-stu-id="a12b5-128">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 
