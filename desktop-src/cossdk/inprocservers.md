---
description: 包含向系統註冊的同進程伺服器清單。 它包含每個元件的物件，該物件會註冊為同進程伺服器。
ms.assetid: 10434de7-c5e3-4fb0-8472-2a581607fcc0
title: InprocServers 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InprocServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 737627c99ac92a96883750bfc43dc3e2a9364d87
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973568"
---
# <a name="inprocservers-collection"></a><span data-ttu-id="887cb-104">InprocServers 集合</span><span class="sxs-lookup"><span data-stu-id="887cb-104">InprocServers collection</span></span>

<span data-ttu-id="887cb-105">包含向系統註冊的同進程伺服器清單。</span><span class="sxs-lookup"><span data-stu-id="887cb-105">Contains a list of the in-process servers registered with the system.</span></span> <span data-ttu-id="887cb-106">它包含每個元件的物件，該物件會註冊為同進程伺服器。</span><span class="sxs-lookup"><span data-stu-id="887cb-106">It contains an object for each component that is registered as an in-process server.</span></span>

<span data-ttu-id="887cb-107">此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法，但不支援 [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)方法。</span><span class="sxs-lookup"><span data-stu-id="887cb-107">This collection supports the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, but not the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) method.</span></span> <span data-ttu-id="887cb-108">若要安裝或匯入元件到應用程式，請在 [**COMAdminCatalog**](comadmincatalog.md) 物件上使用方法。</span><span class="sxs-lookup"><span data-stu-id="887cb-108">To install or import components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="887cb-109">成員</span><span class="sxs-lookup"><span data-stu-id="887cb-109">Members</span></span>

<span data-ttu-id="887cb-110">**InprocServers** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="887cb-110">The **InprocServers** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="887cb-111">相關集合</span><span class="sxs-lookup"><span data-stu-id="887cb-111">Related Collections</span></span>

<span data-ttu-id="887cb-112">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="887cb-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="887cb-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="887cb-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="887cb-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="887cb-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="887cb-115">您可以從下列集合流覽至這個集合：</span><span class="sxs-lookup"><span data-stu-id="887cb-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="887cb-116">**根**</span><span class="sxs-lookup"><span data-stu-id="887cb-116">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="887cb-117">屬性</span><span class="sxs-lookup"><span data-stu-id="887cb-117">Properties</span></span>

<span data-ttu-id="887cb-118">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="887cb-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="887cb-119">Clsid</span><span class="sxs-lookup"><span data-stu-id="887cb-119">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="887cb-120">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="887cb-120">InprocServer32</span></span>](#inprocserver32)
-   [<span data-ttu-id="887cb-121">ProgID</span><span class="sxs-lookup"><span data-stu-id="887cb-121">ProgID</span></span>](#progid)

### <a name="clsid"></a><span data-ttu-id="887cb-122">CLSID</span><span class="sxs-lookup"><span data-stu-id="887cb-122">CLSID</span></span>



| <span data-ttu-id="887cb-123">進入</span><span class="sxs-lookup"><span data-stu-id="887cb-123">Entry</span></span> | <span data-ttu-id="887cb-124">值</span><span class="sxs-lookup"><span data-stu-id="887cb-124">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="887cb-125">描述</span><span class="sxs-lookup"><span data-stu-id="887cb-125">Description</span></span>    | <span data-ttu-id="887cb-126">元件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="887cb-126">A GUID for the component.</span></span> <span data-ttu-id="887cb-127">當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="887cb-127">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="887cb-128">Access</span><span class="sxs-lookup"><span data-stu-id="887cb-128">Access</span></span>         | <span data-ttu-id="887cb-129">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="887cb-129">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="887cb-130">類型</span><span class="sxs-lookup"><span data-stu-id="887cb-130">Type</span></span>           | <span data-ttu-id="887cb-131">String</span><span class="sxs-lookup"><span data-stu-id="887cb-131">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="887cb-132">預設值</span><span class="sxs-lookup"><span data-stu-id="887cb-132">Default</span></span>        | <span data-ttu-id="887cb-133">N/A</span><span class="sxs-lookup"><span data-stu-id="887cb-133">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="887cb-134">最小系統</span><span class="sxs-lookup"><span data-stu-id="887cb-134">Minimum system</span></span> | <span data-ttu-id="887cb-135">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="887cb-135">Windows 2000</span></span>                                                                                                                                              |



 

### <a name="inprocserver32"></a><span data-ttu-id="887cb-136">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="887cb-136">InprocServer32</span></span>



| <span data-ttu-id="887cb-137">進入</span><span class="sxs-lookup"><span data-stu-id="887cb-137">Entry</span></span> | <span data-ttu-id="887cb-138">值</span><span class="sxs-lookup"><span data-stu-id="887cb-138">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="887cb-139">描述</span><span class="sxs-lookup"><span data-stu-id="887cb-139">Description</span></span>    | <span data-ttu-id="887cb-140">元件的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="887cb-140">The file path for the component.</span></span> |
| <span data-ttu-id="887cb-141">Access</span><span class="sxs-lookup"><span data-stu-id="887cb-141">Access</span></span>         | <span data-ttu-id="887cb-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="887cb-142">ReadOnly</span></span>                         |
| <span data-ttu-id="887cb-143">類型</span><span class="sxs-lookup"><span data-stu-id="887cb-143">Type</span></span>           | <span data-ttu-id="887cb-144">String</span><span class="sxs-lookup"><span data-stu-id="887cb-144">String</span></span>                           |
| <span data-ttu-id="887cb-145">預設值</span><span class="sxs-lookup"><span data-stu-id="887cb-145">Default</span></span>        | <span data-ttu-id="887cb-146">N/A</span><span class="sxs-lookup"><span data-stu-id="887cb-146">N/A</span></span>                              |
| <span data-ttu-id="887cb-147">最小系統</span><span class="sxs-lookup"><span data-stu-id="887cb-147">Minimum system</span></span> | <span data-ttu-id="887cb-148">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="887cb-148">Windows 2000</span></span>                     |



 

### <a name="progid"></a><span data-ttu-id="887cb-149">ProgID</span><span class="sxs-lookup"><span data-stu-id="887cb-149">ProgID</span></span>



| <span data-ttu-id="887cb-150">進入</span><span class="sxs-lookup"><span data-stu-id="887cb-150">Entry</span></span> | <span data-ttu-id="887cb-151">值</span><span class="sxs-lookup"><span data-stu-id="887cb-151">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="887cb-152">描述</span><span class="sxs-lookup"><span data-stu-id="887cb-152">Description</span></span>    | <span data-ttu-id="887cb-153">識別元件的名稱。</span><span class="sxs-lookup"><span data-stu-id="887cb-153">A name identifying the component.</span></span> <span data-ttu-id="887cb-154">在這個集合的物件上呼叫 [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="887cb-154">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="887cb-155">Access</span><span class="sxs-lookup"><span data-stu-id="887cb-155">Access</span></span>         | <span data-ttu-id="887cb-156">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="887cb-156">ReadOnly</span></span>                                                                                                                                                            |
| <span data-ttu-id="887cb-157">類型</span><span class="sxs-lookup"><span data-stu-id="887cb-157">Type</span></span>           | <span data-ttu-id="887cb-158">String</span><span class="sxs-lookup"><span data-stu-id="887cb-158">String</span></span>                                                                                                                                                              |
| <span data-ttu-id="887cb-159">預設值</span><span class="sxs-lookup"><span data-stu-id="887cb-159">Default</span></span>        | <span data-ttu-id="887cb-160">N/A</span><span class="sxs-lookup"><span data-stu-id="887cb-160">N/A</span></span>                                                                                                                                                                 |
| <span data-ttu-id="887cb-161">最小系統</span><span class="sxs-lookup"><span data-stu-id="887cb-161">Minimum system</span></span> | <span data-ttu-id="887cb-162">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="887cb-162">Windows 2000</span></span>                                                                                                                                                        |



 

## <a name="see-also"></a><span data-ttu-id="887cb-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="887cb-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="887cb-164">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="887cb-164">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
