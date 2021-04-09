---
title: 使用者介面項目
description: 使用者介面項目
ms.assetid: cb2876fb-632e-4c3d-8a6e-f7c8c4878c3f
keywords:
- Windows Media Player 行動外觀、使用者介面
- Windows Media Player 行動外觀、元素
- 元素，Windows Media Player 行動面板
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91819831d80235dd7f7c41cfcf98965c9fd61c35
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020941"
---
# <a name="user-interface-elements"></a><span data-ttu-id="90a43-106">使用者介面項目</span><span class="sxs-lookup"><span data-stu-id="90a43-106">User Interface Elements</span></span>

<span data-ttu-id="90a43-107">雖然您可以選擇各種功能來控制數字媒體、播放清單和磁片區，但您可以自行決定是否要提供外觀的使用者，以與該功能互動。</span><span class="sxs-lookup"><span data-stu-id="90a43-107">Even though you can choose from a wide range of functionality for controlling digital media, playlists, and volume, it is up to you to provide the user of your skin with a way to interact with that functionality.</span></span> <span data-ttu-id="90a43-108">例如，如果您想要讓使用者開始播放媒體專案，您必須提供使用者介面按鈕元素，當使用者按下按鈕的影像時，就會播放該媒體專案。</span><span class="sxs-lookup"><span data-stu-id="90a43-108">For example, if you want the user to start playing a media item, you must provide a user-interface button element that will cause the media item to play when the user taps the image of your button.</span></span>

<span data-ttu-id="90a43-109">不需要任何專案，但如果您沒有用來播放和停止媒體專案的幾個按鈕，就不會發生太多。</span><span class="sxs-lookup"><span data-stu-id="90a43-109">No elements are required, but if you do not have a few buttons to play and stop the media item, not much will happen.</span></span> <span data-ttu-id="90a43-110">提供音量控制項也是個不錯的主意。</span><span class="sxs-lookup"><span data-stu-id="90a43-110">It is also a good idea to provide a volume control.</span></span>

<span data-ttu-id="90a43-111">使用者介面元素會對應至用來控制數字媒體選取和播放的功能類型。</span><span class="sxs-lookup"><span data-stu-id="90a43-111">User interface elements correspond to types of functionality used to control digital media selection and playback.</span></span>

<span data-ttu-id="90a43-112">提供下列元素。</span><span class="sxs-lookup"><span data-stu-id="90a43-112">The following elements are provided.</span></span>



| <span data-ttu-id="90a43-113">元素</span><span class="sxs-lookup"><span data-stu-id="90a43-113">Element</span></span>                    | <span data-ttu-id="90a43-114">描述</span><span class="sxs-lookup"><span data-stu-id="90a43-114">Description</span></span>                                                                                                                                                                                                                                                             |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90a43-115">按鈕</span><span class="sxs-lookup"><span data-stu-id="90a43-115">Buttons</span></span>](buttons.md)     | <span data-ttu-id="90a43-116">提供許多按鈕類型。</span><span class="sxs-lookup"><span data-stu-id="90a43-116">Many button types are provided.</span></span> <span data-ttu-id="90a43-117">按鈕可以用來開啟或關閉函式，或在兩個函式之間切換。</span><span class="sxs-lookup"><span data-stu-id="90a43-117">Buttons can be used to turn functions on or off or switch between two functions.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="90a43-118">Trackbars</span><span class="sxs-lookup"><span data-stu-id="90a43-118">Trackbars</span></span>](trackbars.md) | <span data-ttu-id="90a43-119">您可以透過 trackbars 提供線性控制項。</span><span class="sxs-lookup"><span data-stu-id="90a43-119">You can provide linear control through trackbars.</span></span> <span data-ttu-id="90a43-120">您會想要使用 trackbars 來變更媒體專案中的音量或播放位置。</span><span class="sxs-lookup"><span data-stu-id="90a43-120">You will want to use trackbars to change the volume or the playback position in a media item.</span></span>                                                                                                                         |
| [<span data-ttu-id="90a43-121">Text</span><span class="sxs-lookup"><span data-stu-id="90a43-121">Text</span></span>](text.md)           | <span data-ttu-id="90a43-122">文字方塊可以用來向使用者顯示文字。</span><span class="sxs-lookup"><span data-stu-id="90a43-122">Text boxes can be used to display text to the user.</span></span> <span data-ttu-id="90a43-123">您可以使用文字方塊來顯示目前現正播放的歌曲名稱。</span><span class="sxs-lookup"><span data-stu-id="90a43-123">A good use of a text box is to display the name of the song currently playing.</span></span>                                                                                                                                      |
| [<span data-ttu-id="90a43-124">Marquee</span><span class="sxs-lookup"><span data-stu-id="90a43-124">Marquee</span></span>](marquee.md)     | <span data-ttu-id="90a43-125">[字幕] 是一個滾動文字方塊，可讓您用來顯示多個文字類別目錄中的文字。</span><span class="sxs-lookup"><span data-stu-id="90a43-125">A marquee is a scrolling text box that you can use to display text from more than one text category.</span></span> <span data-ttu-id="90a43-126">例如，您可以顯示播放清單、播放軌數目，以及追蹤播放次數。</span><span class="sxs-lookup"><span data-stu-id="90a43-126">For example, you can display the playlist, number of tracks, and track number playing.</span></span> <span data-ttu-id="90a43-127">當您沒有足夠的空間，而且有很多人要顯示時，請使用字幕。</span><span class="sxs-lookup"><span data-stu-id="90a43-127">Use a marquee when you don't have much space and you have a lot to display.</span></span> |
| [<span data-ttu-id="90a43-128">狀態</span><span class="sxs-lookup"><span data-stu-id="90a43-128">Status</span></span>](status.md)       | <span data-ttu-id="90a43-129">您可以提供狀態顯示，讓您用來自動顯示文字訊息，通知使用者 Windows Media Player 的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="90a43-129">You can provide a status display that you can use to automatically display text messages that inform the user about the current state of Windows Media Player.</span></span> <span data-ttu-id="90a43-130">例如，當媒體專案為緩衝時，狀態顯示會通知使用者。</span><span class="sxs-lookup"><span data-stu-id="90a43-130">For example, the status display will inform the user when a media item is buffering.</span></span>                     |
| [<span data-ttu-id="90a43-131">影片</span><span class="sxs-lookup"><span data-stu-id="90a43-131">Video</span></span>](video.md)         | <span data-ttu-id="90a43-132">如果您想要播放影片，您可以在面板中提供矩形的影片顯示區域。</span><span class="sxs-lookup"><span data-stu-id="90a43-132">You can provide a rectangular video display area in your skin if you want to play video.</span></span>                                                                                                                                                                                |
| [<span data-ttu-id="90a43-133">評等</span><span class="sxs-lookup"><span data-stu-id="90a43-133">Ratings</span></span>](ratings.md)     | <span data-ttu-id="90a43-134">您可以顯示與目前現正播放之任何 Windows Media 音訊型內容相關聯的評等。</span><span class="sxs-lookup"><span data-stu-id="90a43-134">You can display the rating associated with any Windows Media Audio-based content that is currently playing.</span></span>                                                                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="90a43-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="90a43-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90a43-136">**關於外觀**</span><span class="sxs-lookup"><span data-stu-id="90a43-136">**About Skins**</span></span>](about-skins-mobile.md)
</dt> </dl>

 

 




