---
description: 與 InprocServers 集合相同，不同之處在于此集合也包含本機伺服器。
ms.assetid: b185f568-ec97-4710-b744-5d69e71d6f60
title: LegacyServers 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LegacyServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2ea542fa539ea1eb1cceae0f4cb8ba8dc2012085
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991629"
---
# <a name="legacyservers-collection"></a><span data-ttu-id="ac73d-103">LegacyServers 集合</span><span class="sxs-lookup"><span data-stu-id="ac73d-103">LegacyServers collection</span></span>

<span data-ttu-id="ac73d-104">與 [**InprocServers**](inprocservers.md) 集合相同，不同之處在于此集合也包含本機伺服器。</span><span class="sxs-lookup"><span data-stu-id="ac73d-104">Identical to the [**InprocServers**](inprocservers.md) collection except that this collection also includes local servers.</span></span>

<span data-ttu-id="ac73d-105">此集合不支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。</span><span class="sxs-lookup"><span data-stu-id="ac73d-105">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="ac73d-106">成員</span><span class="sxs-lookup"><span data-stu-id="ac73d-106">Members</span></span>

<span data-ttu-id="ac73d-107">**LegacyServers** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="ac73d-107">The **LegacyServers** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="ac73d-108">相關集合</span><span class="sxs-lookup"><span data-stu-id="ac73d-108">Related Collections</span></span>

<span data-ttu-id="ac73d-109">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="ac73d-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="ac73d-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="ac73d-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="ac73d-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="ac73d-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="ac73d-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="ac73d-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="ac73d-113">您可以從下列集合流覽至這個集合：</span><span class="sxs-lookup"><span data-stu-id="ac73d-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="ac73d-114">**根**</span><span class="sxs-lookup"><span data-stu-id="ac73d-114">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="ac73d-115">屬性</span><span class="sxs-lookup"><span data-stu-id="ac73d-115">Properties</span></span>

<span data-ttu-id="ac73d-116">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="ac73d-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="ac73d-117">ClassName</span><span class="sxs-lookup"><span data-stu-id="ac73d-117">ClassName</span></span>](#classname)
-   [<span data-ttu-id="ac73d-118">Clsid</span><span class="sxs-lookup"><span data-stu-id="ac73d-118">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="ac73d-119">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="ac73d-119">InprocServer32</span></span>](#inprocserver32)
-   [<span data-ttu-id="ac73d-120">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="ac73d-120">LocalServer32</span></span>](#localserver32)
-   [<span data-ttu-id="ac73d-121">ProgID</span><span class="sxs-lookup"><span data-stu-id="ac73d-121">ProgID</span></span>](#progid)

### <a name="classname"></a><span data-ttu-id="ac73d-122">ClassName</span><span class="sxs-lookup"><span data-stu-id="ac73d-122">ClassName</span></span>



| <span data-ttu-id="ac73d-123">進入</span><span class="sxs-lookup"><span data-stu-id="ac73d-123">Entry</span></span> | <span data-ttu-id="ac73d-124">值</span><span class="sxs-lookup"><span data-stu-id="ac73d-124">Value</span></span> |
|----------------|------------------------|
| <span data-ttu-id="ac73d-125">描述</span><span class="sxs-lookup"><span data-stu-id="ac73d-125">Description</span></span>    | <span data-ttu-id="ac73d-126">類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="ac73d-126">The name of the class.</span></span> |
| <span data-ttu-id="ac73d-127">Access</span><span class="sxs-lookup"><span data-stu-id="ac73d-127">Access</span></span>         | <span data-ttu-id="ac73d-128">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ac73d-128">ReadOnly</span></span>               |
| <span data-ttu-id="ac73d-129">類型</span><span class="sxs-lookup"><span data-stu-id="ac73d-129">Type</span></span>           | <span data-ttu-id="ac73d-130">String</span><span class="sxs-lookup"><span data-stu-id="ac73d-130">String</span></span>                 |
| <span data-ttu-id="ac73d-131">預設值</span><span class="sxs-lookup"><span data-stu-id="ac73d-131">Default</span></span>        | <span data-ttu-id="ac73d-132">N/A</span><span class="sxs-lookup"><span data-stu-id="ac73d-132">N/A</span></span>                    |
| <span data-ttu-id="ac73d-133">最小系統</span><span class="sxs-lookup"><span data-stu-id="ac73d-133">Minimum system</span></span> | <span data-ttu-id="ac73d-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ac73d-134">Windows XP</span></span>             |



 

### <a name="clsid"></a><span data-ttu-id="ac73d-135">CLSID</span><span class="sxs-lookup"><span data-stu-id="ac73d-135">CLSID</span></span>



| <span data-ttu-id="ac73d-136">進入</span><span class="sxs-lookup"><span data-stu-id="ac73d-136">Entry</span></span> | <span data-ttu-id="ac73d-137">值</span><span class="sxs-lookup"><span data-stu-id="ac73d-137">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac73d-138">描述</span><span class="sxs-lookup"><span data-stu-id="ac73d-138">Description</span></span>    | <span data-ttu-id="ac73d-139">元件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="ac73d-139">A GUID for the component.</span></span> <span data-ttu-id="ac73d-140">當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="ac73d-140">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="ac73d-141">Access</span><span class="sxs-lookup"><span data-stu-id="ac73d-141">Access</span></span>         | <span data-ttu-id="ac73d-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ac73d-142">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="ac73d-143">類型</span><span class="sxs-lookup"><span data-stu-id="ac73d-143">Type</span></span>           | <span data-ttu-id="ac73d-144">String</span><span class="sxs-lookup"><span data-stu-id="ac73d-144">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="ac73d-145">預設值</span><span class="sxs-lookup"><span data-stu-id="ac73d-145">Default</span></span>        | <span data-ttu-id="ac73d-146">N/A</span><span class="sxs-lookup"><span data-stu-id="ac73d-146">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="ac73d-147">最小系統</span><span class="sxs-lookup"><span data-stu-id="ac73d-147">Minimum system</span></span> | <span data-ttu-id="ac73d-148">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ac73d-148">Windows XP</span></span>                                                                                                                                                |



 

### <a name="inprocserver32"></a><span data-ttu-id="ac73d-149">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="ac73d-149">InprocServer32</span></span>



| <span data-ttu-id="ac73d-150">進入</span><span class="sxs-lookup"><span data-stu-id="ac73d-150">Entry</span></span> | <span data-ttu-id="ac73d-151">值</span><span class="sxs-lookup"><span data-stu-id="ac73d-151">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="ac73d-152">描述</span><span class="sxs-lookup"><span data-stu-id="ac73d-152">Description</span></span>    | <span data-ttu-id="ac73d-153">元件的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="ac73d-153">The file path for the component.</span></span> |
| <span data-ttu-id="ac73d-154">Access</span><span class="sxs-lookup"><span data-stu-id="ac73d-154">Access</span></span>         | <span data-ttu-id="ac73d-155">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ac73d-155">ReadOnly</span></span>                         |
| <span data-ttu-id="ac73d-156">類型</span><span class="sxs-lookup"><span data-stu-id="ac73d-156">Type</span></span>           | <span data-ttu-id="ac73d-157">String</span><span class="sxs-lookup"><span data-stu-id="ac73d-157">String</span></span>                           |
| <span data-ttu-id="ac73d-158">預設值</span><span class="sxs-lookup"><span data-stu-id="ac73d-158">Default</span></span>        | <span data-ttu-id="ac73d-159">N/A</span><span class="sxs-lookup"><span data-stu-id="ac73d-159">N/A</span></span>                              |
| <span data-ttu-id="ac73d-160">最小系統</span><span class="sxs-lookup"><span data-stu-id="ac73d-160">Minimum system</span></span> | <span data-ttu-id="ac73d-161">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ac73d-161">Windows XP</span></span>                       |



 

### <a name="localserver32"></a><span data-ttu-id="ac73d-162">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="ac73d-162">LocalServer32</span></span>



| <span data-ttu-id="ac73d-163">進入</span><span class="sxs-lookup"><span data-stu-id="ac73d-163">Entry</span></span> | <span data-ttu-id="ac73d-164">值</span><span class="sxs-lookup"><span data-stu-id="ac73d-164">Value</span></span> |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="ac73d-165">描述</span><span class="sxs-lookup"><span data-stu-id="ac73d-165">Description</span></span>    | <span data-ttu-id="ac73d-166">指定32位本機伺服器應用程式的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="ac73d-166">Specifies the full path to a 32-bit local server application.</span></span> |
| <span data-ttu-id="ac73d-167">Access</span><span class="sxs-lookup"><span data-stu-id="ac73d-167">Access</span></span>         | <span data-ttu-id="ac73d-168">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ac73d-168">ReadOnly</span></span>                                                      |
| <span data-ttu-id="ac73d-169">類型</span><span class="sxs-lookup"><span data-stu-id="ac73d-169">Type</span></span>           | <span data-ttu-id="ac73d-170">String</span><span class="sxs-lookup"><span data-stu-id="ac73d-170">String</span></span>                                                        |
| <span data-ttu-id="ac73d-171">預設值</span><span class="sxs-lookup"><span data-stu-id="ac73d-171">Default</span></span>        | <span data-ttu-id="ac73d-172">N/A</span><span class="sxs-lookup"><span data-stu-id="ac73d-172">N/A</span></span>                                                           |
| <span data-ttu-id="ac73d-173">最小系統</span><span class="sxs-lookup"><span data-stu-id="ac73d-173">Minimum system</span></span> | <span data-ttu-id="ac73d-174">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ac73d-174">Windows XP</span></span>                                                    |



 

### <a name="progid"></a><span data-ttu-id="ac73d-175">ProgID</span><span class="sxs-lookup"><span data-stu-id="ac73d-175">ProgID</span></span>



| <span data-ttu-id="ac73d-176">進入</span><span class="sxs-lookup"><span data-stu-id="ac73d-176">Entry</span></span> | <span data-ttu-id="ac73d-177">值</span><span class="sxs-lookup"><span data-stu-id="ac73d-177">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac73d-178">描述</span><span class="sxs-lookup"><span data-stu-id="ac73d-178">Description</span></span>    | <span data-ttu-id="ac73d-179">識別元件的名稱。</span><span class="sxs-lookup"><span data-stu-id="ac73d-179">A name identifying the component.</span></span> <span data-ttu-id="ac73d-180">在這個集合的物件上呼叫 [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="ac73d-180">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="ac73d-181">Access</span><span class="sxs-lookup"><span data-stu-id="ac73d-181">Access</span></span>         | <span data-ttu-id="ac73d-182">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ac73d-182">ReadOnly</span></span>                                                                                                                                                            |
| <span data-ttu-id="ac73d-183">類型</span><span class="sxs-lookup"><span data-stu-id="ac73d-183">Type</span></span>           | <span data-ttu-id="ac73d-184">String</span><span class="sxs-lookup"><span data-stu-id="ac73d-184">String</span></span>                                                                                                                                                              |
| <span data-ttu-id="ac73d-185">預設值</span><span class="sxs-lookup"><span data-stu-id="ac73d-185">Default</span></span>        | <span data-ttu-id="ac73d-186">N/A</span><span class="sxs-lookup"><span data-stu-id="ac73d-186">N/A</span></span>                                                                                                                                                                 |
| <span data-ttu-id="ac73d-187">最小系統</span><span class="sxs-lookup"><span data-stu-id="ac73d-187">Minimum system</span></span> | <span data-ttu-id="ac73d-188">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ac73d-188">Windows XP</span></span>                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="ac73d-189">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac73d-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac73d-190">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="ac73d-190">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
