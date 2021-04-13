---
description: 包含在64位電腦上向系統註冊32位元件的同進程伺服器清單。 它包含每個元件的物件。
ms.assetid: 4dbcf059-b09b-4a65-95c9-3a4735c252c3
title: WOWInprocServers 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWInprocServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 43fceababaf6ced44a1ba3aef020900ed1afe4df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510470"
---
# <a name="wowinprocservers-collection"></a><span data-ttu-id="ac64a-104">WOWInprocServers 集合</span><span class="sxs-lookup"><span data-stu-id="ac64a-104">WOWInprocServers collection</span></span>

<span data-ttu-id="ac64a-105">包含在64位電腦上向系統註冊32位元件的同進程伺服器清單。</span><span class="sxs-lookup"><span data-stu-id="ac64a-105">Contains a list of the in-process servers registered with the system for 32-bit components on 64-bit computers.</span></span> <span data-ttu-id="ac64a-106">它包含每個元件的物件。</span><span class="sxs-lookup"><span data-stu-id="ac64a-106">It contains an object for each component.</span></span>

<span data-ttu-id="ac64a-107">此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法，但不支援 [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)方法。</span><span class="sxs-lookup"><span data-stu-id="ac64a-107">This collection supports the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, but not the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) method.</span></span> <span data-ttu-id="ac64a-108">若要安裝或匯入元件到應用程式，請在 [**COMAdminCatalog**](comadmincatalog.md) 物件上使用方法。</span><span class="sxs-lookup"><span data-stu-id="ac64a-108">To install or import components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="ac64a-109">成員</span><span class="sxs-lookup"><span data-stu-id="ac64a-109">Members</span></span>

<span data-ttu-id="ac64a-110">**WOWInprocServers** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="ac64a-110">The **WOWInprocServers** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="ac64a-111">相關集合</span><span class="sxs-lookup"><span data-stu-id="ac64a-111">Related Collections</span></span>

<span data-ttu-id="ac64a-112">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="ac64a-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="ac64a-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="ac64a-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="ac64a-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="ac64a-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="ac64a-115">您可以從下列集合流覽至這個集合：</span><span class="sxs-lookup"><span data-stu-id="ac64a-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="ac64a-116">**根**</span><span class="sxs-lookup"><span data-stu-id="ac64a-116">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="ac64a-117">屬性</span><span class="sxs-lookup"><span data-stu-id="ac64a-117">Properties</span></span>

<span data-ttu-id="ac64a-118">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="ac64a-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="ac64a-119">Clsid</span><span class="sxs-lookup"><span data-stu-id="ac64a-119">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="ac64a-120">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="ac64a-120">InprocServer32</span></span>](#inprocserver32)
-   [<span data-ttu-id="ac64a-121">ProgID</span><span class="sxs-lookup"><span data-stu-id="ac64a-121">ProgID</span></span>](#progid)

### <a name="clsid"></a><span data-ttu-id="ac64a-122">CLSID</span><span class="sxs-lookup"><span data-stu-id="ac64a-122">CLSID</span></span>



| <span data-ttu-id="ac64a-123">進入</span><span class="sxs-lookup"><span data-stu-id="ac64a-123">Entry</span></span> | <span data-ttu-id="ac64a-124">值</span><span class="sxs-lookup"><span data-stu-id="ac64a-124">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac64a-125">描述</span><span class="sxs-lookup"><span data-stu-id="ac64a-125">Description</span></span>    | <span data-ttu-id="ac64a-126">元件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="ac64a-126">A GUID for the component.</span></span> <span data-ttu-id="ac64a-127">當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="ac64a-127">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="ac64a-128">Access</span><span class="sxs-lookup"><span data-stu-id="ac64a-128">Access</span></span>         | <span data-ttu-id="ac64a-129">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ac64a-129">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="ac64a-130">類型</span><span class="sxs-lookup"><span data-stu-id="ac64a-130">Type</span></span>           | <span data-ttu-id="ac64a-131">String</span><span class="sxs-lookup"><span data-stu-id="ac64a-131">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="ac64a-132">預設值</span><span class="sxs-lookup"><span data-stu-id="ac64a-132">Default</span></span>        | <span data-ttu-id="ac64a-133">N/A</span><span class="sxs-lookup"><span data-stu-id="ac64a-133">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="ac64a-134">最小系統</span><span class="sxs-lookup"><span data-stu-id="ac64a-134">Minimum system</span></span> | <span data-ttu-id="ac64a-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ac64a-135">Windows XP</span></span>                                                                                                                                                |



 

### <a name="inprocserver32"></a><span data-ttu-id="ac64a-136">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="ac64a-136">InprocServer32</span></span>



| <span data-ttu-id="ac64a-137">進入</span><span class="sxs-lookup"><span data-stu-id="ac64a-137">Entry</span></span> | <span data-ttu-id="ac64a-138">值</span><span class="sxs-lookup"><span data-stu-id="ac64a-138">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="ac64a-139">描述</span><span class="sxs-lookup"><span data-stu-id="ac64a-139">Description</span></span>    | <span data-ttu-id="ac64a-140">元件的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="ac64a-140">The file path for the component.</span></span> |
| <span data-ttu-id="ac64a-141">Access</span><span class="sxs-lookup"><span data-stu-id="ac64a-141">Access</span></span>         | <span data-ttu-id="ac64a-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ac64a-142">ReadOnly</span></span>                         |
| <span data-ttu-id="ac64a-143">類型</span><span class="sxs-lookup"><span data-stu-id="ac64a-143">Type</span></span>           | <span data-ttu-id="ac64a-144">String</span><span class="sxs-lookup"><span data-stu-id="ac64a-144">String</span></span>                           |
| <span data-ttu-id="ac64a-145">預設值</span><span class="sxs-lookup"><span data-stu-id="ac64a-145">Default</span></span>        | <span data-ttu-id="ac64a-146">N/A</span><span class="sxs-lookup"><span data-stu-id="ac64a-146">N/A</span></span>                              |
| <span data-ttu-id="ac64a-147">最小系統</span><span class="sxs-lookup"><span data-stu-id="ac64a-147">Minimum system</span></span> | <span data-ttu-id="ac64a-148">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ac64a-148">Windows XP</span></span>                       |



 

### <a name="progid"></a><span data-ttu-id="ac64a-149">ProgID</span><span class="sxs-lookup"><span data-stu-id="ac64a-149">ProgID</span></span>



| <span data-ttu-id="ac64a-150">進入</span><span class="sxs-lookup"><span data-stu-id="ac64a-150">Entry</span></span> | <span data-ttu-id="ac64a-151">值</span><span class="sxs-lookup"><span data-stu-id="ac64a-151">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac64a-152">描述</span><span class="sxs-lookup"><span data-stu-id="ac64a-152">Description</span></span>    | <span data-ttu-id="ac64a-153">識別元件的名稱。</span><span class="sxs-lookup"><span data-stu-id="ac64a-153">A name identifying the component.</span></span> <span data-ttu-id="ac64a-154">在這個集合的物件上呼叫 [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="ac64a-154">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="ac64a-155">Access</span><span class="sxs-lookup"><span data-stu-id="ac64a-155">Access</span></span>         | <span data-ttu-id="ac64a-156">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ac64a-156">ReadOnly</span></span>                                                                                                                                                            |
| <span data-ttu-id="ac64a-157">類型</span><span class="sxs-lookup"><span data-stu-id="ac64a-157">Type</span></span>           | <span data-ttu-id="ac64a-158">String</span><span class="sxs-lookup"><span data-stu-id="ac64a-158">String</span></span>                                                                                                                                                              |
| <span data-ttu-id="ac64a-159">預設值</span><span class="sxs-lookup"><span data-stu-id="ac64a-159">Default</span></span>        | <span data-ttu-id="ac64a-160">N/A</span><span class="sxs-lookup"><span data-stu-id="ac64a-160">N/A</span></span>                                                                                                                                                                 |
| <span data-ttu-id="ac64a-161">最小系統</span><span class="sxs-lookup"><span data-stu-id="ac64a-161">Minimum system</span></span> | <span data-ttu-id="ac64a-162">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ac64a-162">Windows XP</span></span>                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="ac64a-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac64a-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac64a-164">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="ac64a-164">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
