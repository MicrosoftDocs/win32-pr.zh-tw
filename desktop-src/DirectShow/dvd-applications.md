---
description: DVD 應用程式
ms.assetid: 6f41e0f1-e550-4ca6-9a80-ce4d498289e2
title: DVD 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acaddc683078acff84b7c90689f82becfb7b1d7c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317716"
---
# <a name="dvd-applications"></a><span data-ttu-id="b2bf5-103">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="b2bf5-103">DVD Applications</span></span>

<span data-ttu-id="b2bf5-104">DirectShow 提供一個稱為「 [DVD](dvd-navigator-filter.md) 導覽器來源篩選」的元件，可簡化 c + + 中的 dvd 流覽工作。</span><span class="sxs-lookup"><span data-stu-id="b2bf5-104">DirectShow provides a component called the [DVD Navigator](dvd-navigator-filter.md) source filter which simplifies DVD navigation tasks in C++.</span></span> <span data-ttu-id="b2bf5-105">DVD 導覽程式具有您在全功能的獨立 DVD 播放程式上找到的所有功能，加上在個人電腦上播放 Dvd 專用的其他功能。</span><span class="sxs-lookup"><span data-stu-id="b2bf5-105">The DVD Navigator has all the capabilities that you find on a full-featured stand-alone DVD player, plus additional capabilities specific to playing DVDs on personal computers.</span></span> <span data-ttu-id="b2bf5-106">使用 DVD 導覽器，c + + 和腳本開發人員可以建立功能完整的 DVD 應用程式，而不需參照 DVD 規格。</span><span class="sxs-lookup"><span data-stu-id="b2bf5-106">Using the DVD Navigator, C++ and scripting developers can create full-featured DVD applications without referring to the DVD specification.</span></span> <span data-ttu-id="b2bf5-107">與解碼器篩選器協調的 DVD 導覽器，也會處理 (CSS 和類比禁止複製) 的區域管理和著作權保護，讓應用程式開發人員與這些詳細資料隔離。</span><span class="sxs-lookup"><span data-stu-id="b2bf5-107">The DVD Navigator, in coordination with the decoder filters, also handles regional management and copyright protection (CSS and analog copy protection), isolating application developers from these details.</span></span>

<span data-ttu-id="b2bf5-108">DVD 導覽器篩選器可在整個 DVD-Video 磁片區上運作，而這是由 VIDEO TS 目錄中的檔案所組成 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b2bf5-108">The DVD Navigator filter works across an entire DVD-Video volume, which consists of the files in the VIDEO\_TS directory.</span></span> <span data-ttu-id="b2bf5-109">與使用個別資料流程或檔案的大部分 DirectShow 來源篩選不同，DVD 導覽器會使用標題、章節和時間代碼的 DVD-Video 結構。</span><span class="sxs-lookup"><span data-stu-id="b2bf5-109">Unlike most DirectShow source filters that work with individual streams or files, the DVD Navigator uses the DVD-Video structure of titles, chapters, and time codes.</span></span> <span data-ttu-id="b2bf5-110">如果開發人員想要在 DirectShow 中播放個別的 MPEG-2 檔案，則應該使用 [mpeg-2 的信號](mpeg-2-demultiplexer.md) ，而不是使用 DVD 瀏覽器篩選器。</span><span class="sxs-lookup"><span data-stu-id="b2bf5-110">Developers wishing to play individual MPEG-2 files in DirectShow should use the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) instead of the DVD Navigator filter.</span></span> <span data-ttu-id="b2bf5-111">如需詳細資訊，請參閱 [DirectShow 中的 Mpeg-2 支援](mpeg-2-support-in-directshow.md) 。</span><span class="sxs-lookup"><span data-stu-id="b2bf5-111">See [MPEG-2 Support in DirectShow](mpeg-2-support-in-directshow.md) for more information.</span></span>

> [!Note]  
> <span data-ttu-id="b2bf5-112">若要播放 Dvd，使用者必須具有 MPEG-2 解碼器。</span><span class="sxs-lookup"><span data-stu-id="b2bf5-112">To play DVDs, the user must have an MPEG-2 decoder.</span></span>

 

<span data-ttu-id="b2bf5-113">此章節包含下列主題。</span><span class="sxs-lookup"><span data-stu-id="b2bf5-113">This section contains the following topics.</span></span>

-   [<span data-ttu-id="b2bf5-114">DirectShow 中的 DVD 支援功能</span><span class="sxs-lookup"><span data-stu-id="b2bf5-114">DVD Support Features in DirectShow</span></span>](dvd-support-features-in-directshow.md)
-   [<span data-ttu-id="b2bf5-115">DVD 基本概念</span><span class="sxs-lookup"><span data-stu-id="b2bf5-115">DVD Basics</span></span>](dvd-basics.md)
-   [<span data-ttu-id="b2bf5-116">建立 DVD 篩選圖形</span><span class="sxs-lookup"><span data-stu-id="b2bf5-116">Building the DVD Filter Graph</span></span>](building-the-dvd-filter-graph.md)
-   [<span data-ttu-id="b2bf5-117">取得 DVD 介面指標</span><span class="sxs-lookup"><span data-stu-id="b2bf5-117">Obtaining the DVD Interface Pointers</span></span>](obtaining-the-dvd-interface-pointers.md)
-   [<span data-ttu-id="b2bf5-118">DVD 命令</span><span class="sxs-lookup"><span data-stu-id="b2bf5-118">DVD Commands</span></span>](dvd-commands.md)
-   [<span data-ttu-id="b2bf5-119">識別有效的 DVD 作業</span><span class="sxs-lookup"><span data-stu-id="b2bf5-119">Identifying Valid DVD Operations</span></span>](identifying-valid-dvd-operations.md)
-   [<span data-ttu-id="b2bf5-120">同步處理 DVD 命令</span><span class="sxs-lookup"><span data-stu-id="b2bf5-120">Synchronizing DVD Commands</span></span>](synchronizing-dvd-commands.md)
-   [<span data-ttu-id="b2bf5-121">DVD 導覽器中的資料流程</span><span class="sxs-lookup"><span data-stu-id="b2bf5-121">Data Flow in the DVD Navigator</span></span>](data-flow-in-the-dvd-navigator.md)
-   [<span data-ttu-id="b2bf5-122">處理 DVD 事件通知</span><span class="sxs-lookup"><span data-stu-id="b2bf5-122">Handling DVD Event Notifications</span></span>](handling-dvd-event-notifications.md)
-   [<span data-ttu-id="b2bf5-123">使用 DVD 功能表</span><span class="sxs-lookup"><span data-stu-id="b2bf5-123">Working With DVD Menus</span></span>](working-with-dvd-menus.md)
-   [<span data-ttu-id="b2bf5-124">音訊和子圖片串流</span><span class="sxs-lookup"><span data-stu-id="b2bf5-124">Audio and Subpicture Streams</span></span>](audio-and-subpicture-streams.md)
-   [<span data-ttu-id="b2bf5-125">強制執行家長管理層級</span><span class="sxs-lookup"><span data-stu-id="b2bf5-125">Enforcing Parental Management Levels</span></span>](enforcing-parental-management-levels.md)
-   [<span data-ttu-id="b2bf5-126">儲存和還原 DvdState 物件</span><span class="sxs-lookup"><span data-stu-id="b2bf5-126">Saving and Restoring DvdState Objects</span></span>](saving-and-restoring-dvdstate-objects.md)
-   [<span data-ttu-id="b2bf5-127">使用 DVD 文字字串</span><span class="sxs-lookup"><span data-stu-id="b2bf5-127">Working with DVD Text Strings</span></span>](working-with-dvd-text-strings.md)
-   [<span data-ttu-id="b2bf5-128">播放卡拉卡拉的音訊串流</span><span class="sxs-lookup"><span data-stu-id="b2bf5-128">Playing Karaoke Audio Streams</span></span>](playing-karaoke-audio-streams.md)
-   [<span data-ttu-id="b2bf5-129">處理光碟 Ejections</span><span class="sxs-lookup"><span data-stu-id="b2bf5-129">Handling Disc Ejections</span></span>](handling-disc-ejections.md)
-   [<span data-ttu-id="b2bf5-130">Windows Vista 中的 DVD 播放增強功能</span><span class="sxs-lookup"><span data-stu-id="b2bf5-130">DVD Playback Enhancements in Windows Vista</span></span>](dvd-playback-enhancements-in-windows-vista.md)
-   [<span data-ttu-id="b2bf5-131">DVD 篩選圖形設定</span><span class="sxs-lookup"><span data-stu-id="b2bf5-131">DVD Filter Graph Configuration</span></span>](dvd-filter-graph-configuration.md)
-   [<span data-ttu-id="b2bf5-132">C + + DVD 參考頁面的快捷方式</span><span class="sxs-lookup"><span data-stu-id="b2bf5-132">Shortcuts to C++ DVD Reference Pages</span></span>](shortcuts-to-c-dvd-reference-pages.md)

<span data-ttu-id="b2bf5-133">如需有關 DVD/MPEG2 解碼器開發的參考，請參閱 [DirectShow 中的 Dvd 解碼器開發](dvd-decoder-development-in-directshow.md)。</span><span class="sxs-lookup"><span data-stu-id="b2bf5-133">For references on DVD/MPEG2 decoder development, see [DVD Decoder Development in DirectShow](dvd-decoder-development-in-directshow.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2bf5-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="b2bf5-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2bf5-135">使用 DirectShow</span><span class="sxs-lookup"><span data-stu-id="b2bf5-135">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



