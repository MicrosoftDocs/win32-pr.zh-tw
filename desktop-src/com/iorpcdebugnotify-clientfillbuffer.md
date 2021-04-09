---
title: IOrpcDebugNotify ClientFillBuffer 方法
description: 從用戶端偵錯工具將資料傳送至伺服器偵錯工具。
ms.assetid: d575cf34-34a2-4951-a87e-7835b2c5b7a0
keywords:
- ClientFillBuffer 方法 COM
- ClientFillBuffer 方法 COM，IOrpcDebugNotify 介面
- IOrpcDebugNotify 介面 COM，ClientFillBuffer 方法
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ClientFillBuffer
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 633f4f0a8a3e135ca60468d24356a3f6e038d062
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686531"
---
# <a name="iorpcdebugnotifyclientfillbuffer-method"></a><span data-ttu-id="c236b-106">IOrpcDebugNotify：： ClientFillBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="c236b-106">IOrpcDebugNotify::ClientFillBuffer method</span></span>

<span data-ttu-id="c236b-107">從用戶端偵錯工具將資料傳送至伺服器偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="c236b-107">Sends data from the client debugger to the server debugger.</span></span>

> [!Note]  
> <span data-ttu-id="c236b-108">包含 **ClientFillBuffer** 函式的匯入程式庫不包含在 Microsoft WINDOWS 軟體開發套件 (SDK) 中。</span><span class="sxs-lookup"><span data-stu-id="c236b-108">An import library containing the **ClientFillBuffer** function is not included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c236b-109">應用程式可以使用 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 和 [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) 函式，從 oleaut.dll 中取出 [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) 的函式指標，並透過 [**IOrpcDebugNotify**](iorpcdebugnotify.md) 介面提供此函數。</span><span class="sxs-lookup"><span data-stu-id="c236b-109">An application can use the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) functions to retrieve a function pointer to [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) from oleaut.dll and provide this function via the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c236b-110">語法</span><span class="sxs-lookup"><span data-stu-id="c236b-110">Syntax</span></span>


```C++
void ClientFillBuffer(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a><span data-ttu-id="c236b-111">參數</span><span class="sxs-lookup"><span data-stu-id="c236b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c236b-112">*lpOrpcDebugAll*</span><span class="sxs-lookup"><span data-stu-id="c236b-112">*lpOrpcDebugAll*</span></span> 
</dt> <dd>

<span data-ttu-id="c236b-113">[**ORPC \_ DBG \_ 所有**](orpc-dbg-all.md)結構的指標，其中包含 COM RPC 系統傳遞給偵錯工具的通知特定資訊。</span><span class="sxs-lookup"><span data-stu-id="c236b-113">A pointer to a [**ORPC\_DBG\_ALL**](orpc-dbg-all.md) structure that contains notification specific information the COM RPC system passes to the debugger.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c236b-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="c236b-114">Return value</span></span>

<span data-ttu-id="c236b-115">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c236b-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c236b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="c236b-116">Requirements</span></span>



| <span data-ttu-id="c236b-117">需求</span><span class="sxs-lookup"><span data-stu-id="c236b-117">Requirement</span></span> | <span data-ttu-id="c236b-118">值</span><span class="sxs-lookup"><span data-stu-id="c236b-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="c236b-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c236b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c236b-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c236b-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="c236b-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c236b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c236b-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c236b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c236b-123">標頭</span><span class="sxs-lookup"><span data-stu-id="c236b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c236b-124"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="c236b-124"><dt>N/A</dt></span></span> </dl> |
| <span data-ttu-id="c236b-125">Idl</span><span class="sxs-lookup"><span data-stu-id="c236b-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c236b-126"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="c236b-126"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c236b-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c236b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c236b-128">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="c236b-128">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="c236b-129">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="c236b-129">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

