---
title: 啟動、暫停和繼續播放
description: 啟動、暫停和繼續播放
ms.assetid: 4af92781-5461-4195-82f5-a9213a9bdbd7
keywords:
- MCIWndPlay 宏
- MCIWndPause 宏
- MCIWndResume 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 734a186b90b8d6701923d0ffa1f743cc8c5ae378
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104184133"
---
# <a name="starting-pausing-and-resuming-playback"></a><span data-ttu-id="46121-106">啟動、暫停和繼續播放</span><span class="sxs-lookup"><span data-stu-id="46121-106">Starting, Pausing, and Resuming Playback</span></span>

<span data-ttu-id="46121-107">[**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) 是最常見的播放宏。</span><span class="sxs-lookup"><span data-stu-id="46121-107">[**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) is the most general playback macro.</span></span> <span data-ttu-id="46121-108">此宏可讓您從目前的播放位置播放檔案或裝置。</span><span class="sxs-lookup"><span data-stu-id="46121-108">This macro lets you play a file or device from the current playback position.</span></span> <span data-ttu-id="46121-109">除非已中斷，否則播放會繼續直到內容結束為止。</span><span class="sxs-lookup"><span data-stu-id="46121-109">Playback continues through the end of the content unless it is interrupted.</span></span>

<span data-ttu-id="46121-110">您可以使用 [**MCIWndPause**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) 宏暫時中斷現正播放的裝置。</span><span class="sxs-lookup"><span data-stu-id="46121-110">You can temporarily interrupt a device that is playing by using the [**MCIWndPause**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) macro.</span></span> <span data-ttu-id="46121-111">若要從暫停的位置繼續播放，請使用 [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) 宏。</span><span class="sxs-lookup"><span data-stu-id="46121-111">To resume playback from the paused position, use the [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) macro.</span></span> <span data-ttu-id="46121-112">有些裝置不支援暫停和繼續命令。</span><span class="sxs-lookup"><span data-stu-id="46121-112">Some devices do not support the pause and resume commands.</span></span> <span data-ttu-id="46121-113">這些裝置通常會將 **MCIWndPause** 對應至 [**MCIWndStop**](/windows/desktop/api/Vfw/nf-vfw-mciwndstop) 宏，以停止播放或錄製。</span><span class="sxs-lookup"><span data-stu-id="46121-113">These devices usually map **MCIWndPause** to the [**MCIWndStop**](/windows/desktop/api/Vfw/nf-vfw-mciwndstop) macro, which stops playback or recording.</span></span> <span data-ttu-id="46121-114">您可以使用 **MCIWndPlay** 重新開機不支援暫停或繼續的裝置，這會從目前的播放位置開始播放。</span><span class="sxs-lookup"><span data-stu-id="46121-114">You can restart a device that does not support pause or resume by using **MCIWndPlay**, which starts playback from the current playback position.</span></span>

 

 




