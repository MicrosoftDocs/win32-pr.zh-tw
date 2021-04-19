---
description: 使用 TopoEdit 新增輸出節點
ms.assetid: 23d60fc7-547b-4ef5-b334-5f1b38e58e92
title: 使用 TopoEdit 新增輸出節點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84dc30631332e8138b35e4bbc0ccde75ec9b0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970411"
---
# <a name="adding-output-nodes-with-topoedit"></a><span data-ttu-id="1ccf5-103">使用 TopoEdit 新增輸出節點</span><span class="sxs-lookup"><span data-stu-id="1ccf5-103">Adding Output Nodes with TopoEdit</span></span>

<span data-ttu-id="1ccf5-104">在拓撲中，輸出節點代表從轉換節點接收媒體資料並呈現播放的媒體接收。</span><span class="sxs-lookup"><span data-stu-id="1ccf5-104">In a topology, an output node represents a media sink that receives media data from a transform node and presents it for playback.</span></span> <span data-ttu-id="1ccf5-105">輸出節點的類型取決於來源節點的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="1ccf5-105">The type of output node depends on the media type of the source node.</span></span>

<span data-ttu-id="1ccf5-106">下表顯示將輸出節點加入拓撲的功能表/工具列命令。</span><span class="sxs-lookup"><span data-stu-id="1ccf5-106">The following table shows the menu/toolbar command for adding an output node to the topology.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1ccf5-107">來源媒體類型</span><span class="sxs-lookup"><span data-stu-id="1ccf5-107">Source media type</span></span></th>
<th><span data-ttu-id="1ccf5-108">功能表/工具列命令</span><span class="sxs-lookup"><span data-stu-id="1ccf5-108">Menu/Toolbar Command</span></span></th>
<th><span data-ttu-id="1ccf5-109">Description</span><span class="sxs-lookup"><span data-stu-id="1ccf5-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1ccf5-110">音訊資料流</span><span class="sxs-lookup"><span data-stu-id="1ccf5-110">Audio stream</span></span></td>
<td><span data-ttu-id="1ccf5-111">在 [ <strong>拓撲</strong> ] 功能表上，按一下 [ <strong>新增 SAR</strong>]。</span><span class="sxs-lookup"><span data-stu-id="1ccf5-111">On the <strong>Topology</strong> menu, click <strong>Add SAR</strong>.</span></span></td>
<td><span data-ttu-id="1ccf5-112">建立串流音訊轉譯器的輸出節點， (SAR) 透過音訊裝置（例如音效卡）播放音訊串流。</span><span class="sxs-lookup"><span data-stu-id="1ccf5-112">Creates an output node for the Streaming Audio Renderer (SAR) that plays an audio stream through an audio device such as a sound card.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1ccf5-113">影片串流</span><span class="sxs-lookup"><span data-stu-id="1ccf5-113">Video stream</span></span></td>
<td><span data-ttu-id="1ccf5-114">在 [ <strong>拓撲</strong> ] 功能表上，按一下 [ <strong>新增 EVR</strong>]。</span><span class="sxs-lookup"><span data-stu-id="1ccf5-114">On the <strong>Topology</strong> menu, click <strong>Add EVR</strong>.</span></span></td>
<td><span data-ttu-id="1ccf5-115">建立增強型影片轉譯器的輸出節點 (EVR) ，以顯示影片串流的畫面格。</span><span class="sxs-lookup"><span data-stu-id="1ccf5-115">Creates an output node for the enhanced video renderer (EVR) that displays frames for a video stream.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1ccf5-116">自訂媒體接收</span><span class="sxs-lookup"><span data-stu-id="1ccf5-116">Custom media sink</span></span></td>
<td><ol>
<li><span data-ttu-id="1ccf5-117">在 [ <strong>拓撲</strong> ] 功能表上，按一下 [ <strong>新增自訂接收</strong>]。</span><span class="sxs-lookup"><span data-stu-id="1ccf5-117">On the <strong>Topology</strong> menu, click <strong>Add Custom Sink</strong>.</span></span><br/> <span data-ttu-id="1ccf5-118">[ <strong>輸入自訂 GUID</strong> ] 對話方塊隨即開啟。</span><span class="sxs-lookup"><span data-stu-id="1ccf5-118">The <strong>Input Custom GUID</strong> dialog box opens.</span></span><br/></li>
<li><p><span data-ttu-id="1ccf5-119">在 [ <strong>GUID：</strong> ] 欄位中，輸入您要新增至拓撲的自訂接收的 GUID。</span><span class="sxs-lookup"><span data-stu-id="1ccf5-119">In the <strong>GUID:</strong> field, enter the GUID of your custom sink that you want to add to the topology.</span></span><br/></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="1ccf5-120">TopoEdit 預期格式應為 &quot; {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} 的 GUID &quot; 。</span><span class="sxs-lookup"><span data-stu-id="1ccf5-120">TopoEdit expects the GUID in the format &quot;{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}&quot;.</span></span> <span data-ttu-id="1ccf5-121">否則，它無法新增節點，並顯示不正確 &quot; GUID &quot; 錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="1ccf5-121">Otherwise, it fails to add the node and displays an &quot;Invalid GUID&quot; error message.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="1ccf5-122">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="1ccf5-122">Click <strong>OK</strong>.</span></span><br/></li>
</ol></td>
<td><span data-ttu-id="1ccf5-123">為自訂媒體來源的資料流程接收建立輸出節點。</span><span class="sxs-lookup"><span data-stu-id="1ccf5-123">Creates an output node for the stream sink for a custom media source.</span></span><br/> <span data-ttu-id="1ccf5-124">自訂接收必須支援 <strong>CoCreateInstance</strong> ，才能以 CLSID 指定接收。</span><span class="sxs-lookup"><span data-stu-id="1ccf5-124">The custom sink must support <strong>CoCreateInstance</strong> so that the sink can be specified with a CLSID.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1ccf5-125">TopoEdit 會建立指定的輸出節點。</span><span class="sxs-lookup"><span data-stu-id="1ccf5-125">TopoEdit creates the specified output node.</span></span> <span data-ttu-id="1ccf5-126">[ **拓撲] 窗格** 會將輸出節點顯示為顯示資料流程接收名稱的綠色方塊。</span><span class="sxs-lookup"><span data-stu-id="1ccf5-126">The **Topology Pane** shows the output node as a green box that shows the name of the stream sink.</span></span>

<span data-ttu-id="1ccf5-127">如需使用媒體基礎 Api 以程式設計方式加入輸出節點的詳細資訊，請參閱 [建立輸出節點](creating-output-nodes.md)。</span><span class="sxs-lookup"><span data-stu-id="1ccf5-127">For information about adding output nodes programmatically by using Media Foundation APIs, see [Creating Output Nodes](creating-output-nodes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ccf5-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="1ccf5-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ccf5-129">使用 TopoEdit 建立拓撲</span><span class="sxs-lookup"><span data-stu-id="1ccf5-129">Building Topologies by Using TopoEdit</span></span>](building-topologies-by-using-topoedit.md)
</dt> <dt>

[<span data-ttu-id="1ccf5-130">串流音訊轉譯器</span><span class="sxs-lookup"><span data-stu-id="1ccf5-130">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> <dt>

[<span data-ttu-id="1ccf5-131">增強的影片轉譯器</span><span class="sxs-lookup"><span data-stu-id="1ccf5-131">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> <dt>

[<span data-ttu-id="1ccf5-132">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="1ccf5-132">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 




