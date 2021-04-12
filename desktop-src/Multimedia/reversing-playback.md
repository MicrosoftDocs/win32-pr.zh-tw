---
title: 反轉播放
description: 反轉播放
ms.assetid: cb7c1293-42d7-4c74-b9e6-cc8899ca7c54
keywords:
- MCIWndPlayReverse 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a708915679f75bfe478c160d71d35b0bcfa48a23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372155"
---
# <a name="reversing-playback"></a><span data-ttu-id="821d9-104">反轉播放</span><span class="sxs-lookup"><span data-stu-id="821d9-104">Reversing Playback</span></span>

<span data-ttu-id="821d9-105">某些裝置支援以反向方向播放。</span><span class="sxs-lookup"><span data-stu-id="821d9-105">Some devices support playback in the reverse direction.</span></span> <span data-ttu-id="821d9-106">您可以使用 [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) 宏，以相反的方向播放這類裝置的內容。</span><span class="sxs-lookup"><span data-stu-id="821d9-106">You can play the content of such a device in the reverse direction by using the [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) macro.</span></span> <span data-ttu-id="821d9-107">此宏會定義從目前播放位置到內容開頭的播放範圍。</span><span class="sxs-lookup"><span data-stu-id="821d9-107">This macro defines the playback scope from the current playback position to the beginning of the content.</span></span> <span data-ttu-id="821d9-108">數位影片裝置 MCIAVI。WINSPOOL.DRV，可以向後播放。</span><span class="sxs-lookup"><span data-stu-id="821d9-108">The digital-video device, MCIAVI.DRV, can play backward.</span></span> <span data-ttu-id="821d9-109">無法回溯播放的裝置（例如 CD 音訊）可以在叫用 **MCIWndPlayReverse** 時發出錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="821d9-109">Devices that cannot play backward, such as CD audio, can issue an error message when **MCIWndPlayReverse** is invoked.</span></span>

 

 




