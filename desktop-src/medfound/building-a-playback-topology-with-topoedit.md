---
description: 使用 TopoEdit 建立播放拓撲
ms.assetid: 4d4c4ff9-dad1-4c79-a44a-2ad20f1bbca0
title: 使用 TopoEdit 建立播放拓撲
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f942984b3ba56ef1288566cee80e7d30026de155
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "106981719"
---
# <a name="building-a-playback-topology-with-topoedit"></a><span data-ttu-id="8a59d-103">使用 TopoEdit 建立播放拓撲</span><span class="sxs-lookup"><span data-stu-id="8a59d-103">Building a Playback Topology with TopoEdit</span></span>

<span data-ttu-id="8a59d-104">TopoEdit 可以自動新增並連接來源、轉換和輸出節點，以建立本機媒體檔案的播放拓撲。</span><span class="sxs-lookup"><span data-stu-id="8a59d-104">TopoEdit can build a playback topology for a local media file by automatically adding and connecting the source, transform, and output nodes.</span></span> <span data-ttu-id="8a59d-105">TopoEdit 不會自動解析拓撲。</span><span class="sxs-lookup"><span data-stu-id="8a59d-105">TopoEdit does not automatically resolve the topology.</span></span> <span data-ttu-id="8a59d-106">若要播放拓撲，請加以解決，然後使用傳輸控制項。</span><span class="sxs-lookup"><span data-stu-id="8a59d-106">To play the topology, resolve it and then use the transport controls.</span></span>

## <a name="to-build-and-play-a-topology-for-a-media-file"></a><span data-ttu-id="8a59d-107">若要建立並播放媒體檔案的拓撲</span><span class="sxs-lookup"><span data-stu-id="8a59d-107">To build and play a topology for a media file</span></span>

1.  <span data-ttu-id="8a59d-108">**在 [檔案**] 功能表上 **，按一下 [** 轉譯檔案]。</span><span class="sxs-lookup"><span data-stu-id="8a59d-108">On the **File** menu, click **Render File**.</span></span>

    <span data-ttu-id="8a59d-109">這會開啟 [ **選取媒體來源** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="8a59d-109">This opens the **Select Media Source** dialog box.</span></span>

2.  <span data-ttu-id="8a59d-110">流覽至媒體檔案所在的資料夾。</span><span class="sxs-lookup"><span data-stu-id="8a59d-110">Navigate to the folder where the media file is located.</span></span>
3.  <span data-ttu-id="8a59d-111">在 [ **檔案名：** ] 欄位中，輸入檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a59d-111">In the **File name:** field, enter the name of the file.</span></span>
4.  <span data-ttu-id="8a59d-112">按一下 [開啟]。</span><span class="sxs-lookup"><span data-stu-id="8a59d-112">Click **Open**.</span></span>

    <span data-ttu-id="8a59d-113">[ **拓撲] 窗格** 會顯示已連線的拓撲。</span><span class="sxs-lookup"><span data-stu-id="8a59d-113">The **Topology Pane** shows the connected topology.</span></span> <span data-ttu-id="8a59d-114">就內部而言，TopoEdit 會執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="8a59d-114">Internally, TopoEdit performs the following tasks:</span></span>

    -   <span data-ttu-id="8a59d-115">列舉媒體檔案中的資料流程，並建立來源節點。</span><span class="sxs-lookup"><span data-stu-id="8a59d-115">Enumerates the streams in the media file and creates the source nodes.</span></span>
    -   <span data-ttu-id="8a59d-116">視來源節點的媒體類型而定，會加入轉換節點，例如「解碼器」。</span><span class="sxs-lookup"><span data-stu-id="8a59d-116">Depending on the media type of the source nodes, adds transform nodes, such as decoders.</span></span>
    -   <span data-ttu-id="8a59d-117">將音訊串流的串流音訊轉譯器 (特別行政區) 接收，以及增強的影片轉譯器 (EVR 影片串流的) 接收器。</span><span class="sxs-lookup"><span data-stu-id="8a59d-117">Adds the Streaming Audio Renderer (SAR) sink for audio stream and the enhanced video renderer (EVR) sink for the video stream.</span></span>
    -   <span data-ttu-id="8a59d-118">連接節點輸入和節點輸出。</span><span class="sxs-lookup"><span data-stu-id="8a59d-118">Connects the node inputs and the node outputs.</span></span>

5.  <span data-ttu-id="8a59d-119">在 [ **拓撲** ] 功能表上，按一下 [ **解析拓撲**]。</span><span class="sxs-lookup"><span data-stu-id="8a59d-119">On the **Topology** menu, click **Resolve Topology**.</span></span>
6.  <span data-ttu-id="8a59d-120">按一下工具列上的 [ **播放** ] 按鈕來播放拓撲。</span><span class="sxs-lookup"><span data-stu-id="8a59d-120">Click the **Play** button on the toolbar to play the topology.</span></span> 下圖顯示 [ **播放** ] 按鈕 :::image type="icon" source="images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg"::: 。

## <a name="related-topics"></a><span data-ttu-id="8a59d-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="8a59d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a59d-123">TopoEdit 中的播放控制項</span><span class="sxs-lookup"><span data-stu-id="8a59d-123">Playback Controls in TopoEdit</span></span>](playback-controls-in-topoedit.md)
</dt> <dt>

[<span data-ttu-id="8a59d-124">使用 TopoEdit 解析拓撲</span><span class="sxs-lookup"><span data-stu-id="8a59d-124">Resolving a Topology with TopoEdit</span></span>](resolving-a-topology-with-topoedit.md)
</dt> <dt>

[<span data-ttu-id="8a59d-125">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="8a59d-125">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



