---
description: 記錄拓撲節點活動
ms.assetid: 853b3900-1214-43b9-bf0e-e45c1159c5f1
title: 記錄拓撲節點活動
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327ca83d0513b97d053e27388bd0f2a418dfb253
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026364"
---
# <a name="logging-topology-node-activities"></a><span data-ttu-id="05bf6-103">記錄拓撲節點活動</span><span class="sxs-lookup"><span data-stu-id="05bf6-103">Logging Topology Node Activities</span></span>

<span data-ttu-id="05bf6-104">TopoEdit 會提供選項，讓您收集轉換節點或拓撲輸出節點的記錄資訊。</span><span class="sxs-lookup"><span data-stu-id="05bf6-104">TopoEdit provides the option for collecting logging information for a transform node or an output node of a topology.</span></span>

## <a name="to-setup-logging"></a><span data-ttu-id="05bf6-105">設定記錄</span><span class="sxs-lookup"><span data-stu-id="05bf6-105">To setup logging</span></span>

1.  <span data-ttu-id="05bf6-106">在 [ **拓撲] 窗格** 上，按一下 [轉換] 節點或輸出節點來選取它。</span><span class="sxs-lookup"><span data-stu-id="05bf6-106">On the **Topology Pane**, select a transform node or an output node by clicking it.</span></span>

2.  <span data-ttu-id="05bf6-107">從 [ **工具** ] 功能表中，按一下 [ **Spy 選取的節點**]。</span><span class="sxs-lookup"><span data-stu-id="05bf6-107">From the **Tools** menu, click **Spy Selected Node**.</span></span>

<span data-ttu-id="05bf6-108">在拓撲建立期間，會將所選節點上的所有方法通話記錄至文字檔。</span><span class="sxs-lookup"><span data-stu-id="05bf6-108">During topology building, all method calls on the selected node are logged to a text file.</span></span> <span data-ttu-id="05bf6-109">這會儲存在媒體檔案所在的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="05bf6-109">This is saved in the folder where the media file is located.</span></span> <span data-ttu-id="05bf6-110">記錄檔會與節點名稱和唯一拓撲節點識別碼一併儲存。</span><span class="sxs-lookup"><span data-stu-id="05bf6-110">The log file is saved with the node name and the unique topology node identifier.</span></span> <span data-ttu-id="05bf6-111">這可確保不會有其他節點寫入記錄檔。</span><span class="sxs-lookup"><span data-stu-id="05bf6-111">This ensures that no other node writes to the log.</span></span> <span data-ttu-id="05bf6-112">若要以程式設計方式取得識別碼，請呼叫 [**IMFTopologyNode：： GetTopoNodeID**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid)。</span><span class="sxs-lookup"><span data-stu-id="05bf6-112">To get the identifier programmatically, call [**IMFTopologyNode::GetTopoNodeID**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid).</span></span>

<span data-ttu-id="05bf6-113">以下是記錄檔的摘錄。</span><span class="sxs-lookup"><span data-stu-id="05bf6-113">The following is an excerpt from a log file.</span></span>

`GetStreamCount(02C9F518 02C9F514) returns 0`

`GetStreamIDs(1 02729720 1 02729760) returns 80004001`

`GetInputCurrentType(0 02C9F4A4) returns c00d6d60`

`GetStreamCount(02C9F518 02C9F514) returns 0`

`GetStreamIDs(1 02729760 1 02729720) returns 80004001`

`SetInputType(0 0012F8D8 0) returns 0`

`--> Arg(2, in) Media type: Audio: MAJOR_TYPE=Audio, PREFER_WAVEFORMATEX=1, SUBTYPE=WMAudioV8, NUM_CHANNELS=2, SAMPLES_PER_SECOND=48000, BLOCK_ALIGNMENT=2048, AVG_BYTES_PER_SECOND=12000, BITS_PER_SAMPLE=16, USER_DATA=<BLOB>, {9D62927D-36BE-4CF2-B5C4-A3926E3E8711}=5760, {9D62927F-36BE-4CF2-B5C4-A3926E3E8711}=674,`

`GetStreamCount(02C9F560 02C9F55C) returns 0`

`GetStreamIDs(1 02729720 1 02729640) returns 80004001`

`GetOutputCurrentType(0 02C9F4B0) returns c00d6d60`

`GetStreamCount(02C9F560 02C9F55C) returns 0`

`GetStreamIDs(1 02729640 1 02729720) returns 80004001`

`GetOutputAvailableType(0 0 02C9F4B0) returns 0`

`--> Arg(3, out) Media type: Audio: MAJOR_TYPE=Audio, PREFER_WAVEFORMATEX=1, SUBTYPE=Float, NUM_CHANNELS=2, SAMPLES_PER_SECOND=48000, BLOCK_ALIGNMENT=8, AVG_BYTES_PER_SECOND=384000, BITS_PER_SAMPLE=32, ALL_SAMPLES_INDEPENDENT=1, FIXED_SIZE_SAMPLES=1,`

`GetStreamCount(02C9F560 02C9F55C) returns 0`

`GetStreamIDs(1 02729720 1 02729640) returns 80004001`

`GetOutputAvailableType(0 1 02C9F4B0) returns 0`

## <a name="related-topics"></a><span data-ttu-id="05bf6-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="05bf6-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05bf6-115">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="05bf6-115">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



