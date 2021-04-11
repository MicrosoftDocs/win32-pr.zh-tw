---
description: DVD 區域資訊的來源
ms.assetid: f4874aa7-c58a-49a3-9474-c621cc19156b
title: DVD 區域資訊的來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac426f995323bfd30d3430dccb4044c5f71a119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944665"
---
# <a name="sources-of-dvd-region-information"></a><span data-ttu-id="8cb04-103">DVD 區域資訊的來源</span><span class="sxs-lookup"><span data-stu-id="8cb04-103">Sources of DVD Region Information</span></span>

<span data-ttu-id="8cb04-104">DVD 區域資訊有三個來源可一起運作，以判斷在 Windows 電腦上播放 DVD 的區域。</span><span class="sxs-lookup"><span data-stu-id="8cb04-104">There are three sources of DVD region information that work together to determine the region for DVD playback on a Windows PC.</span></span>

-   <span data-ttu-id="8cb04-105">DVD 標題。</span><span class="sxs-lookup"><span data-stu-id="8cb04-105">DVD Title.</span></span> <span data-ttu-id="8cb04-106">大部分的 DVD 標題會標示為特定區域。</span><span class="sxs-lookup"><span data-stu-id="8cb04-106">Most DVD titles are marked for a specific region.</span></span> <span data-ttu-id="8cb04-107">有些標題只能在一個區域中播放，有些可在多個區域中播放，其他則可在所有區域中播放。</span><span class="sxs-lookup"><span data-stu-id="8cb04-107">Some titles can be played in only one region, some can be played in multiple regions, and others can be played all regions.</span></span> <span data-ttu-id="8cb04-108">區域1到6是在原始的 DVD-Video 規格中定義。</span><span class="sxs-lookup"><span data-stu-id="8cb04-108">Regions 1 through 6 were defined in the original DVD-Video specification.</span></span> <span data-ttu-id="8cb04-109">區域7目前未定義。</span><span class="sxs-lookup"><span data-stu-id="8cb04-109">Region 7 is currently undefined.</span></span> <span data-ttu-id="8cb04-110">已在1999中新增區域8以進行特殊場地，例如飛機。</span><span class="sxs-lookup"><span data-stu-id="8cb04-110">Region 8 was added in 1999 for special venues, such as airplanes.</span></span> <span data-ttu-id="8cb04-111">沒有視頻區域的 DVD-ROM 光碟 (，) 不應包含任何區域編碼。</span><span class="sxs-lookup"><span data-stu-id="8cb04-111">DVD-ROM discs (those with no video zone) should not contain any region coding.</span></span>
-   <span data-ttu-id="8cb04-112">DVD-ROM 磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="8cb04-112">DVD-ROM Drive.</span></span> <span data-ttu-id="8cb04-113">DVD-ROM 磁片磁碟機有兩種類型： RPC 階段 1 (RPC1) 磁片磁碟機和 RPC 第2階段 (RPC2) 磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="8cb04-113">There are two types of DVD-ROM drives: RPC Phase 1 (RPC1) drives and RPC Phase 2 (RPC2) drives.</span></span> <span data-ttu-id="8cb04-114">RPC1 磁片磁碟機沒有內建的區域管理硬體支援。</span><span class="sxs-lookup"><span data-stu-id="8cb04-114">RPC1 drives do not have built-in hardware support for region management.</span></span> <span data-ttu-id="8cb04-115">對於這些磁片磁碟機，Windows 會維護區域變更計數資訊，而區域只能變更一次。</span><span class="sxs-lookup"><span data-stu-id="8cb04-115">For these drives, Windows maintains the region change count information and the region can be changed only once.</span></span> <span data-ttu-id="8cb04-116">RPC2 磁片磁碟機會維護硬體中的區域變更計數資訊，而一般而言，這類磁片磁碟機的區域最多可以變更5次。</span><span class="sxs-lookup"><span data-stu-id="8cb04-116">RPC2 drives maintain the region change count information in hardware and in general the region of such drives can be changed up to 5 times.</span></span>
-   <span data-ttu-id="8cb04-117">DVD 解碼器。</span><span class="sxs-lookup"><span data-stu-id="8cb04-117">DVD Decoder.</span></span> <span data-ttu-id="8cb04-118">某些 DVD 解碼器、硬體或軟體是針對特定區域而設定。</span><span class="sxs-lookup"><span data-stu-id="8cb04-118">Some DVD decoders, hardware or software, are set for a specific region.</span></span> <span data-ttu-id="8cb04-119">一般情況下，使用者無法變更此解碼器的區域。</span><span class="sxs-lookup"><span data-stu-id="8cb04-119">In general, the user cannot change the decoder's region.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8cb04-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="8cb04-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cb04-121">Windows 中的 DVD 區域變更支援</span><span class="sxs-lookup"><span data-stu-id="8cb04-121">DVD Region Change Support in Windows</span></span>](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



