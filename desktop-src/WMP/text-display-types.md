---
title: 文字顯示類型
description: 文字顯示類型
ms.assetid: 6aa3fc89-e5f5-420f-82e0-c605676078cb
keywords:
- Windows Media Player 行動外觀、文字
- 外觀中的文字、顯示類型
- 外觀，文字
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4fa8871d889a271bcbc59ce7b3118bc05be2eb7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672576"
---
# <a name="text-display-types"></a><span data-ttu-id="14376-106">文字顯示類型</span><span class="sxs-lookup"><span data-stu-id="14376-106">Text Display Types</span></span>

<span data-ttu-id="14376-107">您不需要在面板中包含文字顯示，但您可能會想要在許多情況下。</span><span class="sxs-lookup"><span data-stu-id="14376-107">You do not need to include text displays in your skin, but there are many instances where you might want to.</span></span> <span data-ttu-id="14376-108">例如，您可能想要包含搜尋字幕，讓使用者移至媒體專案中的任何位置，但您也可能想要包含文字顯示，以顯示自目前媒體專案開始播放以來經過的秒數。</span><span class="sxs-lookup"><span data-stu-id="14376-108">For example, you might want to include a Seek trackbar to allow the user to move to any position in the media item, but you also might want to include a text display that shows the number of seconds that have elapsed since the current media item started playing.</span></span>

<span data-ttu-id="14376-109">**顯示方塊**</span><span class="sxs-lookup"><span data-stu-id="14376-109">**Display Boxes**</span></span>

<span data-ttu-id="14376-110">以下是 text 元素可以顯示的數個屬性：</span><span class="sxs-lookup"><span data-stu-id="14376-110">The following are several attributes a text element can display:</span></span>

-   <span data-ttu-id="14376-111">Time</span><span class="sxs-lookup"><span data-stu-id="14376-111">Time</span></span>
-   <span data-ttu-id="14376-112">播放清單</span><span class="sxs-lookup"><span data-stu-id="14376-112">Playlist</span></span>
-   <span data-ttu-id="14376-113">Track\#</span><span class="sxs-lookup"><span data-stu-id="14376-113">Track\#</span></span>
-   <span data-ttu-id="14376-114">\#軌道</span><span class="sxs-lookup"><span data-stu-id="14376-114">\#Tracks</span></span>
-   <span data-ttu-id="14376-115">標題</span><span class="sxs-lookup"><span data-stu-id="14376-115">Title</span></span>
-   <span data-ttu-id="14376-116">作者</span><span class="sxs-lookup"><span data-stu-id="14376-116">Author</span></span>
-   <span data-ttu-id="14376-117">著作權</span><span class="sxs-lookup"><span data-stu-id="14376-117">Copyright</span></span>
-   <span data-ttu-id="14376-118">檔案名稱</span><span class="sxs-lookup"><span data-stu-id="14376-118">Filename</span></span>
-   <span data-ttu-id="14376-119">FilenameExt</span><span class="sxs-lookup"><span data-stu-id="14376-119">FilenameExt</span></span>
-   <span data-ttu-id="14376-120">Bitrate</span><span class="sxs-lookup"><span data-stu-id="14376-120">Bitrate</span></span>
-   <span data-ttu-id="14376-121">頻率</span><span class="sxs-lookup"><span data-stu-id="14376-121">Frequency</span></span>
-   <span data-ttu-id="14376-122">狀態</span><span class="sxs-lookup"><span data-stu-id="14376-122">Status</span></span>
-   <span data-ttu-id="14376-123">VolPercent</span><span class="sxs-lookup"><span data-stu-id="14376-123">VolPercent</span></span>

<span data-ttu-id="14376-124">如需文字顯示類型的詳細資訊，請參閱外觀參考的 [文字](text.md) 區段。</span><span class="sxs-lookup"><span data-stu-id="14376-124">For more information about text display types, see the [Text](text.md) section of the Skin Reference.</span></span>

<span data-ttu-id="14376-125">**滾動字幕**</span><span class="sxs-lookup"><span data-stu-id="14376-125">**Scrolling Marquee**</span></span>

<span data-ttu-id="14376-126">除了使用個別的文字專案，您還可以將一或多個屬性結合成滾動文字字幕。</span><span class="sxs-lookup"><span data-stu-id="14376-126">In addition to using the individual text elements, you can combine one or more attributes into a scrolling text marquee.</span></span> <span data-ttu-id="14376-127">如果您想要在社區域中顯示相關的文字資訊群組，這會很有用。</span><span class="sxs-lookup"><span data-stu-id="14376-127">This is useful if you want to display a grouping of related text information in a small area.</span></span> <span data-ttu-id="14376-128">例如，您可以在字幕中顯示標題、作者和著作權資訊。</span><span class="sxs-lookup"><span data-stu-id="14376-128">For example, you could display Title, Author, and Copyright information in a Marquee.</span></span>

<span data-ttu-id="14376-129">如需建立文字字幕的詳細資訊，請參閱面板參考的 [ [字幕]](marquee.md) 區段。</span><span class="sxs-lookup"><span data-stu-id="14376-129">For more information about creating a text marquee, see the [Marquee](marquee.md) section of the Skin Reference.</span></span>

<span data-ttu-id="14376-130">**狀態顯示**</span><span class="sxs-lookup"><span data-stu-id="14376-130">**Status Display**</span></span>

<span data-ttu-id="14376-131">另一種類型的文字顯示是狀態顯示。</span><span class="sxs-lookup"><span data-stu-id="14376-131">Another type of text display is the status display.</span></span> <span data-ttu-id="14376-132">這可讓您自動顯示 Windows Media Player Mobile 目前狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="14376-132">This lets you automatically display information about the current state of Windows Media Player Mobile.</span></span> <span data-ttu-id="14376-133">例如，當媒體專案為緩衝時，狀態顯示會通知使用者，讓播放程式很容易就能正常運作。</span><span class="sxs-lookup"><span data-stu-id="14376-133">For example, the status display will inform the user when a media item is buffering so that it is evident that the Player is working.</span></span>

<span data-ttu-id="14376-134">下列訊息會出現在狀態顯示中：</span><span class="sxs-lookup"><span data-stu-id="14376-134">The following messages appear in the status display:</span></span>

-   <span data-ttu-id="14376-135">緩衝</span><span class="sxs-lookup"><span data-stu-id="14376-135">Buffering</span></span>
-   <span data-ttu-id="14376-136">Connecting</span><span class="sxs-lookup"><span data-stu-id="14376-136">Connecting</span></span>
-   <span data-ttu-id="14376-137">已暫停</span><span class="sxs-lookup"><span data-stu-id="14376-137">Paused</span></span>
-   <span data-ttu-id="14376-138">正在播放</span><span class="sxs-lookup"><span data-stu-id="14376-138">Playing</span></span>
-   <span data-ttu-id="14376-139">就緒</span><span class="sxs-lookup"><span data-stu-id="14376-139">Ready</span></span>
-   <span data-ttu-id="14376-140">已停止</span><span class="sxs-lookup"><span data-stu-id="14376-140">Stopped</span></span>

> [!Note]  
> <span data-ttu-id="14376-141">播放媒體專案時，狀態顯示會透過子標題、演出者、專輯、內容類型和目前的位元速率來旋轉。</span><span class="sxs-lookup"><span data-stu-id="14376-141">When a media item is playing, the status display will rotate through subtitle, artist, album, genre, and current bitrate.</span></span>

 

<span data-ttu-id="14376-142">如需透過 Status 元素建立狀態顯示的詳細資訊，請參閱面板參考的 [狀態](status.md) 區段。不過，建議您在 Text 元素中使用 status 屬性，而不要使用 Status 元素。</span><span class="sxs-lookup"><span data-stu-id="14376-142">For information about creating a status display through the Status element, see the [Status](status.md) section of the Skin Reference; however, it is preferred that you use the status attribute in the Text element instead of the Status element.</span></span>

## <a name="related-topics"></a><span data-ttu-id="14376-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="14376-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14376-144">**Windows Media Player 行動功能**</span><span class="sxs-lookup"><span data-stu-id="14376-144">**Windows Media Player Mobile Functionality**</span></span>](windows-media-player-mobile-functionality.md)
</dt> </dl>

 

 




