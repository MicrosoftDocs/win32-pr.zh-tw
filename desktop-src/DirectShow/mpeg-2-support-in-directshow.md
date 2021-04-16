---
description: DirectShow 中的 MPEG 2 支援
ms.assetid: a4fe4cc9-86a5-4c83-94be-8901b97c8280
title: DirectShow 中的 MPEG 2 支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f42b0d49159a28b3ad29a0141c296c0fd0076fdd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510210"
---
# <a name="mpeg-2-support-in-directshow"></a><span data-ttu-id="07263-103">DirectShow 中的 MPEG 2 支援</span><span class="sxs-lookup"><span data-stu-id="07263-103">MPEG-2 Support in DirectShow</span></span>

<span data-ttu-id="07263-104">本節說明您可以用來在 DirectShow 中播放 MPEG 2 內容的元件。</span><span class="sxs-lookup"><span data-stu-id="07263-104">This section describes the components that you can use to play MPEG-2 content in DirectShow.</span></span>

> [!Note]  
> <span data-ttu-id="07263-105">雖然 DVD 影片是以 MPEG-2 為基礎，但本節並不說明 DVD 播放或導覽。</span><span class="sxs-lookup"><span data-stu-id="07263-105">Although DVD video is based on MPEG-2, this section does not describe DVD playback or navigation.</span></span> <span data-ttu-id="07263-106">如需有關 DirectShow 中 DVD 的詳細資訊，請參閱 [Dvd 應用程式](dvd-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="07263-106">For information about DVD in DirectShow, see [DVD Applications](dvd-applications.md).</span></span>

 

<span data-ttu-id="07263-107">MPEG-2 資料可以來自本機檔案，或來自即時來源（例如網路廣播或 D VHS 裝置）。</span><span class="sxs-lookup"><span data-stu-id="07263-107">MPEG-2 data can come from a local file, or from a live source, such as a network broadcast or D-VHS device.</span></span> <span data-ttu-id="07263-108">檔案播放稱為「 *提取模式* 」，因為剖析器篩選器會將檔案中的資料提取至篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="07263-108">File playback is called *pull mode* because the parser filter pulls data from the file into the filter graph.</span></span> <span data-ttu-id="07263-109">即時來源稱為 *推送模式* ，因為來源篩選會將資料推送至圖形。</span><span class="sxs-lookup"><span data-stu-id="07263-109">Live sources are called *push mode* because the source filter pushes data into the graph.</span></span>

<span data-ttu-id="07263-110">DirectShow 提供可剖析 MPEG-2 系統資料流程的兩個篩選器：</span><span class="sxs-lookup"><span data-stu-id="07263-110">DirectShow provides two filters that can parse MPEG-2 system streams:</span></span>

-   <span data-ttu-id="07263-111">[Mpeg-2 信號](mpeg-2-demultiplexer.md) ( "demux" ) ：此篩選器支援程式資料流程和傳輸資料流程的推送模式。</span><span class="sxs-lookup"><span data-stu-id="07263-111">[MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) ("demux"): This filter supports push mode for program streams and transport streams.</span></span> <span data-ttu-id="07263-112">在 Windows XP 和更新版本中，它也支援程式資料流程的提取模式。</span><span class="sxs-lookup"><span data-stu-id="07263-112">In Windows XP and later, it also supports pull mode for program streams.</span></span>
-   <span data-ttu-id="07263-113">[Mpeg-2 分隔](mpeg-2-splitter.md)器：此篩選器支援舊版平臺上的程式資料流程提取模式。</span><span class="sxs-lookup"><span data-stu-id="07263-113">[MPEG-2 Splitter](mpeg-2-splitter.md): This filter supports pull mode for program streams on downlevel platforms.</span></span> <span data-ttu-id="07263-114">此篩選器在 Windows XP 及更新版本中已被取代。</span><span class="sxs-lookup"><span data-stu-id="07263-114">This filter is deprecated in Windows XP and later.</span></span>

<span data-ttu-id="07263-115">若要使用 MPEG-2 demux 或 MPEG-2 分隔器，您必須具有可接受 packetized 基礎串流 (PE) 的 DirectShow 相容 MPEG 2 音訊和影片解碼器。</span><span class="sxs-lookup"><span data-stu-id="07263-115">To use the MPEG-2 demux or MPEG-2 splitter, you must have DirectShow-compatible MPEG-2 audio and video decoders that accept packetized elementary streams (PES).</span></span>

<span data-ttu-id="07263-116">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="07263-116">This section contains the following topics:</span></span>

-   [<span data-ttu-id="07263-117">MPEG 2 系統總覽</span><span class="sxs-lookup"><span data-stu-id="07263-117">Overview of MPEG-2 Systems</span></span>](overview-of-mpeg-2-systems.md)
-   [<span data-ttu-id="07263-118">使用 MPEG-2 信號信號</span><span class="sxs-lookup"><span data-stu-id="07263-118">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
-   [<span data-ttu-id="07263-119">使用 MPEG-2 分隔器</span><span class="sxs-lookup"><span data-stu-id="07263-119">Using the MPEG-2 Splitter</span></span>](using-the-mpeg-2-splitter.md)
-   [<span data-ttu-id="07263-120">MPEG 範例屬性</span><span class="sxs-lookup"><span data-stu-id="07263-120">MPEG Sample Properties</span></span>](mpeg-sample-properties.md)

## <a name="related-topics"></a><span data-ttu-id="07263-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="07263-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07263-122">PSI 剖析器篩選範例</span><span class="sxs-lookup"><span data-stu-id="07263-122">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 



