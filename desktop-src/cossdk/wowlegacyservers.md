---
description: WOWLegacyServers 集合的公開屬性主要是與 LegacyServers 集合相同，不同之處在于 WOWLegacyServers 集合是從64位電腦上的32位登錄中繪製。
ms.assetid: 72380276-214c-4f12-b575-deb975d846d3
title: WOWLegacyServers 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWLegacyServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: cf417193ea4cea861f585068d139a855f80242a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973571"
---
# <a name="wowlegacyservers-collection"></a><span data-ttu-id="8e48b-103">WOWLegacyServers 集合</span><span class="sxs-lookup"><span data-stu-id="8e48b-103">WOWLegacyServers collection</span></span>

<span data-ttu-id="8e48b-104">**WOWLegacyServers** 集合的公開屬性主要是與 [**LegacyServers**](legacyservers.md)集合相同，不同之處在于 **WOWLegacyServers** 集合是從64位電腦上的32位登錄中繪製。</span><span class="sxs-lookup"><span data-stu-id="8e48b-104">Exposed properties for the **WOWLegacyServers** collection are intended to be identical to the [**LegacyServers**](legacyservers.md) collection except that the **WOWLegacyServers** collection is drawn from the 32-bit registry on 64-bit computers.</span></span>

<span data-ttu-id="8e48b-105">此集合不支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。</span><span class="sxs-lookup"><span data-stu-id="8e48b-105">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="8e48b-106">成員</span><span class="sxs-lookup"><span data-stu-id="8e48b-106">Members</span></span>

<span data-ttu-id="8e48b-107">**WOWLegacyServers** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="8e48b-107">The **WOWLegacyServers** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="8e48b-108">相關集合</span><span class="sxs-lookup"><span data-stu-id="8e48b-108">Related Collections</span></span>

<span data-ttu-id="8e48b-109">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="8e48b-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="8e48b-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="8e48b-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="8e48b-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="8e48b-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="8e48b-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="8e48b-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="8e48b-113">您可以從下列集合流覽至這個集合：</span><span class="sxs-lookup"><span data-stu-id="8e48b-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="8e48b-114">**根**</span><span class="sxs-lookup"><span data-stu-id="8e48b-114">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="8e48b-115">屬性</span><span class="sxs-lookup"><span data-stu-id="8e48b-115">Properties</span></span>

<span data-ttu-id="8e48b-116">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="8e48b-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="8e48b-117">ClassName</span><span class="sxs-lookup"><span data-stu-id="8e48b-117">ClassName</span></span>](#classname)
-   [<span data-ttu-id="8e48b-118">Clsid</span><span class="sxs-lookup"><span data-stu-id="8e48b-118">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="8e48b-119">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="8e48b-119">InprocServer32</span></span>](#inprocserver32)
-   [<span data-ttu-id="8e48b-120">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="8e48b-120">LocalServer32</span></span>](#localserver32)
-   [<span data-ttu-id="8e48b-121">ProgID</span><span class="sxs-lookup"><span data-stu-id="8e48b-121">ProgID</span></span>](#progid)

### <a name="classname"></a><span data-ttu-id="8e48b-122">ClassName</span><span class="sxs-lookup"><span data-stu-id="8e48b-122">ClassName</span></span>



| <span data-ttu-id="8e48b-123">進入</span><span class="sxs-lookup"><span data-stu-id="8e48b-123">Entry</span></span> | <span data-ttu-id="8e48b-124">值</span><span class="sxs-lookup"><span data-stu-id="8e48b-124">Value</span></span> |
|----------------|------------------------|
| <span data-ttu-id="8e48b-125">描述</span><span class="sxs-lookup"><span data-stu-id="8e48b-125">Description</span></span>    | <span data-ttu-id="8e48b-126">類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e48b-126">The name of the class.</span></span> |
| <span data-ttu-id="8e48b-127">Access</span><span class="sxs-lookup"><span data-stu-id="8e48b-127">Access</span></span>         | <span data-ttu-id="8e48b-128">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="8e48b-128">ReadOnly</span></span>               |
| <span data-ttu-id="8e48b-129">類型</span><span class="sxs-lookup"><span data-stu-id="8e48b-129">Type</span></span>           | <span data-ttu-id="8e48b-130">String</span><span class="sxs-lookup"><span data-stu-id="8e48b-130">String</span></span>                 |
| <span data-ttu-id="8e48b-131">預設值</span><span class="sxs-lookup"><span data-stu-id="8e48b-131">Default</span></span>        | <span data-ttu-id="8e48b-132">N/A</span><span class="sxs-lookup"><span data-stu-id="8e48b-132">N/A</span></span>                    |
| <span data-ttu-id="8e48b-133">最小系統</span><span class="sxs-lookup"><span data-stu-id="8e48b-133">Minimum system</span></span> | <span data-ttu-id="8e48b-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8e48b-134">Windows XP</span></span>             |



 

### <a name="clsid"></a><span data-ttu-id="8e48b-135">CLSID</span><span class="sxs-lookup"><span data-stu-id="8e48b-135">CLSID</span></span>



| <span data-ttu-id="8e48b-136">進入</span><span class="sxs-lookup"><span data-stu-id="8e48b-136">Entry</span></span> | <span data-ttu-id="8e48b-137">值</span><span class="sxs-lookup"><span data-stu-id="8e48b-137">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e48b-138">描述</span><span class="sxs-lookup"><span data-stu-id="8e48b-138">Description</span></span>    | <span data-ttu-id="8e48b-139">元件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="8e48b-139">A GUID for the component.</span></span> <span data-ttu-id="8e48b-140">當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="8e48b-140">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="8e48b-141">Access</span><span class="sxs-lookup"><span data-stu-id="8e48b-141">Access</span></span>         | <span data-ttu-id="8e48b-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="8e48b-142">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="8e48b-143">類型</span><span class="sxs-lookup"><span data-stu-id="8e48b-143">Type</span></span>           | <span data-ttu-id="8e48b-144">String</span><span class="sxs-lookup"><span data-stu-id="8e48b-144">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="8e48b-145">預設值</span><span class="sxs-lookup"><span data-stu-id="8e48b-145">Default</span></span>        | <span data-ttu-id="8e48b-146">N/A</span><span class="sxs-lookup"><span data-stu-id="8e48b-146">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="8e48b-147">最小系統</span><span class="sxs-lookup"><span data-stu-id="8e48b-147">Minimum system</span></span> | <span data-ttu-id="8e48b-148">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8e48b-148">Windows XP</span></span>                                                                                                                                                |



 

### <a name="inprocserver32"></a><span data-ttu-id="8e48b-149">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="8e48b-149">InprocServer32</span></span>



| <span data-ttu-id="8e48b-150">進入</span><span class="sxs-lookup"><span data-stu-id="8e48b-150">Entry</span></span> | <span data-ttu-id="8e48b-151">值</span><span class="sxs-lookup"><span data-stu-id="8e48b-151">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="8e48b-152">描述</span><span class="sxs-lookup"><span data-stu-id="8e48b-152">Description</span></span>    | <span data-ttu-id="8e48b-153">元件的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="8e48b-153">The file path for the component.</span></span> |
| <span data-ttu-id="8e48b-154">Access</span><span class="sxs-lookup"><span data-stu-id="8e48b-154">Access</span></span>         | <span data-ttu-id="8e48b-155">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="8e48b-155">ReadOnly</span></span>                         |
| <span data-ttu-id="8e48b-156">類型</span><span class="sxs-lookup"><span data-stu-id="8e48b-156">Type</span></span>           | <span data-ttu-id="8e48b-157">String</span><span class="sxs-lookup"><span data-stu-id="8e48b-157">String</span></span>                           |
| <span data-ttu-id="8e48b-158">預設值</span><span class="sxs-lookup"><span data-stu-id="8e48b-158">Default</span></span>        | <span data-ttu-id="8e48b-159">N/A</span><span class="sxs-lookup"><span data-stu-id="8e48b-159">N/A</span></span>                              |
| <span data-ttu-id="8e48b-160">最小系統</span><span class="sxs-lookup"><span data-stu-id="8e48b-160">Minimum system</span></span> | <span data-ttu-id="8e48b-161">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8e48b-161">Windows XP</span></span>                       |



 

### <a name="localserver32"></a><span data-ttu-id="8e48b-162">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="8e48b-162">LocalServer32</span></span>



| <span data-ttu-id="8e48b-163">進入</span><span class="sxs-lookup"><span data-stu-id="8e48b-163">Entry</span></span> | <span data-ttu-id="8e48b-164">值</span><span class="sxs-lookup"><span data-stu-id="8e48b-164">Value</span></span> |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="8e48b-165">描述</span><span class="sxs-lookup"><span data-stu-id="8e48b-165">Description</span></span>    | <span data-ttu-id="8e48b-166">指定32位本機伺服器應用程式的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="8e48b-166">Specifies the full path to a 32-bit local server application.</span></span> |
| <span data-ttu-id="8e48b-167">Access</span><span class="sxs-lookup"><span data-stu-id="8e48b-167">Access</span></span>         | <span data-ttu-id="8e48b-168">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="8e48b-168">ReadOnly</span></span>                                                      |
| <span data-ttu-id="8e48b-169">類型</span><span class="sxs-lookup"><span data-stu-id="8e48b-169">Type</span></span>           | <span data-ttu-id="8e48b-170">String</span><span class="sxs-lookup"><span data-stu-id="8e48b-170">String</span></span>                                                        |
| <span data-ttu-id="8e48b-171">預設值</span><span class="sxs-lookup"><span data-stu-id="8e48b-171">Default</span></span>        | <span data-ttu-id="8e48b-172">N/A</span><span class="sxs-lookup"><span data-stu-id="8e48b-172">N/A</span></span>                                                           |
| <span data-ttu-id="8e48b-173">最小系統</span><span class="sxs-lookup"><span data-stu-id="8e48b-173">Minimum system</span></span> | <span data-ttu-id="8e48b-174">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8e48b-174">Windows XP</span></span>                                                    |



 

### <a name="progid"></a><span data-ttu-id="8e48b-175">ProgID</span><span class="sxs-lookup"><span data-stu-id="8e48b-175">ProgID</span></span>



| <span data-ttu-id="8e48b-176">進入</span><span class="sxs-lookup"><span data-stu-id="8e48b-176">Entry</span></span> | <span data-ttu-id="8e48b-177">值</span><span class="sxs-lookup"><span data-stu-id="8e48b-177">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e48b-178">描述</span><span class="sxs-lookup"><span data-stu-id="8e48b-178">Description</span></span>    | <span data-ttu-id="8e48b-179">識別元件的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e48b-179">A name identifying the component.</span></span> <span data-ttu-id="8e48b-180">在這個集合的物件上呼叫 [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="8e48b-180">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="8e48b-181">Access</span><span class="sxs-lookup"><span data-stu-id="8e48b-181">Access</span></span>         | <span data-ttu-id="8e48b-182">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="8e48b-182">ReadOnly</span></span>                                                                                                                                                            |
| <span data-ttu-id="8e48b-183">類型</span><span class="sxs-lookup"><span data-stu-id="8e48b-183">Type</span></span>           | <span data-ttu-id="8e48b-184">String</span><span class="sxs-lookup"><span data-stu-id="8e48b-184">String</span></span>                                                                                                                                                              |
| <span data-ttu-id="8e48b-185">預設值</span><span class="sxs-lookup"><span data-stu-id="8e48b-185">Default</span></span>        | <span data-ttu-id="8e48b-186">N/A</span><span class="sxs-lookup"><span data-stu-id="8e48b-186">N/A</span></span>                                                                                                                                                                 |
| <span data-ttu-id="8e48b-187">最小系統</span><span class="sxs-lookup"><span data-stu-id="8e48b-187">Minimum system</span></span> | <span data-ttu-id="8e48b-188">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8e48b-188">Windows XP</span></span>                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="8e48b-189">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8e48b-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e48b-190">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="8e48b-190">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
