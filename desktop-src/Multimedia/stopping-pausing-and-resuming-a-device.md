---
title: 停止、暫停和繼續裝置
description: 停止、暫停和繼續裝置
ms.assetid: df9ca4ab-4711-44dd-a058-909f291a1652
keywords:
- MCI_STOP 命令
- MCI_PAUSE 命令
- MCI_RESUME 命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ddcd9618608226dec108d62754964fe6401d429
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673335"
---
# <a name="stopping-pausing-and-resuming-a-device"></a><span data-ttu-id="ca768-106">停止、暫停和繼續裝置</span><span class="sxs-lookup"><span data-stu-id="ca768-106">Stopping, Pausing, and Resuming a Device</span></span>

<span data-ttu-id="ca768-107">[**Stop**](stop.md) ([**MCI \_ stop**](mci-stop.md)) 命令會暫停裝置的播放或錄製。</span><span class="sxs-lookup"><span data-stu-id="ca768-107">The [**stop**](stop.md) ([**MCI\_STOP**](mci-stop.md)) command suspends the playing or recording of a device.</span></span> <span data-ttu-id="ca768-108">許多裝置也支援 [**pause**](pause.md) ([**MCI \_ pause**](mci-pause.md)) 命令。</span><span class="sxs-lookup"><span data-stu-id="ca768-108">Many devices also support the [**pause**](pause.md) ([**MCI\_PAUSE**](mci-pause.md)) command.</span></span> <span data-ttu-id="ca768-109">[ **停止** ] 和 [ **暫停** ] 之間的差異取決於裝置。</span><span class="sxs-lookup"><span data-stu-id="ca768-109">The difference between **stop** and **pause** depends on the device.</span></span> <span data-ttu-id="ca768-110">通常會 **暫停** 暫止作業，但讓裝置準備好繼續播放或立即錄製。</span><span class="sxs-lookup"><span data-stu-id="ca768-110">Usually **pause** suspends operation but leaves the device ready to resume playing or recording immediately.</span></span>

<span data-ttu-id="ca768-111">使用 [**play**](play.md) ([**mci \_ play**](mci-play.md)) 或 [**記錄**](record.md) ([**MCI \_ 記錄**](mci-record.md)) 命令以重新開機裝置，將以 "to" (mci 指定的位置重設為) \_ ，然後 \_ 在裝置暫停或停止之前從 (旗標) mci。</span><span class="sxs-lookup"><span data-stu-id="ca768-111">Using the [**play**](play.md) ([**MCI\_PLAY**](mci-play.md)) or [**record**](record.md) ([**MCI\_RECORD**](mci-record.md)) command to restart a device resets the locations specified with the "to" (MCI\_TO) and "from" (MCI\_FROM) flags before the device was paused or stopped.</span></span> <span data-ttu-id="ca768-112">如果沒有 "from" 旗標，這些命令會將起始位置重設為目前的位置。</span><span class="sxs-lookup"><span data-stu-id="ca768-112">Without the "from" flag, these commands reset the starting location to the current position.</span></span> <span data-ttu-id="ca768-113">如果沒有「到」旗標，則會將結束位置重設為媒體的結尾。</span><span class="sxs-lookup"><span data-stu-id="ca768-113">Without the "to" flag, they reset the ending location to the end of the media.</span></span> <span data-ttu-id="ca768-114">若要繼續播放或錄製，而不重設先前指定的停止位置，請使用 **play** 或 **record** 命令的 "to" 旗標來指定結束位置。</span><span class="sxs-lookup"><span data-stu-id="ca768-114">To continue playing or recording without resetting a previously specified stop position, use the **play** or **record** command's "to" flag to specify an ending position.</span></span>

<span data-ttu-id="ca768-115">某些裝置支援 [**resume**](resume.md) ([**MCI \_ resume**](mci-resume.md)) 命令以重新開機已暫停的裝置。</span><span class="sxs-lookup"><span data-stu-id="ca768-115">Some devices support the [**resume**](resume.md) ([**MCI\_RESUME**](mci-resume.md)) command to restart a paused device.</span></span> <span data-ttu-id="ca768-116">此命令不會變更以 [**pause**](pause.md)命令前面的 **play** 或 **record** 命令指定的 "to" 和 "from" 位置。</span><span class="sxs-lookup"><span data-stu-id="ca768-116">This command does not change the "to" and "from" locations specified with the **play** or **record** command that preceded the [**pause**](pause.md) command.</span></span>

 

 




