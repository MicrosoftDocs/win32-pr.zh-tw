---
description: 關於影片捕獲裝置
ms.assetid: 1bf6e64f-c3cf-45a4-9f87-1b8cf503d98b
title: 關於影片捕獲裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98ab9797c11b5c22f6196a5b4e781e50ce34edec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687864"
---
# <a name="about-video-capture-devices"></a><span data-ttu-id="2f1ae-103">關於影片捕獲裝置</span><span class="sxs-lookup"><span data-stu-id="2f1ae-103">About Video Capture Devices</span></span>

<span data-ttu-id="2f1ae-104">大部分新的影片捕獲裝置都會使用 Windows Driver Model (WDM) 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="2f1ae-104">Most new video capture devices use Windows Driver Model (WDM) drivers.</span></span> <span data-ttu-id="2f1ae-105">在 WDM 架構中，Microsoft 提供一組與硬體無關的驅動程式，稱為類別驅動程式，硬體廠商則提供硬體特定的 minidrivers。</span><span class="sxs-lookup"><span data-stu-id="2f1ae-105">In the WDM architecture, Microsoft supplies a set of hardware-independent drivers, called class drivers, and the hardware vendor provides hardware-specific minidrivers.</span></span> <span data-ttu-id="2f1ae-106">迷你驅動程式會實作用於裝置的任何函式;針對大部分的函式，迷你驅動程式會呼叫 Microsoft class 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="2f1ae-106">A minidriver implements any functions that are specific to the device; for most functions, the minidriver calls the Microsoft class driver.</span></span>

<span data-ttu-id="2f1ae-107">在 DirectShow 篩選圖形中，任何 WDM 捕獲裝置都會顯示為 [Wdm 影片捕獲](wdm-video-capture-filter.md) 篩選器。</span><span class="sxs-lookup"><span data-stu-id="2f1ae-107">In a DirectShow filter graph, any WDM capture device appears as the [WDM Video Capture](wdm-video-capture-filter.md) filter.</span></span> <span data-ttu-id="2f1ae-108">WDM 影片捕獲篩選器會根據驅動程式的特性來設定本身。</span><span class="sxs-lookup"><span data-stu-id="2f1ae-108">The WDM Video Capture filter configures itself based on the characteristics of the driver.</span></span> <span data-ttu-id="2f1ae-109">它會顯示在驅動程式所提供的名稱底下，在圖形中的任何位置都不會看到名為「WDM 影片捕獲篩選器」的篩選。</span><span class="sxs-lookup"><span data-stu-id="2f1ae-109">It appears under a name provided by the driver — you will not see a filter called "WDM Video Capture Filter" anywhere in the graph.</span></span>

<span data-ttu-id="2f1ae-110">某些較舊的捕獲裝置仍會使用適用于 Windows (VFW) 驅動程式的影片。</span><span class="sxs-lookup"><span data-stu-id="2f1ae-110">Some older capture devices still use Video for Windows (VFW) drivers.</span></span> <span data-ttu-id="2f1ae-111">雖然這些驅動程式現在已過時，但可透過 [VFW Capture](vfw-capture-filter.md) 篩選器在 DirectShow 中受到支援。</span><span class="sxs-lookup"><span data-stu-id="2f1ae-111">Although these drivers are now obsolete, they are supported in DirectShow through the [VFW Capture](vfw-capture-filter.md) filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f1ae-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="2f1ae-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f1ae-113">關於 DirectShow 中的影片捕獲</span><span class="sxs-lookup"><span data-stu-id="2f1ae-113">About Video Capture in DirectShow</span></span>](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



