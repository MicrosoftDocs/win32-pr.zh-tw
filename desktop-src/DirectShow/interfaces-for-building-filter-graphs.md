---
description: 建立篩選圖形的介面
ms.assetid: 18d5217a-7f4e-49e9-ac14-2f4ba229e065
title: 建立篩選圖形的介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862d581f44a711cc6f2aa094210571995b15005b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687683"
---
# <a name="interfaces-for-building-filter-graphs"></a><span data-ttu-id="cc092-103">建立篩選圖形的介面</span><span class="sxs-lookup"><span data-stu-id="cc092-103">Interfaces for Building Filter Graphs</span></span>

<span data-ttu-id="cc092-104">應用程式會使用這些介面來建立各種類型的篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="cc092-104">Applications use these interfaces to build various types of filter graphs.</span></span>



| <span data-ttu-id="cc092-105">介面</span><span class="sxs-lookup"><span data-stu-id="cc092-105">Interface</span></span>                                                  | <span data-ttu-id="cc092-106">描述</span><span class="sxs-lookup"><span data-stu-id="cc092-106">Description</span></span>                                                 |
|------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="cc092-107">**IAMFilterGraphCallback**</span><span class="sxs-lookup"><span data-stu-id="cc092-107">**IAMFilterGraphCallback**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamfiltergraphcallback)   | <span data-ttu-id="cc092-108">如果無法轉譯 pin，則接收回呼通知。</span><span class="sxs-lookup"><span data-stu-id="cc092-108">Receive callback notifications if a pin cannot be rendered.</span></span> |
| [<span data-ttu-id="cc092-109">**IAMGraphBuilderCallback**</span><span class="sxs-lookup"><span data-stu-id="cc092-109">**IAMGraphBuilderCallback**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) | <span data-ttu-id="cc092-110">在圖形建立期間提供回呼機制。</span><span class="sxs-lookup"><span data-stu-id="cc092-110">Provides a callback mechanism during graph building.</span></span>        |
| [<span data-ttu-id="cc092-111">**ICaptureGraphBuilder2**</span><span class="sxs-lookup"><span data-stu-id="cc092-111">**ICaptureGraphBuilder2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)     | <span data-ttu-id="cc092-112">影片捕獲的組建篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="cc092-112">Build filter graphs for video capture.</span></span>                      |
| [<span data-ttu-id="cc092-113">**ICreateDevEnum**</span><span class="sxs-lookup"><span data-stu-id="cc092-113">**ICreateDevEnum**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum)                   | <span data-ttu-id="cc092-114">列舉系統裝置，例如「捕獲裝置」。</span><span class="sxs-lookup"><span data-stu-id="cc092-114">Enumerate system devices, such as capture devices.</span></span>          |
| [<span data-ttu-id="cc092-115">**IDvdGraphBuilder**</span><span class="sxs-lookup"><span data-stu-id="cc092-115">**IDvdGraphBuilder**</span></span>](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder)               | <span data-ttu-id="cc092-116">建立 DVD 流覽和播放的篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="cc092-116">Build filter graphs for DVD navigation and playback.</span></span>        |
| [<span data-ttu-id="cc092-117">**IEnumFilters**</span><span class="sxs-lookup"><span data-stu-id="cc092-117">**IEnumFilters**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ienumfilters)                       | <span data-ttu-id="cc092-118">列舉圖形中的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="cc092-118">Enumerate the filters in the graph.</span></span>                         |
| [<span data-ttu-id="cc092-119">**IFilterGraph2**</span><span class="sxs-lookup"><span data-stu-id="cc092-119">**IFilterGraph2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2)                     | <span data-ttu-id="cc092-120">加入、移除或連接篩選。</span><span class="sxs-lookup"><span data-stu-id="cc092-120">Add, remove, or connect filters.</span></span>                            |
| [<span data-ttu-id="cc092-121">**IFilterMapper2**</span><span class="sxs-lookup"><span data-stu-id="cc092-121">**IFilterMapper2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)                   | <span data-ttu-id="cc092-122">列舉在使用者的系統上註冊的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="cc092-122">Enumerate the filters registered on the user's system.</span></span>      |
| [<span data-ttu-id="cc092-123">**IGraphBuilder**</span><span class="sxs-lookup"><span data-stu-id="cc092-123">**IGraphBuilder**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)                     | <span data-ttu-id="cc092-124">建立檔案播放或自訂用途的篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="cc092-124">Build filter graphs for file playback or for custom uses.</span></span>   |
| [<span data-ttu-id="cc092-125">**IGraphConfig**</span><span class="sxs-lookup"><span data-stu-id="cc092-125">**IGraphConfig**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)                       | <span data-ttu-id="cc092-126">以動態方式重新設定篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="cc092-126">Dynamically reconfigure a filter graph.</span></span>                     |
| [<span data-ttu-id="cc092-127">**IGraphVersion**</span><span class="sxs-lookup"><span data-stu-id="cc092-127">**IGraphVersion**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphversion)                     | <span data-ttu-id="cc092-128">判斷圖形何時變更。</span><span class="sxs-lookup"><span data-stu-id="cc092-128">Determine when the graph changes.</span></span>                           |



 

 

 



