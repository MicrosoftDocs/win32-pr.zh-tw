---
description: 持續追蹤從父要求產生的子要求。
ms.assetid: e1d98eae-6fc1-489b-aa8b-2e86bac5c65a
ms.tgt_platform: multiple
title: 'IWbemCausalityAccess 介面 (Wbemint .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: db4c7a76b04b659cd467f7a4a7a9a8c1ba42721f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978279"
---
# <a name="iwbemcausalityaccess-interface"></a><span data-ttu-id="d314f-103">IWbemCausalityAccess 介面</span><span class="sxs-lookup"><span data-stu-id="d314f-103">IWbemCausalityAccess interface</span></span>

<span data-ttu-id="d314f-104">**IWbemCausalityAccess** 介面會持續追蹤從父要求產生的子要求。</span><span class="sxs-lookup"><span data-stu-id="d314f-104">The **IWbemCausalityAccess** interface keeps track of child requests that are generated from a parent request.</span></span> <span data-ttu-id="d314f-105">您可以針對 [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)使用 (QI) 的查詢介面，來取得 **IWbemCausalityAccess** 物件。</span><span class="sxs-lookup"><span data-stu-id="d314f-105">You can obtain an **IWbemCausalityAccess** object by using a query interface (QI) for [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext).</span></span> <span data-ttu-id="d314f-106">每個要求都是由全域唯一識別碼 (GUID) 來識別，而且可以有父要求或可能是最上層要求。</span><span class="sxs-lookup"><span data-stu-id="d314f-106">Each request is identified by a Globally Unique Identifier (GUID) and can have a parent request or can be a top request.</span></span> <span data-ttu-id="d314f-107">GUID 是唯一的128位數位。</span><span class="sxs-lookup"><span data-stu-id="d314f-107">A GUID is a unique 128-bit number.</span></span> <span data-ttu-id="d314f-108">例如，5b2fc63a-8af4-44cb-960c-aefdced908d6。</span><span class="sxs-lookup"><span data-stu-id="d314f-108">For example, 5b2fc63a-8af4-44cb-960c-aefdced908d6.</span></span>

## <a name="members"></a><span data-ttu-id="d314f-109">成員</span><span class="sxs-lookup"><span data-stu-id="d314f-109">Members</span></span>

<span data-ttu-id="d314f-110">**IWbemCausalityAccess** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="d314f-110">The **IWbemCausalityAccess** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d314f-111">**IWbemCausalityAccess** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d314f-111">**IWbemCausalityAccess** also has these types of members:</span></span>

-   [<span data-ttu-id="d314f-112">方法</span><span class="sxs-lookup"><span data-stu-id="d314f-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d314f-113">方法</span><span class="sxs-lookup"><span data-stu-id="d314f-113">Methods</span></span>

<span data-ttu-id="d314f-114">**IWbemCausalityAccess** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d314f-114">The **IWbemCausalityAccess** interface has these methods.</span></span>



| <span data-ttu-id="d314f-115">方法</span><span class="sxs-lookup"><span data-stu-id="d314f-115">Method</span></span>                                                    | <span data-ttu-id="d314f-116">描述</span><span class="sxs-lookup"><span data-stu-id="d314f-116">Description</span></span>                                                                                                                                                             |
|:----------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d314f-117">**GetRequestId**</span><span class="sxs-lookup"><span data-stu-id="d314f-117">**GetRequestId**</span></span>](iwbemcausalityaccess-getrequestid.md) | <span data-ttu-id="d314f-118">傳回要求的唯一 GUID 識別碼。</span><span class="sxs-lookup"><span data-stu-id="d314f-118">Returns a unique GUID identifier for a request.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="d314f-119">**IsChildOf**</span><span class="sxs-lookup"><span data-stu-id="d314f-119">**IsChildOf**</span></span>](iwbemcausalityaccess-ischildof.md)       | <span data-ttu-id="d314f-120">判斷要求是否為指定之父系要求的子系。</span><span class="sxs-lookup"><span data-stu-id="d314f-120">Determines if a request is a child of a specified parent request.</span></span> <span data-ttu-id="d314f-121">父要求可以有多個子要求，每個要求都是由唯一的 GUID 值所識別。</span><span class="sxs-lookup"><span data-stu-id="d314f-121">A parent request can have multiple child requests, each identified by a unique GUID value.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d314f-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="d314f-122">Requirements</span></span>



| <span data-ttu-id="d314f-123">需求</span><span class="sxs-lookup"><span data-stu-id="d314f-123">Requirement</span></span> | <span data-ttu-id="d314f-124">值</span><span class="sxs-lookup"><span data-stu-id="d314f-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d314f-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d314f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d314f-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d314f-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d314f-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d314f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d314f-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d314f-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d314f-129">標頭</span><span class="sxs-lookup"><span data-stu-id="d314f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d314f-130"><dt>Wbemint。h</dt></span><span class="sxs-lookup"><span data-stu-id="d314f-130"><dt>Wbemint.h</dt></span></span> </dl>    |
| <span data-ttu-id="d314f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d314f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d314f-132"><dt>Fastprox.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d314f-132"><dt>Fastprox.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d314f-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d314f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d314f-134">適用于 WMI 的 COM API</span><span class="sxs-lookup"><span data-stu-id="d314f-134">COM API for WMI</span></span>](com-api-for-wmi.md)
</dt> </dl>

 

