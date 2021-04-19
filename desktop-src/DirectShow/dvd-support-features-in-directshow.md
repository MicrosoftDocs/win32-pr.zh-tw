---
description: DirectShow 中的 DVD 支援功能
ms.assetid: 20dc1067-696e-4f53-9c77-0f2da237c5af
title: DirectShow 中的 DVD 支援功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 035af51bbe44ec8dcc95f199c502b71d37d834f6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970691"
---
# <a name="dvd-support-features-in-directshow"></a><span data-ttu-id="7f3e6-103">DirectShow 中的 DVD 支援功能</span><span class="sxs-lookup"><span data-stu-id="7f3e6-103">DVD Support Features in DirectShow</span></span>

<span data-ttu-id="7f3e6-104">[Dvd](dvd-navigator-filter.md)導覽篩選器的功能是透過兩個介面（ [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)）公開，這會提供 DVD 導覽器的「設定」方法，而 [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)則提供「get」方法。</span><span class="sxs-lookup"><span data-stu-id="7f3e6-104">The functionality of the [DVD Navigator](dvd-navigator-filter.md) filter is exposed through two interfaces, [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2), which provides the "set" methods for the DVD Navigator, and [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2), which provides the "get" methods.</span></span>

<span data-ttu-id="7f3e6-105">DVD 導覽器支援下列功能：</span><span class="sxs-lookup"><span data-stu-id="7f3e6-105">The DVD Navigator supports the following features:</span></span>

-   <span data-ttu-id="7f3e6-106">卡拉卡拉支援：您可以使用 DVD 導覽器來撰寫 DVD 卡拉卡拉應用程式。</span><span class="sxs-lookup"><span data-stu-id="7f3e6-106">Karaoke support: You can write a DVD-karaoke application using the DVD Navigator.</span></span> <span data-ttu-id="7f3e6-107"> (這需要相容的解碼器。 ) </span><span class="sxs-lookup"><span data-stu-id="7f3e6-107">(This requires a compatible decoder.)</span></span>
-   <span data-ttu-id="7f3e6-108">簡化 DVD 文字資訊字串的存取： DVD 導覽器會剖析這些字串，並讓應用程式輕鬆地列舉、識別及取出它們。</span><span class="sxs-lookup"><span data-stu-id="7f3e6-108">Simplified access to DVD text information strings: The DVD Navigator parses these strings and enables applications to easily enumerate, identify, and retrieve them.</span></span>
-   <span data-ttu-id="7f3e6-109">透過 IBasicAudio 的音訊音量控制[ ](/windows/desktop/api/Control/nn-control-ibasicaudio)</span><span class="sxs-lookup"><span data-stu-id="7f3e6-109">Audio volume control through [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio)</span></span>
-   <span data-ttu-id="7f3e6-110">支援在發出 Stop 命令時自訂 DVD 瀏覽器的行為：應用程式可以指示 DVD 導覽器在重新開機篩選圖形時，從目前的位置繼續，或從光碟開頭開始播放。</span><span class="sxs-lookup"><span data-stu-id="7f3e6-110">Support for customizing the DVD Navigator's behavior when the Stop command is issued: Applications can instruct the DVD Navigator to either resume from the current location when restarting the filter graph, or start play from the beginning of the disc.</span></span>
-   <span data-ttu-id="7f3e6-111">數位劇院系統 (DTS) 和索尼動態數位音效 (SDD) 音訊支援。</span><span class="sxs-lookup"><span data-stu-id="7f3e6-111">Digital Theater Systems (DTS) and Sony Dynamic Digital Sound (SDDS) audio support.</span></span> <span data-ttu-id="7f3e6-112">音訊瀏覽器會辨識 DTS 和 SDD 音訊串流，並傳遞給音訊解碼器。</span><span class="sxs-lookup"><span data-stu-id="7f3e6-112">DTS and SDDS audio streams are recognized by the DVD Navigator and passed to the audio decoder.</span></span> <span data-ttu-id="7f3e6-113"> (需要協力廠商 DTS 相容或 SDD 相容的解碼器，以解碼和播放音訊。 ) </span><span class="sxs-lookup"><span data-stu-id="7f3e6-113">(A third-party DTS-compatible or SDDS-compatible decoder is required to decode and play the audio.)</span></span>
-   <span data-ttu-id="7f3e6-114">改進家長監護變更的支援： DVD 導覽器可讓應用程式接受、拒絕或忽略光碟中的家長監護變更命令。</span><span class="sxs-lookup"><span data-stu-id="7f3e6-114">Improved support for parental level changes: The DVD Navigator enables an application to accept, reject, or ignore parental level change commands from the disc.</span></span>
-   <span data-ttu-id="7f3e6-115">管理 DVD 導覽器狀態和同步處理命令的 Advanced 選項</span><span class="sxs-lookup"><span data-stu-id="7f3e6-115">Advanced options for managing the state of the DVD Navigator and synchronizing commands</span></span>
-   <span data-ttu-id="7f3e6-116">支援框架逐步執行、框架精確搜尋和反向播放。</span><span class="sxs-lookup"><span data-stu-id="7f3e6-116">Support for frame stepping, frame-accurate seeking, and reverse play.</span></span> <span data-ttu-id="7f3e6-117">這些功能需要支援的視頻解碼器。</span><span class="sxs-lookup"><span data-stu-id="7f3e6-117">These features require a video decoder that supports them.</span></span>
-   <span data-ttu-id="7f3e6-118">將目前位置儲存在標題中的功能，並隨時返回。</span><span class="sxs-lookup"><span data-stu-id="7f3e6-118">The ability to save the current location in a title and return to it at any time.</span></span>
-   <span data-ttu-id="7f3e6-119">針對非連續的 PGC 標題中的時間事件簡化支援：對於非連續的 PGC 標題，DVD 導覽器會將原始的時間代碼資訊轉送到應用程式。</span><span class="sxs-lookup"><span data-stu-id="7f3e6-119">Simplified support for time events in non-sequential PGC titles: For non-sequential PGC titles, the DVD Navigator relays the raw time code information to the application.</span></span>
-   <span data-ttu-id="7f3e6-120">時間碼資訊。</span><span class="sxs-lookup"><span data-stu-id="7f3e6-120">Time code information.</span></span> <span data-ttu-id="7f3e6-121">[**DVD \_ HMSF 時間 \_ 碼**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode)結構可用來取代二進位編碼的 decimal (BCD) 格式。</span><span class="sxs-lookup"><span data-stu-id="7f3e6-121">The [**DVD\_HMSF\_TIMECODE**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) structure can be used in place of the binary coded decimal (BCD) format.</span></span> <span data-ttu-id="7f3e6-122">**DVD \_HMSF 時間 \_ 碼** 包含很容易存取的成員（小時、分鐘、秒和框架），而且可以在 **ULONG** 之間轉換。</span><span class="sxs-lookup"><span data-stu-id="7f3e6-122">**DVD\_HMSF\_TIMECODE** contains easily accessed members for hours, minutes, seconds, and frames, and can be cast to/from a **ULONG**.</span></span>
-   <span data-ttu-id="7f3e6-123">控制篩選圖形是否在搜尋作業之後排清的能力：圖形緩衝區在任何指定時間最多可以包含幾秒鐘的影片。</span><span class="sxs-lookup"><span data-stu-id="7f3e6-123">The ability to control whether the filter graph flushes after a seek operation: The graph buffers can contain up to a few seconds of video at any given time.</span></span> <span data-ttu-id="7f3e6-124">您可以指示圖形在搜尋後完成播放已緩衝的影片，或立即在新位置開始播放。</span><span class="sxs-lookup"><span data-stu-id="7f3e6-124">You can instruct the graph to either finish playing the buffered video after a seek, or begin playing immediately at the new location.</span></span>
-   <span data-ttu-id="7f3e6-125">在一般參數暫存器中設定值的能力，這是熟悉想要執行先進功能之 DVD 規格的先進功能。</span><span class="sxs-lookup"><span data-stu-id="7f3e6-125">The ability to set values in general parameter registers: An advanced feature for those familiar with the DVD specification who wish to implement advanced functionality.</span></span>
-   <span data-ttu-id="7f3e6-126">產生數值光碟識別碼的能力，適用于所有實際用途</span><span class="sxs-lookup"><span data-stu-id="7f3e6-126">The ability to generate numeric disc identifiers that are for all practical purposes unique</span></span>

### <a name="what-background-do-i-need-to-write-a-dvd-application"></a><span data-ttu-id="7f3e6-127">我需要什麼背景才能撰寫 DVD 應用程式？</span><span class="sxs-lookup"><span data-stu-id="7f3e6-127">What Background Do I Need to Write a DVD Application?</span></span>

<span data-ttu-id="7f3e6-128">所有應用程式開發人員都應該對 DVD 技術所提供的功能有基本的認識，例如家長管理層級、多個音訊和子圖片串流，以及角度區塊。</span><span class="sxs-lookup"><span data-stu-id="7f3e6-128">All application developers should have a basic familiarity with the features provided by DVD technology such as parental management levels, multiple audio and subpicture streams, and angle blocks.</span></span> <span data-ttu-id="7f3e6-129">[DVD 基本概念](dvd-basics.md) 簡要說明這些功能;協力廠商發行集提供更完整的說明。</span><span class="sxs-lookup"><span data-stu-id="7f3e6-129">[DVD Basics](dvd-basics.md) briefly describes each of these features; more complete descriptions are available in third-party publications.</span></span> <span data-ttu-id="7f3e6-130">除非您想要在附錄 J 命令集以外執行先進的功能，否則不需要參照 DVD 規格。</span><span class="sxs-lookup"><span data-stu-id="7f3e6-130">You don't need to refer to the DVD specification unless you intend to implement advanced features beyond the Annex J command set.</span></span>

<span data-ttu-id="7f3e6-131">使用 DirectShow 的 c/c + + 開發人員應該熟悉 COM 用戶端程式設計技術，例如建立 COM 物件以及取得和釋放 COM 介面指標。</span><span class="sxs-lookup"><span data-stu-id="7f3e6-131">C/C++ developers using DirectShow should be familiar with COM client programming techniques such as creating COM objects and obtaining and releasing COM interface pointers.</span></span> <span data-ttu-id="7f3e6-132">您可能也需要篩選圖形作業的一般知識，因為您可能需要直接存取和操作圖形。</span><span class="sxs-lookup"><span data-stu-id="7f3e6-132">You might also need a general knowledge of filter graph operations, because you might need to access and manipulate the graph directly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f3e6-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="7f3e6-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f3e6-134">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="7f3e6-134">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



