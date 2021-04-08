---
title: DVD
description: DVD
ms.assetid: b3634a28-b1d6-44a5-97e4-fcc1f655d652
keywords:
- Windows Media Player，遷移 Dvd
- Windows Media Player 物件模型、Dvd
- 物件模型、Dvd
- Windows Media Player ActiveX 控制項、Dvd
- ActiveX 控制項、Dvd
- Windows Media Player Mobile ActiveX 控制項、Dvd
- Windows Media Player 行動裝置，遷移 Dvd
- 遷移指南、Dvd
- DVD 遷移
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e0a19818ac01b5e3d6138f896f26fe674c5ef2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673951"
---
# <a name="dvd"></a><span data-ttu-id="d5de1-112">DVD</span><span class="sxs-lookup"><span data-stu-id="d5de1-112">DVD</span></span>

<span data-ttu-id="d5de1-113">Windows Media Player 6.4 ActiveX 控制項包含一個 **dvd** 物件，它會公開各種不同的方法和屬性，以及一個用來處理 DVD 內容的事件。</span><span class="sxs-lookup"><span data-stu-id="d5de1-113">The Windows Media Player 6.4 ActiveX control contains a **DVD** object that exposes a variety of methods and properties, and one event, for dealing specifically with DVD content.</span></span> <span data-ttu-id="d5de1-114">例如，若要判斷可用的 DVD 標題數目，請使用 **Player6**。**titlesAvailable** 屬性：</span><span class="sxs-lookup"><span data-stu-id="d5de1-114">For instance, to determine the number of DVD titles available, you use the **Player6**.**titlesAvailable** property:</span></span>


```C++
var numTitles = WMP64.DVD.TitlesAvailable;

```



<span data-ttu-id="d5de1-115">Windows Media Player 7 或更新版本的物件模型，可實現更整合的 DVD 方法。</span><span class="sxs-lookup"><span data-stu-id="d5de1-115">The Windows Media Player 7 or later object model implements a more integrated approach to DVD.</span></span> <span data-ttu-id="d5de1-116">只有在需要時，才會實作為 DVD 專屬的屬性、方法和事件。</span><span class="sxs-lookup"><span data-stu-id="d5de1-116">DVD-specific properties, methods, and events are implemented only where needed.</span></span> <span data-ttu-id="d5de1-117">否則，現有的物件模型功能會如您所預期般與 DVD 媒體搭配使用。</span><span class="sxs-lookup"><span data-stu-id="d5de1-117">Otherwise, existing object model functionality works with DVD media as you might expect.</span></span> <span data-ttu-id="d5de1-118">例如，若要判斷使用 Windows Media Player 7 或更新版本時可用的 DVD 標題數目，您可以從 **Cdrom** 物件取出 **播放清單** 物件：</span><span class="sxs-lookup"><span data-stu-id="d5de1-118">For example, to determine the number of DVD titles available when using Windows Media Player 7 or later, you retrieve a **Playlist** object from the **Cdrom** object:</span></span>


```C++
var dvdTitles = WMP9.cdromCollection.item(0).playlist;

```



<span data-ttu-id="d5de1-119">上述範例會使用代表第一個磁片磁碟機 DVD 媒體的第一個專案來抓取 **播放清單** 物件。</span><span class="sxs-lookup"><span data-stu-id="d5de1-119">The preceding example retrieves a **Playlist** object with a first entry representing the DVD media in the first drive.</span></span> <span data-ttu-id="d5de1-120">其他專案代表個別的 DVD 標題。</span><span class="sxs-lookup"><span data-stu-id="d5de1-120">Additional entries represent individual DVD titles.</span></span> <span data-ttu-id="d5de1-121">因此，可用的標題數目可以計算如下：</span><span class="sxs-lookup"><span data-stu-id="d5de1-121">Therefore, the number of titles available can be calculated as follows:</span></span>


```C++
var numTitles = dvdTitles.count - 1;

```



<span data-ttu-id="d5de1-122">以下是從6.4 版進行遷移時要牢記在心的主要差異：</span><span class="sxs-lookup"><span data-stu-id="d5de1-122">Here are the main differences to keep in mind when migrating from version 6.4:</span></span>

-   <span data-ttu-id="d5de1-123">只有使用 Windows XP 或更新版本的 Windows Media Player 以及 Windows XP 作業系統或更新版本時，才支援 DVD 播放。</span><span class="sxs-lookup"><span data-stu-id="d5de1-123">DVD playback is supported only when using Windows Media Player for Windows XP or later and the Windows XP operating system or later.</span></span>
-   <span data-ttu-id="d5de1-124">DVD-ROM 磁片磁碟機的列舉方式與使用 **CdromCollection** 物件的 cd-rom 光碟機完全一樣。</span><span class="sxs-lookup"><span data-stu-id="d5de1-124">DVD-ROM drives are enumerated exactly like CD-ROM drives using the **CdromCollection** object.</span></span>
-   <span data-ttu-id="d5de1-125">使用 **Cdrom** 物件管理個別的 dvd-rom 光碟機。</span><span class="sxs-lookup"><span data-stu-id="d5de1-125">Individual DVD-ROM drives are managed using the **Cdrom** object.</span></span>
-   <span data-ttu-id="d5de1-126">**Dvd** 物件以方法和一個屬性（特別是使用 DVD）來擴充物件模型。</span><span class="sxs-lookup"><span data-stu-id="d5de1-126">The **DVD** object extends the object model with methods and one property specifically for working with DVD.</span></span>
-   <span data-ttu-id="d5de1-127">**OpenPlaylistSwitch** 和 **DomainChange** 有兩個新的事件，尤其是使用 DVD。</span><span class="sxs-lookup"><span data-stu-id="d5de1-127">There are two new events, **OpenPlaylistSwitch** and **DomainChange**, specifically for working with DVD.</span></span>
-   <span data-ttu-id="d5de1-128">DVD 內容是使用 **播放清單** 物件和 **媒體** 物件來組織。</span><span class="sxs-lookup"><span data-stu-id="d5de1-128">DVD content is organized using **Playlist** objects and **Media** objects.</span></span>
-   <span data-ttu-id="d5de1-129">您可以使用 (Windows Media Player 9 系列或更新版本) 的 **控制項** 物件所提供的語言功能來管理 DVD 語言。</span><span class="sxs-lookup"><span data-stu-id="d5de1-129">DVD languages are managed using the language functionality available from the **Controls** object (Windows Media Player 9 Series or later).</span></span>
-   <span data-ttu-id="d5de1-130">DVD 的傳輸控制項和位置資訊與其他數位媒體類型的運作方式相同。</span><span class="sxs-lookup"><span data-stu-id="d5de1-130">Transport controls and position information for DVD work the same as for other digital media types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5de1-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="d5de1-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5de1-132">**物件模型遷移指南**</span><span class="sxs-lookup"><span data-stu-id="d5de1-132">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> <dt>

[<span data-ttu-id="d5de1-133">**使用 Windows Media Player 控制項搭配 Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="d5de1-133">**Using the Windows Media Player Control with Visual Basic**</span></span>](using-the-windows-media-player-control-with-visual-basic.md)
</dt> </dl>

 

 




