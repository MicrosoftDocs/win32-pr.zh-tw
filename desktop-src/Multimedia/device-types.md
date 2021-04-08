---
title: 裝置類型
description: 裝置類型
ms.assetid: 6556fa6a-5906-4afb-ab7d-ef41a0e22d13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27ed77debb663a1d90e03512832ca83e6e276d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674844"
---
# <a name="device-types"></a><span data-ttu-id="5d01f-103">裝置類型</span><span class="sxs-lookup"><span data-stu-id="5d01f-103">Device Types</span></span>

<span data-ttu-id="5d01f-104">MCI 會辨識出一組基本的 *裝置類型*。</span><span class="sxs-lookup"><span data-stu-id="5d01f-104">MCI recognizes a basic set of *device types*.</span></span> <span data-ttu-id="5d01f-105">裝置類型是共用通用命令集的一組 MCI 驅動程式，可用來控制類似的多媒體裝置或資料檔案。</span><span class="sxs-lookup"><span data-stu-id="5d01f-105">A device type is a set of MCI drivers that share a common command set and are used to control similar multimedia devices or data files.</span></span> <span data-ttu-id="5d01f-106">許多 MCI 命令（例如 [**open**](open.md) ([**MCI \_ 開啟**](mci-open.md)) ）都會要求您指定裝置類型。</span><span class="sxs-lookup"><span data-stu-id="5d01f-106">Many MCI commands, such as [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)), require you to specify a device type.</span></span>

<span data-ttu-id="5d01f-107">下表列出已定義的裝置類型。</span><span class="sxs-lookup"><span data-stu-id="5d01f-107">The following table lists the defined device types.</span></span> <span data-ttu-id="5d01f-108">目前的 MCI 執行包含這些裝置子集的命令集。</span><span class="sxs-lookup"><span data-stu-id="5d01f-108">The current implementation of MCI includes command sets for a subset of these devices.</span></span>



| <span data-ttu-id="5d01f-109">裝置類型</span><span class="sxs-lookup"><span data-stu-id="5d01f-109">Device type</span></span>      | <span data-ttu-id="5d01f-110">常數</span><span class="sxs-lookup"><span data-stu-id="5d01f-110">Constant</span></span>                      | <span data-ttu-id="5d01f-111">描述</span><span class="sxs-lookup"><span data-stu-id="5d01f-111">Description</span></span>                                      |
|------------------|-------------------------------|--------------------------------------------------|
| <span data-ttu-id="5d01f-112">**cdaudio**</span><span class="sxs-lookup"><span data-stu-id="5d01f-112">**cdaudio**</span></span>      | <span data-ttu-id="5d01f-113">MCI \_ DEVTYPE \_ CD \_ 音訊</span><span class="sxs-lookup"><span data-stu-id="5d01f-113">MCI\_DEVTYPE\_CD\_AUDIO</span></span>       | <span data-ttu-id="5d01f-114">CD 音訊播放機</span><span class="sxs-lookup"><span data-stu-id="5d01f-114">CD audio player</span></span>                                  |
| <span data-ttu-id="5d01f-115">**Dat**</span><span class="sxs-lookup"><span data-stu-id="5d01f-115">**dat**</span></span>          | <span data-ttu-id="5d01f-116">MCI \_ DEVTYPE \_ DAT</span><span class="sxs-lookup"><span data-stu-id="5d01f-116">MCI\_DEVTYPE\_DAT</span></span>             | <span data-ttu-id="5d01f-117">數位音訊磁帶播放機</span><span class="sxs-lookup"><span data-stu-id="5d01f-117">Digital-audio tape player</span></span>                        |
| <span data-ttu-id="5d01f-118">**digitalvideo**</span><span class="sxs-lookup"><span data-stu-id="5d01f-118">**digitalvideo**</span></span> | <span data-ttu-id="5d01f-119">MCI \_ DEVTYPE \_ 數位 \_ 影片</span><span class="sxs-lookup"><span data-stu-id="5d01f-119">MCI\_DEVTYPE\_DIGITAL\_VIDEO</span></span>  | <span data-ttu-id="5d01f-120">視窗中的數位影片 (非 GDI 型) </span><span class="sxs-lookup"><span data-stu-id="5d01f-120">Digital video in a window (not GDI-based)</span></span>        |
| <span data-ttu-id="5d01f-121">**其他**</span><span class="sxs-lookup"><span data-stu-id="5d01f-121">**other**</span></span>        | <span data-ttu-id="5d01f-122">MCI \_ DEVTYPE \_ 其他</span><span class="sxs-lookup"><span data-stu-id="5d01f-122">MCI\_DEVTYPE\_OTHER</span></span>           | <span data-ttu-id="5d01f-123">未定義的 MCI 裝置</span><span class="sxs-lookup"><span data-stu-id="5d01f-123">Undefined MCI device</span></span>                             |
| <span data-ttu-id="5d01f-124">**覆蓋**</span><span class="sxs-lookup"><span data-stu-id="5d01f-124">**overlay**</span></span>      | <span data-ttu-id="5d01f-125">MCI \_ DEVTYPE 重迭 \_</span><span class="sxs-lookup"><span data-stu-id="5d01f-125">MCI\_DEVTYPE\_OVERLAY</span></span>         | <span data-ttu-id="5d01f-126">在視窗中將裝置 (類比影片重迭) </span><span class="sxs-lookup"><span data-stu-id="5d01f-126">Overlay device (analog video in a window)</span></span>        |
| <span data-ttu-id="5d01f-127">**掃描器**</span><span class="sxs-lookup"><span data-stu-id="5d01f-127">**scanner**</span></span>      | <span data-ttu-id="5d01f-128">MCI \_ DEVTYPE \_ 掃描器</span><span class="sxs-lookup"><span data-stu-id="5d01f-128">MCI\_DEVTYPE\_SCANNER</span></span>         | <span data-ttu-id="5d01f-129">影像掃描器</span><span class="sxs-lookup"><span data-stu-id="5d01f-129">Image scanner</span></span>                                    |
| <span data-ttu-id="5d01f-130">**排序器**</span><span class="sxs-lookup"><span data-stu-id="5d01f-130">**sequencer**</span></span>    | <span data-ttu-id="5d01f-131">MCI \_ DEVTYPE \_ SEQUENCER</span><span class="sxs-lookup"><span data-stu-id="5d01f-131">MCI\_DEVTYPE\_SEQUENCER</span></span>       | <span data-ttu-id="5d01f-132">MIDI sequencer</span><span class="sxs-lookup"><span data-stu-id="5d01f-132">MIDI sequencer</span></span>                                   |
| <span data-ttu-id="5d01f-133">**錄影機**</span><span class="sxs-lookup"><span data-stu-id="5d01f-133">**vcr**</span></span>          | <span data-ttu-id="5d01f-134">MCI \_ DEVTYPE \_ VCR</span><span class="sxs-lookup"><span data-stu-id="5d01f-134">MCI\_DEVTYPE\_VCR</span></span>             | <span data-ttu-id="5d01f-135">影片-卡帶錄製器或播放機</span><span class="sxs-lookup"><span data-stu-id="5d01f-135">Video-cassette recorder or player</span></span>                |
| <span data-ttu-id="5d01f-136">**videodisc**</span><span class="sxs-lookup"><span data-stu-id="5d01f-136">**videodisc**</span></span>    | <span data-ttu-id="5d01f-137">MCI \_ DEVTYPE \_ VIDEODISC</span><span class="sxs-lookup"><span data-stu-id="5d01f-137">MCI\_DEVTYPE\_VIDEODISC</span></span>       | <span data-ttu-id="5d01f-138">Videodisc player</span><span class="sxs-lookup"><span data-stu-id="5d01f-138">Videodisc player</span></span>                                 |
| <span data-ttu-id="5d01f-139">**waveaudio**</span><span class="sxs-lookup"><span data-stu-id="5d01f-139">**waveaudio**</span></span>    | <span data-ttu-id="5d01f-140">MCI \_ DEVTYPE \_ 波形 \_ 音訊</span><span class="sxs-lookup"><span data-stu-id="5d01f-140">MCI\_DEVTYPE\_WAVEFORM\_AUDIO</span></span> | <span data-ttu-id="5d01f-141">播放數位化波形檔案的音訊裝置</span><span class="sxs-lookup"><span data-stu-id="5d01f-141">Audio device that plays digitized waveform files</span></span> |



 

<span data-ttu-id="5d01f-142">在本檔中，裝置類型的名稱為粗體。</span><span class="sxs-lookup"><span data-stu-id="5d01f-142">In this document, the names of device types are bold.</span></span> <span data-ttu-id="5d01f-143">裝置類型名稱會與命令字串介面一起使用。</span><span class="sxs-lookup"><span data-stu-id="5d01f-143">Device-type names are used with the command-string interface.</span></span> <span data-ttu-id="5d01f-144">裝置類型常數可搭配命令訊息介面使用。</span><span class="sxs-lookup"><span data-stu-id="5d01f-144">Device-type constants are used with the command-message interface.</span></span>

 

 




