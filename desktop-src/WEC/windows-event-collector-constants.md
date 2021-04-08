---
title: 'Windows 事件收集器常數 (Evcoll .h) '
description: Windows 事件收集器 SDK 包含下列常數。
ms.assetid: 2ba862f9-6849-43b3-8914-e18ede1d63c0
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- EC_VARIANT_TYPE_MASK
- EC_VARIANT_TYPE_ARRAY
- EC_READ_ACCESS
- EC_WRITE_ACCESS
- EC_OPEN_ALWAYS
- EC_CREATE_NEW
- EC_OPEN_EXISTING
api_location:
- Evcoll.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf6e7e99186e2148bf6ec3400aadf760a79a2331
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685468"
---
# <a name="windows-event-collector-constants"></a><span data-ttu-id="42b77-103">Windows 事件收集器常數</span><span class="sxs-lookup"><span data-stu-id="42b77-103">Windows Event Collector Constants</span></span>

<span data-ttu-id="42b77-104">Windows 事件收集器 SDK 包含下列常數。</span><span class="sxs-lookup"><span data-stu-id="42b77-104">The Windows Event Collector SDK contains the following constants.</span></span>

<dl> <dt>

<span data-ttu-id="42b77-105"><span id="EC_VARIANT_TYPE_MASK"></span><span id="ec_variant_type_mask"></span>**EC \_ VARIANT \_ 類型 \_ 遮罩**</span><span class="sxs-lookup"><span data-stu-id="42b77-105"><span id="EC_VARIANT_TYPE_MASK"></span><span id="ec_variant_type_mask"></span>**EC\_VARIANT\_TYPE\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42b77-106">0x7f</span><span class="sxs-lookup"><span data-stu-id="42b77-106">0x7f</span></span>
</dt> <dt>



<span data-ttu-id="42b77-107">用來從 [**EC \_ 變異**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant)的 **type** 屬性中遮罩陣列位，以將變數值的型別解壓縮。</span><span class="sxs-lookup"><span data-stu-id="42b77-107">Used to mask out the array bit from the **Type** property of an [**EC\_VARIANT**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant) to extract the type of the variant value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42b77-108"><span id="EC_VARIANT_TYPE_ARRAY"></span><span id="ec_variant_type_array"></span>**EC \_ VARIANT \_ 類型 \_ 陣列**</span><span class="sxs-lookup"><span data-stu-id="42b77-108"><span id="EC_VARIANT_TYPE_ARRAY"></span><span id="ec_variant_type_array"></span>**EC\_VARIANT\_TYPE\_ARRAY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42b77-109">128 (0x80) </span><span class="sxs-lookup"><span data-stu-id="42b77-109">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="42b77-110">當您在 [**EC \_ 變異**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant)的 **Type** 屬性中設定此位時，變數會包含值陣列的指標，而不是值本身。</span><span class="sxs-lookup"><span data-stu-id="42b77-110">When this bit is set in the **Type** property of an [**EC\_VARIANT**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant), the variant contains a pointer to an array of values, rather than the value itself.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42b77-111"><span id="EC_READ_ACCESS"></span><span id="ec_read_access"></span>**EC \_ 讀取 \_ 許可權**</span><span class="sxs-lookup"><span data-stu-id="42b77-111"><span id="EC_READ_ACCESS"></span><span id="ec_read_access"></span>**EC\_READ\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42b77-112">1</span><span class="sxs-lookup"><span data-stu-id="42b77-112">1</span></span>
</dt> <dt>



<span data-ttu-id="42b77-113">讀取存取控制許可權，允許從事件收集器讀取資訊。</span><span class="sxs-lookup"><span data-stu-id="42b77-113">Read access control permission that allows information to be read from the event collector.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42b77-114"><span id="EC_WRITE_ACCESS"></span><span id="ec_write_access"></span>**EC \_ 寫入 \_ 許可權**</span><span class="sxs-lookup"><span data-stu-id="42b77-114"><span id="EC_WRITE_ACCESS"></span><span id="ec_write_access"></span>**EC\_WRITE\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42b77-115">2</span><span class="sxs-lookup"><span data-stu-id="42b77-115">2</span></span>
</dt> <dt>



<span data-ttu-id="42b77-116">寫入存取控制許可權，允許將資訊寫入事件收集器。</span><span class="sxs-lookup"><span data-stu-id="42b77-116">Write access control permission that allows information to be written to the event collector.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42b77-117"><span id="EC_OPEN_ALWAYS"></span><span id="ec_open_always"></span>**EC \_ \_ 永遠開啟**</span><span class="sxs-lookup"><span data-stu-id="42b77-117"><span id="EC_OPEN_ALWAYS"></span><span id="ec_open_always"></span>**EC\_OPEN\_ALWAYS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42b77-118">0</span><span class="sxs-lookup"><span data-stu-id="42b77-118">0</span></span>
</dt> <dt>



<span data-ttu-id="42b77-119">開啟現有的訂用帳戶，或建立訂用帳戶（如果不存在的話）。</span><span class="sxs-lookup"><span data-stu-id="42b77-119">Opens an existing subscription or creates the subscription if it does not exist.</span></span> <span data-ttu-id="42b77-120">由 [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) 方法所使用。</span><span class="sxs-lookup"><span data-stu-id="42b77-120">Used by the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42b77-121"><span id="EC_CREATE_NEW"></span><span id="ec_create_new"></span>**EC \_ 建立 \_ 新的**</span><span class="sxs-lookup"><span data-stu-id="42b77-121"><span id="EC_CREATE_NEW"></span><span id="ec_create_new"></span>**EC\_CREATE\_NEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42b77-122">1</span><span class="sxs-lookup"><span data-stu-id="42b77-122">1</span></span>
</dt> <dt>



<span data-ttu-id="42b77-123">傳遞至 [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) 函數的旗標，指定應建立新的訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="42b77-123">A flag passed to the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) function specifying that a new subscription should be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42b77-124"><span id="EC_OPEN_EXISTING"></span><span id="ec_open_existing"></span>**EC \_ 開啟 \_ 現有的**</span><span class="sxs-lookup"><span data-stu-id="42b77-124"><span id="EC_OPEN_EXISTING"></span><span id="ec_open_existing"></span>**EC\_OPEN\_EXISTING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42b77-125">2</span><span class="sxs-lookup"><span data-stu-id="42b77-125">2</span></span>
</dt> <dt>



<span data-ttu-id="42b77-126">傳遞至 [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) 函數的旗標，指定應開啟現有的訂閱。</span><span class="sxs-lookup"><span data-stu-id="42b77-126">A flag passed to the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) function specifying that an existing subscription should be opened.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="42b77-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="42b77-127">Requirements</span></span>



| <span data-ttu-id="42b77-128">需求</span><span class="sxs-lookup"><span data-stu-id="42b77-128">Requirement</span></span> | <span data-ttu-id="42b77-129">值</span><span class="sxs-lookup"><span data-stu-id="42b77-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="42b77-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="42b77-130">Minimum supported client</span></span><br/> | <span data-ttu-id="42b77-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="42b77-131">Windows Vista</span></span><br/>                                                            |
| <span data-ttu-id="42b77-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="42b77-132">Minimum supported server</span></span><br/> | <span data-ttu-id="42b77-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42b77-133">Windows Server 2008</span></span><br/>                                                      |
| <span data-ttu-id="42b77-134">標頭</span><span class="sxs-lookup"><span data-stu-id="42b77-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="42b77-135"><dt>Evcoll。h</dt></span><span class="sxs-lookup"><span data-stu-id="42b77-135"><dt>Evcoll.h</dt></span></span> </dl> |



 

 





