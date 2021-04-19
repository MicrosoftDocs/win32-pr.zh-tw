---
description: LINEADDRESSSHARING \_ 位旗標常數描述可在各行之間共用位址的各種方式。
ms.assetid: f37ba549-c8dc-4a7c-bfe6-8e5f733d9750
title: 'LINEADDRESSSHARING_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 785c7e924ffc958d3fe14b739bb2eb28dec322a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977730"
---
# <a name="lineaddresssharing_-constants"></a><span data-ttu-id="b7c1c-103">LINEADDRESSSHARING \_ 常數</span><span class="sxs-lookup"><span data-stu-id="b7c1c-103">LINEADDRESSSHARING\_ Constants</span></span>

<span data-ttu-id="b7c1c-104">**LINEADDRESSSHARING \_** 位旗標常數描述可在各行之間共用位址的各種方式。</span><span class="sxs-lookup"><span data-stu-id="b7c1c-104">The **LINEADDRESSSHARING\_** bit-flag constants describe various ways an address can be shared between lines.</span></span>

<dl> <dt>

<span data-ttu-id="b7c1c-105"><span id="LINEADDRESSSHARING_PRIVATE"></span><span id="lineaddresssharing_private"></span>**LINEADDRESSSHARING \_ 私用**</span><span class="sxs-lookup"><span data-stu-id="b7c1c-105"><span id="LINEADDRESSSHARING_PRIVATE"></span><span id="lineaddresssharing_private"></span>**LINEADDRESSSHARING\_PRIVATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7c1c-106">位址對使用者的行而言是私用的;它不會指派給任何其他工作站。</span><span class="sxs-lookup"><span data-stu-id="b7c1c-106">The address is private to the user's line; it is not assigned to any other station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7c1c-107"><span id="LINEADDRESSSHARING_BRIDGEDEXCL"></span><span id="lineaddresssharing_bridgedexcl"></span>**LINEADDRESSSHARING \_ BRIDGEDEXCL**</span><span class="sxs-lookup"><span data-stu-id="b7c1c-107"><span id="LINEADDRESSSHARING_BRIDGEDEXCL"></span><span id="lineaddresssharing_bridgedexcl"></span>**LINEADDRESSSHARING\_BRIDGEDEXCL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7c1c-108">位址會橋接于一或多個其他工作站。</span><span class="sxs-lookup"><span data-stu-id="b7c1c-108">The address is bridged to one or more other stations.</span></span> <span data-ttu-id="b7c1c-109">在該行上啟用呼叫的第一行將可獨佔存取其上可能存在的位址和呼叫。</span><span class="sxs-lookup"><span data-stu-id="b7c1c-109">The first line to activate a call on the line will have exclusive access to the address and calls that may exist on it.</span></span> <span data-ttu-id="b7c1c-110">其他線條在使用時，將無法使用橋接位址。</span><span class="sxs-lookup"><span data-stu-id="b7c1c-110">Other lines will not be able to use the bridged address while it is in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7c1c-111"><span id="LINEADDRESSSHARING_BRIDGEDNEW"></span><span id="lineaddresssharing_bridgednew"></span>**LINEADDRESSSHARING \_ BRIDGEDNEW**</span><span class="sxs-lookup"><span data-stu-id="b7c1c-111"><span id="LINEADDRESSSHARING_BRIDGEDNEW"></span><span id="lineaddresssharing_bridgednew"></span>**LINEADDRESSSHARING\_BRIDGEDNEW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7c1c-112">位址會與一或多個其他工作站橋接。</span><span class="sxs-lookup"><span data-stu-id="b7c1c-112">The address is bridged with one or more other stations.</span></span> <span data-ttu-id="b7c1c-113">在該行上啟用呼叫的第一行，只會對對應的呼叫擁有獨佔存取權。</span><span class="sxs-lookup"><span data-stu-id="b7c1c-113">The first line to activate a call on the line will have exclusive access to only the corresponding call.</span></span> <span data-ttu-id="b7c1c-114">使用該位址的其他應用程式將會產生新的和不同的呼叫外觀。</span><span class="sxs-lookup"><span data-stu-id="b7c1c-114">Other applications that use the address will result in new and separate call appearances.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7c1c-115"><span id="LINEADDRESSSHARING_BRIDGEDSHARED"></span><span id="lineaddresssharing_bridgedshared"></span>**LINEADDRESSSHARING \_ BRIDGEDSHARED**</span><span class="sxs-lookup"><span data-stu-id="b7c1c-115"><span id="LINEADDRESSSHARING_BRIDGEDSHARED"></span><span id="lineaddresssharing_bridgedshared"></span>**LINEADDRESSSHARING\_BRIDGEDSHARED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7c1c-116">位址會橋接一或多個其他行。</span><span class="sxs-lookup"><span data-stu-id="b7c1c-116">The address is bridged with one or more other lines.</span></span> <span data-ttu-id="b7c1c-117">所有橋接方都可以共用位址的呼叫，然後以會議的形式運作。</span><span class="sxs-lookup"><span data-stu-id="b7c1c-117">All bridged parties can share in calls on the address, which then functions as a conference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7c1c-118"><span id="LINEADDRESSSHARING_MONITORED"></span><span id="lineaddresssharing_monitored"></span>**\_受監視的 LINEADDRESSSHARING**</span><span class="sxs-lookup"><span data-stu-id="b7c1c-118"><span id="LINEADDRESSSHARING_MONITORED"></span><span id="lineaddresssharing_monitored"></span>**LINEADDRESSSHARING\_MONITORED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7c1c-119">這是將閒置/忙碌狀態設為可供這一行使用的位址。</span><span class="sxs-lookup"><span data-stu-id="b7c1c-119">This is an address whose idle/busy status is made available to this line.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b7c1c-120">備註</span><span class="sxs-lookup"><span data-stu-id="b7c1c-120">Remarks</span></span>

<span data-ttu-id="b7c1c-121">無延伸。</span><span class="sxs-lookup"><span data-stu-id="b7c1c-121">No extensibility.</span></span> <span data-ttu-id="b7c1c-122">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="b7c1c-122">All 32 bits are reserved.</span></span>

<span data-ttu-id="b7c1c-123">在各行之間共用位址的方式，可能會影響該位址的行為。</span><span class="sxs-lookup"><span data-stu-id="b7c1c-123">The way in which an address is shared across lines can affect the behavior of that address.</span></span> <span data-ttu-id="b7c1c-124">[**行 \_CALLSTATE**](line-callstate.md) 和 [**LINE \_ ADDRESSSTATE**](line-addressstate.md) 訊息會傳送至應用程式，以回應銜接站的活動。</span><span class="sxs-lookup"><span data-stu-id="b7c1c-124">[**LINE\_CALLSTATE**](line-callstate.md) and [**LINE\_ADDRESSSTATE**](line-addressstate.md) messages are sent to the application in response to activities by the bridging stations.</span></span> <span data-ttu-id="b7c1c-125">透過這些訊息，應用程式可以追蹤位址的狀態。</span><span class="sxs-lookup"><span data-stu-id="b7c1c-125">It is through these messages that an application can track the status of the address.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7c1c-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7c1c-126">Requirements</span></span>



| <span data-ttu-id="b7c1c-127">需求</span><span class="sxs-lookup"><span data-stu-id="b7c1c-127">Requirement</span></span> | <span data-ttu-id="b7c1c-128">值</span><span class="sxs-lookup"><span data-stu-id="b7c1c-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b7c1c-129">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="b7c1c-129">TAPI version</span></span><br/> | <span data-ttu-id="b7c1c-130">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="b7c1c-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="b7c1c-131">標頭</span><span class="sxs-lookup"><span data-stu-id="b7c1c-131">Header</span></span><br/>       | <dl> <span data-ttu-id="b7c1c-132"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="b7c1c-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7c1c-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7c1c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7c1c-134">**行 \_ ADDRESSSTATE**</span><span class="sxs-lookup"><span data-stu-id="b7c1c-134">**LINE\_ADDRESSSTATE**</span></span>](line-addressstate.md)
</dt> <dt>

[<span data-ttu-id="b7c1c-135">**行 \_ CALLSTATE**</span><span class="sxs-lookup"><span data-stu-id="b7c1c-135">**LINE\_CALLSTATE**</span></span>](line-callstate.md)
</dt> </dl>

 

 




