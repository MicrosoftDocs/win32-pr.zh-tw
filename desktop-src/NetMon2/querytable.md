---
description: 此資料表結構會提供目前使用網路監視器來捕捉網路資料的電腦清單。
ms.assetid: b701a6d5-df6d-4ee9-b008-a568a410dc14
title: " (Netmon .h 的) 的"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- QUERYTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 2b2976a56b43c55fccb9acb0c593b0dfd37e4404
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980811"
---
# <a name="querytable-structure"></a><span data-ttu-id="b684f-103">的</span><span class="sxs-lookup"><span data-stu-id="b684f-103">QUERYTABLE structure</span></span>

<span data-ttu-id="b684f-104">此 **資料表結構會** 提供目前使用網路監視器來捕捉網路資料的電腦清單。</span><span class="sxs-lookup"><span data-stu-id="b684f-104">The **QUERYTABLE** structure provides a list of the computers that are currently using Network Monitor to capture network data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b684f-105">語法</span><span class="sxs-lookup"><span data-stu-id="b684f-105">Syntax</span></span>


```C++
typedef struct _QUERYTABLE {
  DWORD        nStationQueries;
  STATIONQUERY StationQuery[1];
} QUERYTABLE, *LPQUERYTABLE;
```



## <a name="members"></a><span data-ttu-id="b684f-106">成員</span><span class="sxs-lookup"><span data-stu-id="b684f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b684f-107">**nStationQueries**</span><span class="sxs-lookup"><span data-stu-id="b684f-107">**nStationQueries**</span></span>
</dt> <dd>

<span data-ttu-id="b684f-108">輸入時，您要網路監視器傳回的電腦數目上限。</span><span class="sxs-lookup"><span data-stu-id="b684f-108">On input, the maximum number of computers you want Network Monitor to return.</span></span>

<span data-ttu-id="b684f-109">在輸出時，網路監視器所傳回的 [STATIONQUERY](stationquery.md) 結構數目。</span><span class="sxs-lookup"><span data-stu-id="b684f-109">On output, the number of [STATIONQUERY](stationquery.md) structures returned by Network Monitor.</span></span> <span data-ttu-id="b684f-110">每個 **STATIONQUERY** 結構都代表目前正在捕獲資料的電腦。</span><span class="sxs-lookup"><span data-stu-id="b684f-110">Each **STATIONQUERY** structure represents a computer that is currently capturing data.</span></span>

</dd> <dt>

<span data-ttu-id="b684f-111">**StationQuery**</span><span class="sxs-lookup"><span data-stu-id="b684f-111">**StationQuery**</span></span>
</dt> <dd>

<span data-ttu-id="b684f-112">在輸入時，為空白 [STATIONQUERY](stationquery.md) 結構的陣列，其中包含在 **nStationQueries** 中指定的元素數目。</span><span class="sxs-lookup"><span data-stu-id="b684f-112">On input, an array of empty [STATIONQUERY](stationquery.md) structures that contains the number of elements specified in **nStationQueries**.</span></span>

<span data-ttu-id="b684f-113">在輸出時，為正在捕捉資料的每部電腦填入已填滿的 [STATIONQUERY](stationquery.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="b684f-113">On output, a filled [STATIONQUERY](stationquery.md) structure for each computer that is capturing data.</span></span> <span data-ttu-id="b684f-114">**NStationQueries** 會傳回已填滿的元素數目。</span><span class="sxs-lookup"><span data-stu-id="b684f-114">The number of filled elements is returned by **nStationQueries**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b684f-115">備註</span><span class="sxs-lookup"><span data-stu-id="b684f-115">Remarks</span></span>

<span data-ttu-id="b684f-116">此結構和 [STATIONQUERY](stationquery.md) 陣列的記憶體必須由呼叫應用程式佈建，並在不再需要資訊之後釋放。</span><span class="sxs-lookup"><span data-stu-id="b684f-116">The memory for this structure and the [STATIONQUERY](stationquery.md) array must be allocated by the calling application and freed after the information is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b684f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="b684f-117">Requirements</span></span>



| <span data-ttu-id="b684f-118">需求</span><span class="sxs-lookup"><span data-stu-id="b684f-118">Requirement</span></span> | <span data-ttu-id="b684f-119">值</span><span class="sxs-lookup"><span data-stu-id="b684f-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b684f-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b684f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b684f-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b684f-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b684f-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b684f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b684f-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b684f-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b684f-124">標頭</span><span class="sxs-lookup"><span data-stu-id="b684f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b684f-125"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="b684f-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b684f-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b684f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b684f-127">IDelaydC::QueryStations</span><span class="sxs-lookup"><span data-stu-id="b684f-127">IDelaydC::QueryStations</span></span>](idelaydc-querystations.md)
</dt> <dt>

[<span data-ttu-id="b684f-128">IESP::QueryStations</span><span class="sxs-lookup"><span data-stu-id="b684f-128">IESP::QueryStations</span></span>](iesp-querystations.md)
</dt> <dt>

[<span data-ttu-id="b684f-129">IRTC::QueryStations</span><span class="sxs-lookup"><span data-stu-id="b684f-129">IRTC::QueryStations</span></span>](irtc-querystations.md)
</dt> <dt>

[<span data-ttu-id="b684f-130">IStats::QueryStations</span><span class="sxs-lookup"><span data-stu-id="b684f-130">IStats::QueryStations</span></span>](istats-querystations.md)
</dt> <dt>

[<span data-ttu-id="b684f-131">STATIONQUERY</span><span class="sxs-lookup"><span data-stu-id="b684f-131">STATIONQUERY</span></span>](stationquery.md)
</dt> </dl>

 

 




