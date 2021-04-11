---
title: ORPC_DBG_ALL 結構
description: ORPC \_ DBG \_ ALL 結構是用來將參數傳遞至 IOrpcDebugNotify 介面的方法。
ms.assetid: 05371beb-9202-40a6-96d2-4b91497e2ee9
keywords:
- ORPC_DBG_ALL 結構 COM
- LPORPC_DBG_ALL 結構指標 COM
topic_type:
- apiref
api_name:
- ORPC_DBG_ALL
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a17f5b09e5fe2f668bf2bcd21e2e7fe6f0f766a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094208"
---
# <a name="orpc_dbg_all-structure"></a><span data-ttu-id="73796-105">ORPC \_ DBG \_ ALL 結構</span><span class="sxs-lookup"><span data-stu-id="73796-105">ORPC\_DBG\_ALL structure</span></span>

<span data-ttu-id="73796-106">**ORPC \_ DBG \_ ALL** 結構是用來將參數傳遞至 [**IOrpcDebugNotify**](iorpcdebugnotify.md)介面的方法。</span><span class="sxs-lookup"><span data-stu-id="73796-106">The **ORPC\_DBG\_ALL** structure is used to pass parameters to the methods of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

> [!Note]  
> <span data-ttu-id="73796-107">[**IOrpcDebugNotify**](iorpcdebugnotify.md)介面的每個方法都會使用不同的成員組合。</span><span class="sxs-lookup"><span data-stu-id="73796-107">Each method of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface uses a different combination of the members below.</span></span> <span data-ttu-id="73796-108">如果成員未表示為方法所使用，則會在傳遞至該方法時未定義。</span><span class="sxs-lookup"><span data-stu-id="73796-108">If a member is not indicated as used by a method, it is undefined when passed to that method.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="73796-109">語法</span><span class="sxs-lookup"><span data-stu-id="73796-109">Syntax</span></span>


```C++
typedef struct ORPC_DBG_ALL {
  BYTE              *pSignature;
  RPCOLEMESSAGE     *pMessage;
  const IID         *refiid;
  IRpcChannelBuffer *pChannel;
  IUnknown          *pUnkProxyMgr;
  void              *pInterface;
  IUnknown          *pUnkObject;
  HRESULT           hresult;
  void              *pvBuffer;
  ULONG             *cbBuffer;
  ULONG             *lpcbBuffer;
  void              *reserved;
} ORPC_DBG_ALL, *LPORPC_DBG_ALL;
```



## <a name="members"></a><span data-ttu-id="73796-110">成員</span><span class="sxs-lookup"><span data-stu-id="73796-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="73796-111">**pSignature**</span><span class="sxs-lookup"><span data-stu-id="73796-111">**pSignature**</span></span>
</dt> <dd>

<span data-ttu-id="73796-112">**位元組** 緩衝區的指標，其中包含：</span><span class="sxs-lookup"><span data-stu-id="73796-112">A pointer to a **BYTE** buffer that contains:</span></span>

-   <span data-ttu-id="73796-113">前四個位元組：遞增記憶體順序中的 ASCII 字元 "MARB"。</span><span class="sxs-lookup"><span data-stu-id="73796-113">First four bytes: the ASCII characters "MARB" in increasing memory order.</span></span>
-   <span data-ttu-id="73796-114">接下來的16個位元組：識別所呼叫之通知的 **GUID** 。</span><span class="sxs-lookup"><span data-stu-id="73796-114">Next 16 bytes: A **GUID** that identifies the notification being called.</span></span> <span data-ttu-id="73796-115">它包含下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="73796-115">It contains one of the following:</span></span>
    1.  <span data-ttu-id="73796-116">[**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md)：9ED14F80-9673-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="73796-116">[**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md): 9ED14F80-9673-101A-B07B-00DD01113F11</span></span>
    2.  <span data-ttu-id="73796-117">[**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md):D a45f3e0-9673-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="73796-117">[**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md):DA45F3E0-9673-101A-B07B-00DD01113F11</span></span>
    3.  <span data-ttu-id="73796-118">[**ClientNotify**](iorpcdebugnotify-clientnotify.md)：4F60E540-9674-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="73796-118">[**ClientNotify**](iorpcdebugnotify-clientnotify.md):4F60E540-9674-101A-B07B-00DD01113F11</span></span>
    4.  <span data-ttu-id="73796-119">[**ServerNotify**](iorpcdebugnotify-servernotify.md)：1084FA00-9674-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="73796-119">[**ServerNotify**](iorpcdebugnotify-servernotify.md):1084FA00-9674-101A-B07B-00DD01113F11</span></span>
    5.  <span data-ttu-id="73796-120">[**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)：22080240-9674-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="73796-120">[**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md):22080240-9674-101A-B07B-00DD01113F11</span></span>
    6.  <span data-ttu-id="73796-121">[**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)：2FC09500-9674-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="73796-121">[**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md):2FC09500-9674-101A-B07B-00DD01113F11</span></span>
-   <span data-ttu-id="73796-122">接下來四個位元組：保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="73796-122">Next four-bytes: Reserved for future use.</span></span>

> [!Note]
>
> <span data-ttu-id="73796-123">供 [**IOrpcDebugNotify**](iorpcdebugnotify.md) 介面的所有方法使用。</span><span class="sxs-lookup"><span data-stu-id="73796-123">Used by all methods of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

 

</dd> <dt>

<span data-ttu-id="73796-124">**pMessage**</span><span class="sxs-lookup"><span data-stu-id="73796-124">**pMessage**</span></span>
</dt> <dd>

<span data-ttu-id="73796-125">[**RPCOLEMESSAGE**](/windows/win32/api/objidlbase/ns-objidlbase-rpcolemessage)結構的指標，其中包含 RPC 資料封送處理資訊。</span><span class="sxs-lookup"><span data-stu-id="73796-125">A pointer to an [**RPCOLEMESSAGE**](/windows/win32/api/objidlbase/ns-objidlbase-rpcolemessage) structure that contains RPC data marshalling information.</span></span>

> [!Note]
>
> <span data-ttu-id="73796-126">由 [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md)、 [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md)、 [**ClientNotify**](iorpcdebugnotify-clientnotify.md)、 [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)、 [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)和 [**ServerNotify**](iorpcdebugnotify-servernotify.md) 方法所使用。</span><span class="sxs-lookup"><span data-stu-id="73796-126">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="73796-127">**refiid**</span><span class="sxs-lookup"><span data-stu-id="73796-127">**refiid**</span></span>
</dt> <dd>

<span data-ttu-id="73796-128">[**IOrpcDebugNotify**](iorpcdebugnotify.md)介面的 IID 指標。</span><span class="sxs-lookup"><span data-stu-id="73796-128">A pointer to the IID of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

> [!Note]
>
> <span data-ttu-id="73796-129">由 [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md)、 [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md)、 [**ClientNotify**](iorpcdebugnotify-clientnotify.md)、 [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)、 [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)和 [**ServerNotify**](iorpcdebugnotify-servernotify.md) 方法所使用。</span><span class="sxs-lookup"><span data-stu-id="73796-129">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="73796-130">**pChannel**</span><span class="sxs-lookup"><span data-stu-id="73796-130">**pChannel**</span></span>
</dt> <dd>

<span data-ttu-id="73796-131">伺服器上 COM RPC 通道實 [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="73796-131">A pointer to the [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) interface of the COM RPC channel implementation on the server.</span></span>

> [!Note]
>
> <span data-ttu-id="73796-132">由 [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)、 [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)和 [**ServerNotify**](iorpcdebugnotify-servernotify.md) 方法所使用。</span><span class="sxs-lookup"><span data-stu-id="73796-132">Used by the [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="73796-133">**pUnkProxyMgr**</span><span class="sxs-lookup"><span data-stu-id="73796-133">**pUnkProxyMgr**</span></span>
</dt> <dd>

<span data-ttu-id="73796-134">此偵錯工具調用所涉及之物件的 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="73796-134">A pointer to the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface of the object involved in this debugger invocation.</span></span> <span data-ttu-id="73796-135">可能是 **Null**，但這會減少偵錯工具的功能。</span><span class="sxs-lookup"><span data-stu-id="73796-135">May be **NULL**, however, this reduces debugger functionality.</span></span>

> [!Note]
>
> <span data-ttu-id="73796-136">由 [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md)、 [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md)和 [**ClientNotify**](iorpcdebugnotify-clientnotify.md) 方法所使用。</span><span class="sxs-lookup"><span data-stu-id="73796-136">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), and [**ClientNotify**](iorpcdebugnotify-clientnotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="73796-137">**pInterface**</span><span class="sxs-lookup"><span data-stu-id="73796-137">**pInterface**</span></span>
</dt> <dd>

<span data-ttu-id="73796-138">此 RPC 將叫用之方法的 COM 介面指標。</span><span class="sxs-lookup"><span data-stu-id="73796-138">A pointer to the COM interface of the method that will be invoked by this RPC.</span></span> <span data-ttu-id="73796-139">不得為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="73796-139">Must not be **NULL**.</span></span>

> [!Note]
>
> <span data-ttu-id="73796-140">由 [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)、 [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)和 [**ServerNotify**](iorpcdebugnotify-servernotify.md) 方法所使用。</span><span class="sxs-lookup"><span data-stu-id="73796-140">Used by the [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="73796-141">**>punkobject**</span><span class="sxs-lookup"><span data-stu-id="73796-141">**pUnkObject**</span></span>
</dt> <dd>

<span data-ttu-id="73796-142">必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="73796-142">Must be **NULL**.</span></span>

> [!Note]
>
> <span data-ttu-id="73796-143">由 [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)、 [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)和 [**ServerNotify**](iorpcdebugnotify-servernotify.md) 方法所使用。</span><span class="sxs-lookup"><span data-stu-id="73796-143">Used by the [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="73796-144">**hresult**</span><span class="sxs-lookup"><span data-stu-id="73796-144">**hresult**</span></span>
</dt> <dd>

<span data-ttu-id="73796-145">以下是每個通知的成員用途變更：</span><span class="sxs-lookup"><span data-stu-id="73796-145">This member's purpose changes for each of the notifications below:</span></span>

<span data-ttu-id="73796-146">[**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md)：用戶端偵錯工具將傳送至伺服器偵錯工具的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="73796-146">[**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md): the number of bytes the client debugger will transmit to the server debugger.</span></span> <span data-ttu-id="73796-147">如果為零，則不需要傳送任何資訊。</span><span class="sxs-lookup"><span data-stu-id="73796-147">If zero, no information need be transmitted.</span></span>

<span data-ttu-id="73796-148">[**ClientNotify**](iorpcdebugnotify-clientnotify.md)：最後一個 RPC 的 **HRESULT** 。</span><span class="sxs-lookup"><span data-stu-id="73796-148">[**ClientNotify**](iorpcdebugnotify-clientnotify.md): the **HRESULT** of the last RPC.</span></span>

<span data-ttu-id="73796-149">[**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)：用戶端偵錯工具將傳送至伺服器偵錯工具的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="73796-149">[**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md): the number of bytes the client debugger will transmit to the server debugger.</span></span> <span data-ttu-id="73796-150">如果為零，則不需要傳送任何資訊。</span><span class="sxs-lookup"><span data-stu-id="73796-150">If zero, no information need be transmitted.</span></span>

> [!Note]
>
> <span data-ttu-id="73796-151">由 [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md)、 [**ClientNotify**](iorpcdebugnotify-clientnotify.md)和 [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md) 方法所使用。</span><span class="sxs-lookup"><span data-stu-id="73796-151">Used by the [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), and [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="73796-152">**pvBuffer**</span><span class="sxs-lookup"><span data-stu-id="73796-152">**pvBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="73796-153">[**ORPC \_ DBG \_ 緩衝區**](orpc-dbg-buffer.md)結構的指標，其中包含 RPC 封送處理的偵錯工具資訊。</span><span class="sxs-lookup"><span data-stu-id="73796-153">A pointer to an [**ORPC\_DBG\_BUFFER**](orpc-dbg-buffer.md) structure that contains the RPC marshalled debug information.</span></span> <span data-ttu-id="73796-154">如果 **cbBuffer** 為零，則為未定義。</span><span class="sxs-lookup"><span data-stu-id="73796-154">Is undefined if **cbBuffer** is zero.</span></span>

> [!Note]
>
> <span data-ttu-id="73796-155">由 [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md)、 [**ClientNotify**](iorpcdebugnotify-clientnotify.md)、 [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)和 [**ServerNotify**](iorpcdebugnotify-servernotify.md) 方法所使用。</span><span class="sxs-lookup"><span data-stu-id="73796-155">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="73796-156">**cbBuffer**</span><span class="sxs-lookup"><span data-stu-id="73796-156">**cbBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="73796-157">**PvBuffer** 所指向之資料的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="73796-157">The length, in bytes, of the data pointed to by **pvBuffer**.</span></span>

> [!Note]
>
> <span data-ttu-id="73796-158">由 [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md)、 [**ClientNotify**](iorpcdebugnotify-clientnotify.md)、 [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)和 [**ServerNotify**](iorpcdebugnotify-servernotify.md) 方法所使用。</span><span class="sxs-lookup"><span data-stu-id="73796-158">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="73796-159">**lpcbBuffer**</span><span class="sxs-lookup"><span data-stu-id="73796-159">**lpcbBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="73796-160">用戶端偵錯工具將傳送至伺服器偵錯工具的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="73796-160">The number of bytes the client debugger will transmit to the server debugger.</span></span> <span data-ttu-id="73796-161">如果為零，則不需要傳送任何資訊。</span><span class="sxs-lookup"><span data-stu-id="73796-161">If zero, no information need be transmitted.</span></span> <span data-ttu-id="73796-162">此值會取代 **hresult** 中傳回的值。</span><span class="sxs-lookup"><span data-stu-id="73796-162">This value supersedes the value returned in **hresult**.</span></span>

> [!Note]
>
> <span data-ttu-id="73796-163">由 [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md)、 [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md) 方法使用。</span><span class="sxs-lookup"><span data-stu-id="73796-163">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="73796-164">**保留**</span><span class="sxs-lookup"><span data-stu-id="73796-164">**reserved**</span></span>
</dt> <dd>

<span data-ttu-id="73796-165">保留的。</span><span class="sxs-lookup"><span data-stu-id="73796-165">Reserved.</span></span> <span data-ttu-id="73796-166">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="73796-166">Do not use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="73796-167">規格需求</span><span class="sxs-lookup"><span data-stu-id="73796-167">Requirements</span></span>



| <span data-ttu-id="73796-168">需求</span><span class="sxs-lookup"><span data-stu-id="73796-168">Requirement</span></span> | <span data-ttu-id="73796-169">值</span><span class="sxs-lookup"><span data-stu-id="73796-169">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="73796-170">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73796-170">Minimum supported client</span></span><br/> | <span data-ttu-id="73796-171">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73796-171">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="73796-172">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73796-172">Minimum supported server</span></span><br/> | <span data-ttu-id="73796-173">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73796-173">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="73796-174">標頭</span><span class="sxs-lookup"><span data-stu-id="73796-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="73796-175"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="73796-175"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73796-176">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73796-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73796-177">**ORPC \_ DBG \_ 緩衝區**</span><span class="sxs-lookup"><span data-stu-id="73796-177">**ORPC\_DBG\_BUFFER**</span></span>](orpc-dbg-buffer.md)
</dt> <dt>

[<span data-ttu-id="73796-178">**ORPC \_ INIT 引數 \_**</span><span class="sxs-lookup"><span data-stu-id="73796-178">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="73796-179">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="73796-179">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="73796-180">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="73796-180">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

