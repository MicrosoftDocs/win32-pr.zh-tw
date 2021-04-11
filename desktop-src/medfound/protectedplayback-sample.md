---
description: 顯示如何在 Microsoft 媒體基礎中播放受保護的媒體內容。
ms.assetid: e4a47e1c-16aa-45c1-8aa8-8929d6e1e653
title: ProtectedPlayback 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee64b2a64ce4d40b6f15c2e5afb3b9a39e84c619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691628"
---
# <a name="protectedplayback-sample"></a><span data-ttu-id="3a201-103">ProtectedPlayback 範例</span><span class="sxs-lookup"><span data-stu-id="3a201-103">ProtectedPlayback Sample</span></span>

<span data-ttu-id="3a201-104">顯示如何在 Microsoft 媒體基礎中播放受保護的媒體內容。</span><span class="sxs-lookup"><span data-stu-id="3a201-104">Shows how to play protected media content in Microsoft Media Foundation.</span></span>

## <a name="usage"></a><span data-ttu-id="3a201-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="3a201-105">Usage</span></span>

<span data-ttu-id="3a201-106">ProtectedPlayback 範例會建立 Windows 應用程式。</span><span class="sxs-lookup"><span data-stu-id="3a201-106">The ProtectedPlayback sample builds a Windows application.</span></span>

<span data-ttu-id="3a201-107">若要播放本機媒體檔案，請 **選取 [檔案**] 功能表中的 [**開啟** 檔案]。</span><span class="sxs-lookup"><span data-stu-id="3a201-107">To play a local media file, select **Open File** from the **File** menu.</span></span> <span data-ttu-id="3a201-108">若要依 URL 指定檔案，請 **選取 [檔案**] 功能表中的 [**開啟 URL** ]。</span><span class="sxs-lookup"><span data-stu-id="3a201-108">To specify a file by URL, select **Open URL** from the **File** menu.</span></span> <span data-ttu-id="3a201-109">當您選取檔案之後，播放會自動開始。</span><span class="sxs-lookup"><span data-stu-id="3a201-109">After you select a file, playback begins automatically.</span></span> <span data-ttu-id="3a201-110">若要暫停播放，請按下空格鍵。</span><span class="sxs-lookup"><span data-stu-id="3a201-110">To pause playback, press the SPACEBAR.</span></span> <span data-ttu-id="3a201-111">若要繼續播放，請再次按下空格鍵。</span><span class="sxs-lookup"><span data-stu-id="3a201-111">To resume playback, press the SPACEBAR again.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="3a201-112">示範的 Api</span><span class="sxs-lookup"><span data-stu-id="3a201-112">APIs Demonstrated</span></span>

<span data-ttu-id="3a201-113">這個範例會示範下列媒體基礎介面：</span><span class="sxs-lookup"><span data-stu-id="3a201-113">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="3a201-114">**IMFContentEnabler**</span><span class="sxs-lookup"><span data-stu-id="3a201-114">**IMFContentEnabler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
-   [<span data-ttu-id="3a201-115">**IMFContentProtectionManager**</span><span class="sxs-lookup"><span data-stu-id="3a201-115">**IMFContentProtectionManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)

## <a name="requirements"></a><span data-ttu-id="3a201-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a201-116">Requirements</span></span>



| <span data-ttu-id="3a201-117">產品</span><span class="sxs-lookup"><span data-stu-id="3a201-117">Product</span></span>                                                        | <span data-ttu-id="3a201-118">版本</span><span class="sxs-lookup"><span data-stu-id="3a201-118">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="3a201-119">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="3a201-119">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="3a201-120">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3a201-120">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="3a201-121">下載範例</span><span class="sxs-lookup"><span data-stu-id="3a201-121">Downloading the Sample</span></span>

<span data-ttu-id="3a201-122">此範例可在 [Windows 傳統範例 github 存放庫](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback)中取得。</span><span class="sxs-lookup"><span data-stu-id="3a201-122">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a201-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="3a201-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a201-124">如何播放受保護的媒體檔案</span><span class="sxs-lookup"><span data-stu-id="3a201-124">How to Play Protected Media Files</span></span>](how-to-play-protected-media-files.md)
</dt> <dt>

[<span data-ttu-id="3a201-125">媒體基礎 SDK 範例</span><span class="sxs-lookup"><span data-stu-id="3a201-125">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

<span data-ttu-id="3a201-126">[MFPlayer 範例](/previous-versions//bb970516(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3a201-126">[MFPlayer Sample](/previous-versions//bb970516(v=vs.85))</span></span>
</dt> </dl>

 

 
