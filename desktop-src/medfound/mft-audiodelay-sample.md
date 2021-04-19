---
description: MFT \_ AudioDelay 範例
ms.assetid: 08f119f9-cacd-4000-96b6-60c8c0055e9c
title: MFT_AudioDelay 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d382ce7d1c5e9475bef85f11ef9754345e123b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996633"
---
# <a name="mft_audiodelay-sample"></a><span data-ttu-id="34fc8-103">MFT \_ AudioDelay 範例</span><span class="sxs-lookup"><span data-stu-id="34fc8-103">MFT\_AudioDelay Sample</span></span>

<span data-ttu-id="34fc8-104">說明如何將音訊效果實作為媒體基礎轉換 (MFT) 。</span><span class="sxs-lookup"><span data-stu-id="34fc8-104">Shows how to implement an audio effect as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="34fc8-105">音訊延遲 MFT 接受 PCM 音訊做為輸入、套用延遲 (回應) 效果，以及輸出修改過的音訊資料。</span><span class="sxs-lookup"><span data-stu-id="34fc8-105">The audio delay MFT accepts PCM audio as input, applies a delay (echo) effect, and outputs the modified audio data.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="34fc8-106">示範的 Api</span><span class="sxs-lookup"><span data-stu-id="34fc8-106">APIs Demonstrated</span></span>

<span data-ttu-id="34fc8-107">這個範例會示範下列 Microsoft 媒體基礎介面：</span><span class="sxs-lookup"><span data-stu-id="34fc8-107">This sample demonstrates the following Microsoft Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="34fc8-108">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="34fc8-108">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="usage"></a><span data-ttu-id="34fc8-109">使用方式</span><span class="sxs-lookup"><span data-stu-id="34fc8-109">Usage</span></span>

<span data-ttu-id="34fc8-110">MFT \_ AudioDelay 範例會建立一個 DLL，它是 MFT 的 COM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="34fc8-110">The MFT\_AudioDelay sample builds a DLL that is a COM server for the MFT.</span></span> <span data-ttu-id="34fc8-111">使用 MFT 之前，您必須先註冊 DLL。</span><span class="sxs-lookup"><span data-stu-id="34fc8-111">Before using the MFT, you must register the DLL.</span></span> <span data-ttu-id="34fc8-112">您可以使用 TopoEdit 工具來建立包含音訊延遲 MFT 的拓撲。</span><span class="sxs-lookup"><span data-stu-id="34fc8-112">You can use the TopoEdit tool to build a topology that includes the audio delay MFT.</span></span> <span data-ttu-id="34fc8-113">如需 TopoEdit 的詳細資訊，請參閱 [TopoEdit](topoedit.md)。</span><span class="sxs-lookup"><span data-stu-id="34fc8-113">For more information about TopoEdit, see [TopoEdit](topoedit.md).</span></span> <span data-ttu-id="34fc8-114">您也可以修改 [PlaybackFX 範例](/previous-versions//bb970336(v=vs.85)) 以使用 MFT。</span><span class="sxs-lookup"><span data-stu-id="34fc8-114">You can also modify the [PlaybackFX Sample](/previous-versions//bb970336(v=vs.85)) to use the MFT.</span></span> <span data-ttu-id="34fc8-115">您將需要修改 AddBranchToPartialTopology 函式。</span><span class="sxs-lookup"><span data-stu-id="34fc8-115">You will need to modify the AddBranchToPartialTopology function in Player.cpp.</span></span> <span data-ttu-id="34fc8-116">從下列程式程式碼變更：</span><span class="sxs-lookup"><span data-stu-id="34fc8-116">Change the following line from:</span></span>

``` syntax
else if (majorType == MFMediaType_Audio)
{
    hr = CreateAudioBranch(pTopology, pSourceNode, GUID_NULL);
}
```

<span data-ttu-id="34fc8-117">變更為：</span><span class="sxs-lookup"><span data-stu-id="34fc8-117">To:</span></span>

``` syntax
else if (majorType == MFMediaType_Audio)
{
    hr = CreateAudioBranch(pTopology, pSourceNode, CLSID_DelayMFT);
}
```

<span data-ttu-id="34fc8-118">值 CLSID \_ DelayMFT 是在 MFT \_ AudioDelay 範例資料夾的標頭檔 AudioDelayUuids 中宣告的。</span><span class="sxs-lookup"><span data-stu-id="34fc8-118">The value CLSID\_DelayMFT is declared in the header file AudioDelayUuids.h in the MFT\_AudioDelay sample folder.</span></span>

## <a name="requirements"></a><span data-ttu-id="34fc8-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="34fc8-119">Requirements</span></span>



| <span data-ttu-id="34fc8-120">產品</span><span class="sxs-lookup"><span data-stu-id="34fc8-120">Product</span></span>                                                        | <span data-ttu-id="34fc8-121">版本</span><span class="sxs-lookup"><span data-stu-id="34fc8-121">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="34fc8-122">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="34fc8-122">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="34fc8-123">Windows 7</span><span class="sxs-lookup"><span data-stu-id="34fc8-123">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="34fc8-124">下載範例</span><span class="sxs-lookup"><span data-stu-id="34fc8-124">Downloading the Sample</span></span>

<span data-ttu-id="34fc8-125">此範例可在 [Windows 傳統範例 github 存放庫](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_audiodelay)中取得。</span><span class="sxs-lookup"><span data-stu-id="34fc8-125">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_audiodelay).</span></span>

## <a name="related-topics"></a><span data-ttu-id="34fc8-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="34fc8-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34fc8-127">媒體基礎 SDK 範例</span><span class="sxs-lookup"><span data-stu-id="34fc8-127">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="34fc8-128">媒體基礎轉換</span><span class="sxs-lookup"><span data-stu-id="34fc8-128">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="34fc8-129">MFT \_ 灰階範例</span><span class="sxs-lookup"><span data-stu-id="34fc8-129">MFT\_Grayscale Sample</span></span>](mft-grayscale-sample.md)
</dt> <dt>

[<span data-ttu-id="34fc8-130">撰寫自訂的 MFT</span><span class="sxs-lookup"><span data-stu-id="34fc8-130">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 
