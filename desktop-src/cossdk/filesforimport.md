---
description: 抓取匯入之應用程式的資訊。
ms.assetid: 9ed4bc3f-3490-4c36-ba94-bc803886a4d2
title: FilesForImport 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FilesForImport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8e7ba3b0bd44cf2f6bb40ecf89f86dd68c21cf3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111028"
---
# <a name="filesforimport-collection"></a><span data-ttu-id="0c90c-103">FilesForImport 集合</span><span class="sxs-lookup"><span data-stu-id="0c90c-103">FilesForImport collection</span></span>

<span data-ttu-id="0c90c-104">抓取匯入之應用程式的資訊。</span><span class="sxs-lookup"><span data-stu-id="0c90c-104">Retrieves information for applications that are imported.</span></span>

<span data-ttu-id="0c90c-105">此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。</span><span class="sxs-lookup"><span data-stu-id="0c90c-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="0c90c-106">成員</span><span class="sxs-lookup"><span data-stu-id="0c90c-106">Members</span></span>

<span data-ttu-id="0c90c-107">**FilesForImport** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="0c90c-107">The **FilesForImport** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="0c90c-108">相關集合</span><span class="sxs-lookup"><span data-stu-id="0c90c-108">Related Collections</span></span>

<span data-ttu-id="0c90c-109">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="0c90c-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="0c90c-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="0c90c-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="0c90c-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="0c90c-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="0c90c-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="0c90c-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="0c90c-113">您可以從下列集合流覽至這個集合：</span><span class="sxs-lookup"><span data-stu-id="0c90c-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="0c90c-114">**根**</span><span class="sxs-lookup"><span data-stu-id="0c90c-114">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="0c90c-115">屬性</span><span class="sxs-lookup"><span data-stu-id="0c90c-115">Properties</span></span>

<span data-ttu-id="0c90c-116">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="0c90c-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="0c90c-117">ApplicationFileName</span><span class="sxs-lookup"><span data-stu-id="0c90c-117">ApplicationFileName</span></span>](#applicationfilename)
-   [<span data-ttu-id="0c90c-118">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="0c90c-118">ApplicationName</span></span>](#applicationname)
-   [<span data-ttu-id="0c90c-119">說明</span><span class="sxs-lookup"><span data-stu-id="0c90c-119">Description</span></span>](#partitiondescription)
-   [<span data-ttu-id="0c90c-120">FileName</span><span class="sxs-lookup"><span data-stu-id="0c90c-120">FileName</span></span>](#applicationfilename)
-   [<span data-ttu-id="0c90c-121">HasUsers</span><span class="sxs-lookup"><span data-stu-id="0c90c-121">HasUsers</span></span>](#hasusers)
-   [<span data-ttu-id="0c90c-122">IsProxy</span><span class="sxs-lookup"><span data-stu-id="0c90c-122">IsProxy</span></span>](#isproxy)
-   [<span data-ttu-id="0c90c-123">IsService</span><span class="sxs-lookup"><span data-stu-id="0c90c-123">IsService</span></span>](#isservice)
-   [<span data-ttu-id="0c90c-124">PartitionDescription</span><span class="sxs-lookup"><span data-stu-id="0c90c-124">PartitionDescription</span></span>](#partitiondescription)
-   [<span data-ttu-id="0c90c-125">PartitionID</span><span class="sxs-lookup"><span data-stu-id="0c90c-125">PartitionID</span></span>](#partitionid)
-   [<span data-ttu-id="0c90c-126">PartitionName</span><span class="sxs-lookup"><span data-stu-id="0c90c-126">PartitionName</span></span>](#partitionname)

### <a name="applicationfilename"></a><span data-ttu-id="0c90c-127">ApplicationFileName</span><span class="sxs-lookup"><span data-stu-id="0c90c-127">ApplicationFileName</span></span>



| <span data-ttu-id="0c90c-128">進入</span><span class="sxs-lookup"><span data-stu-id="0c90c-128">Entry</span></span> | <span data-ttu-id="0c90c-129">值</span><span class="sxs-lookup"><span data-stu-id="0c90c-129">Value</span></span> |
|----------------|------------------------------------------------------------------------------|
| <span data-ttu-id="0c90c-130">描述</span><span class="sxs-lookup"><span data-stu-id="0c90c-130">Description</span></span>    | <span data-ttu-id="0c90c-131">包含可匯入之應用程式的 MSI 檔案名。</span><span class="sxs-lookup"><span data-stu-id="0c90c-131">The name of the MSI file that contains the application that can be imported.</span></span> |
| <span data-ttu-id="0c90c-132">Access</span><span class="sxs-lookup"><span data-stu-id="0c90c-132">Access</span></span>         | <span data-ttu-id="0c90c-133">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="0c90c-133">ReadOnly</span></span>                                                                     |
| <span data-ttu-id="0c90c-134">類型</span><span class="sxs-lookup"><span data-stu-id="0c90c-134">Type</span></span>           | <span data-ttu-id="0c90c-135">String</span><span class="sxs-lookup"><span data-stu-id="0c90c-135">String</span></span>                                                                       |
| <span data-ttu-id="0c90c-136">預設值</span><span class="sxs-lookup"><span data-stu-id="0c90c-136">Default</span></span>        | <span data-ttu-id="0c90c-137">N/A</span><span class="sxs-lookup"><span data-stu-id="0c90c-137">N/A</span></span>                                                                          |
| <span data-ttu-id="0c90c-138">最小系統</span><span class="sxs-lookup"><span data-stu-id="0c90c-138">Minimum system</span></span> | <span data-ttu-id="0c90c-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0c90c-139">Windows XP</span></span>                                                                   |



 

### <a name="applicationname"></a><span data-ttu-id="0c90c-140">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="0c90c-140">ApplicationName</span></span>



| <span data-ttu-id="0c90c-141">進入</span><span class="sxs-lookup"><span data-stu-id="0c90c-141">Entry</span></span> | <span data-ttu-id="0c90c-142">值</span><span class="sxs-lookup"><span data-stu-id="0c90c-142">Value</span></span> |
|----------------|------------------------------|
| <span data-ttu-id="0c90c-143">描述</span><span class="sxs-lookup"><span data-stu-id="0c90c-143">Description</span></span>    | <span data-ttu-id="0c90c-144">應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="0c90c-144">The name of the application.</span></span> |
| <span data-ttu-id="0c90c-145">Access</span><span class="sxs-lookup"><span data-stu-id="0c90c-145">Access</span></span>         | <span data-ttu-id="0c90c-146">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="0c90c-146">ReadOnly</span></span>                     |
| <span data-ttu-id="0c90c-147">類型</span><span class="sxs-lookup"><span data-stu-id="0c90c-147">Type</span></span>           | <span data-ttu-id="0c90c-148">String</span><span class="sxs-lookup"><span data-stu-id="0c90c-148">String</span></span>                       |
| <span data-ttu-id="0c90c-149">預設值</span><span class="sxs-lookup"><span data-stu-id="0c90c-149">Default</span></span>        | <span data-ttu-id="0c90c-150">""</span><span class="sxs-lookup"><span data-stu-id="0c90c-150">""</span></span>                           |
| <span data-ttu-id="0c90c-151">最小系統</span><span class="sxs-lookup"><span data-stu-id="0c90c-151">Minimum system</span></span> | <span data-ttu-id="0c90c-152">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0c90c-152">Windows XP</span></span>                   |



 

### <a name="description"></a><span data-ttu-id="0c90c-153">Description</span><span class="sxs-lookup"><span data-stu-id="0c90c-153">Description</span></span>



| <span data-ttu-id="0c90c-154">進入</span><span class="sxs-lookup"><span data-stu-id="0c90c-154">Entry</span></span> | <span data-ttu-id="0c90c-155">值</span><span class="sxs-lookup"><span data-stu-id="0c90c-155">Value</span></span> |
|----------------|-----------------------------------|
| <span data-ttu-id="0c90c-156">描述</span><span class="sxs-lookup"><span data-stu-id="0c90c-156">Description</span></span>    | <span data-ttu-id="0c90c-157">應用程式的描述。</span><span class="sxs-lookup"><span data-stu-id="0c90c-157">A description of the application.</span></span> |
| <span data-ttu-id="0c90c-158">Access</span><span class="sxs-lookup"><span data-stu-id="0c90c-158">Access</span></span>         | <span data-ttu-id="0c90c-159">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="0c90c-159">ReadOnly</span></span>                          |
| <span data-ttu-id="0c90c-160">類型</span><span class="sxs-lookup"><span data-stu-id="0c90c-160">Type</span></span>           | <span data-ttu-id="0c90c-161">String</span><span class="sxs-lookup"><span data-stu-id="0c90c-161">String</span></span>                            |
| <span data-ttu-id="0c90c-162">預設值</span><span class="sxs-lookup"><span data-stu-id="0c90c-162">Default</span></span>        | <span data-ttu-id="0c90c-163">""</span><span class="sxs-lookup"><span data-stu-id="0c90c-163">""</span></span>                                |
| <span data-ttu-id="0c90c-164">最小系統</span><span class="sxs-lookup"><span data-stu-id="0c90c-164">Minimum system</span></span> | <span data-ttu-id="0c90c-165">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0c90c-165">Windows XP</span></span>                        |



 

### <a name="filename"></a><span data-ttu-id="0c90c-166">FileName</span><span class="sxs-lookup"><span data-stu-id="0c90c-166">FileName</span></span>



| <span data-ttu-id="0c90c-167">進入</span><span class="sxs-lookup"><span data-stu-id="0c90c-167">Entry</span></span> | <span data-ttu-id="0c90c-168">值</span><span class="sxs-lookup"><span data-stu-id="0c90c-168">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c90c-169">描述</span><span class="sxs-lookup"><span data-stu-id="0c90c-169">Description</span></span>    | <span data-ttu-id="0c90c-170">包含應用程式的 DLL 或 EXE 檔案名。</span><span class="sxs-lookup"><span data-stu-id="0c90c-170">The name of the DLL or EXE file that contains the application.</span></span> <span data-ttu-id="0c90c-171">當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 或 [**名稱**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0c90c-171">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="0c90c-172">Access</span><span class="sxs-lookup"><span data-stu-id="0c90c-172">Access</span></span>         | <span data-ttu-id="0c90c-173">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="0c90c-173">ReadOnly</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="0c90c-174">類型</span><span class="sxs-lookup"><span data-stu-id="0c90c-174">Type</span></span>           | <span data-ttu-id="0c90c-175">String</span><span class="sxs-lookup"><span data-stu-id="0c90c-175">String</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="0c90c-176">預設值</span><span class="sxs-lookup"><span data-stu-id="0c90c-176">Default</span></span>        | <span data-ttu-id="0c90c-177">""</span><span class="sxs-lookup"><span data-stu-id="0c90c-177">""</span></span>                                                                                                                                                                                                                                    |
| <span data-ttu-id="0c90c-178">最小系統</span><span class="sxs-lookup"><span data-stu-id="0c90c-178">Minimum system</span></span> | <span data-ttu-id="0c90c-179">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0c90c-179">Windows XP</span></span>                                                                                                                                                                                                                            |



 

### <a name="hasusers"></a><span data-ttu-id="0c90c-180">HasUsers</span><span class="sxs-lookup"><span data-stu-id="0c90c-180">HasUsers</span></span>



| <span data-ttu-id="0c90c-181">進入</span><span class="sxs-lookup"><span data-stu-id="0c90c-181">Entry</span></span> | <span data-ttu-id="0c90c-182">值</span><span class="sxs-lookup"><span data-stu-id="0c90c-182">Value</span></span> |
|----------------|--------------------------------------------------|
| <span data-ttu-id="0c90c-183">描述</span><span class="sxs-lookup"><span data-stu-id="0c90c-183">Description</span></span>    | <span data-ttu-id="0c90c-184">指出應用程式是否有任何使用者。</span><span class="sxs-lookup"><span data-stu-id="0c90c-184">Indicates whether the application has any users.</span></span> |
| <span data-ttu-id="0c90c-185">Access</span><span class="sxs-lookup"><span data-stu-id="0c90c-185">Access</span></span>         | <span data-ttu-id="0c90c-186">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="0c90c-186">ReadOnly</span></span>                                         |
| <span data-ttu-id="0c90c-187">類型</span><span class="sxs-lookup"><span data-stu-id="0c90c-187">Type</span></span>           | <span data-ttu-id="0c90c-188">Bool</span><span class="sxs-lookup"><span data-stu-id="0c90c-188">Bool</span></span>                                             |
| <span data-ttu-id="0c90c-189">預設</span><span class="sxs-lookup"><span data-stu-id="0c90c-189">Default</span></span>        | <span data-ttu-id="0c90c-190">否</span><span class="sxs-lookup"><span data-stu-id="0c90c-190">False</span></span>                                            |
| <span data-ttu-id="0c90c-191">最小系統</span><span class="sxs-lookup"><span data-stu-id="0c90c-191">Minimum system</span></span> | <span data-ttu-id="0c90c-192">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0c90c-192">Windows XP</span></span>                                       |



 

### <a name="isproxy"></a><span data-ttu-id="0c90c-193">IsProxy</span><span class="sxs-lookup"><span data-stu-id="0c90c-193">IsProxy</span></span>



| <span data-ttu-id="0c90c-194">進入</span><span class="sxs-lookup"><span data-stu-id="0c90c-194">Entry</span></span> | <span data-ttu-id="0c90c-195">值</span><span class="sxs-lookup"><span data-stu-id="0c90c-195">Value</span></span> |
|----------------|-----------------------------------------------|
| <span data-ttu-id="0c90c-196">描述</span><span class="sxs-lookup"><span data-stu-id="0c90c-196">Description</span></span>    | <span data-ttu-id="0c90c-197">指出應用程式是否為 proxy。</span><span class="sxs-lookup"><span data-stu-id="0c90c-197">Indicates whether the application is a proxy.</span></span> |
| <span data-ttu-id="0c90c-198">Access</span><span class="sxs-lookup"><span data-stu-id="0c90c-198">Access</span></span>         | <span data-ttu-id="0c90c-199">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="0c90c-199">ReadOnly</span></span>                                      |
| <span data-ttu-id="0c90c-200">類型</span><span class="sxs-lookup"><span data-stu-id="0c90c-200">Type</span></span>           | <span data-ttu-id="0c90c-201">Bool</span><span class="sxs-lookup"><span data-stu-id="0c90c-201">Bool</span></span>                                          |
| <span data-ttu-id="0c90c-202">預設</span><span class="sxs-lookup"><span data-stu-id="0c90c-202">Default</span></span>        | <span data-ttu-id="0c90c-203">否</span><span class="sxs-lookup"><span data-stu-id="0c90c-203">False</span></span>                                         |
| <span data-ttu-id="0c90c-204">最小系統</span><span class="sxs-lookup"><span data-stu-id="0c90c-204">Minimum system</span></span> | <span data-ttu-id="0c90c-205">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0c90c-205">Windows XP</span></span>                                    |



 

### <a name="isservice"></a><span data-ttu-id="0c90c-206">IsService</span><span class="sxs-lookup"><span data-stu-id="0c90c-206">IsService</span></span>



| <span data-ttu-id="0c90c-207">進入</span><span class="sxs-lookup"><span data-stu-id="0c90c-207">Entry</span></span> | <span data-ttu-id="0c90c-208">值</span><span class="sxs-lookup"><span data-stu-id="0c90c-208">Value</span></span> |
|----------------|-------------------------------------------------|
| <span data-ttu-id="0c90c-209">描述</span><span class="sxs-lookup"><span data-stu-id="0c90c-209">Description</span></span>    | <span data-ttu-id="0c90c-210">指出應用程式是否為服務。</span><span class="sxs-lookup"><span data-stu-id="0c90c-210">Indicates whether the application is a service.</span></span> |
| <span data-ttu-id="0c90c-211">Access</span><span class="sxs-lookup"><span data-stu-id="0c90c-211">Access</span></span>         | <span data-ttu-id="0c90c-212">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="0c90c-212">ReadOnly</span></span>                                        |
| <span data-ttu-id="0c90c-213">類型</span><span class="sxs-lookup"><span data-stu-id="0c90c-213">Type</span></span>           | <span data-ttu-id="0c90c-214">Bool</span><span class="sxs-lookup"><span data-stu-id="0c90c-214">Bool</span></span>                                            |
| <span data-ttu-id="0c90c-215">預設</span><span class="sxs-lookup"><span data-stu-id="0c90c-215">Default</span></span>        | <span data-ttu-id="0c90c-216">否</span><span class="sxs-lookup"><span data-stu-id="0c90c-216">False</span></span>                                           |
| <span data-ttu-id="0c90c-217">最小系統</span><span class="sxs-lookup"><span data-stu-id="0c90c-217">Minimum system</span></span> | <span data-ttu-id="0c90c-218">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0c90c-218">Windows XP</span></span>                                      |



 

### <a name="partitiondescription"></a><span data-ttu-id="0c90c-219">PartitionDescription</span><span class="sxs-lookup"><span data-stu-id="0c90c-219">PartitionDescription</span></span>



| <span data-ttu-id="0c90c-220">進入</span><span class="sxs-lookup"><span data-stu-id="0c90c-220">Entry</span></span> | <span data-ttu-id="0c90c-221">值</span><span class="sxs-lookup"><span data-stu-id="0c90c-221">Value</span></span> |
|----------------|-----------------------------------------------|
| <span data-ttu-id="0c90c-222">描述</span><span class="sxs-lookup"><span data-stu-id="0c90c-222">Description</span></span>    | <span data-ttu-id="0c90c-223">應用程式分割區的描述。</span><span class="sxs-lookup"><span data-stu-id="0c90c-223">A description of the application's partition.</span></span> |
| <span data-ttu-id="0c90c-224">Access</span><span class="sxs-lookup"><span data-stu-id="0c90c-224">Access</span></span>         | <span data-ttu-id="0c90c-225">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="0c90c-225">ReadOnly</span></span>                                      |
| <span data-ttu-id="0c90c-226">類型</span><span class="sxs-lookup"><span data-stu-id="0c90c-226">Type</span></span>           | <span data-ttu-id="0c90c-227">String</span><span class="sxs-lookup"><span data-stu-id="0c90c-227">String</span></span>                                        |
| <span data-ttu-id="0c90c-228">預設值</span><span class="sxs-lookup"><span data-stu-id="0c90c-228">Default</span></span>        | <span data-ttu-id="0c90c-229">""</span><span class="sxs-lookup"><span data-stu-id="0c90c-229">""</span></span>                                            |
| <span data-ttu-id="0c90c-230">最小系統</span><span class="sxs-lookup"><span data-stu-id="0c90c-230">Minimum system</span></span> | <span data-ttu-id="0c90c-231">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0c90c-231">Windows Server 2003</span></span>                           |



 

### <a name="partitionid"></a><span data-ttu-id="0c90c-232">PartitionID</span><span class="sxs-lookup"><span data-stu-id="0c90c-232">PartitionID</span></span>



| <span data-ttu-id="0c90c-233">進入</span><span class="sxs-lookup"><span data-stu-id="0c90c-233">Entry</span></span> | <span data-ttu-id="0c90c-234">值</span><span class="sxs-lookup"><span data-stu-id="0c90c-234">Value</span></span> |
|----------------|------------------------------------------|
| <span data-ttu-id="0c90c-235">描述</span><span class="sxs-lookup"><span data-stu-id="0c90c-235">Description</span></span>    | <span data-ttu-id="0c90c-236">應用程式磁碟分割的 GUID。</span><span class="sxs-lookup"><span data-stu-id="0c90c-236">The GUID of the application's partition.</span></span> |
| <span data-ttu-id="0c90c-237">Access</span><span class="sxs-lookup"><span data-stu-id="0c90c-237">Access</span></span>         | <span data-ttu-id="0c90c-238">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="0c90c-238">ReadOnly</span></span>                                 |
| <span data-ttu-id="0c90c-239">類型</span><span class="sxs-lookup"><span data-stu-id="0c90c-239">Type</span></span>           | <span data-ttu-id="0c90c-240">String</span><span class="sxs-lookup"><span data-stu-id="0c90c-240">String</span></span>                                   |
| <span data-ttu-id="0c90c-241">預設值</span><span class="sxs-lookup"><span data-stu-id="0c90c-241">Default</span></span>        | <span data-ttu-id="0c90c-242">""</span><span class="sxs-lookup"><span data-stu-id="0c90c-242">""</span></span>                                       |
| <span data-ttu-id="0c90c-243">最小系統</span><span class="sxs-lookup"><span data-stu-id="0c90c-243">Minimum system</span></span> | <span data-ttu-id="0c90c-244">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0c90c-244">Windows Server 2003</span></span>                      |



 

### <a name="partitionname"></a><span data-ttu-id="0c90c-245">PartitionName</span><span class="sxs-lookup"><span data-stu-id="0c90c-245">PartitionName</span></span>



| <span data-ttu-id="0c90c-246">進入</span><span class="sxs-lookup"><span data-stu-id="0c90c-246">Entry</span></span> | <span data-ttu-id="0c90c-247">值</span><span class="sxs-lookup"><span data-stu-id="0c90c-247">Value</span></span> |
|----------------|------------------------------------------|
| <span data-ttu-id="0c90c-248">描述</span><span class="sxs-lookup"><span data-stu-id="0c90c-248">Description</span></span>    | <span data-ttu-id="0c90c-249">應用程式的資料分割名稱。</span><span class="sxs-lookup"><span data-stu-id="0c90c-249">The name of the application's partition.</span></span> |
| <span data-ttu-id="0c90c-250">Access</span><span class="sxs-lookup"><span data-stu-id="0c90c-250">Access</span></span>         | <span data-ttu-id="0c90c-251">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="0c90c-251">ReadOnly</span></span>                                 |
| <span data-ttu-id="0c90c-252">類型</span><span class="sxs-lookup"><span data-stu-id="0c90c-252">Type</span></span>           | <span data-ttu-id="0c90c-253">String</span><span class="sxs-lookup"><span data-stu-id="0c90c-253">String</span></span>                                   |
| <span data-ttu-id="0c90c-254">預設值</span><span class="sxs-lookup"><span data-stu-id="0c90c-254">Default</span></span>        | <span data-ttu-id="0c90c-255">""</span><span class="sxs-lookup"><span data-stu-id="0c90c-255">""</span></span>                                       |
| <span data-ttu-id="0c90c-256">最小系統</span><span class="sxs-lookup"><span data-stu-id="0c90c-256">Minimum system</span></span> | <span data-ttu-id="0c90c-257">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0c90c-257">Windows Server 2003</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="0c90c-258">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c90c-258">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c90c-259">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="0c90c-259">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
