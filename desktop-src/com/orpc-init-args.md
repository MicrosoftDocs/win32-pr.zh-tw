---
title: ORPC_INIT_ARGS 結構
description: ORPC INIT ARGS （引數） \_ \_ 結構包含用來初始化使用 IOrpcDebugNotify 介面進行遠端偵錯的資訊。
ms.assetid: be7646c7-3394-45ae-ae8f-9cee68bbc789
keywords:
- ORPC_INIT_ARGS 結構 COM
- LPORPC_INIT_ARGS 結構指標 COM
topic_type:
- apiref
api_name:
- ORPC_INIT_ARGS
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e7dca0209f745d5034bde2da852829b99d7dcb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094204"
---
# <a name="orpc_init_args-structure"></a><span data-ttu-id="664aa-105">ORPC \_ INIT \_ ARGS 變數結構</span><span class="sxs-lookup"><span data-stu-id="664aa-105">ORPC\_INIT\_ARGS structure</span></span>

<span data-ttu-id="664aa-106">**ORPC \_ INIT \_ ARGS** （引數）結構包含用來初始化使用 [**IOrpcDebugNotify**](iorpcdebugnotify.md)介面進行遠端偵錯的資訊。</span><span class="sxs-lookup"><span data-stu-id="664aa-106">The **ORPC\_INIT\_ARGS** structure contains information used to initialize remote debugging using the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="664aa-107">語法</span><span class="sxs-lookup"><span data-stu-id="664aa-107">Syntax</span></span>


```C++
typedef struct ORPC_INIT_ARGS {
  IOrpcDebugNotify *lpIntfOrpcDebug;
  void             *pvPSN;
  DWORD            *dwReserved1;
  DWORD            *dwReserved2;
} ORPC_INIT_ARGS, *LPORPC_INIT_ARGS;
```



## <a name="members"></a><span data-ttu-id="664aa-108">成員</span><span class="sxs-lookup"><span data-stu-id="664aa-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="664aa-109">**lpIntfOrpcDebug**</span><span class="sxs-lookup"><span data-stu-id="664aa-109">**lpIntfOrpcDebug**</span></span>
</dt> <dd>

<span data-ttu-id="664aa-110">[**IOrpcDebugNotify**](iorpcdebugnotify.md)介面的指標，可供同進程偵錯工具使用。</span><span class="sxs-lookup"><span data-stu-id="664aa-110">A pointer to the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface for use by in-process debuggers.</span></span> <span data-ttu-id="664aa-111">如果偵錯工具不在進程中或為 Macintosh 系統，此欄位必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="664aa-111">If the debugger is not in-process or is a Macintosh system, this field must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="664aa-112">**pvPSN**</span><span class="sxs-lookup"><span data-stu-id="664aa-112">**pvPSN**</span></span>
</dt> <dd>

<span data-ttu-id="664aa-113">偵錯工具之進程式號的指標。</span><span class="sxs-lookup"><span data-stu-id="664aa-113">A pointer to the Macintosh process serial number of the debuggee's process.</span></span> <span data-ttu-id="664aa-114">如果偵錯工具不是 Macintosh 系統，此欄位必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="664aa-114">If the debuggee is not a Macintosh system, this field must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="664aa-115">**dwReserved1**</span><span class="sxs-lookup"><span data-stu-id="664aa-115">**dwReserved1**</span></span>
</dt> <dd>

<span data-ttu-id="664aa-116">保留的。</span><span class="sxs-lookup"><span data-stu-id="664aa-116">Reserved.</span></span> <span data-ttu-id="664aa-117">必須是 0。</span><span class="sxs-lookup"><span data-stu-id="664aa-117">Must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="664aa-118">**dwReserved2**</span><span class="sxs-lookup"><span data-stu-id="664aa-118">**dwReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="664aa-119">保留的。</span><span class="sxs-lookup"><span data-stu-id="664aa-119">Reserved.</span></span> <span data-ttu-id="664aa-120">必須是 0。</span><span class="sxs-lookup"><span data-stu-id="664aa-120">Must be 0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="664aa-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="664aa-121">Requirements</span></span>



| <span data-ttu-id="664aa-122">需求</span><span class="sxs-lookup"><span data-stu-id="664aa-122">Requirement</span></span> | <span data-ttu-id="664aa-123">值</span><span class="sxs-lookup"><span data-stu-id="664aa-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="664aa-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="664aa-124">Minimum supported client</span></span><br/> | <span data-ttu-id="664aa-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="664aa-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="664aa-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="664aa-126">Minimum supported server</span></span><br/> | <span data-ttu-id="664aa-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="664aa-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="664aa-128">標頭</span><span class="sxs-lookup"><span data-stu-id="664aa-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="664aa-129"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="664aa-129"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="664aa-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="664aa-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="664aa-131">**ORPC \_ DBG \_ ALL**</span><span class="sxs-lookup"><span data-stu-id="664aa-131">**ORPC\_DBG\_ALL**</span></span>](orpc-dbg-all.md)
</dt> <dt>

[<span data-ttu-id="664aa-132">**ORPC \_ DBG \_ 緩衝區**</span><span class="sxs-lookup"><span data-stu-id="664aa-132">**ORPC\_DBG\_BUFFER**</span></span>](orpc-dbg-buffer.md)
</dt> <dt>

[<span data-ttu-id="664aa-133">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="664aa-133">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="664aa-134">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="664aa-134">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

 





