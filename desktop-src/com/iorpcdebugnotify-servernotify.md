---
title: IOrpcDebugNotify ServerNotify 方法
description: 通知伺服器來自用戶端的傳入偵錯工具要求。
ms.assetid: 6c868b9e-f25b-4d27-80ff-697d0c005b8d
keywords:
- ServerNotify 方法 COM
- ServerNotify 方法 COM，IOrpcDebugNotify 介面
- IOrpcDebugNotify 介面 COM，ServerNotify 方法
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ServerNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d6dab7cf68b305e83212045851a88e1cdecdde9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935057"
---
# <a name="iorpcdebugnotifyservernotify-method"></a><span data-ttu-id="60f3f-106">IOrpcDebugNotify：： ServerNotify 方法</span><span class="sxs-lookup"><span data-stu-id="60f3f-106">IOrpcDebugNotify::ServerNotify method</span></span>

<span data-ttu-id="60f3f-107">通知伺服器來自用戶端的傳入偵錯工具要求。</span><span class="sxs-lookup"><span data-stu-id="60f3f-107">Informs the server of an incoming debugger request from the client.</span></span>

> [!Note]  
> <span data-ttu-id="60f3f-108">包含 **ServerNotify** 函式的匯入程式庫不包含在 Microsoft WINDOWS 軟體開發套件 (SDK) 中。</span><span class="sxs-lookup"><span data-stu-id="60f3f-108">An import library containing the **ServerNotify** function is not included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="60f3f-109">應用程式可以使用 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 和 [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) 函式，從 oleaut.dll 中取出 [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) 的函式指標，並透過 [**IOrpcDebugNotify**](iorpcdebugnotify.md) 介面提供此函數。</span><span class="sxs-lookup"><span data-stu-id="60f3f-109">An application can use the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) functions to retrieve a function pointer to [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) from oleaut.dll and provide this function via the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="60f3f-110">語法</span><span class="sxs-lookup"><span data-stu-id="60f3f-110">Syntax</span></span>


```C++
void ServerNotify(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a><span data-ttu-id="60f3f-111">參數</span><span class="sxs-lookup"><span data-stu-id="60f3f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60f3f-112">*lpOrpcDebugAll*</span><span class="sxs-lookup"><span data-stu-id="60f3f-112">*lpOrpcDebugAll*</span></span> 
</dt> <dd>

<span data-ttu-id="60f3f-113">[**ORPC \_ DBG \_ 所有**](orpc-dbg-all.md)結構的指標，其中包含 COM RPC 系統傳遞給偵錯工具的通知特定資訊。</span><span class="sxs-lookup"><span data-stu-id="60f3f-113">A pointer to a [**ORPC\_DBG\_ALL**](orpc-dbg-all.md) structure that contains notification specific information the COM RPC system passes to the debugger.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60f3f-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="60f3f-114">Return value</span></span>

<span data-ttu-id="60f3f-115">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="60f3f-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="60f3f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="60f3f-116">Requirements</span></span>



| <span data-ttu-id="60f3f-117">需求</span><span class="sxs-lookup"><span data-stu-id="60f3f-117">Requirement</span></span> | <span data-ttu-id="60f3f-118">值</span><span class="sxs-lookup"><span data-stu-id="60f3f-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="60f3f-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="60f3f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="60f3f-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="60f3f-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="60f3f-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="60f3f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="60f3f-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="60f3f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="60f3f-123">標頭</span><span class="sxs-lookup"><span data-stu-id="60f3f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="60f3f-124"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="60f3f-124"><dt>N/A</dt></span></span> </dl> |
| <span data-ttu-id="60f3f-125">Idl</span><span class="sxs-lookup"><span data-stu-id="60f3f-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="60f3f-126"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="60f3f-126"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60f3f-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="60f3f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60f3f-128">**ORPC \_ INIT 引數 \_**</span><span class="sxs-lookup"><span data-stu-id="60f3f-128">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="60f3f-129">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="60f3f-129">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="60f3f-130">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="60f3f-130">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

