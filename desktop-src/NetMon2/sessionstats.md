---
description: SESSIONSTATS 結構提供會話的相關統計資料。
ms.assetid: 51a6a601-634e-4d97-8c85-d3961400a2d1
title: 'SESSIONSTATS 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SESSIONSTATS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4eddfa6b0a45627c59e61fd083eb11b8d5f26caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192213"
---
# <a name="sessionstats-structure"></a><span data-ttu-id="8f7f8-103">SESSIONSTATS 結構</span><span class="sxs-lookup"><span data-stu-id="8f7f8-103">SESSIONSTATS structure</span></span>

<span data-ttu-id="8f7f8-104">**SESSIONSTATS** 結構提供 [*會話*](s.md)的相關統計資料。</span><span class="sxs-lookup"><span data-stu-id="8f7f8-104">The **SESSIONSTATS** structure provides statistics about a [*session*](s.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8f7f8-105">語法</span><span class="sxs-lookup"><span data-stu-id="8f7f8-105">Syntax</span></span>


```C++
typedef struct _SESSIONSTATS {
  DWORD NextSession;
  DWORD StationOwner;
  DWORD StationPartner;
  DWORD Flags;
  DWORD TotalPacketsSent;
} SESSIONSTATS, *LPSESSIONSTATS;
```



## <a name="members"></a><span data-ttu-id="8f7f8-106">成員</span><span class="sxs-lookup"><span data-stu-id="8f7f8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8f7f8-107">**NextSession**</span><span class="sxs-lookup"><span data-stu-id="8f7f8-107">**NextSession**</span></span>
</dt> <dd>

<span data-ttu-id="8f7f8-108">站擁有者下一個會話的索引。</span><span class="sxs-lookup"><span data-stu-id="8f7f8-108">Index of the station owner's next session.</span></span>

</dd> <dt>

<span data-ttu-id="8f7f8-109">**StationOwner**</span><span class="sxs-lookup"><span data-stu-id="8f7f8-109">**StationOwner**</span></span>
</dt> <dd>

<span data-ttu-id="8f7f8-110">關聯 [STATIONSTATS](stationstats.md) 結構陣列中的擁有者站索引。</span><span class="sxs-lookup"><span data-stu-id="8f7f8-110">Index of a owner station within the associated [STATIONSTATS](stationstats.md) structure array.</span></span> <span data-ttu-id="8f7f8-111">擁有者工作站是起始會話的站，也就是傳送會話封包的站。</span><span class="sxs-lookup"><span data-stu-id="8f7f8-111">The owner station is the station that initiated the session, the station that sent the packets of the session.</span></span>

</dd> <dt>

<span data-ttu-id="8f7f8-112">**StationPartner**</span><span class="sxs-lookup"><span data-stu-id="8f7f8-112">**StationPartner**</span></span>
</dt> <dd>

<span data-ttu-id="8f7f8-113">相關聯之 [STATIONSTATS](stationstats.md) 結構陣列內其他站的索引。</span><span class="sxs-lookup"><span data-stu-id="8f7f8-113">Index of the other station within the associated [STATIONSTATS](stationstats.md) structure array.</span></span> <span data-ttu-id="8f7f8-114">夥伴工作站是接收會話封包的站。</span><span class="sxs-lookup"><span data-stu-id="8f7f8-114">The partner station is the station that received the packets of the session.</span></span>

</dd> <dt>

<span data-ttu-id="8f7f8-115">**旗標**</span><span class="sxs-lookup"><span data-stu-id="8f7f8-115">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="8f7f8-116">這個成員已過時。</span><span class="sxs-lookup"><span data-stu-id="8f7f8-116">This member is obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="8f7f8-117">**TotalPacketsSent**</span><span class="sxs-lookup"><span data-stu-id="8f7f8-117">**TotalPacketsSent**</span></span>
</dt> <dd>

<span data-ttu-id="8f7f8-118">會話中傳送的封包數目。</span><span class="sxs-lookup"><span data-stu-id="8f7f8-118">Number of packets sent in the session.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f7f8-119">備註</span><span class="sxs-lookup"><span data-stu-id="8f7f8-119">Remarks</span></span>

<span data-ttu-id="8f7f8-120">網路監視器會將會話和站資訊儲存在兩個相關聯的陣列中，其元素分別為 **SESSIONSTATS** 和 [STATIONSTATS](stationstats.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="8f7f8-120">Network Monitor stores session and station information in two associated arrays, whose elements are **SESSIONSTATS** and [STATIONSTATS](stationstats.md) structures respectively.</span></span> <span data-ttu-id="8f7f8-121">這些結構的成員可以用來在兩者之間進行導覽。</span><span class="sxs-lookup"><span data-stu-id="8f7f8-121">The members of these structures can be used to navigate between them.</span></span> <span data-ttu-id="8f7f8-122">例如，若要移至特定工作站擁有者的下一個會話，請使用 **NextSession**。</span><span class="sxs-lookup"><span data-stu-id="8f7f8-122">For example, to move to the next session for a specific station owner, use **NextSession**.</span></span> <span data-ttu-id="8f7f8-123">若要跳至 STATIONSTATS 陣列中會話的擁有者和夥伴站，請使用 **StationOwner** 和 **StationPartner** 中提供的索引。</span><span class="sxs-lookup"><span data-stu-id="8f7f8-123">To jump to the owner and partner station of the session in the STATIONSTATS array, use the index provided in **StationOwner** and **StationPartner**.</span></span>

> [!Note]  
> <span data-ttu-id="8f7f8-124">SESSIONSTATS 陣列包含目前 capture 中每個會話的元素。</span><span class="sxs-lookup"><span data-stu-id="8f7f8-124">The SESSIONSTATS array contains an element for each session in the current capture.</span></span> <span data-ttu-id="8f7f8-125">網路監視器用來將專案新增至 SESSIONSTATS 陣列的演算法，會根據在進行中時，有效率地記錄資訊。</span><span class="sxs-lookup"><span data-stu-id="8f7f8-125">The algorithm Network Monitor uses to add elements to the SESSIONSTATS array is based on efficiently recording information while the capture is in progress.</span></span> <span data-ttu-id="8f7f8-126">因此，特定擁有者工作站的下一個會話不一定是陣列中的下一個元素。</span><span class="sxs-lookup"><span data-stu-id="8f7f8-126">Consequently, the next session for a specific owner station is not always the next element in the array.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8f7f8-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f7f8-127">Requirements</span></span>



| <span data-ttu-id="8f7f8-128">需求</span><span class="sxs-lookup"><span data-stu-id="8f7f8-128">Requirement</span></span> | <span data-ttu-id="8f7f8-129">值</span><span class="sxs-lookup"><span data-stu-id="8f7f8-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8f7f8-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8f7f8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8f7f8-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f7f8-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8f7f8-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8f7f8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8f7f8-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f7f8-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8f7f8-134">標頭</span><span class="sxs-lookup"><span data-stu-id="8f7f8-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f7f8-135"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="8f7f8-135"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f7f8-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f7f8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f7f8-137">IDelaydC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="8f7f8-137">IDelaydC::GetConversationStatistics</span></span>](idelaydc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="8f7f8-138">IRTC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="8f7f8-138">IRTC::GetConversationStatistics</span></span>](irtc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="8f7f8-139">IStats::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="8f7f8-139">IStats::GetConversationStatistics</span></span>](istats-getconversationstatistics.md)
</dt> </dl>

 

 




