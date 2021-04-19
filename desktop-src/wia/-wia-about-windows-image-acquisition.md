---
description: Windows 映像取得 (WIA) 介面是 (DDI) 的 API 和設備磁碟機介面。
ms.assetid: 725543f8-6e33-4e22-904c-95cbec0388c8
title: 關於 Windows 映像取得
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80eed6289f7a30476ea6889c947577ad003b656e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974285"
---
# <a name="about-windows-image-acquisition"></a><span data-ttu-id="cdf94-103">關於 Windows 映像取得</span><span class="sxs-lookup"><span data-stu-id="cdf94-103">About Windows Image Acquisition</span></span>

<span data-ttu-id="cdf94-104">Windows 映像取得 (WIA) 介面是 (DDI) 的 API 和設備磁碟機介面。</span><span class="sxs-lookup"><span data-stu-id="cdf94-104">The Windows Image Acquisition (WIA) interface is both an API and a device driver interface (DDI).</span></span> <span data-ttu-id="cdf94-105">WIA API 的設計目的是要讓應用程式能夠：</span><span class="sxs-lookup"><span data-stu-id="cdf94-105">The WIA API is designed to allow applications to:</span></span>

-   <span data-ttu-id="cdf94-106">在穩固且穩定的環境中執行。</span><span class="sxs-lookup"><span data-stu-id="cdf94-106">Run in a robust and stable environment.</span></span>
-   <span data-ttu-id="cdf94-107">將互通性問題降至最低。</span><span class="sxs-lookup"><span data-stu-id="cdf94-107">Minimize interoperability problems.</span></span>
-   <span data-ttu-id="cdf94-108">列舉可用的映射取得裝置。</span><span class="sxs-lookup"><span data-stu-id="cdf94-108">Enumerate available image acquisition devices.</span></span>
-   <span data-ttu-id="cdf94-109">同時建立多個裝置的連接。</span><span class="sxs-lookup"><span data-stu-id="cdf94-109">Create connections to multiple devices simultaneously.</span></span>
-   <span data-ttu-id="cdf94-110">以標準且可擴充的方式查詢裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="cdf94-110">Query properties of devices in a standard and expandable manner.</span></span>
-   <span data-ttu-id="cdf94-111">使用標準和高效能傳輸機制來取得裝置資料。</span><span class="sxs-lookup"><span data-stu-id="cdf94-111">Acquire device data using standard and high performance transfer mechanisms.</span></span>
-   <span data-ttu-id="cdf94-112">維護資料傳輸之間的影像屬性。</span><span class="sxs-lookup"><span data-stu-id="cdf94-112">Maintain image properties across data transfers.</span></span>
-   <span data-ttu-id="cdf94-113">收到各種裝置事件的通知。</span><span class="sxs-lookup"><span data-stu-id="cdf94-113">Be notified of a wide variety of device events.</span></span>

<span data-ttu-id="cdf94-114">WIADDI 的設計目的是要將硬體廠商必須撰寫的程式碼數量降到最低，同時維持製作個別解決方案的彈性。</span><span class="sxs-lookup"><span data-stu-id="cdf94-114">The WIADDI is designed to minimize the amount of code a hardware vendor must write, while maintaining the flexibility to craft individual solutions.</span></span> <span data-ttu-id="cdf94-115">這可透過下列方式完成：</span><span class="sxs-lookup"><span data-stu-id="cdf94-115">This is accomplished by:</span></span>

-   <span data-ttu-id="cdf94-116">提供可執行大部分驅動程式作業的標準裝置服務程式庫。</span><span class="sxs-lookup"><span data-stu-id="cdf94-116">Providing a standard device service library that performs most driver operations.</span></span>
-   <span data-ttu-id="cdf94-117">提升產業裝置通訊標準，讓一個 WIA 驅動程式支援大部分的 WIA 裝置。</span><span class="sxs-lookup"><span data-stu-id="cdf94-117">Promoting industry device communications standards so that one WIA driver supports most WIA devices.</span></span> <span data-ttu-id="cdf94-118">例如，圖片傳輸通訊協定 (PTP) 。</span><span class="sxs-lookup"><span data-stu-id="cdf94-118">For example, Picture Transfer Protocol (PTP).</span></span>
-   <span data-ttu-id="cdf94-119">允許設備磁碟機支援自訂介面，而不需要使用標準裝置服務程式庫。</span><span class="sxs-lookup"><span data-stu-id="cdf94-119">Allowing the device driver to support custom interfaces, while not requiring that it use the standard device service library.</span></span> <span data-ttu-id="cdf94-120">不過，驅動程式仍然需要執行標準的 WIA 介面。</span><span class="sxs-lookup"><span data-stu-id="cdf94-120">However, drivers still need to implement the standard WIA interfaces.</span></span>

<span data-ttu-id="cdf94-121">本節提供下欄區域中的 WIA 介面簡短總覽：</span><span class="sxs-lookup"><span data-stu-id="cdf94-121">This section presents a brief overview of the WIA interface in the following areas:</span></span>

-   [<span data-ttu-id="cdf94-122">WIA 架構</span><span class="sxs-lookup"><span data-stu-id="cdf94-122">WIA Architecture</span></span>](-wia-wia-architecture.md)
-   [<span data-ttu-id="cdf94-123">STI 相容性</span><span class="sxs-lookup"><span data-stu-id="cdf94-123">STI Compatibility</span></span>](-wia-sti-compatibility.md)
-   [<span data-ttu-id="cdf94-124">TWAIN 相容性</span><span class="sxs-lookup"><span data-stu-id="cdf94-124">TWAIN Compatibility</span></span>](-wia-twain-compatibility.md)
-   [<span data-ttu-id="cdf94-125">WIA 裝置管理員</span><span class="sxs-lookup"><span data-stu-id="cdf94-125">WIA Device Manager</span></span>](-wia-wia-device-manager.md)
-   [<span data-ttu-id="cdf94-126">WIA 迷你驅動程式服務程式庫</span><span class="sxs-lookup"><span data-stu-id="cdf94-126">WIA Minidriver Service Library</span></span>](-wia-wia-minidriver-service-library.md)
-   [<span data-ttu-id="cdf94-127">WIA 迷你驅動程式</span><span class="sxs-lookup"><span data-stu-id="cdf94-127">WIA Minidriver</span></span>](-wia-wia-minidriver.md)

 

 



