---
title: IOrpcDebugNotify 介面
description: 提供遠端偵錯功能。
ms.assetid: f91987c0-2e4b-4872-8ed6-e208a23baa49
keywords:
- IOrpcDebugNotify 介面 COM
- IOrpcDebugNotify 介面 COM，描述
topic_type:
- apiref
api_name:
- IOrpcDebugNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4db08daf93997b2a7fa0ed383591cb5d111ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509426"
---
# <a name="iorpcdebugnotify-interface"></a><span data-ttu-id="39e1a-105">IOrpcDebugNotify 介面</span><span class="sxs-lookup"><span data-stu-id="39e1a-105">IOrpcDebugNotify interface</span></span>

<span data-ttu-id="39e1a-106">提供遠端偵錯功能。</span><span class="sxs-lookup"><span data-stu-id="39e1a-106">Provides remote debugging functionality.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="39e1a-107">執行時機</span><span class="sxs-lookup"><span data-stu-id="39e1a-107">When to implement</span></span>

<span data-ttu-id="39e1a-108">執行此介面可讓您透過 RPC 進行遠端偵錯。</span><span class="sxs-lookup"><span data-stu-id="39e1a-108">Implement this interface to enable remote debugging over RPC.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="39e1a-109">使用時機</span><span class="sxs-lookup"><span data-stu-id="39e1a-109">When to use</span></span>

<span data-ttu-id="39e1a-110">當「軟體例外狀況」不應該用於 COM 偵錯工具通知時，此介面應該用於同進程遠端偵錯程式。</span><span class="sxs-lookup"><span data-stu-id="39e1a-110">This interface should be used for in-process remote debugging when software exceptions should not be used for the COM debugger notifications.</span></span> <span data-ttu-id="39e1a-111">它可讓同進程偵錯工具透過使用這些方法的直接呼叫來通知。</span><span class="sxs-lookup"><span data-stu-id="39e1a-111">It enables in-process debuggers to be notified by direct calls using these methods.</span></span>

## <a name="members"></a><span data-ttu-id="39e1a-112">成員</span><span class="sxs-lookup"><span data-stu-id="39e1a-112">Members</span></span>

<span data-ttu-id="39e1a-113">**IOrpcDebugNotify** 介面繼承自 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="39e1a-113">The **IOrpcDebugNotify** interface inherits from the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="39e1a-114">**IOrpcDebugNotify** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="39e1a-114">**IOrpcDebugNotify** also has these types of members:</span></span>

-   [<span data-ttu-id="39e1a-115">方法</span><span class="sxs-lookup"><span data-stu-id="39e1a-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="39e1a-116">方法</span><span class="sxs-lookup"><span data-stu-id="39e1a-116">Methods</span></span>

<span data-ttu-id="39e1a-117">**IOrpcDebugNotify** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="39e1a-117">The **IOrpcDebugNotify** interface has these methods.</span></span>



| <span data-ttu-id="39e1a-118">方法</span><span class="sxs-lookup"><span data-stu-id="39e1a-118">Method</span></span>                                                              | <span data-ttu-id="39e1a-119">描述</span><span class="sxs-lookup"><span data-stu-id="39e1a-119">Description</span></span>                                                                    |
|:--------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="39e1a-120">**ClientFillBuffer**</span><span class="sxs-lookup"><span data-stu-id="39e1a-120">**ClientFillBuffer**</span></span>](iorpcdebugnotify-clientfillbuffer.md)       | <span data-ttu-id="39e1a-121">從用戶端偵錯工具將資料傳送至伺服器偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="39e1a-121">Sends data from the client debugger to the server debugger.</span></span><br/>         |
| [<span data-ttu-id="39e1a-122">**ClientGetBufferSize**</span><span class="sxs-lookup"><span data-stu-id="39e1a-122">**ClientGetBufferSize**</span></span>](iorpcdebugnotify-clientgetbuffersize.md) | <span data-ttu-id="39e1a-123">從用戶端偵錯工具抓取 RPC 緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="39e1a-123">Retrieves the RPC buffer size from the client-side debugger.</span></span><br/>        |
| [<span data-ttu-id="39e1a-124">**ClientNotify**</span><span class="sxs-lookup"><span data-stu-id="39e1a-124">**ClientNotify**</span></span>](iorpcdebugnotify-clientnotify.md)               | <span data-ttu-id="39e1a-125">通知用戶端傳出的偵錯工具要求至伺服器。</span><span class="sxs-lookup"><span data-stu-id="39e1a-125">Informs the client of an outgoing debugger request to the server.</span></span><br/>   |
| [<span data-ttu-id="39e1a-126">**ServerFillBuffer**</span><span class="sxs-lookup"><span data-stu-id="39e1a-126">**ServerFillBuffer**</span></span>](iorpcdebugnotify-serverfillbuffer.md)       | <span data-ttu-id="39e1a-127">從伺服器偵錯工具將資料傳送至用戶端偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="39e1a-127">Sends data from the server debugger to the client debugger.</span></span><br/>         |
| [<span data-ttu-id="39e1a-128">**ServerGetBufferSize**</span><span class="sxs-lookup"><span data-stu-id="39e1a-128">**ServerGetBufferSize**</span></span>](iorpcdebugnotify-servergetbuffersize.md) | <span data-ttu-id="39e1a-129">從伺服器端偵錯工具抓取 RPC 緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="39e1a-129">Retrieves the RPC buffer size from the server-side debugger.</span></span><br/>        |
| [<span data-ttu-id="39e1a-130">**ServerNotify**</span><span class="sxs-lookup"><span data-stu-id="39e1a-130">**ServerNotify**</span></span>](iorpcdebugnotify-servernotify.md)               | <span data-ttu-id="39e1a-131">通知伺服器來自用戶端的傳入偵錯工具要求。</span><span class="sxs-lookup"><span data-stu-id="39e1a-131">Informs the server of an incoming debugger request from the client.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="39e1a-132">備註</span><span class="sxs-lookup"><span data-stu-id="39e1a-132">Remarks</span></span>

<span data-ttu-id="39e1a-133">包含 **IOrpcDebugNotify** 介面的匯入程式庫不包含在 Microsoft WINDOWS 軟體開發套件 (SDK) 中。</span><span class="sxs-lookup"><span data-stu-id="39e1a-133">An import library containing the **IOrpcDebugNotify** interface is not included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="39e1a-134">應用程式可以使用 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 和 [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) 函式，從 oleaut.dll 中取出 [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) 的函式指標，並透過 **IOrpcDebugNotify** 介面提供這些方法。</span><span class="sxs-lookup"><span data-stu-id="39e1a-134">An application can use the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) functions to retrieve a function pointer to [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) from oleaut.dll and provide these methods via the **IOrpcDebugNotify** interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="39e1a-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="39e1a-135">Requirements</span></span>



| <span data-ttu-id="39e1a-136">需求</span><span class="sxs-lookup"><span data-stu-id="39e1a-136">Requirement</span></span> | <span data-ttu-id="39e1a-137">值</span><span class="sxs-lookup"><span data-stu-id="39e1a-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="39e1a-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="39e1a-138">Minimum supported client</span></span><br/> | <span data-ttu-id="39e1a-139">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39e1a-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="39e1a-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="39e1a-140">Minimum supported server</span></span><br/> | <span data-ttu-id="39e1a-141">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39e1a-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="39e1a-142">標頭</span><span class="sxs-lookup"><span data-stu-id="39e1a-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="39e1a-143"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="39e1a-143"><dt>N/A</dt></span></span> </dl> |
| <span data-ttu-id="39e1a-144">Idl</span><span class="sxs-lookup"><span data-stu-id="39e1a-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="39e1a-145"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="39e1a-145"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39e1a-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39e1a-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39e1a-147">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="39e1a-147">**IUnknown**</span></span>](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)
</dt> <dt>

[<span data-ttu-id="39e1a-148">**ORPC \_ DBG \_ ALL**</span><span class="sxs-lookup"><span data-stu-id="39e1a-148">**ORPC\_DBG\_ALL**</span></span>](orpc-dbg-all.md)
</dt> <dt>

[<span data-ttu-id="39e1a-149">**ORPC \_ DBG \_ 緩衝區**</span><span class="sxs-lookup"><span data-stu-id="39e1a-149">**ORPC\_DBG\_BUFFER**</span></span>](orpc-dbg-buffer.md)
</dt> <dt>

[<span data-ttu-id="39e1a-150">**ORPC \_ INIT 引數 \_**</span><span class="sxs-lookup"><span data-stu-id="39e1a-150">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="39e1a-151">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="39e1a-151">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> </dl>

 

