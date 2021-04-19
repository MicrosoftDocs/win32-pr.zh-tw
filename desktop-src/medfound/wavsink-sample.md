---
description: WavSink 範例
ms.assetid: 9e1af25f-d55c-45db-8c76-abf814e16700
title: WavSink 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e96ecca551b6ea3e6837f211f0afcb34818d635
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979073"
---
# <a name="wavsink-sample"></a><span data-ttu-id="adb87-103">WavSink 範例</span><span class="sxs-lookup"><span data-stu-id="adb87-103">WavSink Sample</span></span>

<span data-ttu-id="adb87-104">顯示如何在 Microsoft 媒體基礎中執行自訂媒體接收器。</span><span class="sxs-lookup"><span data-stu-id="adb87-104">Shows how to implement a custom media sink in Microsoft Media Foundation.</span></span> <span data-ttu-id="adb87-105">此範例會執行封存接收器，以將未壓縮的 PCM 音訊寫入 .wav 檔案。</span><span class="sxs-lookup"><span data-stu-id="adb87-105">The sample implements an archive sink that writes uncompressed PCM audio to a .wav file.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="adb87-106">示範的 Api</span><span class="sxs-lookup"><span data-stu-id="adb87-106">APIs Demonstrated</span></span>

<span data-ttu-id="adb87-107">這個範例會示範下列媒體基礎介面：</span><span class="sxs-lookup"><span data-stu-id="adb87-107">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="adb87-108">**IMFClockStateSink**</span><span class="sxs-lookup"><span data-stu-id="adb87-108">**IMFClockStateSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [<span data-ttu-id="adb87-109">**IMFFinalizableMediaSink**</span><span class="sxs-lookup"><span data-stu-id="adb87-109">**IMFFinalizableMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)
-   [<span data-ttu-id="adb87-110">**IMFMediaSink**</span><span class="sxs-lookup"><span data-stu-id="adb87-110">**IMFMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)
-   [<span data-ttu-id="adb87-111">**IMFMediaTypeHandler**</span><span class="sxs-lookup"><span data-stu-id="adb87-111">**IMFMediaTypeHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)
-   [<span data-ttu-id="adb87-112">**IMFStreamSink**</span><span class="sxs-lookup"><span data-stu-id="adb87-112">**IMFStreamSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)

## <a name="usage"></a><span data-ttu-id="adb87-113">使用方式</span><span class="sxs-lookup"><span data-stu-id="adb87-113">Usage</span></span>

<span data-ttu-id="adb87-114">WavSink 範例包含兩個 Visual Studio 專案：</span><span class="sxs-lookup"><span data-stu-id="adb87-114">The WavSink sample contains two Visual Studio projects:</span></span>

-   <span data-ttu-id="adb87-115">WavSink 會建立包含媒體接收執行的靜態程式庫。</span><span class="sxs-lookup"><span data-stu-id="adb87-115">WavSink.vcproj builds a static library that contains the media sink implementation.</span></span>
-   <span data-ttu-id="adb87-116">WriteWavFile 會建立一個主控台應用程式，該應用程式會使用媒體接收器來產生 .wav 檔。</span><span class="sxs-lookup"><span data-stu-id="adb87-116">WriteWavFile.vcproj builds a console application that uses the media sink to produce a .wav file.</span></span> <span data-ttu-id="adb87-117">此應用程式會連結至 WavSink 專案所建立的程式庫。</span><span class="sxs-lookup"><span data-stu-id="adb87-117">This application links to the library created by the WavSink project.</span></span>

## <a name="requirements"></a><span data-ttu-id="adb87-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="adb87-118">Requirements</span></span>



| <span data-ttu-id="adb87-119">產品</span><span class="sxs-lookup"><span data-stu-id="adb87-119">Product</span></span>                                                        | <span data-ttu-id="adb87-120">版本</span><span class="sxs-lookup"><span data-stu-id="adb87-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="adb87-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="adb87-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="adb87-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="adb87-122">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="adb87-123">下載範例</span><span class="sxs-lookup"><span data-stu-id="adb87-123">Downloading the Sample</span></span>

<span data-ttu-id="adb87-124">此範例可在 [Windows 傳統範例 github 存放庫](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsink)中取得。</span><span class="sxs-lookup"><span data-stu-id="adb87-124">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsink).</span></span>

## <a name="related-topics"></a><span data-ttu-id="adb87-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="adb87-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adb87-126">媒體基礎 SDK 範例</span><span class="sxs-lookup"><span data-stu-id="adb87-126">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="adb87-127">媒體接收器</span><span class="sxs-lookup"><span data-stu-id="adb87-127">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 



