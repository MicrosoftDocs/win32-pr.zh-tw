---
description: 抓取有關處理多個物件之方法的延伸錯誤資訊，例如在 COMAdminCatalogCollection 物件上填入和 SaveChanges，以及在 COMAdminCatalog 物件上安裝、匯入或匯出應用程式或元件的方法。
ms.assetid: cf612fc4-55dd-4706-8c41-2654ca922b9a
title: ErrorInfo 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ErrorInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: ebcb4b89eee51b475869cfc62676feda10e53084
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468389"
---
# <a name="errorinfo-collection"></a><span data-ttu-id="76ea5-103">ErrorInfo 集合</span><span class="sxs-lookup"><span data-stu-id="76ea5-103">ErrorInfo collection</span></span>

<span data-ttu-id="76ea5-104">抓取有關處理多個物件之方法的延伸錯誤資訊，例如在 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件上 [**填入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate)和 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) ，以及在 [**COMAdminCatalog**](comadmincatalog.md)物件上安裝、匯入或匯出應用程式或元件的方法。</span><span class="sxs-lookup"><span data-stu-id="76ea5-104">Retrieves extended error information regarding methods that deal with multiple objects, such as [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) and [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, and methods to install, import, or export applications or components on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

<span data-ttu-id="76ea5-105">在 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)上使用 [**>getcollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection)方法，以存取與原創組合（具有錯誤）相關聯的 **ErrorInfo** 集合。</span><span class="sxs-lookup"><span data-stu-id="76ea5-105">Use the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) method on a [**COMAdminCatalogCollection**](comadmincatalogcollection.md) to access the **ErrorInfo** collection associated with the original collection that has an error.</span></span>

<span data-ttu-id="76ea5-106">一旦發生錯誤，您就必須立即在 **ErrorInfo** 上呼叫 [**>getcollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) ;否則會遺失錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="76ea5-106">You must call [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) on **ErrorInfo** immediately after an error occurs; otherwise, the error information is lost.</span></span>

<span data-ttu-id="76ea5-107">此集合不支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。</span><span class="sxs-lookup"><span data-stu-id="76ea5-107">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="76ea5-108">成員</span><span class="sxs-lookup"><span data-stu-id="76ea5-108">Members</span></span>

<span data-ttu-id="76ea5-109">**ErrorInfo** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="76ea5-109">The **ErrorInfo** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="76ea5-110">相關集合</span><span class="sxs-lookup"><span data-stu-id="76ea5-110">Related Collections</span></span>

<span data-ttu-id="76ea5-111">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="76ea5-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="76ea5-112">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="76ea5-112">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="76ea5-113">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="76ea5-113">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="76ea5-114">除了 **ErrorInfo**、 [**InprocServers**](inprocservers.md)、 [**PropertyInfo**](propertyinfo.md)、 [**RelatedCollectionInfo**](relatedcollectioninfo.md)、 [**Root**](root.md)和 [**WOWInprocServers**](wowinprocservers.md)之外，您可以從每個集合流覽至這個集合。</span><span class="sxs-lookup"><span data-stu-id="76ea5-114">You can navigate to this collection from every collection except for **ErrorInfo**, [**InprocServers**](inprocservers.md), [**PropertyInfo**](propertyinfo.md), [**RelatedCollectionInfo**](relatedcollectioninfo.md), [**Root**](root.md), and [**WOWInprocServers**](wowinprocservers.md).</span></span>

## <a name="properties"></a><span data-ttu-id="76ea5-115">屬性</span><span class="sxs-lookup"><span data-stu-id="76ea5-115">Properties</span></span>

<span data-ttu-id="76ea5-116">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="76ea5-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="76ea5-117">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="76ea5-117">ErrorCode</span></span>](#errorcode)
-   [<span data-ttu-id="76ea5-118">MajorRef</span><span class="sxs-lookup"><span data-stu-id="76ea5-118">MajorRef</span></span>](#majorref)
-   [<span data-ttu-id="76ea5-119">MinorRef</span><span class="sxs-lookup"><span data-stu-id="76ea5-119">MinorRef</span></span>](#minorref)
-   [<span data-ttu-id="76ea5-120">名稱</span><span class="sxs-lookup"><span data-stu-id="76ea5-120">Name</span></span>](#name)

### <a name="errorcode"></a><span data-ttu-id="76ea5-121">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="76ea5-121">ErrorCode</span></span>



| <span data-ttu-id="76ea5-122">進入</span><span class="sxs-lookup"><span data-stu-id="76ea5-122">Entry</span></span> | <span data-ttu-id="76ea5-123">值</span><span class="sxs-lookup"><span data-stu-id="76ea5-123">Value</span></span> |
|----------------|----------------------------------------|
| <span data-ttu-id="76ea5-124">描述</span><span class="sxs-lookup"><span data-stu-id="76ea5-124">Description</span></span>    | <span data-ttu-id="76ea5-125">物件或檔案的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="76ea5-125">The error code for the object or file.</span></span> |
| <span data-ttu-id="76ea5-126">Access</span><span class="sxs-lookup"><span data-stu-id="76ea5-126">Access</span></span>         | <span data-ttu-id="76ea5-127">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="76ea5-127">ReadOnly</span></span>                               |
| <span data-ttu-id="76ea5-128">類型</span><span class="sxs-lookup"><span data-stu-id="76ea5-128">Type</span></span>           | <span data-ttu-id="76ea5-129">String</span><span class="sxs-lookup"><span data-stu-id="76ea5-129">String</span></span>                                 |
| <span data-ttu-id="76ea5-130">預設</span><span class="sxs-lookup"><span data-stu-id="76ea5-130">Default</span></span>        | <span data-ttu-id="76ea5-131">None</span><span class="sxs-lookup"><span data-stu-id="76ea5-131">None</span></span>                                   |
| <span data-ttu-id="76ea5-132">最小系統</span><span class="sxs-lookup"><span data-stu-id="76ea5-132">Minimum system</span></span> | <span data-ttu-id="76ea5-133">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="76ea5-133">Windows 2000</span></span>                           |



 

### <a name="majorref"></a><span data-ttu-id="76ea5-134">MajorRef</span><span class="sxs-lookup"><span data-stu-id="76ea5-134">MajorRef</span></span>



| <span data-ttu-id="76ea5-135">進入</span><span class="sxs-lookup"><span data-stu-id="76ea5-135">Entry</span></span> | <span data-ttu-id="76ea5-136">值</span><span class="sxs-lookup"><span data-stu-id="76ea5-136">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76ea5-137">描述</span><span class="sxs-lookup"><span data-stu-id="76ea5-137">Description</span></span>    | <span data-ttu-id="76ea5-138">發生錯誤之物件的索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 屬性值。</span><span class="sxs-lookup"><span data-stu-id="76ea5-138">The [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property value for the object that has an error.</span></span> <span data-ttu-id="76ea5-139">例如，如果集合中的特定物件上的 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) 呼叫失敗，則會將該物件的索引 **鍵** 屬性值報告為 MajorRef 值。</span><span class="sxs-lookup"><span data-stu-id="76ea5-139">For example, if a [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) call for a collection fails on a particular object in the collection, the **Key** property value for that object is reported as the MajorRef value.</span></span> <span data-ttu-id="76ea5-140">您可以使用這個屬性來查看無法更新的專案，或找出無法安裝的元件或 DLL。</span><span class="sxs-lookup"><span data-stu-id="76ea5-140">Use this property to look at the item that fails to update or to find the component or DLL that fails to install.</span></span> |
| <span data-ttu-id="76ea5-141">Access</span><span class="sxs-lookup"><span data-stu-id="76ea5-141">Access</span></span>         | <span data-ttu-id="76ea5-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="76ea5-142">ReadOnly</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="76ea5-143">類型</span><span class="sxs-lookup"><span data-stu-id="76ea5-143">Type</span></span>           | <span data-ttu-id="76ea5-144">String</span><span class="sxs-lookup"><span data-stu-id="76ea5-144">String</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="76ea5-145">預設</span><span class="sxs-lookup"><span data-stu-id="76ea5-145">Default</span></span>        | <span data-ttu-id="76ea5-146">None</span><span class="sxs-lookup"><span data-stu-id="76ea5-146">None</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="76ea5-147">最小系統</span><span class="sxs-lookup"><span data-stu-id="76ea5-147">Minimum system</span></span> | <span data-ttu-id="76ea5-148">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="76ea5-148">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="minorref"></a><span data-ttu-id="76ea5-149">MinorRef</span><span class="sxs-lookup"><span data-stu-id="76ea5-149">MinorRef</span></span>



| <span data-ttu-id="76ea5-150">進入</span><span class="sxs-lookup"><span data-stu-id="76ea5-150">Entry</span></span> | <span data-ttu-id="76ea5-151">值</span><span class="sxs-lookup"><span data-stu-id="76ea5-151">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76ea5-152">描述</span><span class="sxs-lookup"><span data-stu-id="76ea5-152">Description</span></span>    | <span data-ttu-id="76ea5-153">具有錯誤之專案的精確規格，例如屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="76ea5-153">A precise specification of the item that has an error, such as a property name.</span></span> <span data-ttu-id="76ea5-154">如果發生多個錯誤，或在不適用的內容中，MinorRef 為 <Invalid> 。</span><span class="sxs-lookup"><span data-stu-id="76ea5-154">If multiple errors occur or in contexts in which this doesn't apply, MinorRef is <Invalid>.</span></span> |
| <span data-ttu-id="76ea5-155">Access</span><span class="sxs-lookup"><span data-stu-id="76ea5-155">Access</span></span>         | <span data-ttu-id="76ea5-156">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="76ea5-156">ReadOnly</span></span>                                                                                                                                                                          |
| <span data-ttu-id="76ea5-157">類型</span><span class="sxs-lookup"><span data-stu-id="76ea5-157">Type</span></span>           | <span data-ttu-id="76ea5-158">String</span><span class="sxs-lookup"><span data-stu-id="76ea5-158">String</span></span>                                                                                                                                                                            |
| <span data-ttu-id="76ea5-159">預設</span><span class="sxs-lookup"><span data-stu-id="76ea5-159">Default</span></span>        | <span data-ttu-id="76ea5-160">None</span><span class="sxs-lookup"><span data-stu-id="76ea5-160">None</span></span>                                                                                                                                                                              |
| <span data-ttu-id="76ea5-161">最小系統</span><span class="sxs-lookup"><span data-stu-id="76ea5-161">Minimum system</span></span> | <span data-ttu-id="76ea5-162">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="76ea5-162">Windows 2000</span></span>                                                                                                                                                                      |



 

### <a name="name"></a><span data-ttu-id="76ea5-163">Name</span><span class="sxs-lookup"><span data-stu-id="76ea5-163">Name</span></span>



| <span data-ttu-id="76ea5-164">進入</span><span class="sxs-lookup"><span data-stu-id="76ea5-164">Entry</span></span> | <span data-ttu-id="76ea5-165">值</span><span class="sxs-lookup"><span data-stu-id="76ea5-165">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76ea5-166">描述</span><span class="sxs-lookup"><span data-stu-id="76ea5-166">Description</span></span>    | <span data-ttu-id="76ea5-167">有錯誤的物件或檔案名。</span><span class="sxs-lookup"><span data-stu-id="76ea5-167">The name of the object or file that has an error.</span></span> <span data-ttu-id="76ea5-168">當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 或 [**名稱**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="76ea5-168">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="76ea5-169">Access</span><span class="sxs-lookup"><span data-stu-id="76ea5-169">Access</span></span>         | <span data-ttu-id="76ea5-170">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="76ea5-170">ReadOnly</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="76ea5-171">類型</span><span class="sxs-lookup"><span data-stu-id="76ea5-171">Type</span></span>           | <span data-ttu-id="76ea5-172">String</span><span class="sxs-lookup"><span data-stu-id="76ea5-172">String</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="76ea5-173">預設</span><span class="sxs-lookup"><span data-stu-id="76ea5-173">Default</span></span>        | <span data-ttu-id="76ea5-174">None</span><span class="sxs-lookup"><span data-stu-id="76ea5-174">None</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="76ea5-175">最小系統</span><span class="sxs-lookup"><span data-stu-id="76ea5-175">Minimum system</span></span> | <span data-ttu-id="76ea5-176">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="76ea5-176">Windows 2000</span></span>                                                                                                                                                                                                             |



 

## <a name="see-also"></a><span data-ttu-id="76ea5-177">另請參閱</span><span class="sxs-lookup"><span data-stu-id="76ea5-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76ea5-178">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="76ea5-178">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
