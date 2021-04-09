---
description: 監視器會以即時模式接收已捕捉的網路畫面。 網路封包提供者會使用 IRTC COM 介面的提供者來捕捉框架 (NPP) ，然後在其中一個監視中將兩個執行執行緒的監視器傳遞給監視器。
ms.assetid: 50aa9da2-3a8a-4514-9b1b-9c8364d074d0
title: Real-Time 的捕獲
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24bdf5bc451173a98d1c4428674d308f8b3b8d79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852916"
---
# <a name="real-time-captures"></a><span data-ttu-id="13303-104">Real-Time 的捕獲</span><span class="sxs-lookup"><span data-stu-id="13303-104">Real-Time Captures</span></span>

<span data-ttu-id="13303-105">監視器會以即時模式接收已捕捉的網路畫面。</span><span class="sxs-lookup"><span data-stu-id="13303-105">Monitors receive captured network frames in real-time mode.</span></span> <span data-ttu-id="13303-106">[*網路封包提供者*](n.md)會使用提供者的 [IRTC](irtc.md) COM 介面 (NPP) 來捕捉框架，然後將這些框架傳遞給其中一個監視的兩個執行執行緒中的監視器。</span><span class="sxs-lookup"><span data-stu-id="13303-106">The frames are captured by a [*network packet provider*](n.md) (NPP) using the provider's [IRTC](irtc.md) COM interface, and passed on to the monitor in one of the monitor's two execution threads.</span></span>

<span data-ttu-id="13303-107">監視器可將 [*捕獲篩選器*](c.md) 傳遞至提供框架的 NPP，以限制它們必須處理的畫面格數目。</span><span class="sxs-lookup"><span data-stu-id="13303-107">Monitors can limit the number of frames they have to process by passing a [*capture filter*](c.md) to the NPP that is supplying the frames.</span></span> <span data-ttu-id="13303-108">一般而言，特定監視是設計來監看特定類型的流量，例如 HTTP、RIPX 或 SMB。</span><span class="sxs-lookup"><span data-stu-id="13303-108">Typically, a specific monitor is designed to watch for specific types of traffic, such as HTTP, RIPX, or SMB.</span></span> <span data-ttu-id="13303-109">不同于使用精密剖析器來選取要分析之資訊的專家，監視器必須檢查每個框架是否有設計偵測的條件。</span><span class="sxs-lookup"><span data-stu-id="13303-109">Unlike experts, which use sophisticated parsers to select the information to be analyzed, a monitor must examine each frame for the conditions it was designed to detect.</span></span> <span data-ttu-id="13303-110">這個框架框架的方法背後的原因是效能。</span><span class="sxs-lookup"><span data-stu-id="13303-110">The reason behind this frame-by-frame approach is performance.</span></span> <span data-ttu-id="13303-111">監視器必須快速處理其框架，使其不會落在驅動程式後方，以提供 NPP 的畫面。</span><span class="sxs-lookup"><span data-stu-id="13303-111">A monitor must process its frames quickly enough so that it does not fall behind the driver supplying the frames to the NPP.</span></span> <span data-ttu-id="13303-112">否則，資料將會遺失。</span><span class="sxs-lookup"><span data-stu-id="13303-112">Otherwise, data will be lost.</span></span>

 

 



