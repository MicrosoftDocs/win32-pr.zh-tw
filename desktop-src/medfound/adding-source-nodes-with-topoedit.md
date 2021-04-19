---
description: 使用 TopoEdit 新增來源節點
ms.assetid: f42227eb-a988-4eaa-9c18-b3ac270cd7a2
title: 使用 TopoEdit 新增來源節點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12456e76f64d44d9c335dec1ea171c732e4040c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970193"
---
# <a name="adding-source-nodes-with-topoedit"></a><span data-ttu-id="47e87-103">使用 TopoEdit 新增來源節點</span><span class="sxs-lookup"><span data-stu-id="47e87-103">Adding Source Nodes with TopoEdit</span></span>

<span data-ttu-id="47e87-104">來源節點代表媒體檔案中的資料流程。</span><span class="sxs-lookup"><span data-stu-id="47e87-104">A source node represents a stream in a media file.</span></span> <span data-ttu-id="47e87-105">若要在 TopoEdit 中建立來源節點，請指定媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="47e87-105">To create a source node in TopoEdit, you specify a media file.</span></span> <span data-ttu-id="47e87-106">TopoEdit 會列舉檔案中的資料流程，並建立適當的來源節點。</span><span class="sxs-lookup"><span data-stu-id="47e87-106">TopoEdit enumerates the streams in the file and creates the appropriate source nodes.</span></span>

<span data-ttu-id="47e87-107">如需使用媒體基礎 Api 以程式設計方式新增來源節點的相關資訊，請參閱 [建立來源節點](creating-source-nodes.md)。</span><span class="sxs-lookup"><span data-stu-id="47e87-107">For information about adding source nodes programmatically by using Media Foundation APIs, see [Creating Source Nodes](creating-source-nodes.md).</span></span>

## <a name="to-add-a-source-node-to-a-topology"></a><span data-ttu-id="47e87-108">將來源節點新增至拓撲</span><span class="sxs-lookup"><span data-stu-id="47e87-108">To add a source node to a topology</span></span>

1.  <span data-ttu-id="47e87-109">在 [ **拓撲** ] 功能表上，按一下 [ **新增來源**]。</span><span class="sxs-lookup"><span data-stu-id="47e87-109">On the **Topology** menu, click **Add Source**.</span></span>

    <span data-ttu-id="47e87-110">[ **選取媒體來源** ] 對話方塊隨即開啟。</span><span class="sxs-lookup"><span data-stu-id="47e87-110">The **Select Media Source** dialog box opens.</span></span>

2.  <span data-ttu-id="47e87-111">流覽至媒體檔案所在的資料夾。</span><span class="sxs-lookup"><span data-stu-id="47e87-111">Navigate to the folder where the media file is located.</span></span>

3.  <span data-ttu-id="47e87-112">在 [ **檔案名：** ] 欄位中，輸入檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="47e87-112">In the **File name:** field, enter the name of the file.</span></span>

4.  <span data-ttu-id="47e87-113">按一下 [開啟]。</span><span class="sxs-lookup"><span data-stu-id="47e87-113">Click **Open**.</span></span>

<span data-ttu-id="47e87-114">TopoEdit 會建立資料流程的來源節點。</span><span class="sxs-lookup"><span data-stu-id="47e87-114">TopoEdit creates source nodes for the streams.</span></span> <span data-ttu-id="47e87-115">[ **拓撲] 窗格** 會顯示灰色方塊中所含的來源節點，以顯示媒體檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="47e87-115">The **Topology Pane** shows the source node contained in a grey box that shows the name of the media file.</span></span> <span data-ttu-id="47e87-116">來源節點會顯示節點的資料流程類型。</span><span class="sxs-lookup"><span data-stu-id="47e87-116">The source node shows the stream type of the node.</span></span>

## <a name="related-topics"></a><span data-ttu-id="47e87-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="47e87-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47e87-118">使用 TopoEdit 建立拓撲</span><span class="sxs-lookup"><span data-stu-id="47e87-118">Building Topologies by Using TopoEdit</span></span>](building-topologies-by-using-topoedit.md)
</dt> <dt>

[<span data-ttu-id="47e87-119">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="47e87-119">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



