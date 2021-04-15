---
description: 包含 DCOM 要使用的通訊協定清單。 它包含每個通訊協定的物件。
ms.assetid: f553ce01-39b6-4dc3-9696-978b390a5c7d
title: DCOMProtocols 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DCOMProtocols
api_type:
- COM
api_location: ''
ms.openlocfilehash: 705940dae0f7ebe885db4c295714df538c56c705
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468193"
---
# <a name="dcomprotocols-collection"></a><span data-ttu-id="307f0-104">DCOMProtocols 集合</span><span class="sxs-lookup"><span data-stu-id="307f0-104">DCOMProtocols collection</span></span>

<span data-ttu-id="307f0-105">包含 DCOM 要使用的通訊協定清單。</span><span class="sxs-lookup"><span data-stu-id="307f0-105">Contains a list of the protocols to be used by DCOM.</span></span> <span data-ttu-id="307f0-106">它包含每個通訊協定的物件。</span><span class="sxs-lookup"><span data-stu-id="307f0-106">It contains an object for each protocol.</span></span>

<span data-ttu-id="307f0-107">此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。</span><span class="sxs-lookup"><span data-stu-id="307f0-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="307f0-108">成員</span><span class="sxs-lookup"><span data-stu-id="307f0-108">Members</span></span>

<span data-ttu-id="307f0-109">**DCOMProtocols** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="307f0-109">The **DCOMProtocols** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="307f0-110">相關集合</span><span class="sxs-lookup"><span data-stu-id="307f0-110">Related Collections</span></span>

<span data-ttu-id="307f0-111">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="307f0-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="307f0-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="307f0-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="307f0-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="307f0-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="307f0-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="307f0-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="307f0-115">您可以從下列集合流覽至這個集合：</span><span class="sxs-lookup"><span data-stu-id="307f0-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="307f0-116">**根**</span><span class="sxs-lookup"><span data-stu-id="307f0-116">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="307f0-117">屬性</span><span class="sxs-lookup"><span data-stu-id="307f0-117">Properties</span></span>

<span data-ttu-id="307f0-118">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="307f0-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="307f0-119">名稱</span><span class="sxs-lookup"><span data-stu-id="307f0-119">Name</span></span>](#name)
-   [<span data-ttu-id="307f0-120">順序</span><span class="sxs-lookup"><span data-stu-id="307f0-120">Order</span></span>](#order)
-   [<span data-ttu-id="307f0-121">ProtocolCode</span><span class="sxs-lookup"><span data-stu-id="307f0-121">ProtocolCode</span></span>](#protocolcode)

### <a name="name"></a><span data-ttu-id="307f0-122">Name</span><span class="sxs-lookup"><span data-stu-id="307f0-122">Name</span></span>



| <span data-ttu-id="307f0-123">進入</span><span class="sxs-lookup"><span data-stu-id="307f0-123">Entry</span></span> | <span data-ttu-id="307f0-124">值</span><span class="sxs-lookup"><span data-stu-id="307f0-124">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307f0-125">描述</span><span class="sxs-lookup"><span data-stu-id="307f0-125">Description</span></span>    | <span data-ttu-id="307f0-126">通訊協定的名稱。</span><span class="sxs-lookup"><span data-stu-id="307f0-126">The name of the protocol.</span></span> <span data-ttu-id="307f0-127">在這個集合的物件上呼叫 [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="307f0-127">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="307f0-128">Access</span><span class="sxs-lookup"><span data-stu-id="307f0-128">Access</span></span>         | <span data-ttu-id="307f0-129">讀寫</span><span class="sxs-lookup"><span data-stu-id="307f0-129">ReadWrite</span></span>                                                                                                                                                   |
| <span data-ttu-id="307f0-130">類型</span><span class="sxs-lookup"><span data-stu-id="307f0-130">Type</span></span>           | <span data-ttu-id="307f0-131">String</span><span class="sxs-lookup"><span data-stu-id="307f0-131">String</span></span>                                                                                                                                                      |
| <span data-ttu-id="307f0-132">預設值</span><span class="sxs-lookup"><span data-stu-id="307f0-132">Default</span></span>        | <span data-ttu-id="307f0-133">「新的通訊協定」</span><span class="sxs-lookup"><span data-stu-id="307f0-133">"New Protocol"</span></span>                                                                                                                                              |
| <span data-ttu-id="307f0-134">最小系統</span><span class="sxs-lookup"><span data-stu-id="307f0-134">Minimum system</span></span> | <span data-ttu-id="307f0-135">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307f0-135">Windows 2000</span></span>                                                                                                                                                |



 

### <a name="order"></a><span data-ttu-id="307f0-136">單</span><span class="sxs-lookup"><span data-stu-id="307f0-136">Order</span></span>



| <span data-ttu-id="307f0-137">進入</span><span class="sxs-lookup"><span data-stu-id="307f0-137">Entry</span></span> | <span data-ttu-id="307f0-138">值</span><span class="sxs-lookup"><span data-stu-id="307f0-138">Value</span></span> |
|----------------|-----------------------------------------|
| <span data-ttu-id="307f0-139">描述</span><span class="sxs-lookup"><span data-stu-id="307f0-139">Description</span></span>    | <span data-ttu-id="307f0-140">嘗試通訊協定的順序。</span><span class="sxs-lookup"><span data-stu-id="307f0-140">The order in which to try the protocol.</span></span> |
| <span data-ttu-id="307f0-141">Access</span><span class="sxs-lookup"><span data-stu-id="307f0-141">Access</span></span>         | <span data-ttu-id="307f0-142">讀寫</span><span class="sxs-lookup"><span data-stu-id="307f0-142">ReadWrite</span></span>                               |
| <span data-ttu-id="307f0-143">類型</span><span class="sxs-lookup"><span data-stu-id="307f0-143">Type</span></span>           | <span data-ttu-id="307f0-144">Long (0-65000) </span><span class="sxs-lookup"><span data-stu-id="307f0-144">Long (0-65000)</span></span>                          |
| <span data-ttu-id="307f0-145">預設</span><span class="sxs-lookup"><span data-stu-id="307f0-145">Default</span></span>        | <span data-ttu-id="307f0-146">0</span><span class="sxs-lookup"><span data-stu-id="307f0-146">0</span></span>                                       |
| <span data-ttu-id="307f0-147">最小系統</span><span class="sxs-lookup"><span data-stu-id="307f0-147">Minimum system</span></span> | <span data-ttu-id="307f0-148">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307f0-148">Windows 2000</span></span>                            |



 

### <a name="protocolcode"></a><span data-ttu-id="307f0-149">ProtocolCode</span><span class="sxs-lookup"><span data-stu-id="307f0-149">ProtocolCode</span></span>



| <span data-ttu-id="307f0-150">進入</span><span class="sxs-lookup"><span data-stu-id="307f0-150">Entry</span></span> | <span data-ttu-id="307f0-151">值</span><span class="sxs-lookup"><span data-stu-id="307f0-151">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307f0-152">描述</span><span class="sxs-lookup"><span data-stu-id="307f0-152">Description</span></span>    | <span data-ttu-id="307f0-153">指定 RPC 通訊協定序列的程式碼。</span><span class="sxs-lookup"><span data-stu-id="307f0-153">The code specifying the RPC protocol sequence.</span></span> <span data-ttu-id="307f0-154">支援的通訊協定代碼包含下列各項： ncacn \_ ip \_ tcp、ncacn \_ HTTP、ncacn \_ spx。</span><span class="sxs-lookup"><span data-stu-id="307f0-154">The supported protocol codes include the following: ncacn\_ip\_tcp, ncacn\_http, ncacn\_spx.</span></span> <span data-ttu-id="307f0-155">當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="307f0-155">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="307f0-156">Access</span><span class="sxs-lookup"><span data-stu-id="307f0-156">Access</span></span>         | <span data-ttu-id="307f0-157">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="307f0-157">WriteOnce</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="307f0-158">類型</span><span class="sxs-lookup"><span data-stu-id="307f0-158">Type</span></span>           | <span data-ttu-id="307f0-159">String</span><span class="sxs-lookup"><span data-stu-id="307f0-159">String</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="307f0-160">預設值</span><span class="sxs-lookup"><span data-stu-id="307f0-160">Default</span></span>        | <span data-ttu-id="307f0-161">""</span><span class="sxs-lookup"><span data-stu-id="307f0-161">""</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="307f0-162">最小系統</span><span class="sxs-lookup"><span data-stu-id="307f0-162">Minimum system</span></span> | <span data-ttu-id="307f0-163">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="307f0-163">Windows 2000</span></span>                                                                                                                                                                                                                                                                |



 

## <a name="see-also"></a><span data-ttu-id="307f0-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="307f0-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="307f0-165">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="307f0-165">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
