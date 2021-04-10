---
description: Microsoft Windows 網路元件已針對效能和擴充性而開發。
ms.assetid: 2160b93e-c126-4592-972c-d9cc14eec745
title: 高效能的 Windows 通訊端應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0496198ef3a8f11e6a840fd75d0083899d23d5a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026218"
---
# <a name="high-performance-windows-sockets-applications"></a><span data-ttu-id="4a7f7-103">高效能的 Windows 通訊端應用程式</span><span class="sxs-lookup"><span data-stu-id="4a7f7-103">High-performance Windows Sockets Applications</span></span>

<span data-ttu-id="4a7f7-104">Microsoft Windows 網路元件已針對效能和擴充性而開發。</span><span class="sxs-lookup"><span data-stu-id="4a7f7-104">Microsoft Windows networking components have been developed for performance and scalability.</span></span> <span data-ttu-id="4a7f7-105">這可讓應用程式將可用的網路頻寬最大化。</span><span class="sxs-lookup"><span data-stu-id="4a7f7-105">This enables applications to maximize available network bandwidth.</span></span> <span data-ttu-id="4a7f7-106">Windows 通訊端和 Windows TCP/IP 通訊協定堆疊已經過微調和簡化。</span><span class="sxs-lookup"><span data-stu-id="4a7f7-106">Windows Sockets and the Windows TCP/IP protocol stack have been tuned and streamlined.</span></span> <span data-ttu-id="4a7f7-107">如此一來，正確撰寫的 Windows 應用程式可以達成異常的輸送量和效能，如下列事實所示：</span><span class="sxs-lookup"><span data-stu-id="4a7f7-107">As a result, properly written Windows applications can achieve exceptional throughput and performance, as the following facts illustrate:</span></span>

-   <span data-ttu-id="4a7f7-108">Windows 能夠提供超過200000的同時 TCP 連線。</span><span class="sxs-lookup"><span data-stu-id="4a7f7-108">Windows is capable of servicing over 200,000 simultaneous TCP connections.</span></span>
-   <span data-ttu-id="4a7f7-109">在 SPECWeb96 所進行的測試中，Windows 上的 Internet information Server 會提供每秒25000個 HTTP 要求的服務。</span><span class="sxs-lookup"><span data-stu-id="4a7f7-109">In a test conducted by SPECWeb96, Internet Information Server on Windows serviced over 25,000 HTTP requests per second.</span></span>
-   <span data-ttu-id="4a7f7-110">Windows 在包含10個躍點的跨洲 gigabit 網路上設定超過750Mbps 的傳輸記錄。</span><span class="sxs-lookup"><span data-stu-id="4a7f7-110">Windows set a transmission record of over 750Mbps on a transcontinental gigabit network consisting of 10 hops.</span></span>

<span data-ttu-id="4a7f7-111">這些成就說明 Windows TCP/IP 可非常快速地處理資料。</span><span class="sxs-lookup"><span data-stu-id="4a7f7-111">These achievements illustrate that Windows TCP/IP processes data very quickly.</span></span> <span data-ttu-id="4a7f7-112">但是，許多應用程式都不會利用 Windows、TCP/IP 和 Windows 通訊端效能功能，因為它們不會在阻礙的技術中執行。</span><span class="sxs-lookup"><span data-stu-id="4a7f7-112">Many applications, however, do not take advantage of the Windows, TCP/IP, and Windows Sockets performance capabilities because they unknowingly implement performance-hampering techniques.</span></span>

<span data-ttu-id="4a7f7-113">在本指南中，您將瞭解如何找出常見的程式設計錯誤，以及如何避免這些錯誤。</span><span class="sxs-lookup"><span data-stu-id="4a7f7-113">In this guide, you will learn to identify common programming mistakes and how to avoid them.</span></span> <span data-ttu-id="4a7f7-114">然後，您將學習可讓 Windows 通訊端應用程式以最佳方式執行的技術。</span><span class="sxs-lookup"><span data-stu-id="4a7f7-114">Then, you will learn techniques that enable Windows Sockets applications to perform optimally.</span></span> <span data-ttu-id="4a7f7-115">本指南會在六個章節中提供。</span><span class="sxs-lookup"><span data-stu-id="4a7f7-115">This guide is presented in six sections.</span></span> <span data-ttu-id="4a7f7-116">區段的順序是刻意的;若要充分利用本指南，請依序閱讀。</span><span class="sxs-lookup"><span data-stu-id="4a7f7-116">The order of the sections is intentional; to get the most out of this guide, read it in order.</span></span> <span data-ttu-id="4a7f7-117">下表提供每個區段的連結，以及每個主題的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="4a7f7-117">The following table provides links to each section, as well as a brief description of each topic.</span></span>



| <span data-ttu-id="4a7f7-118">主題</span><span class="sxs-lookup"><span data-stu-id="4a7f7-118">Topic</span></span>                                                                                            | <span data-ttu-id="4a7f7-119">描述</span><span class="sxs-lookup"><span data-stu-id="4a7f7-119">Description</span></span>                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4a7f7-120">網路術語</span><span class="sxs-lookup"><span data-stu-id="4a7f7-120">Network Terminology</span></span>](network-terminology-2.md)                                                 | <span data-ttu-id="4a7f7-121">定義瞭解網路應用程式效能所需的網路術語和計量。</span><span class="sxs-lookup"><span data-stu-id="4a7f7-121">Defines networking terminology and metrics necessary to understanding the performance of a network application.</span></span>                                     |
| [<span data-ttu-id="4a7f7-122">效能維度</span><span class="sxs-lookup"><span data-stu-id="4a7f7-122">Performance Dimensions</span></span>](performance-dimensions-2.md)                                           | <span data-ttu-id="4a7f7-123">討論影響應用程式的認知和實際網路效能的效能維度。</span><span class="sxs-lookup"><span data-stu-id="4a7f7-123">Discusses performance dimensions that affect the perceived and actual network performance of an application.</span></span>                                        |
| [<span data-ttu-id="4a7f7-124">TCP/IP 特性</span><span class="sxs-lookup"><span data-stu-id="4a7f7-124">TCP/IP Characteristics</span></span>](tcp-ip-characteristics-2.md)                                           | <span data-ttu-id="4a7f7-125">定義可能導致寫入不良應用程式效能問題的 TCP/IP 通訊協定特性。</span><span class="sxs-lookup"><span data-stu-id="4a7f7-125">Defines TCP/IP protocol characteristics that can result in performance issues for a poorly written application.</span></span>                                     |
| [<span data-ttu-id="4a7f7-126">應用程式行為</span><span class="sxs-lookup"><span data-stu-id="4a7f7-126">Application Behavior</span></span>](application-behavior-2.md)                                               | <span data-ttu-id="4a7f7-127">說明如何辨識效能不良之網路應用程式的徵兆。</span><span class="sxs-lookup"><span data-stu-id="4a7f7-127">Explains how to recognize the signs of a poorly performing network application.</span></span>                                                                     |
| [<span data-ttu-id="4a7f7-128">改善應用程式緩慢</span><span class="sxs-lookup"><span data-stu-id="4a7f7-128">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)                               | <span data-ttu-id="4a7f7-129">提供應用程式設計問題的範例，這些問題會對效能不佳的應用程式造成影響，並變更程式碼以改善效能。</span><span class="sxs-lookup"><span data-stu-id="4a7f7-129">Provides samples of application design issues that contribute to a poorly performing application, and makes changes to code to improve performance.</span></span> |
| [<span data-ttu-id="4a7f7-130">互動式應用程式的最佳作法</span><span class="sxs-lookup"><span data-stu-id="4a7f7-130">Best Practices for Interactive Applications</span></span>](best-practices-for-interactive-applications-2.md) | <span data-ttu-id="4a7f7-131">列出開發最佳互動式網路應用程式所採用的最佳做法。</span><span class="sxs-lookup"><span data-stu-id="4a7f7-131">Lists the best practices to employ for developing optimal interactive network applications.</span></span>                                                         |



 

 

 



