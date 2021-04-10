---
description: STATIONSTATS 結構會提供目前 capture 所描述之特定工作站的相關統計資料。
ms.assetid: f85d53d6-f496-4242-875f-e173c76b046a
title: 'STATIONSTATS 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STATIONSTATS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 0b37d4570fe8f4c27ea66e6350b79e14a10e544e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026558"
---
# <a name="stationstats-structure"></a><span data-ttu-id="5d36e-103">STATIONSTATS 結構</span><span class="sxs-lookup"><span data-stu-id="5d36e-103">STATIONSTATS structure</span></span>

<span data-ttu-id="5d36e-104">**STATIONSTATS** 結構會提供目前 capture 所描述之特定 [*工作站*](s.md)的相關統計資料。</span><span class="sxs-lookup"><span data-stu-id="5d36e-104">The **STATIONSTATS** structure provides statistics about a specific [*station*](s.md) described by the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d36e-105">語法</span><span class="sxs-lookup"><span data-stu-id="5d36e-105">Syntax</span></span>


```C++
typedef struct _STATIONSTATS {
  DWORD NextStationStats;
  DWORD SessionPartnerList;
  DWORD Flags;
  BYTE  StationAddress[6];
  WORD  Pad;
  DWORD TotalPacketsReceived;
  DWORD TotalDirectedPacketsSent;
  DWORD TotalBroadcastPacketsSent;
  DWORD TotalMulticastPacketsSent;
  DWORD TotalBytesReceived;
  DWORD TotalBytesSent;
} STATIONSTATS, *LPSTATIONSTATS;
```



## <a name="members"></a><span data-ttu-id="5d36e-106">成員</span><span class="sxs-lookup"><span data-stu-id="5d36e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5d36e-107">**NextStationStats**</span><span class="sxs-lookup"><span data-stu-id="5d36e-107">**NextStationStats**</span></span>
</dt> <dd>

<span data-ttu-id="5d36e-108">**STATIONSTATS** 結構陣列中記錄的下一個站索引。</span><span class="sxs-lookup"><span data-stu-id="5d36e-108">Index of the next station recorded in the **STATIONSTATS** structure array.</span></span>

</dd> <dt>

<span data-ttu-id="5d36e-109">**SessionPartnerList**</span><span class="sxs-lookup"><span data-stu-id="5d36e-109">**SessionPartnerList**</span></span>
</dt> <dd>

<span data-ttu-id="5d36e-110">站夥伴清單的索引。</span><span class="sxs-lookup"><span data-stu-id="5d36e-110">Index of the station partner list.</span></span>

</dd> <dt>

<span data-ttu-id="5d36e-111">**旗標**</span><span class="sxs-lookup"><span data-stu-id="5d36e-111">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="5d36e-112">這個成員已過時。</span><span class="sxs-lookup"><span data-stu-id="5d36e-112">This member is obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="5d36e-113">**StationAddress**</span><span class="sxs-lookup"><span data-stu-id="5d36e-113">**StationAddress**</span></span>
</dt> <dd>

<span data-ttu-id="5d36e-114">工作站的 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="5d36e-114">The MAC address of the station.</span></span>

</dd> <dt>

<span data-ttu-id="5d36e-115">**墊**</span><span class="sxs-lookup"><span data-stu-id="5d36e-115">**Pad**</span></span>
</dt> <dd>

<span data-ttu-id="5d36e-116">**DWORD** 對齊。</span><span class="sxs-lookup"><span data-stu-id="5d36e-116">**DWORD** alignment.</span></span>

</dd> <dt>

<span data-ttu-id="5d36e-117">**TotalPacketsReceived**</span><span class="sxs-lookup"><span data-stu-id="5d36e-117">**TotalPacketsReceived**</span></span>
</dt> <dd>

<span data-ttu-id="5d36e-118">傳送至工作站的封包總數。</span><span class="sxs-lookup"><span data-stu-id="5d36e-118">Total number of packets sent to the station.</span></span>

</dd> <dt>

<span data-ttu-id="5d36e-119">**TotalDirectedPacketsSent**</span><span class="sxs-lookup"><span data-stu-id="5d36e-119">**TotalDirectedPacketsSent**</span></span>
</dt> <dd>

<span data-ttu-id="5d36e-120">站送出的導向封包總數。</span><span class="sxs-lookup"><span data-stu-id="5d36e-120">Total number of directed packets sent by the station.</span></span>

</dd> <dt>

<span data-ttu-id="5d36e-121">**TotalBroadcastPacketsSent**</span><span class="sxs-lookup"><span data-stu-id="5d36e-121">**TotalBroadcastPacketsSent**</span></span>
</dt> <dd>

<span data-ttu-id="5d36e-122">廣播導向封包總數 (MAC 位址 FF FF ff ff ff ff) 由工作站傳送。</span><span class="sxs-lookup"><span data-stu-id="5d36e-122">Total number of broadcast-directed packets (MAC address FF FF FF FF FF FF) sent by the station.</span></span>

</dd> <dt>

<span data-ttu-id="5d36e-123">**TotalMulticastPacketsSent**</span><span class="sxs-lookup"><span data-stu-id="5d36e-123">**TotalMulticastPacketsSent**</span></span>
</dt> <dd>

<span data-ttu-id="5d36e-124">目的地位址中設定的多播封包總數 (群組位) 由工作站傳送。</span><span class="sxs-lookup"><span data-stu-id="5d36e-124">Total number of multicast packets (Group bit set in destination address) sent by the station.</span></span>

</dd> <dt>

<span data-ttu-id="5d36e-125">**TotalBytesReceived**</span><span class="sxs-lookup"><span data-stu-id="5d36e-125">**TotalBytesReceived**</span></span>
</dt> <dd>

<span data-ttu-id="5d36e-126">傳送至工作站的位元組總數。</span><span class="sxs-lookup"><span data-stu-id="5d36e-126">Total number of bytes sent to the station.</span></span>

</dd> <dt>

<span data-ttu-id="5d36e-127">**TotalBytesSent**</span><span class="sxs-lookup"><span data-stu-id="5d36e-127">**TotalBytesSent**</span></span>
</dt> <dd>

<span data-ttu-id="5d36e-128">工作站傳送的位元組總數。</span><span class="sxs-lookup"><span data-stu-id="5d36e-128">Total number of bytes sent by the station.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d36e-129">備註</span><span class="sxs-lookup"><span data-stu-id="5d36e-129">Remarks</span></span>

<span data-ttu-id="5d36e-130">網路監視器會將會話和站資訊儲存在兩個相關聯的陣列中。</span><span class="sxs-lookup"><span data-stu-id="5d36e-130">Network Monitor stores session and station information in two associated arrays.</span></span> <span data-ttu-id="5d36e-131">其元素分別為 [SESSIONSTATS](sessionstats.md) 和 **STATIONSTATS** 結構。</span><span class="sxs-lookup"><span data-stu-id="5d36e-131">whose elements are [SESSIONSTATS](sessionstats.md) and **STATIONSTATS** structures respectively.</span></span> <span data-ttu-id="5d36e-132">這些結構的成員可以用來在兩者之間進行導覽。</span><span class="sxs-lookup"><span data-stu-id="5d36e-132">The members of these structures can be used to navigate between them.</span></span> <span data-ttu-id="5d36e-133">例如，若要移至下一個站，請使用 **NextStationStats**。</span><span class="sxs-lookup"><span data-stu-id="5d36e-133">For example, to move to the next station use **NextStationStats**.</span></span> <span data-ttu-id="5d36e-134">若要跳至 SESSIONSTATS 陣列中的會話夥伴清單，請使用 **SessionPartnerList** 中提供的索引。</span><span class="sxs-lookup"><span data-stu-id="5d36e-134">To jump to the session partner list in the SESSIONSTATS array, use the index provided in **SessionPartnerList**.</span></span>

> [!Note]  
> <span data-ttu-id="5d36e-135">**STATIONSTATS** 陣列包含目前捕獲期間使用的每個工作站的元素。</span><span class="sxs-lookup"><span data-stu-id="5d36e-135">The **STATIONSTATS** array contains an element for each station used during the current capture.</span></span> <span data-ttu-id="5d36e-136">網路監視器用來將專案加入至這個陣列的演算法，是以最有效率的方式，在進行捕獲時記錄資訊。</span><span class="sxs-lookup"><span data-stu-id="5d36e-136">The algorithm Network Monitor uses to add elements to this array is based on the most efficient way to record information while the capture is in progress.</span></span> <span data-ttu-id="5d36e-137">因此，下一個站不一定是陣列中的下一個元素。</span><span class="sxs-lookup"><span data-stu-id="5d36e-137">Consequently, the next station is not always the next element in the array.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5d36e-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d36e-138">Requirements</span></span>



| <span data-ttu-id="5d36e-139">需求</span><span class="sxs-lookup"><span data-stu-id="5d36e-139">Requirement</span></span> | <span data-ttu-id="5d36e-140">值</span><span class="sxs-lookup"><span data-stu-id="5d36e-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5d36e-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5d36e-141">Minimum supported client</span></span><br/> | <span data-ttu-id="5d36e-142">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d36e-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5d36e-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5d36e-143">Minimum supported server</span></span><br/> | <span data-ttu-id="5d36e-144">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d36e-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5d36e-145">標頭</span><span class="sxs-lookup"><span data-stu-id="5d36e-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d36e-146"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="5d36e-146"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d36e-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d36e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d36e-148">IDelaydC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="5d36e-148">IDelaydC::GetConversationStatistics</span></span>](idelaydc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="5d36e-149">IRTC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="5d36e-149">IRTC::GetConversationStatistics</span></span>](irtc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="5d36e-150">IStats::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="5d36e-150">IStats::GetConversationStatistics</span></span>](istats-getconversationstatistics.md)
</dt> </dl>

 

 




