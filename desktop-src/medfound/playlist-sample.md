---
description: 播放清單範例
ms.assetid: ffe663ce-3e9a-4dfc-8904-6f055332c119
title: 播放清單範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f83d05762385d0de43a5d7f2bcd73cda2c6e2d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987427"
---
# <a name="playlist-sample"></a><span data-ttu-id="9edf5-103">播放清單範例</span><span class="sxs-lookup"><span data-stu-id="9edf5-103">Playlist Sample</span></span>

<span data-ttu-id="9edf5-104">顯示如何使用 Microsoft 媒體基礎播放播放清單中的音訊檔案序列。</span><span class="sxs-lookup"><span data-stu-id="9edf5-104">Shows how to use Microsoft Media Foundation to play a sequence of audio files in a playlist.</span></span> <span data-ttu-id="9edf5-105">此範例會使用 [Sequencer 來源](sequencer-source.md) 來建立和管理播放清單。</span><span class="sxs-lookup"><span data-stu-id="9edf5-105">The sample uses the [Sequencer Source](sequencer-source.md) to create and manage the playlist.</span></span>

> [!Note]  
> <span data-ttu-id="9edf5-106">SDK 中已不再包含此範例。</span><span class="sxs-lookup"><span data-stu-id="9edf5-106">This sample is no longer included in the SDK.</span></span>

 

## <a name="apis-demonstrated"></a><span data-ttu-id="9edf5-107">示範的 Api</span><span class="sxs-lookup"><span data-stu-id="9edf5-107">APIs Demonstrated</span></span>

<span data-ttu-id="9edf5-108">這個範例會示範下列媒體基礎介面：</span><span class="sxs-lookup"><span data-stu-id="9edf5-108">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="9edf5-109">**IMFMediaSourceTopologyProvider**</span><span class="sxs-lookup"><span data-stu-id="9edf5-109">**IMFMediaSourceTopologyProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
-   [<span data-ttu-id="9edf5-110">**IMFMediaSession**</span><span class="sxs-lookup"><span data-stu-id="9edf5-110">**IMFMediaSession**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
-   [<span data-ttu-id="9edf5-111">**IMFSequencerSource**</span><span class="sxs-lookup"><span data-stu-id="9edf5-111">**IMFSequencerSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)

## <a name="usage"></a><span data-ttu-id="9edf5-112">使用方式</span><span class="sxs-lookup"><span data-stu-id="9edf5-112">Usage</span></span>

<span data-ttu-id="9edf5-113">播放清單範例會建立 Windows 應用程式。</span><span class="sxs-lookup"><span data-stu-id="9edf5-113">The Playlist sample builds a Windows application.</span></span>

-   <span data-ttu-id="9edf5-114">若要建立新的播放清單，請 **選取 [檔案**] 功能表中的 [**加入至播放清單**]。</span><span class="sxs-lookup"><span data-stu-id="9edf5-114">To create a new playlist, select **Add to Playlist** from the **File** menu.</span></span> <span data-ttu-id="9edf5-115">在 [ **開啟** 檔案] 對話方塊中，選取一或多個音訊檔案。</span><span class="sxs-lookup"><span data-stu-id="9edf5-115">In the **Open File** dialog, select one or more audio files.</span></span> <span data-ttu-id="9edf5-116">檔案會新增至播放清單。</span><span class="sxs-lookup"><span data-stu-id="9edf5-116">The files are added to the playlist.</span></span>
-   <span data-ttu-id="9edf5-117">若要播放順序，請按一下 [ **播放**]。</span><span class="sxs-lookup"><span data-stu-id="9edf5-117">To play the sequence, click **Play**.</span></span>
-   <span data-ttu-id="9edf5-118">若要暫停目前的區段，請按一下 [ **暫停**]。</span><span class="sxs-lookup"><span data-stu-id="9edf5-118">To pause the current segment, click **Pause**.</span></span>
-   <span data-ttu-id="9edf5-119">若要停止目前的區段，請按一下 [ **停止**]。</span><span class="sxs-lookup"><span data-stu-id="9edf5-119">To stop the current segment, click **Stop**.</span></span>
-   <span data-ttu-id="9edf5-120">若要略過檔案，請按兩下播放清單中的專案。</span><span class="sxs-lookup"><span data-stu-id="9edf5-120">To skip to a file, double-click the item in the playlist.</span></span>
-   <span data-ttu-id="9edf5-121">若要從播放清單中刪除檔案，請選取播放清單中的專案。</span><span class="sxs-lookup"><span data-stu-id="9edf5-121">To delete a file from the playlist, select the item in the playlist.</span></span> <span data-ttu-id="9edf5-122">然後選取 [檔案] 功能表中 **的 [** **從播放清單移除**]。</span><span class="sxs-lookup"><span data-stu-id="9edf5-122">Then select **Remove from Playlist** from the **File** menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="9edf5-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="9edf5-123">Requirements</span></span>



| <span data-ttu-id="9edf5-124">產品</span><span class="sxs-lookup"><span data-stu-id="9edf5-124">Product</span></span>                                                        | <span data-ttu-id="9edf5-125">版本</span><span class="sxs-lookup"><span data-stu-id="9edf5-125">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="9edf5-126">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="9edf5-126">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="9edf5-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9edf5-127">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="9edf5-128">下載範例</span><span class="sxs-lookup"><span data-stu-id="9edf5-128">Downloading the Sample</span></span>

<span data-ttu-id="9edf5-129">下列位置提供此範例。</span><span class="sxs-lookup"><span data-stu-id="9edf5-129">This sample is available in the following locations.</span></span>



| <span data-ttu-id="9edf5-130">Location</span><span class="sxs-lookup"><span data-stu-id="9edf5-130">Location</span></span>                                                     | <span data-ttu-id="9edf5-131">路徑/URL</span><span class="sxs-lookup"><span data-stu-id="9edf5-131">Path/URL</span></span>                                                   |
|--------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="9edf5-132">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="9edf5-132">Windows SDK</span></span>](https://www.microsoft.com/download/details.aspx?id=8279) | <span data-ttu-id="9edf5-133">*SDK 根目錄* \\範例 \\ 多媒體 \\ mediafoundation \\ 播放清單</span><span class="sxs-lookup"><span data-stu-id="9edf5-133">*SDK Root*\\Samples\\multimedia\\mediafoundation\\Playlist</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9edf5-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="9edf5-134">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9edf5-135">[BasicPlayback 範例](/previous-versions//bb970475(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9edf5-135">[BasicPlayback Sample](/previous-versions//bb970475(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9edf5-136">媒體基礎 SDK 範例</span><span class="sxs-lookup"><span data-stu-id="9edf5-136">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="9edf5-137">Sequencer 來源</span><span class="sxs-lookup"><span data-stu-id="9edf5-137">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 
