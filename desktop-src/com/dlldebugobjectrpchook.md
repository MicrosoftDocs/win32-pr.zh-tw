---
title: DllDebugObjectRPCHook 函式
description: 由 COM Dll 匯出，以啟用遠端偵錯程式。
ms.assetid: a0f8bf12-0889-452d-84d0-255c5c143bc1
keywords:
- DllDebugObjectRPCHook 函式 COM
topic_type:
- apiref
api_name:
- DllDebugObjectRPCHook
api_location:
- ole32.dll
- API-MS-Win-Core-Com-private-l1-1-0.dll
- ComBase.dll
- API-MS-Win-Core-COM-Private-l1-1-1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62fffe6cc2d9ca650442d0a1c3fea2048fc6c84b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968997"
---
# <a name="dlldebugobjectrpchook-function"></a><span data-ttu-id="09202-104">DllDebugObjectRPCHook 函式</span><span class="sxs-lookup"><span data-stu-id="09202-104">DllDebugObjectRPCHook function</span></span>

<span data-ttu-id="09202-105">由 COM Dll 匯出，以啟用遠端偵錯程式。</span><span class="sxs-lookup"><span data-stu-id="09202-105">Exported by COM DLLs to enable remote debugging.</span></span>

## <a name="syntax"></a><span data-ttu-id="09202-106">語法</span><span class="sxs-lookup"><span data-stu-id="09202-106">Syntax</span></span>


```C++
BOOL WINAPI DllDebugObjectRPCHook(
   BOOL             fTrace,
   LPORPC_INIT_ARGS lpOrpcInitArgs
);
```



## <a name="parameters"></a><span data-ttu-id="09202-107">參數</span><span class="sxs-lookup"><span data-stu-id="09202-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09202-108">*fTrace*</span><span class="sxs-lookup"><span data-stu-id="09202-108">*fTrace*</span></span> 
</dt> <dd>

<span data-ttu-id="09202-109">若 **為 TRUE**，則會啟用遠端偵錯程式。</span><span class="sxs-lookup"><span data-stu-id="09202-109">If **TRUE**, remote debugging is enabled.</span></span> <span data-ttu-id="09202-110">如果 **為 FALSE**，則不會啟用遠端偵錯程式。</span><span class="sxs-lookup"><span data-stu-id="09202-110">If **FALSE**, remote debugging is not enabled.</span></span>

</dd> <dt>

<span data-ttu-id="09202-111">*lpOrpcInitArgs*</span><span class="sxs-lookup"><span data-stu-id="09202-111">*lpOrpcInitArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="09202-112">[**ORPC \_ INIT \_ ARGS**](orpc-init-args.md)引數結構的指標。</span><span class="sxs-lookup"><span data-stu-id="09202-112">A pointer to an [**ORPC\_INIT\_ARGS**](orpc-init-args.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09202-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="09202-113">Return value</span></span>

<span data-ttu-id="09202-114">如果成功，**則為 TRUE** ，否則為 **FALSE**</span><span class="sxs-lookup"><span data-stu-id="09202-114">**TRUE** if successful, **FALSE** otherwise</span></span>

## <a name="requirements"></a><span data-ttu-id="09202-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="09202-115">Requirements</span></span>



| <span data-ttu-id="09202-116">需求</span><span class="sxs-lookup"><span data-stu-id="09202-116">Requirement</span></span> | <span data-ttu-id="09202-117">值</span><span class="sxs-lookup"><span data-stu-id="09202-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="09202-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="09202-118">Minimum supported client</span></span><br/> | <span data-ttu-id="09202-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09202-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="09202-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="09202-120">Minimum supported server</span></span><br/> | <span data-ttu-id="09202-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09202-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="09202-122">標頭</span><span class="sxs-lookup"><span data-stu-id="09202-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="09202-123"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="09202-123"><dt>N/A</dt></span></span> </dl>       |
| <span data-ttu-id="09202-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="09202-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="09202-125"><dt>Ole32.lib .lib</dt></span><span class="sxs-lookup"><span data-stu-id="09202-125"><dt>Ole32.lib</dt></span></span> </dl> |
| <span data-ttu-id="09202-126">DLL</span><span class="sxs-lookup"><span data-stu-id="09202-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09202-127"><dt>Ole32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09202-127"><dt>Ole32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09202-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="09202-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09202-129">**ORPC \_ DBG \_ ALL**</span><span class="sxs-lookup"><span data-stu-id="09202-129">**ORPC\_DBG\_ALL**</span></span>](orpc-dbg-all.md)
</dt> <dt>

[<span data-ttu-id="09202-130">**ORPC \_ DBG \_ 緩衝區**</span><span class="sxs-lookup"><span data-stu-id="09202-130">**ORPC\_DBG\_BUFFER**</span></span>](orpc-dbg-buffer.md)
</dt> <dt>

[<span data-ttu-id="09202-131">**ORPC \_ INIT 引數 \_**</span><span class="sxs-lookup"><span data-stu-id="09202-131">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="09202-132">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="09202-132">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

 





