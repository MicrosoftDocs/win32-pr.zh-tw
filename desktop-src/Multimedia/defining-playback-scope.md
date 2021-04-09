---
title: 定義播放範圍
description: 定義播放範圍
ms.assetid: f2563226-7af1-4cb3-b468-c59738feeda2
keywords:
- MCIWndPlayFrom 宏
- MCIWndPlayTo 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518fc80588147c4ccbbca619452b714333a8a34d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932187"
---
# <a name="defining-playback-scope"></a><span data-ttu-id="efa7a-105">定義播放範圍</span><span class="sxs-lookup"><span data-stu-id="efa7a-105">Defining Playback Scope</span></span>

<span data-ttu-id="efa7a-106">MCIWnd 提供可讓您定義播放 *範圍* 的宏。</span><span class="sxs-lookup"><span data-stu-id="efa7a-106">MCIWnd provides macros that allow you to define the playback *scope*.</span></span> <span data-ttu-id="efa7a-107">範圍是您想要播放播放的部分。</span><span class="sxs-lookup"><span data-stu-id="efa7a-107">The scope is the portion of the playback you want to play.</span></span> <span data-ttu-id="efa7a-108">例如，您可以使用 [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) 宏，從開始位置以外的位置播放內容。</span><span class="sxs-lookup"><span data-stu-id="efa7a-108">For example, you can play the content from a position other than the beginning position by using the [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) macro.</span></span> <span data-ttu-id="efa7a-109">此宏會移至指定的位置、開始播放，然後繼續至內容的結尾。</span><span class="sxs-lookup"><span data-stu-id="efa7a-109">This macro moves to the specified position, begins playback, and continues to the end of the content.</span></span> <span data-ttu-id="efa7a-110">同樣地，您可以使用 [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) 宏來播放內容到指定的結束點。</span><span class="sxs-lookup"><span data-stu-id="efa7a-110">Similarly, you can play the content to a specified end point by using the [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) macro.</span></span> <span data-ttu-id="efa7a-111">這個宏會從目前的播放位置開始播放，直到到達指定的位置或到達內容的結尾為止（以先達到者為准）。</span><span class="sxs-lookup"><span data-stu-id="efa7a-111">This macro starts at the current playback position and plays until it reaches the specified position or the end of the content is reached, whichever comes first.</span></span>

<span data-ttu-id="efa7a-112">此外，您也可以使用 [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) 宏來定義開始和結束位置。</span><span class="sxs-lookup"><span data-stu-id="efa7a-112">Also, you can define both the beginning and ending positions by using the [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) macro.</span></span> <span data-ttu-id="efa7a-113">這個宏會移至指定的開始位置並播放，直到到達指定的結束位置或內容結尾為止。</span><span class="sxs-lookup"><span data-stu-id="efa7a-113">This macro moves to the specified starting position and plays until the specified ending position or the end of the content is reached.</span></span>

 

 




