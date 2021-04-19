---
description: ADDRESSPAIR 結構會建立 capture 篩選器。
ms.assetid: 0dd2bcaa-5e0f-448f-969e-14b923a01a2f
title: 'ADDRESSPAIR 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESSPAIR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7960a8bb1c3ed1b2fc86c93f371b2f05d299b97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979899"
---
# <a name="addresspair-structure"></a><span data-ttu-id="2cda0-103">ADDRESSPAIR 結構</span><span class="sxs-lookup"><span data-stu-id="2cda0-103">ADDRESSPAIR structure</span></span>

<span data-ttu-id="2cda0-104">**ADDRESSPAIR** 結構會建立 capture 篩選器。</span><span class="sxs-lookup"><span data-stu-id="2cda0-104">The **ADDRESSPAIR** structure constructs a capture filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cda0-105">語法</span><span class="sxs-lookup"><span data-stu-id="2cda0-105">Syntax</span></span>


```C++
typedef struct _ADDRESSPAIR {
  WORD    AddressFlags;
  WORD    NalReserved;
  ADDRESS DstAddress;
  ADDRESS SrcAddress;
} ADDRESSPAIR, *LPADDRESSPAIR;
```



## <a name="members"></a><span data-ttu-id="2cda0-106">成員</span><span class="sxs-lookup"><span data-stu-id="2cda0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2cda0-107">**AddressFlags**</span><span class="sxs-lookup"><span data-stu-id="2cda0-107">**AddressFlags**</span></span>
</dt> <dd>

<span data-ttu-id="2cda0-108">描述捕獲篩選器所使用之位址的旗標。</span><span class="sxs-lookup"><span data-stu-id="2cda0-108">Flags that describe the addresses used by a capture filter.</span></span> <span data-ttu-id="2cda0-109">如需詳細資訊，請參閱「備註」。</span><span class="sxs-lookup"><span data-stu-id="2cda0-109">See Remarks for more information.</span></span>



| <span data-ttu-id="2cda0-110">值</span><span class="sxs-lookup"><span data-stu-id="2cda0-110">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="2cda0-111">意義</span><span class="sxs-lookup"><span data-stu-id="2cda0-111">Meaning</span></span>                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="ADDRESS_FLAGS_MATCH_DST"></span><span id="address_flags_match_dst"></span><dl> <span data-ttu-id="2cda0-112"><dt>**位址 \_ 旗標 \_ 符合 \_ DST**</dt></span><span class="sxs-lookup"><span data-stu-id="2cda0-112"><dt>**ADDRESS\_FLAGS\_MATCH\_DST**</dt></span></span> </dl>                 | <span data-ttu-id="2cda0-113">符合目的地位址。</span><span class="sxs-lookup"><span data-stu-id="2cda0-113">Matches the destination address.</span></span><br/>                              |
| <span id="ADDRESS_FLAGS_MATCH_SRC"></span><span id="address_flags_match_src"></span><dl> <span data-ttu-id="2cda0-114"><dt>**位址 \_ 旗標 \_ 符合 \_ SRC**</dt></span><span class="sxs-lookup"><span data-stu-id="2cda0-114"><dt>**ADDRESS\_FLAGS\_MATCH\_SRC**</dt></span></span> </dl>                 | <span data-ttu-id="2cda0-115">符合來源位址。</span><span class="sxs-lookup"><span data-stu-id="2cda0-115">Matches the source address.</span></span><br/>                                   |
| <span id="ADDRESS_FLAGS_EXCLUDED"></span><span id="address_flags_excluded"></span><dl> <span data-ttu-id="2cda0-116"><dt>**排除的位址 \_ 旗標 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2cda0-116"><dt>**ADDRESS\_FLAGS\_EXCLUDED**</dt></span></span> </dl>                     | <span data-ttu-id="2cda0-117">如果找到此位址，則排除框架。</span><span class="sxs-lookup"><span data-stu-id="2cda0-117">Excludes the frame if this address is found.</span></span><br/>                  |
| <span id="ADDRESS_FLAGS_DST_GROUP_ADDR"></span><span id="address_flags_dst_group_addr"></span><dl> <span data-ttu-id="2cda0-118"><dt>**位址 \_ 旗標 \_ DST \_ 群組 \_ 位址**</dt></span><span class="sxs-lookup"><span data-stu-id="2cda0-118"><dt>**ADDRESS\_FLAGS\_DST\_GROUP\_ADDR**</dt></span></span> </dl> | <span data-ttu-id="2cda0-119">僅符合群組位。</span><span class="sxs-lookup"><span data-stu-id="2cda0-119">Matches group bit only.</span></span> <span data-ttu-id="2cda0-120">將此用於廣播類型的訊息。</span><span class="sxs-lookup"><span data-stu-id="2cda0-120">Use this for broadcast-type messages.</span></span><br/> |
| <span id="ADDRESS_FLAGS_MATCH_BOTH"></span><span id="address_flags_match_both"></span><dl> <span data-ttu-id="2cda0-121"><dt>**\_ \_ 符合兩者的位址旗標 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2cda0-121"><dt>**ADDRESS\_FLAGS\_MATCH\_BOTH**</dt></span></span> </dl>              | <span data-ttu-id="2cda0-122">符合目的地和來源位址。</span><span class="sxs-lookup"><span data-stu-id="2cda0-122">Matches destination and source addresses.</span></span><br/>                     |



 

</dd> <dt>

<span data-ttu-id="2cda0-123">**NalReserved**</span><span class="sxs-lookup"><span data-stu-id="2cda0-123">**NalReserved**</span></span>
</dt> <dd>

<span data-ttu-id="2cda0-124">這是保留的。</span><span class="sxs-lookup"><span data-stu-id="2cda0-124">This is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="2cda0-125">**DstAddress**</span><span class="sxs-lookup"><span data-stu-id="2cda0-125">**DstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="2cda0-126">位址配對元素的目的地位址。</span><span class="sxs-lookup"><span data-stu-id="2cda0-126">Destination address of the address pair element.</span></span>

</dd> <dt>

<span data-ttu-id="2cda0-127">**SrcAddress**</span><span class="sxs-lookup"><span data-stu-id="2cda0-127">**SrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="2cda0-128">位址配對元素的來源位址。</span><span class="sxs-lookup"><span data-stu-id="2cda0-128">Source address of the address pair element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2cda0-129">備註</span><span class="sxs-lookup"><span data-stu-id="2cda0-129">Remarks</span></span>

<span data-ttu-id="2cda0-130">您可以結合 **AddressFlags** 成員的旗標。</span><span class="sxs-lookup"><span data-stu-id="2cda0-130">The flags of the **AddressFlags** member can be combined.</span></span> <span data-ttu-id="2cda0-131">例如，下列設定會在偵測到指定的來源位址時排除框架。</span><span class="sxs-lookup"><span data-stu-id="2cda0-131">For example the following setting excludes the frame if the specified source address is detected.</span></span>

``` syntax
ADDRESS_FLAGS_MATCH_SOURCE|ADDRESS_FLAGS_EXCLUDED
```

<span data-ttu-id="2cda0-132">如需有關如何執行此結構的詳細資訊，請參閱「 [捕獲篩選準則](capture-filters.md)」。</span><span class="sxs-lookup"><span data-stu-id="2cda0-132">For more information about implementing this structure, see [Capture Filters](capture-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2cda0-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="2cda0-133">Requirements</span></span>



| <span data-ttu-id="2cda0-134">需求</span><span class="sxs-lookup"><span data-stu-id="2cda0-134">Requirement</span></span> | <span data-ttu-id="2cda0-135">值</span><span class="sxs-lookup"><span data-stu-id="2cda0-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2cda0-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2cda0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2cda0-137">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2cda0-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2cda0-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2cda0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2cda0-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2cda0-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2cda0-140">標頭</span><span class="sxs-lookup"><span data-stu-id="2cda0-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cda0-141"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="2cda0-141"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cda0-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2cda0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cda0-143">CAPTUREFILTER</span><span class="sxs-lookup"><span data-stu-id="2cda0-143">CAPTUREFILTER</span></span>](capturefilter.md)
</dt> </dl>

 

 




