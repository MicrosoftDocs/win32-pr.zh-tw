---
description: Windows 映像取得 (WIA) 掃描器裝置會實作為 IWiaItem 物件的階層式樹狀結構。
ms.assetid: d716faec-9ace-422d-b6eb-ad4d86c1b0fd
title: WIA 1.0 中的 WIA 掃描器裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443277b0b580a481b523739cd5bc21642d827252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690556"
---
# <a name="wia-scanner-devices-in-wia-10"></a><span data-ttu-id="d6c75-103">WIA 1.0 中的 WIA 掃描器裝置</span><span class="sxs-lookup"><span data-stu-id="d6c75-103">WIA Scanner Devices in WIA 1.0</span></span>

> [!Note]  
> <span data-ttu-id="d6c75-104">本主題討論使用 windows 映射取得 (WIA) 1.0 服務 (（Windows XP 或更早的) 所支援）之應用程式的掃描器裝置樹狀目錄。</span><span class="sxs-lookup"><span data-stu-id="d6c75-104">This topic discusses the scanner device tree for applications that use the Windows Image Acquisition (WIA) 1.0 service (which is supported on Windows XP or earlier).</span></span> <span data-ttu-id="d6c75-105">如需 windows Vista 或更新版本) 所支援的 Windows 映像取得之裝置樹 (WIA) 2.0 (專案的詳細資訊，請參閱 [關於 IWiaItem2 專案樹狀結構](-wia-about-item-tree.md)。</span><span class="sxs-lookup"><span data-stu-id="d6c75-105">For information on the device tree of Windows Image Acquisition (WIA) 2.0 items (which are supported on Windows Vista or later), see [About the IWiaItem2 Item Tree](-wia-about-item-tree.md).</span></span>

 

<span data-ttu-id="d6c75-106">Windows 映像取得 (WIA) 掃描器裝置會實作為 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) 物件的階層式樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="d6c75-106">The Windows Image Acquisition (WIA) scanner device is implemented as a hierarchical tree of [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) objects.</span></span> <span data-ttu-id="d6c75-107">從根專案，應用程式可能會：</span><span class="sxs-lookup"><span data-stu-id="d6c75-107">From the root item an application may:</span></span>

-   <span data-ttu-id="d6c75-108">查詢掃描器功能</span><span class="sxs-lookup"><span data-stu-id="d6c75-108">Query scanner capabilities</span></span>
-   <span data-ttu-id="d6c75-109">設定掃描器裝置屬性</span><span class="sxs-lookup"><span data-stu-id="d6c75-109">Set scanner device properties</span></span>
-   <span data-ttu-id="d6c75-110">控制檔送紙器</span><span class="sxs-lookup"><span data-stu-id="d6c75-110">Control the document feeder</span></span>

<span data-ttu-id="d6c75-111">WIA 掃描器裝置與 WIA 攝影機裝置不同，因為在一般情況下，它不會將多個映射儲存在記憶體中。</span><span class="sxs-lookup"><span data-stu-id="d6c75-111">A WIA scanner device is different from a WIA camera device because, in general, it does not store multiple images in memory.</span></span>

<span data-ttu-id="d6c75-112">在根專案底下，典型的掃描器物件具有單一 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) 物件，代表裝置的資料收集功能，也就是掃描專案。</span><span class="sxs-lookup"><span data-stu-id="d6c75-112">Underneath the root item, a typical scanner object has a single [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) object that represents the data collecting functionality of the device, the Scan Item.</span></span> <span data-ttu-id="d6c75-113">此專案已設定 [**WiaItemTypeFile**](-wia-wia-item-type-flags.md) 旗標，以表示可以在此專案上進行資料傳輸。</span><span class="sxs-lookup"><span data-stu-id="d6c75-113">This item has the [**WiaItemTypeFile**](-wia-wia-item-type-flags.md) flag set to indicate that data transfers on this item are possible.</span></span> <span data-ttu-id="d6c75-114">應用程式會藉由設定掃描專案的屬性來設定掃描，然後執行掃描，並使用資料傳輸介面傳送資料。</span><span class="sxs-lookup"><span data-stu-id="d6c75-114">An application sets up a scan by setting the properties of the scan item, then performs the scan and transfers the data using a data transfer interface.</span></span>

<span data-ttu-id="d6c75-115">下圖說明典型掃描器的 WIA 執行：</span><span class="sxs-lookup"><span data-stu-id="d6c75-115">The following diagram illustrates the WIA implementation for a typical scanner:</span></span>

![一般掃描器的 wia 執行](images/wiscantr.gif)

<span data-ttu-id="d6c75-117">典型的雙工掃描器會以 WIA 中的一個 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) 物件來表示。</span><span class="sxs-lookup"><span data-stu-id="d6c75-117">A typical duplex scanner is represented in WIA by having one [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) object.</span></span> <span data-ttu-id="d6c75-118">每個頁面會依序存取一次資料傳輸的上一頁和上一頁資料。</span><span class="sxs-lookup"><span data-stu-id="d6c75-118">Front- and back-page data is accessed sequentially one data transfer per page.</span></span> <span data-ttu-id="d6c75-119">因此，雙工掃描器的表示方式與典型掃描器的標記法相同。</span><span class="sxs-lookup"><span data-stu-id="d6c75-119">Therefore, the representation of a duplex scanner is identical to the representation of a typical scanner.</span></span>

<span data-ttu-id="d6c75-120">可以在單一掃描工作中掃描多個投影片的投影片掃描器，會將每個個別的影像表示為個別的 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) 物件。</span><span class="sxs-lookup"><span data-stu-id="d6c75-120">A slide scanner capable of scanning multiple slides in a single scan operation represents each separate image as a separate [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) object.</span></span>

<span data-ttu-id="d6c75-121">下圖說明投影片掃描器的 WIA 標記法：</span><span class="sxs-lookup"><span data-stu-id="d6c75-121">The following diagram illustrates the WIA representation of a slide scanner:</span></span>

![投影片掃描器](images/wislscan.gif)

 

 



