---
description: DirectShow 系統總覽
ms.assetid: aea1ab83-4c48-4b61-8a20-0ee6ad62ebe3
title: DirectShow 系統總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833fed4031c95ddb4ecbf91e7bb27c27741acc18
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509808"
---
# <a name="directshow-system-overview"></a><span data-ttu-id="79560-103">DirectShow 系統總覽</span><span class="sxs-lookup"><span data-stu-id="79560-103">DirectShow System Overview</span></span>

<span data-ttu-id="79560-104">**多媒體的挑戰**</span><span class="sxs-lookup"><span data-stu-id="79560-104">**The Challenge of Multimedia**</span></span>

<span data-ttu-id="79560-105">使用多媒體會帶來幾項重大挑戰：</span><span class="sxs-lookup"><span data-stu-id="79560-105">Working with multimedia presents several major challenges:</span></span>

-   <span data-ttu-id="79560-106">多媒體串流包含大量資料，必須非常快速地處理。</span><span class="sxs-lookup"><span data-stu-id="79560-106">Multimedia streams contain large amounts of data, which must be processed very quickly.</span></span>
-   <span data-ttu-id="79560-107">音訊和影片必須進行同步處理，以同時開始和停止，並以相同的速率播放。</span><span class="sxs-lookup"><span data-stu-id="79560-107">Audio and video must be synchronized so that it starts and stops at the same time, and plays at the same rate.</span></span>
-   <span data-ttu-id="79560-108">資料可能來自許多來源，包括本機檔案、電腦網路、電視廣播和攝影機。</span><span class="sxs-lookup"><span data-stu-id="79560-108">Data can come from many sources, including local files, computer networks, television broadcasts, and video cameras.</span></span>
-   <span data-ttu-id="79560-109">資料有各種不同的格式，例如 Audio-Video 交錯 (AVI) 、先進的串流格式 (ASF) 、運動圖片專家群組 (MPEG) 和數位視訊 (DV) 。</span><span class="sxs-lookup"><span data-stu-id="79560-109">Data comes in a variety of formats, such as Audio-Video Interleaved (AVI), Advanced Streaming Format (ASF), Motion Picture Experts Group (MPEG), and Digital Video (DV).</span></span>
-   <span data-ttu-id="79560-110">程式設計師事先不知道使用者的系統上會有哪些硬體裝置。</span><span class="sxs-lookup"><span data-stu-id="79560-110">The programmer does not know in advance what hardware devices will be present on the end-user's system.</span></span>

<span data-ttu-id="79560-111">**DirectShow 解決方案**</span><span class="sxs-lookup"><span data-stu-id="79560-111">**The DirectShow Solution**</span></span>

<span data-ttu-id="79560-112">DirectShow 的設計目的是要解決這些挑戰。</span><span class="sxs-lookup"><span data-stu-id="79560-112">DirectShow is designed to address each of these challenges.</span></span> <span data-ttu-id="79560-113">其主要設計目標是要簡化在 Windows 平臺上建立數位媒體應用程式的工作，方法是將應用程式與資料傳輸、硬體差異和同步處理的複雜性隔離。</span><span class="sxs-lookup"><span data-stu-id="79560-113">Its main design goal is to simplify the task of creating digital media applications on the Windows platform, by isolating applications from the complexities of data transports, hardware differences, and synchronization.</span></span>

<span data-ttu-id="79560-114">為了達成串流影片和音訊所需的輸送量，DirectShow 盡可能使用 Direct3D 和 DirectSound。</span><span class="sxs-lookup"><span data-stu-id="79560-114">To achieve the throughput needed to stream video and audio, DirectShow uses Direct3D and DirectSound whenever possible.</span></span> <span data-ttu-id="79560-115">這些技術會將資料有效率地轉譯成使用者的音效和圖形卡。</span><span class="sxs-lookup"><span data-stu-id="79560-115">These technologies render data efficiently to the user's sound and graphics cards.</span></span> <span data-ttu-id="79560-116">DirectShow 會以時間戳記範例封裝媒體資料來同步播放。</span><span class="sxs-lookup"><span data-stu-id="79560-116">DirectShow synchronizes playback by encapsulating media data in time-stamped samples.</span></span> <span data-ttu-id="79560-117">為了處理可能的各種來源、格式和硬體裝置，DirectShow 使用模組化架構，其中應用程式會混合使用並符合不同的軟體元件（稱為 *篩選器*）。</span><span class="sxs-lookup"><span data-stu-id="79560-117">To handle the variety of sources, formats, and hardware devices that are possible, DirectShow uses a modular architecture, in which the application mixes and matches different software components called *filters*.</span></span>

<span data-ttu-id="79560-118">DirectShow 提供的篩選器可支援根據 Windows Driver Model (WDM) 來捕捉和調整裝置，以及支援 Windows (VfW) 捕捉卡的較舊影片的篩選器，以及針對音訊壓縮管理員所撰寫的編解碼器 (BC-VCM-LVM-HYPERV) 介面。</span><span class="sxs-lookup"><span data-stu-id="79560-118">DirectShow provides filters that support capture and tuning devices based on the Windows Driver Model (WDM), as well as filters that support older Video for Windows (VfW) capture cards, and codecs written for the Audio Compression Manager (ACM) and Video Compression Manager (VCM) interfaces.</span></span>

<span data-ttu-id="79560-119">下圖顯示應用程式、DirectShow 元件，以及一些 DirectShow 支援的硬體和軟體元件之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="79560-119">The following diagram shows the relationship between an application, the DirectShow components, and some of the hardware and software components that DirectShow supports.</span></span>

![高層級架構](images/arch-oview2.png)

<span data-ttu-id="79560-121">如下所示，DirectShow 篩選器會與各種裝置（包括本機檔案系統、電視調諧器和影片捕捉卡、VfW 編解碼器、影片顯示 (透過 DirectDraw 或 GDI) ），以及透過 DirectSound)  (的音效卡進行通訊。</span><span class="sxs-lookup"><span data-stu-id="79560-121">As illustrated here, DirectShow filters communicate with, and control, a wide variety of devices, including the local file system, TV tuner and video capture cards, VfW codecs, the video display (through DirectDraw or GDI), and the sound card (through DirectSound).</span></span> <span data-ttu-id="79560-122">因此，DirectShow 會將應用程式與這些裝置的許多複雜性隔離開來。</span><span class="sxs-lookup"><span data-stu-id="79560-122">Thus, DirectShow insulates the application from many of the complexities of these devices.</span></span> <span data-ttu-id="79560-123">DirectShow 也提供特定檔案格式的原生壓縮和解壓縮篩選。</span><span class="sxs-lookup"><span data-stu-id="79560-123">DirectShow also provides native compression and decompression filters for certain file formats.</span></span>

## <a name="related-topics"></a><span data-ttu-id="79560-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="79560-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79560-125">關於 DirectShow</span><span class="sxs-lookup"><span data-stu-id="79560-125">About DirectShow</span></span>](about-directshow.md)
</dt> </dl>

 

 



