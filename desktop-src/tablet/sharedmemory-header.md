---
description: 儲存共用記憶體區段的相關資訊。
ms.assetid: 73a650ee-110c-43f2-a5e2-783d52fd29ee
title: SHAREDMEMORY_HEADER 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SHAREDMEMORY_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 695f3ef09cb5e7e67de757ee3926df6fde7ddff5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997832"
---
# <a name="sharedmemory_header-structure"></a><span data-ttu-id="92ea0-103">SHAREDMEMORY \_ 標頭結構</span><span class="sxs-lookup"><span data-stu-id="92ea0-103">SHAREDMEMORY\_HEADER structure</span></span>

<span data-ttu-id="92ea0-104">儲存共用記憶體區段的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="92ea0-104">Stores information about shared memory sections.</span></span>

## <a name="syntax"></a><span data-ttu-id="92ea0-105">語法</span><span class="sxs-lookup"><span data-stu-id="92ea0-105">Syntax</span></span>


```C++
typedef struct _SHAREDMEMORY_HEADER {
  DWORD             cbTotal;
  DWORD             cbOffsetSns;
  DWORD             idxEvent;
  DWORD             dwEvent;
  CURSOR_ID         cid;
  DWORD             sn;
  SYSTEM_EVENT      sysEvt;
  SYSTEM_EVENT_DATA sysEvtData;
  DWORD             cPackets;
  DWORD             cbPackets;
  BOOL              fSnsPresent;
} SHAREDMEMORY_HEADER, *PSHAREDMEMORY_HEADER;
```



## <a name="members"></a><span data-ttu-id="92ea0-106">成員</span><span class="sxs-lookup"><span data-stu-id="92ea0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="92ea0-107">**cbTotal**</span><span class="sxs-lookup"><span data-stu-id="92ea0-107">**cbTotal**</span></span>
</dt> <dd>

<span data-ttu-id="92ea0-108">此標頭結構所參考之資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="92ea0-108">The size, in bytes, of the data referenced by this header structure.</span></span>

</dd> <dt>

<span data-ttu-id="92ea0-109">**cbOffsetSns**</span><span class="sxs-lookup"><span data-stu-id="92ea0-109">**cbOffsetSns**</span></span>
</dt> <dd>

<span data-ttu-id="92ea0-110">序號與標頭結構之間的位移大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="92ea0-110">The size, in bytes, that the serial numbers are offset from the header structure.</span></span>

</dd> <dt>

<span data-ttu-id="92ea0-111">**idxEvent**</span><span class="sxs-lookup"><span data-stu-id="92ea0-111">**idxEvent**</span></span>
</dt> <dd>

<span data-ttu-id="92ea0-112">事件索引。</span><span class="sxs-lookup"><span data-stu-id="92ea0-112">The event index.</span></span> <span data-ttu-id="92ea0-113">此值會隨著連續的事件遞增。</span><span class="sxs-lookup"><span data-stu-id="92ea0-113">This value is incremented with successive events.</span></span>

</dd> <dt>

<span data-ttu-id="92ea0-114">**dwEvent**</span><span class="sxs-lookup"><span data-stu-id="92ea0-114">**dwEvent**</span></span>
</dt> <dd>

<span data-ttu-id="92ea0-115">與此標頭相關聯的事件。</span><span class="sxs-lookup"><span data-stu-id="92ea0-115">The event associated with this header.</span></span>

</dd> <dt>

<span data-ttu-id="92ea0-116">**Cid**</span><span class="sxs-lookup"><span data-stu-id="92ea0-116">**cid**</span></span>
</dt> <dd>

<span data-ttu-id="92ea0-117">共用記憶體標頭所參考的資料指標識別碼。</span><span class="sxs-lookup"><span data-stu-id="92ea0-117">The cursor identifier referenced by the shared memory header.</span></span>

</dd> <dt>

<span data-ttu-id="92ea0-118">**sn**</span><span class="sxs-lookup"><span data-stu-id="92ea0-118">**sn**</span></span>
</dt> <dd>

<span data-ttu-id="92ea0-119">共用記憶體標頭的序號。</span><span class="sxs-lookup"><span data-stu-id="92ea0-119">The serial number for the shared memory header.</span></span>

</dd> <dt>

<span data-ttu-id="92ea0-120">**sysEvt**</span><span class="sxs-lookup"><span data-stu-id="92ea0-120">**sysEvt**</span></span>
</dt> <dd>

<span data-ttu-id="92ea0-121">\_ \* 與此標頭相關聯的系統事件（前置詞為 SE）。</span><span class="sxs-lookup"><span data-stu-id="92ea0-121">The system event, prefixed SE\_\*, associated with this header.</span></span> <span data-ttu-id="92ea0-122">如需詳細資訊，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="92ea0-122">See the remarks section for more information.</span></span>

</dd> <dt>

<span data-ttu-id="92ea0-123">**sysEvtData**</span><span class="sxs-lookup"><span data-stu-id="92ea0-123">**sysEvtData**</span></span>
</dt> <dd>

<span data-ttu-id="92ea0-124">與系統事件相關聯的 [**系統 \_ 事件 \_ 資料**](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data) 結構。</span><span class="sxs-lookup"><span data-stu-id="92ea0-124">The [**SYSTEM\_EVENT\_DATA**](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data) structure associated with the system event.</span></span>

</dd> <dt>

<span data-ttu-id="92ea0-125">**cPackets**</span><span class="sxs-lookup"><span data-stu-id="92ea0-125">**cPackets**</span></span>
</dt> <dd>

<span data-ttu-id="92ea0-126">與目前共用記憶體區段關聯的封包計數。</span><span class="sxs-lookup"><span data-stu-id="92ea0-126">A count of the packets associated with the current shared memory section.</span></span>

</dd> <dt>

<span data-ttu-id="92ea0-127">**cbPackets**</span><span class="sxs-lookup"><span data-stu-id="92ea0-127">**cbPackets**</span></span>
</dt> <dd>

<span data-ttu-id="92ea0-128">與目前共用記憶體區段相關聯的封包大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="92ea0-128">The size, in bytes, of the packets associated with the current shared memory section.</span></span>

</dd> <dt>

<span data-ttu-id="92ea0-129">**fSnsPresent**</span><span class="sxs-lookup"><span data-stu-id="92ea0-129">**fSnsPresent**</span></span>
</dt> <dd>

<span data-ttu-id="92ea0-130">指出序號是否存在於目前的共用記憶體區段中的旗標。</span><span class="sxs-lookup"><span data-stu-id="92ea0-130">A flag indicating whether serial numbers are present in the current shared memory section.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="92ea0-131">備註</span><span class="sxs-lookup"><span data-stu-id="92ea0-131">Remarks</span></span>

<span data-ttu-id="92ea0-132">下列是針對 **sysEvt** 成員定義的值。</span><span class="sxs-lookup"><span data-stu-id="92ea0-132">The following values are defined for the **sysEvt** member.</span></span>


```C++
#define SE_NONE                  0x00000000
#define SE_TAP                   0x00000010
#define SE_DBL_TAP               0x00000011
#define SE_RIGHT_TAP             0x00000012
#define SE_DRAG                  0x00000013
#define SE_RIGHT_DRAG            0x00000014
#define SE_HOLD_ENTER            0x00000015
#define SE_HOLD_LEAVE            0x00000016
#define SE_HOVER_ENTER           0x00000017
#define SE_HOVER_LEAVE           0x00000018
#define SE_FLICK                 0x0000001F
```



## <a name="see-also"></a><span data-ttu-id="92ea0-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="92ea0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92ea0-134">**系統 \_ 事件 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="92ea0-134">**SYSTEM\_EVENT\_DATA**</span></span>](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data)
</dt> </dl>

 

 



