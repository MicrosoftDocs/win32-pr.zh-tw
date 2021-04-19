---
description: UPDATE \_ 事件結構會更新事件。 此結構會透過 NPP 的事件狀態回呼程式，傳回給呼叫的應用程式。
ms.assetid: 6896be5a-f986-44ff-a18b-010f7b9858aa
title: 'UPDATE_EVENT 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UPDATE_EVENT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3da45020a68114182a71b25ff9bba380d3f89eee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978916"
---
# <a name="update_event-structure"></a><span data-ttu-id="665c3-104">更新 \_ 事件結構</span><span class="sxs-lookup"><span data-stu-id="665c3-104">UPDATE\_EVENT structure</span></span>

<span data-ttu-id="665c3-105">**UPDATE \_ 事件** 結構會更新事件。</span><span class="sxs-lookup"><span data-stu-id="665c3-105">The **UPDATE\_EVENT** structure updates events.</span></span> <span data-ttu-id="665c3-106">此結構會透過 NPP 的事件狀態回呼程式，傳回給呼叫的應用程式。</span><span class="sxs-lookup"><span data-stu-id="665c3-106">This structure is passed back to the calling application via the event status callback procedure by the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="665c3-107">語法</span><span class="sxs-lookup"><span data-stu-id="665c3-107">Syntax</span></span>


```C++
typedef struct _UPDATE_EVENT {
  USHORT       Event;
  DWORD        Action;
  DWORD        Status;
  DWORD        Value;
  __int64      TimeStamp;
  DWORD_PTR    lpUserContext;
  DWORD_PTR    lpReserved;
  UINT         FramesDropped;
  union {
    DWORD                        Reserved;
    LPFRAMETABLE                 lpFrameTable;
    DWORD_PTR                    lpPacketQueue;
    SECURITY_PERMISSION_RESPONSE SecurityResponse;
  };
  LPSTATISTICS lpFinalStats;
} UPDATE_EVENT, *PUPDATE_EVENT;
```



## <a name="members"></a><span data-ttu-id="665c3-108">成員</span><span class="sxs-lookup"><span data-stu-id="665c3-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="665c3-109">**事件**</span><span class="sxs-lookup"><span data-stu-id="665c3-109">**Event**</span></span>
</dt> <dd>

<span data-ttu-id="665c3-110">實際記錄的事件。</span><span class="sxs-lookup"><span data-stu-id="665c3-110">Actual event being recorded.</span></span>

</dd> <dt>

<span data-ttu-id="665c3-111">**動作**</span><span class="sxs-lookup"><span data-stu-id="665c3-111">**Action**</span></span>
</dt> <dd>

<span data-ttu-id="665c3-112">採取的動作。</span><span class="sxs-lookup"><span data-stu-id="665c3-112">The action taken.</span></span>

</dd> <dt>

<span data-ttu-id="665c3-113">**狀態**</span><span class="sxs-lookup"><span data-stu-id="665c3-113">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="665c3-114">網路狀態指示。</span><span class="sxs-lookup"><span data-stu-id="665c3-114">Network status indication.</span></span>

</dd> <dt>

<span data-ttu-id="665c3-115">**值**</span><span class="sxs-lookup"><span data-stu-id="665c3-115">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="665c3-116">輔助計數器變數。</span><span class="sxs-lookup"><span data-stu-id="665c3-116">Auxiliary counter variable.</span></span>

</dd> <dt>

<span data-ttu-id="665c3-117">**時間 戳**</span><span class="sxs-lookup"><span data-stu-id="665c3-117">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="665c3-118">標示的事件（以微秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="665c3-118">The marked events, in microseconds.</span></span>

</dd> <dt>

<span data-ttu-id="665c3-119">**lpUserCoNtext**</span><span class="sxs-lookup"><span data-stu-id="665c3-119">**lpUserContext**</span></span>
</dt> <dd>

<span data-ttu-id="665c3-120">應用程式所提供的使用者內容。</span><span class="sxs-lookup"><span data-stu-id="665c3-120">User context given by the application.</span></span>

</dd> <dt>

<span data-ttu-id="665c3-121">**lpReserved**</span><span class="sxs-lookup"><span data-stu-id="665c3-121">**lpReserved**</span></span>
</dt> <dd>

<span data-ttu-id="665c3-122">驅動程式或 NAL 使用。</span><span class="sxs-lookup"><span data-stu-id="665c3-122">Driver or NAL use.</span></span>

</dd> <dt>

<span data-ttu-id="665c3-123">**FramesDropped**</span><span class="sxs-lookup"><span data-stu-id="665c3-123">**FramesDropped**</span></span>
</dt> <dd>

<span data-ttu-id="665c3-124">放在指定緩衝區中的 RTF 框架。</span><span class="sxs-lookup"><span data-stu-id="665c3-124">RTF frames dropped in the specified buffer.</span></span>

</dd> <dt>

<span data-ttu-id="665c3-125">**已保留**</span><span class="sxs-lookup"><span data-stu-id="665c3-125">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="665c3-126">此切換選項不會傳回任何資料。</span><span class="sxs-lookup"><span data-stu-id="665c3-126">No data comes back with this switch option.</span></span>

</dd> <dt>

<span data-ttu-id="665c3-127">**lpFrameTable**</span><span class="sxs-lookup"><span data-stu-id="665c3-127">**lpFrameTable**</span></span>
</dt> <dd>

<span data-ttu-id="665c3-128">僅限 RTF。</span><span class="sxs-lookup"><span data-stu-id="665c3-128">RTF only.</span></span>

</dd> <dt>

<span data-ttu-id="665c3-129">**lpPacketQueue**</span><span class="sxs-lookup"><span data-stu-id="665c3-129">**lpPacketQueue**</span></span>
</dt> <dd>

<span data-ttu-id="665c3-130">適用于傳輸。</span><span class="sxs-lookup"><span data-stu-id="665c3-130">For transmits.</span></span>

</dd> <dt>

<span data-ttu-id="665c3-131">**SecurityResponse**</span><span class="sxs-lookup"><span data-stu-id="665c3-131">**SecurityResponse**</span></span>
</dt> <dd>

<span data-ttu-id="665c3-132">遠端安全性監視器回應。</span><span class="sxs-lookup"><span data-stu-id="665c3-132">Remote security monitor response.</span></span>

</dd> <dt>

<span data-ttu-id="665c3-133">**lpFinalStats**</span><span class="sxs-lookup"><span data-stu-id="665c3-133">**lpFinalStats**</span></span>
</dt> <dd>

<span data-ttu-id="665c3-134">這只會填入非安全性相關的停止 (例如，觸發程式) 。</span><span class="sxs-lookup"><span data-stu-id="665c3-134">This is only filled in on non-security related stops (for example, triggers).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="665c3-135">備註</span><span class="sxs-lookup"><span data-stu-id="665c3-135">Remarks</span></span>

<span data-ttu-id="665c3-136">C + + 使用者應該注意，此回呼的宣告應該在標頭檔的公開部分中：</span><span class="sxs-lookup"><span data-stu-id="665c3-136">C++ users should note that the declaration for this callback should be in the public part of the header file:</span></span>

``` syntax
static WINAPI DWORD NetworkCallback( UPDATE_EVENT events);
```

<span data-ttu-id="665c3-137">此實應位於 .cpp 檔案的 protected 區段中：</span><span class="sxs-lookup"><span data-stu-id="665c3-137">The implementation should be in the protected section of the .cpp file:</span></span>

``` syntax
DWORD WINAPI ClassName::NetworkCallback( UPDATE_EVENT events) {};
```

## <a name="requirements"></a><span data-ttu-id="665c3-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="665c3-138">Requirements</span></span>



| <span data-ttu-id="665c3-139">需求</span><span class="sxs-lookup"><span data-stu-id="665c3-139">Requirement</span></span> | <span data-ttu-id="665c3-140">值</span><span class="sxs-lookup"><span data-stu-id="665c3-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="665c3-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="665c3-141">Minimum supported client</span></span><br/> | <span data-ttu-id="665c3-142">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="665c3-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="665c3-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="665c3-143">Minimum supported server</span></span><br/> | <span data-ttu-id="665c3-144">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="665c3-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="665c3-145">標頭</span><span class="sxs-lookup"><span data-stu-id="665c3-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="665c3-146"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="665c3-146"><dt>Netmon.h</dt></span></span> </dl> |



 

 




