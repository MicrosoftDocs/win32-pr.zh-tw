---
description: 查看拓撲資訊
ms.assetid: d687ecd3-9ad6-46d5-b927-d9b99af2002f
title: 查看拓撲資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c4e6808fb2414de14817c63f9f4736acc9223f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988731"
---
# <a name="viewing-topology-information"></a><span data-ttu-id="3275b-103">查看拓撲資訊</span><span class="sxs-lookup"><span data-stu-id="3275b-103">Viewing Topology Information</span></span>

<span data-ttu-id="3275b-104">在 TopoEdit 中，每個拓撲專案（例如節點、節點輸入和節點輸出）都有一個相關聯的屬性存放區，可管理節點的行為。</span><span class="sxs-lookup"><span data-stu-id="3275b-104">In TopoEdit, each topology item, such as nodes, node inputs, and node outputs, has an associated attribute store that manages the behavior of the node.</span></span> <span data-ttu-id="3275b-105">若要查看屬性，請選取專案，[ **屬性] 窗格** 會顯示資訊。</span><span class="sxs-lookup"><span data-stu-id="3275b-105">To see the attributes, select the item, and the **Attributes Pane** displays the information.</span></span> <span data-ttu-id="3275b-106">針對從 XML 檔案載入的拓撲，某些節點可能不會顯示整個屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="3275b-106">For topologies that are loaded from an XML file, some of the nodes may not display the entire attribute store.</span></span> <span data-ttu-id="3275b-107">若要查看整個屬性存放區，請解決拓撲。</span><span class="sxs-lookup"><span data-stu-id="3275b-107">To see the entire attribute store, resolve the topology.</span></span> <span data-ttu-id="3275b-108">如需詳細資訊，請參閱 [使用 TopoEdit 解析拓撲](resolving-a-topology-with-topoedit.md)。</span><span class="sxs-lookup"><span data-stu-id="3275b-108">For more information, see [Resolving a Topology with TopoEdit](resolving-a-topology-with-topoedit.md).</span></span>

<span data-ttu-id="3275b-109">下表顯示拓撲專案和窗格所顯示的屬性。</span><span class="sxs-lookup"><span data-stu-id="3275b-109">The following table shows the topology item and the attributes that the pane displays.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3275b-110">拓撲專案</span><span class="sxs-lookup"><span data-stu-id="3275b-110">Topology item</span></span></th>
<th><span data-ttu-id="3275b-111">屬性</span><span class="sxs-lookup"><span data-stu-id="3275b-111">Attributes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3275b-112">拓撲節點</span><span class="sxs-lookup"><span data-stu-id="3275b-112">Topology nodes</span></span></td>
<td><ul>
<li><span data-ttu-id="3275b-113">所有節點的<a href="topology-node-attributes.md">拓撲節點屬性</a>。</span><span class="sxs-lookup"><span data-stu-id="3275b-113"><a href="topology-node-attributes.md">Topology Node Attributes</a> for all nodes.</span></span><br/></li>
<li><span data-ttu-id="3275b-114">僅適用于來源節點的<a href="presentation-descriptor-attributes.md">呈現描述項屬性</a>。</span><span class="sxs-lookup"><span data-stu-id="3275b-114"><a href="presentation-descriptor-attributes.md">Presentation Descriptor Attributes</a> for source nodes only.</span></span><br/></li>
<li><span data-ttu-id="3275b-115">轉換和輸出節點的輸入和輸出信任授權單位資訊。</span><span class="sxs-lookup"><span data-stu-id="3275b-115">Input and output trust authority information for transform and output nodes.</span></span><br/></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3275b-116">節點輸入</span><span class="sxs-lookup"><span data-stu-id="3275b-116">Node input</span></span></td>
<td><ul>
<li><span data-ttu-id="3275b-117">所有節點的<a href="media-type-attributes.md">媒體類型屬性</a>。</span><span class="sxs-lookup"><span data-stu-id="3275b-117"><a href="media-type-attributes.md">Media Type Attributes</a> for all nodes.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3275b-118">節點輸出</span><span class="sxs-lookup"><span data-stu-id="3275b-118">Node output</span></span></td>
<td><ul>
<li><span data-ttu-id="3275b-119">僅適用于來源節點的<a href="stream-descriptor-attributes.md">串流描述項屬性</a>。</span><span class="sxs-lookup"><span data-stu-id="3275b-119"><a href="stream-descriptor-attributes.md">Stream Descriptor Attributes</a> for source nodes only.</span></span><br/></li>
<li><span data-ttu-id="3275b-120">所有節點的<a href="media-type-attributes.md">媒體類型屬性</a>。</span><span class="sxs-lookup"><span data-stu-id="3275b-120"><a href="media-type-attributes.md">Media Type Attributes</a> for all nodes.</span></span><br/></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3275b-121">除了指標參考和陣列值以外，屬性值可以變更。</span><span class="sxs-lookup"><span data-stu-id="3275b-121">The attribute values, except for pointer references and array values, can be changed.</span></span> <span data-ttu-id="3275b-122">若要變更屬性值，請輸入屬性旁的新值，然後按一下 [**屬性] 窗格** 上的 [**儲存**]。</span><span class="sxs-lookup"><span data-stu-id="3275b-122">To change an attribute value, type in the new value next to the attribute and click **Save** on the **Attributes Pane**.</span></span> <span data-ttu-id="3275b-123">新的值會在屬性存放區中更新，並只在解析之後套用至拓撲。</span><span class="sxs-lookup"><span data-stu-id="3275b-123">The new value is updated in the attribute store and applied to the topology only after it is resolved.</span></span>

## <a name="to-add-a-new-attribute-for-a-node"></a><span data-ttu-id="3275b-124">加入節點的新屬性</span><span class="sxs-lookup"><span data-stu-id="3275b-124">To add a new attribute for a node</span></span>

1.  <span data-ttu-id="3275b-125">按一下 [ **拓撲] 窗格** 上的節點，以選取該節點。</span><span class="sxs-lookup"><span data-stu-id="3275b-125">Select the node by clicking it on the **Topology Pane**.</span></span>

    <span data-ttu-id="3275b-126">節點上設定的屬性會顯示在 [ **屬性] 窗格** 中。</span><span class="sxs-lookup"><span data-stu-id="3275b-126">The attributes that are set on the node are shown on the **Attributes Pane**.</span></span>

2.  <span data-ttu-id="3275b-127">在 [ **屬性] 窗格** 中，按一下 [ **新增**]。</span><span class="sxs-lookup"><span data-stu-id="3275b-127">On the **Attributes Pane**, click **Add**.</span></span>

    <span data-ttu-id="3275b-128">這會開啟 [ **加入屬性** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="3275b-128">This opens the **Add Attribute** dialog box.</span></span>

3.  <span data-ttu-id="3275b-129">從第一個下拉式清單中，選擇 [屬性] 類別。</span><span class="sxs-lookup"><span data-stu-id="3275b-129">From the first drop-down list, choose the Attribute category.</span></span>

    <span data-ttu-id="3275b-130">這些分類相依于拓撲節點。</span><span class="sxs-lookup"><span data-stu-id="3275b-130">The categories depend on the topology node.</span></span> <span data-ttu-id="3275b-131">例如，針對來源節點，下拉式清單會顯示 **展示描述項屬性** 和 **節點屬性** 做為可用的類別。</span><span class="sxs-lookup"><span data-stu-id="3275b-131">For example, for the source node, the drop-down list shows **Presentation Descriptor Attributes** and **Node Attributes** as the available categories.</span></span>

4.  <span data-ttu-id="3275b-132">從第二個下拉式清單中，選擇您想要在節點上設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="3275b-132">From the second drop-down list, choose the attribute that you want to set on the node.</span></span>

5.  <span data-ttu-id="3275b-133">在編輯方塊中，加入屬性的值。</span><span class="sxs-lookup"><span data-stu-id="3275b-133">In the edit box, add the value for the attribute.</span></span>

6.  <span data-ttu-id="3275b-134">按一下 [ **新增** ] 以加入屬性並返回主視窗，或按一下 [ **取消** ] 取消作業。</span><span class="sxs-lookup"><span data-stu-id="3275b-134">Click **Add** to add the attribute and return to the main window, or click **Cancel** to cancel the operation.</span></span>

7.  <span data-ttu-id="3275b-135">在 [ **拓撲** ] 功能表中，按一下 [ **解析拓撲** ]，將新屬性設定為拓撲。</span><span class="sxs-lookup"><span data-stu-id="3275b-135">From the **Topology** menu, click **Resolve Topology** to set the new attribute to the topology.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3275b-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="3275b-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3275b-137">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="3275b-137">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 




