---
title: 物件模型
description: 下表列出可透過 Windows 篩選平台 (WFP) 所提供的各種 API 集合來操作的物件類型。
ms.assetid: 6931583f-785c-4e27-b5e4-d185d23a54ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa90b4757a39617616c6f83b6b79fe322b2e64c8
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104023086"
---
# <a name="object-model"></a><span data-ttu-id="3858d-103">物件模型</span><span class="sxs-lookup"><span data-stu-id="3858d-103">Object Model</span></span>

<span data-ttu-id="3858d-104">下表列出可透過 Windows 篩選平台 (WFP) 所提供的各種 API 集合來操作的物件類型。</span><span class="sxs-lookup"><span data-stu-id="3858d-104">The following table lists the object types that can be manipulated through the various API sets supplied by the Windows Filtering Platform (WFP).</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3858d-105">物件類型</span><span class="sxs-lookup"><span data-stu-id="3858d-105">Object Type</span></span></th>
<th><span data-ttu-id="3858d-106">Description</span><span class="sxs-lookup"><span data-stu-id="3858d-106">Description</span></span></th>
<th><span data-ttu-id="3858d-107">範例屬性</span><span class="sxs-lookup"><span data-stu-id="3858d-107">Sample Properties</span></span></th>
<th><span data-ttu-id="3858d-108">範例</span><span class="sxs-lookup"><span data-stu-id="3858d-108">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3858d-109">篩選</span><span class="sxs-lookup"><span data-stu-id="3858d-109">Filter</span></span></td>
<td><span data-ttu-id="3858d-110">控制分類的規則。</span><span class="sxs-lookup"><span data-stu-id="3858d-110">A rule that governs classification.</span></span> <span data-ttu-id="3858d-111">如果符合條件，則會叫用動作。</span><span class="sxs-lookup"><span data-stu-id="3858d-111">If the conditions are met, the action is invoked.</span></span> <br/> <span data-ttu-id="3858d-112">這是 WFP 公開的最複雜物件，因為它會將所有其他物件類型系結在一起。</span><span class="sxs-lookup"><span data-stu-id="3858d-112">This is the most complex object exposed by WFP since it ties together all the other object types.</span></span> <br/></td>
<td><ul>
<li><span data-ttu-id="3858d-113">條件陣列</span><span class="sxs-lookup"><span data-stu-id="3858d-113">Array of conditions</span></span></li>
<li><span data-ttu-id="3858d-114">動作 (允許、封鎖、標注) </span><span class="sxs-lookup"><span data-stu-id="3858d-114">Action (Permit, Block, Callout)</span></span></li>
<li><span data-ttu-id="3858d-115"><a href="filter-weight-assignment.md">Weight</a></span><span class="sxs-lookup"><span data-stu-id="3858d-115"><a href="filter-weight-assignment.md">Weight</a></span></span></li>
<li><span data-ttu-id="3858d-116">Context</span><span class="sxs-lookup"><span data-stu-id="3858d-116">Context</span></span></li>
</ul></td>
<td><span data-ttu-id="3858d-117">&quot;封鎖 TCP 埠大於1024的流量。&quot;</span><span class="sxs-lookup"><span data-stu-id="3858d-117">&quot;Block traffic with a TCP port greater than 1024.&quot;</span></span> <br/> <span data-ttu-id="3858d-118">&quot;未受保護之所有流量的識別碼。&quot;</span><span class="sxs-lookup"><span data-stu-id="3858d-118">&quot;Callout to IDS for all traffic that is not secured.&quot;</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3858d-119">圖說文字</span><span class="sxs-lookup"><span data-stu-id="3858d-119">Callout</span></span></td>
<td><span data-ttu-id="3858d-120">參與分類進程的一組函數。</span><span class="sxs-lookup"><span data-stu-id="3858d-120">A set of functions that participate in the classification process.</span></span><br/> <span data-ttu-id="3858d-121">它可讓您在符合特定條件時進行自訂封包處理。</span><span class="sxs-lookup"><span data-stu-id="3858d-121">It allows for custom packet processing to be done when certain conditions are met.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="3858d-122">識別碼</span><span class="sxs-lookup"><span data-stu-id="3858d-122">ID</span></span></li>
<li><span data-ttu-id="3858d-123">適用的圖層</span><span class="sxs-lookup"><span data-stu-id="3858d-123">Applicable layer</span></span></li>
</ul></td>
<td><span data-ttu-id="3858d-124">NAT 驅動程式</span><span class="sxs-lookup"><span data-stu-id="3858d-124">The NAT driver</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3858d-125">層</span><span class="sxs-lookup"><span data-stu-id="3858d-125">Layer</span></span></td>
<td><span data-ttu-id="3858d-126">篩選引擎中的篩選容器。</span><span class="sxs-lookup"><span data-stu-id="3858d-126">A filter container in the filter engine.</span></span> <br/> <span data-ttu-id="3858d-127">代表在網路流量處理中叫用篩選引擎的特定點。</span><span class="sxs-lookup"><span data-stu-id="3858d-127">Represents a specific point in network traffic processing where the filter engine is invoked.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="3858d-128">可以新增至圖層之篩選準則的架構</span><span class="sxs-lookup"><span data-stu-id="3858d-128">Schema for filters that can be added to the layer</span></span></li>
</ul></td>
<td><span data-ttu-id="3858d-129">輸入傳輸層</span><span class="sxs-lookup"><span data-stu-id="3858d-129">The Inbound Transport Layer</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3858d-130">子圖層</span><span class="sxs-lookup"><span data-stu-id="3858d-130">Sub-layer</span></span></td>
<td><span data-ttu-id="3858d-131">圖層的子元件，用於 <a href="filter-arbitration.md">篩選仲裁</a>。</span><span class="sxs-lookup"><span data-stu-id="3858d-131">A sub-component of a layer, used in <a href="filter-arbitration.md">filter arbitration</a>.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="3858d-132">Weight</span><span class="sxs-lookup"><span data-stu-id="3858d-132">Weight</span></span></li>
</ul></td>
<td><span data-ttu-id="3858d-133">IPsec 通道子層</span><span class="sxs-lookup"><span data-stu-id="3858d-133">The IPsec Tunnel sub-layer</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3858d-134">提供者</span><span class="sxs-lookup"><span data-stu-id="3858d-134">Provider</span></span></td>
<td><span data-ttu-id="3858d-135">在 WFP 上建立解決方案的原則提供者。</span><span class="sxs-lookup"><span data-stu-id="3858d-135">A policy provider that has built a solution on WFP.</span></span><br/> <span data-ttu-id="3858d-136">它僅供管理之用;它不會影響執行時間封包處理。</span><span class="sxs-lookup"><span data-stu-id="3858d-136">It is used solely for management; it does not affect run-time packet processing.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="3858d-137">識別碼</span><span class="sxs-lookup"><span data-stu-id="3858d-137">ID</span></span></li>
<li><span data-ttu-id="3858d-138">服務名稱</span><span class="sxs-lookup"><span data-stu-id="3858d-138">Service name</span></span></li>
</ul></td>
<td><span data-ttu-id="3858d-139">具有進階安全性的 Windows 防火牆</span><span class="sxs-lookup"><span data-stu-id="3858d-139">Windows Firewall with Advanced Security</span></span><br/> <span data-ttu-id="3858d-140">協力廠商 URL 篩選應用程式</span><span class="sxs-lookup"><span data-stu-id="3858d-140">A 3rd-party URL filtering application</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3858d-141">提供者內容</span><span class="sxs-lookup"><span data-stu-id="3858d-141">Provider Context</span></span></td>
<td><span data-ttu-id="3858d-142">原則提供者用來儲存任意內容資訊的資料 blob。</span><span class="sxs-lookup"><span data-stu-id="3858d-142">A data blob used by a policy provider to store arbitrary context information.</span></span> <br/> <span data-ttu-id="3858d-143">它是用來將自訂設定資訊傳遞給標注。</span><span class="sxs-lookup"><span data-stu-id="3858d-143">It is used to pass custom configuration information to a callout.</span></span><br/> <span data-ttu-id="3858d-144">使用內容資訊最常見的方式，是讓篩選參考提供者內容。</span><span class="sxs-lookup"><span data-stu-id="3858d-144">The most common way to use the context information is to have filters reference a provider context.</span></span> <br/></td>
<td><ul>
<li><span data-ttu-id="3858d-145">識別碼</span><span class="sxs-lookup"><span data-stu-id="3858d-145">ID</span></span></li>
<li><span data-ttu-id="3858d-146">資料 blob</span><span class="sxs-lookup"><span data-stu-id="3858d-146">Data blob</span></span></li>
</ul></td>
<td><span data-ttu-id="3858d-147">IPsec 會將驗證設定儲存在基礎篩選引擎 ( BFE) 。</span><span class="sxs-lookup"><span data-stu-id="3858d-147">IPsec stores authentication settings in the Base Filtering Engine ( BFE).</span></span> <span data-ttu-id="3858d-148">&quot; &quot; 篩選準則的內容屬性會指出用於篩選器所描述之流量的驗證設定。</span><span class="sxs-lookup"><span data-stu-id="3858d-148">The &quot;Context&quot; property of a filter indicates the authentication settings to use for the traffic that the filter describes.</span></span><br/> <span data-ttu-id="3858d-149">SSL 憑證選取填充碼會將認證資訊儲存在提供者內容中。</span><span class="sxs-lookup"><span data-stu-id="3858d-149">The SSL certification selection shim will store certification information in a provider context.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3858d-150">WFP API 所公開的物件類型具有一致的語法。</span><span class="sxs-lookup"><span data-stu-id="3858d-150">The object types exposed by WFP API have consistent semantics.</span></span> <span data-ttu-id="3858d-151">針對所有物件類型，新增、列舉、訂閱等等的動作都很類似。</span><span class="sxs-lookup"><span data-stu-id="3858d-151">The actions of add, enumerate, subscribe, and so on are similar for all object types.</span></span>

<span data-ttu-id="3858d-152">每個物件類型都是以資料結構來表示 (例如 [**FWPM \_ FILTER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0)) 。</span><span class="sxs-lookup"><span data-stu-id="3858d-152">Each object type is represented by a data structure (for example, [**FWPM\_FILTER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0)).</span></span> <span data-ttu-id="3858d-153">為了將 WFP API 所公開的不同資料結構數目降至最低，您可以使用相同的資料結構來加入新物件，以及抓取現有物件。</span><span class="sxs-lookup"><span data-stu-id="3858d-153">In order to minimize the number of different data structures exposed by the WFP API, the same data structure is used for both adding new objects and retrieving existing ones.</span></span> <span data-ttu-id="3858d-154">因此，在加入新的物件時，會忽略每個資料結構中的欄位，因為這些欄位是由基礎篩選引擎填入 (BFE) ，而不是由呼叫端所填入。</span><span class="sxs-lookup"><span data-stu-id="3858d-154">Thus, there may be fields in each data structure that are ignored when adding a new object since these fields are filled in by the Base Filtering Engine (BFE), and not by the caller.</span></span> <span data-ttu-id="3858d-155">例如， **FWPM \_ FILTER0** 資料結構有一個 **filterId** 欄位，其中包含對應 **FWPS \_ FILTER0** 的 **LUID** 。</span><span class="sxs-lookup"><span data-stu-id="3858d-155">For example, an **FWPM\_FILTER0** data structure has a **filterId** field that contains the **LUID** of the corresponding **FWPS\_FILTER0**.</span></span> <span data-ttu-id="3858d-156">此 **LUID** 是由 BFE 所指派，因此在 [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)的呼叫中會忽略此欄位。</span><span class="sxs-lookup"><span data-stu-id="3858d-156">This **LUID** is assigned by BFE, and thus, this field is ignored in the call to [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3858d-157">相關主題</span><span class="sxs-lookup"><span data-stu-id="3858d-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3858d-158">物件管理</span><span class="sxs-lookup"><span data-stu-id="3858d-158">Object Management</span></span>](object-management.md)
</dt> </dl>

 

 





