---
description: 示範如何使用 Microsoft 媒體基礎將音訊從媒體檔案解碼。
ms.assetid: 29822e6b-8598-4133-b181-7fb0854553b7
title: 音訊剪輯範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0e4a3e515d08e2cafd2ab2ba451a528f3d5677
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972155"
---
# <a name="audio-clip-sample"></a><span data-ttu-id="7eb6d-103">音訊剪輯範例</span><span class="sxs-lookup"><span data-stu-id="7eb6d-103">Audio Clip Sample</span></span>

<span data-ttu-id="7eb6d-104">示範如何使用 Microsoft 媒體基礎將音訊從媒體檔案解碼。</span><span class="sxs-lookup"><span data-stu-id="7eb6d-104">Shows how to use Microsoft Media Foundation to decode audio from a media file.</span></span>

<span data-ttu-id="7eb6d-105">音訊剪輯範例應用程式會從媒體檔案讀取音訊資料，並將未壓縮的音訊寫入 WAVE 檔。</span><span class="sxs-lookup"><span data-stu-id="7eb6d-105">The Audio Clip sample application reads audio data from a media file and writes the uncompressed audio to a WAVE file.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="7eb6d-106">示範的 Api</span><span class="sxs-lookup"><span data-stu-id="7eb6d-106">APIs Demonstrated</span></span>

<span data-ttu-id="7eb6d-107">這個範例會示範下列媒體基礎介面：</span><span class="sxs-lookup"><span data-stu-id="7eb6d-107">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="7eb6d-108">**IMFSourceReader**</span><span class="sxs-lookup"><span data-stu-id="7eb6d-108">**IMFSourceReader**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)

## <a name="usage"></a><span data-ttu-id="7eb6d-109">使用方式</span><span class="sxs-lookup"><span data-stu-id="7eb6d-109">Usage</span></span>

<span data-ttu-id="7eb6d-110">此範例是命令列應用程式。</span><span class="sxs-lookup"><span data-stu-id="7eb6d-110">This sample is a command-line application.</span></span> <span data-ttu-id="7eb6d-111">它會使用下列命令列引數：</span><span class="sxs-lookup"><span data-stu-id="7eb6d-111">It uses the following command-line arguments:</span></span>

``` syntax
audioclip.exe inputfile outputfile.wav
```

-   <span data-ttu-id="7eb6d-112">inputfile：包含音訊資料流程的檔案名。</span><span class="sxs-lookup"><span data-stu-id="7eb6d-112">inputfile: The name of a file that contains an audio stream.</span></span>
-   <span data-ttu-id="7eb6d-113">outputfile .wav：要寫入的 WAVE 檔案名稱。</span><span class="sxs-lookup"><span data-stu-id="7eb6d-113">outputfile.wav: The name of the WAVE file to write.</span></span>

## <a name="requirements"></a><span data-ttu-id="7eb6d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7eb6d-114">Requirements</span></span>



| <span data-ttu-id="7eb6d-115">產品</span><span class="sxs-lookup"><span data-stu-id="7eb6d-115">Product</span></span>                                                        | <span data-ttu-id="7eb6d-116">版本</span><span class="sxs-lookup"><span data-stu-id="7eb6d-116">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="7eb6d-117">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="7eb6d-117">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="7eb6d-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7eb6d-118">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="7eb6d-119">下載範例</span><span class="sxs-lookup"><span data-stu-id="7eb6d-119">Downloading the Sample</span></span>

<span data-ttu-id="7eb6d-120">此範例可在 [Windows 傳統範例 github 存放庫](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip)中取得。</span><span class="sxs-lookup"><span data-stu-id="7eb6d-120">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7eb6d-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="7eb6d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7eb6d-122">媒體基礎 SDK 範例</span><span class="sxs-lookup"><span data-stu-id="7eb6d-122">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="7eb6d-123">來源讀取程式</span><span class="sxs-lookup"><span data-stu-id="7eb6d-123">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="7eb6d-124">教學課程：解碼音訊</span><span class="sxs-lookup"><span data-stu-id="7eb6d-124">Tutorial: Decoding Audio</span></span>](tutorial--decoding-audio.md)
</dt> </dl>

 

 



