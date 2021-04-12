---
description: 將完整事件寫入至會話。
title: EtwEventWriteFull
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EtwEventWriteFull
api_type:
- HeaderDef
api_location:
- ntetw.h
ms.openlocfilehash: 5ea3de0dba842544b0ffacc785fb138bdda571a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936399"
---
# <a name="etweventwritefull-function"></a><span data-ttu-id="62b5f-103">EtwEventWriteFull 函式</span><span class="sxs-lookup"><span data-stu-id="62b5f-103">EtwEventWriteFull function</span></span>

<span data-ttu-id="62b5f-104">[EtwEventWriteFull 函式和它所傳回的結構是作業系統的內部，而且可能會從某個 Windows 版本變更為另一個版本。]</span><span class="sxs-lookup"><span data-stu-id="62b5f-104">[The EtwEventWriteFull function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.]</span></span>

<span data-ttu-id="62b5f-105">將完整事件寫入至會話。</span><span class="sxs-lookup"><span data-stu-id="62b5f-105">Writes a full event to a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="62b5f-106">語法</span><span class="sxs-lookup"><span data-stu-id="62b5f-106">Syntax</span></span>

```C++
ULONG
EVNTAPI
EtwEventWriteFull(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR EventDescriptor,
    __in USHORT EventProperty,
    __in_opt LPCGUID ActivityId,
    __in_opt LPCGUID RelatedActivityId,
    __in ULONG UserDataCount,
    __in_ecount_opt(UserDataCount) PEVENT_DATA_DESCRIPTOR UserData
    );
```

## <a name="parameters"></a><span data-ttu-id="62b5f-107">參數</span><span class="sxs-lookup"><span data-stu-id="62b5f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62b5f-108">*RegHandle*</span><span class="sxs-lookup"><span data-stu-id="62b5f-108">*RegHandle*</span></span>
</dt> <dd>

<span data-ttu-id="62b5f-109">提供者的 RegHandle。</span><span class="sxs-lookup"><span data-stu-id="62b5f-109">RegHandle for the provider.</span></span>

</dd> <dt>

<span data-ttu-id="62b5f-110">*EventDescriptor*</span><span class="sxs-lookup"><span data-stu-id="62b5f-110">*EventDescriptor*</span></span> 
</dt> <dd>

<span data-ttu-id="62b5f-111">要記錄之事件的事件描述項。</span><span class="sxs-lookup"><span data-stu-id="62b5f-111">Event Descriptor of the event to log.</span></span>

</dd> <dt>

<span data-ttu-id="62b5f-112">*EventProperty*</span><span class="sxs-lookup"><span data-stu-id="62b5f-112">*EventProperty*</span></span>
</dt> <dd>

<span data-ttu-id="62b5f-113">使用者指定的旗標。</span><span class="sxs-lookup"><span data-stu-id="62b5f-113">Flag given by the user.</span></span>

</dd> <dt>

<span data-ttu-id="62b5f-114">*ActivityId*</span><span class="sxs-lookup"><span data-stu-id="62b5f-114">*ActivityId*</span></span>
</dt> <dd>

<span data-ttu-id="62b5f-115">活動識別碼。</span><span class="sxs-lookup"><span data-stu-id="62b5f-115">Activity Id.</span></span>

</dd> <dt>

<span data-ttu-id="62b5f-116">*RelatedActivityId*</span><span class="sxs-lookup"><span data-stu-id="62b5f-116">*RelatedActivityId*</span></span>
</dt> <dd>

<span data-ttu-id="62b5f-117">相關的活動識別碼。</span><span class="sxs-lookup"><span data-stu-id="62b5f-117">Related activity Id.</span></span>

</dd> <dt>

<span data-ttu-id="62b5f-118">*UserDataCount*</span><span class="sxs-lookup"><span data-stu-id="62b5f-118">*UserDataCount*</span></span>
</dt> <dd>

<span data-ttu-id="62b5f-119">使用者資料項目的數目。</span><span class="sxs-lookup"><span data-stu-id="62b5f-119">The number of user data items.</span></span>

</dd> <dt>

<span data-ttu-id="62b5f-120">*UserData*</span><span class="sxs-lookup"><span data-stu-id="62b5f-120">*UserData*</span></span>
</dt> <dd>

<span data-ttu-id="62b5f-121">使用者資料項目陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="62b5f-121">Pointer to an array of user data items.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62b5f-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="62b5f-122">Return value</span></span>

<span data-ttu-id="62b5f-123">Win32 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="62b5f-123">A Win32 error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="62b5f-124">備註</span><span class="sxs-lookup"><span data-stu-id="62b5f-124">Remarks</span></span>

<span data-ttu-id="62b5f-125">EtwEventWriteFull 函式和它所傳回的結構是作業系統的內部，而且可能會從某個 Windows 版本變更為另一個。</span><span class="sxs-lookup"><span data-stu-id="62b5f-125">The EtwEventWriteFull function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.</span></span> <span data-ttu-id="62b5f-126">若要維持應用程式的相容性，最好改為使用公用函數。</span><span class="sxs-lookup"><span data-stu-id="62b5f-126">To maintain the compatibility of your application, it is better to use public functions instead.</span></span>


## <a name="requirements"></a><span data-ttu-id="62b5f-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="62b5f-127">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="62b5f-128">**目標平台**</span><span class="sxs-lookup"><span data-stu-id="62b5f-128">**Target Platform**</span></span> | <span data-ttu-id="62b5f-129">Windows</span><span class="sxs-lookup"><span data-stu-id="62b5f-129">Windows</span></span> |
| <span data-ttu-id="62b5f-130">**標頭**</span><span class="sxs-lookup"><span data-stu-id="62b5f-130">**Header**</span></span> | <span data-ttu-id="62b5f-131">ntetw。h</span><span class="sxs-lookup"><span data-stu-id="62b5f-131">ntetw.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="62b5f-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62b5f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62b5f-133">EventWrite</span><span class="sxs-lookup"><span data-stu-id="62b5f-133">EventWrite</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventwrite)
</dt> <dt>

[<span data-ttu-id="62b5f-134">EventWriteEx</span><span class="sxs-lookup"><span data-stu-id="62b5f-134">EventWriteEx</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex)
</dt></dl>
