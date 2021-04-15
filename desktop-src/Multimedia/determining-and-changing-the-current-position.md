---
title: 判斷及變更目前的位置
description: 判斷及變更目前的位置
ms.assetid: 20f78dcd-3259-43c2-8da3-8cfc299252e6
keywords:
- MCIWndGetStart 宏
- MCIWndGetEnd 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84a8e7022bdfcede526a730014a07deaf22fe66d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462285"
---
# <a name="determining-and-changing-the-current-position"></a><span data-ttu-id="578c2-105">判斷及變更目前的位置</span><span class="sxs-lookup"><span data-stu-id="578c2-105">Determining and Changing the Current Position</span></span>

<span data-ttu-id="578c2-106">當檔案或裝置與 MCIWnd 視窗相關聯時，會一開始就在內容開頭設定播放位置，不論媒體類型為何。</span><span class="sxs-lookup"><span data-stu-id="578c2-106">When a file or device is associated with an MCIWnd window, the playback position is initially set at the start of the content, regardless of the media type.</span></span> <span data-ttu-id="578c2-107">在播放期間，播放位置會以線性方式在內容中移動，如果播放是不中斷的，最後會到達內容的結尾。</span><span class="sxs-lookup"><span data-stu-id="578c2-107">During playback, the playback position moves linearly through the content and, if playback is uninterrupted, eventually reaches the end of the content.</span></span> <span data-ttu-id="578c2-108">如果發生中斷，則目前的播放位置是停止或暫停播放的位置。</span><span class="sxs-lookup"><span data-stu-id="578c2-108">If an interruption occurs, the current playback position is the location at which playback was stopped or paused.</span></span>

<span data-ttu-id="578c2-109">您可以使用 [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) 和 [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) 宏來取出內容開頭和結尾的位置。</span><span class="sxs-lookup"><span data-stu-id="578c2-109">You can retrieve the locations for the beginning and end of the content by using the [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) and [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) macros.</span></span> <span data-ttu-id="578c2-110">您可以藉由從 **MCIWndGetEnd** 所傳回的值減去 **MCIWndGetStart** 傳回的值，或使用 [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength)宏來判斷內容的長度。</span><span class="sxs-lookup"><span data-stu-id="578c2-110">You can determine the length of the content by subtracting the value returned by **MCIWndGetStart** from the value returned by **MCIWndGetEnd**, or by using the [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) macro.</span></span> <span data-ttu-id="578c2-111">您可以使用 [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) 宏來取出目前的播放位置，也可以使用 [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) 宏，以以 null 終止的字串形式取出播放位置。</span><span class="sxs-lookup"><span data-stu-id="578c2-111">You can retrieve the current playback position by using the [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) macro, or you can retrieve the playback position as a null-terminated string by using the [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) macro.</span></span>

<span data-ttu-id="578c2-112">若要變更目前的播放位置，請使用 [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome)、 [**MCIWndEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndend)和 [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) 宏。</span><span class="sxs-lookup"><span data-stu-id="578c2-112">To change the current playback position, use the [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome), [**MCIWndEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndend), and [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) macros.</span></span> <span data-ttu-id="578c2-113">您可以使用 **MCIWndHome** 或使用 **MCIWndEnd**，將播放位置移至內容的開頭。</span><span class="sxs-lookup"><span data-stu-id="578c2-113">You can move the playback position to the start of the content by using **MCIWndHome** or to the end of the content by using **MCIWndEnd**.</span></span> <span data-ttu-id="578c2-114">使用 **MCIWndSeek** 將播放位置移至內容中的任何位置。</span><span class="sxs-lookup"><span data-stu-id="578c2-114">Use **MCIWndSeek** to move the playback position to any location in the content.</span></span>

<span data-ttu-id="578c2-115">您也可以使用 [**MCIWndStep**](/windows/desktop/api/Vfw/nf-vfw-mciwndstep) 宏來逐步執行內容。</span><span class="sxs-lookup"><span data-stu-id="578c2-115">You can also step through the content by using the [**MCIWndStep**](/windows/desktop/api/Vfw/nf-vfw-mciwndstep) macro.</span></span> <span data-ttu-id="578c2-116">從目前的播放位置開始，此宏會以指定的增量向前或向後移動播放位置。</span><span class="sxs-lookup"><span data-stu-id="578c2-116">Beginning from the current playback position, this macro moves the playback position forward or backward by a specified increment.</span></span>

> [!Note]  
> <span data-ttu-id="578c2-117">用來指定位置的單位會因不同的媒體類型和裝置而有所不同。</span><span class="sxs-lookup"><span data-stu-id="578c2-117">The units used to specify position vary among the different media types and devices.</span></span> <span data-ttu-id="578c2-118">例如，MCIAVI 裝置所使用之 AVI 檔案的播放位置會以畫面格來測量;CD 音訊、波形音訊和 MIDI 檔案的播放位置會以毫秒為單位來測量。</span><span class="sxs-lookup"><span data-stu-id="578c2-118">For example, the playback position for AVI files used by the MCIAVI device is measured in frames; the playback position for CD audio, waveform-audio, and MIDI files is measured in milliseconds.</span></span>

 

<span data-ttu-id="578c2-119">其他媒體類型和協力廠商裝置的裝置可能會使用其他單位。</span><span class="sxs-lookup"><span data-stu-id="578c2-119">Devices for other media types and third-party devices might use other units.</span></span> <span data-ttu-id="578c2-120">如需決定這些單位的詳細資訊，請參閱 [播放增強功能](playback-enhancements.md)。</span><span class="sxs-lookup"><span data-stu-id="578c2-120">For information about determining these units, see [Playback Enhancements](playback-enhancements.md).</span></span>

 

 




