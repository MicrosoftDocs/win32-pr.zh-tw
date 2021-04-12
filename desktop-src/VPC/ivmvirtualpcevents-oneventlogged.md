---
title: 'IVMVirtualPCEvents OnEventLogged 方法 (VPCCOMInterfaces .h) '
description: 接收 Windows Virtual PC 記錄事件的通知。
ms.assetid: 89439e8e-e9bf-409e-a129-525b9feb8fdd
keywords:
- OnEventLogged 方法 Virtual PC
- OnEventLogged 方法 Virtual PC，IVMVirtualPCEvents 介面
- IVMVirtualPCEvents 介面 Virtual PC，OnEventLogged 方法
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents.OnEventLogged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 196d480383f488c9c0885e95857c8d1a053d5887
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508727"
---
# <a name="ivmvirtualpceventsoneventlogged-method"></a><span data-ttu-id="3bd66-106">IVMVirtualPCEvents：： OnEventLogged 方法</span><span class="sxs-lookup"><span data-stu-id="3bd66-106">IVMVirtualPCEvents::OnEventLogged method</span></span>

<span data-ttu-id="3bd66-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="3bd66-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3bd66-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="3bd66-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3bd66-109">接收 Windows Virtual PC 記錄事件的通知。</span><span class="sxs-lookup"><span data-stu-id="3bd66-109">Receives notification that Windows Virtual PC logs an event.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bd66-110">語法</span><span class="sxs-lookup"><span data-stu-id="3bd66-110">Syntax</span></span>


```C++
HRESULT OnEventLogged(
  [in] long logMessageID
);
```



## <a name="parameters"></a><span data-ttu-id="3bd66-111">參數</span><span class="sxs-lookup"><span data-stu-id="3bd66-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bd66-112">*logMessageID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3bd66-112">*logMessageID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bd66-113">已記錄之事件記錄檔訊息的訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="3bd66-113">The message identifier of the event log message that was logged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bd66-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="3bd66-114">Return value</span></span>

<span data-ttu-id="3bd66-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="3bd66-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3bd66-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3bd66-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bd66-117">備註</span><span class="sxs-lookup"><span data-stu-id="3bd66-117">Remarks</span></span>

<span data-ttu-id="3bd66-118">當 Windows Virtual PC 將訊息記錄到 Windows 事件記錄檔時，就會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="3bd66-118">This method is called when Windows Virtual PC logs a message to the Windows event log.</span></span> <span data-ttu-id="3bd66-119">用戶端程式必須執行這個介面方法，以接收來自 [**IVMVirtualPC**](ivmvirtualpc.md)的 **vmVirtualPCEvent \_ EventLogged** 事件的通知。</span><span class="sxs-lookup"><span data-stu-id="3bd66-119">The client program must implement this interface method to receive notification of the **vmVirtualPCEvent\_EventLogged** event originating from [**IVMVirtualPC**](ivmvirtualpc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3bd66-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="3bd66-120">Requirements</span></span>



| <span data-ttu-id="3bd66-121">需求</span><span class="sxs-lookup"><span data-stu-id="3bd66-121">Requirement</span></span> | <span data-ttu-id="3bd66-122">值</span><span class="sxs-lookup"><span data-stu-id="3bd66-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bd66-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3bd66-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3bd66-124">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3bd66-124">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3bd66-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3bd66-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3bd66-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="3bd66-126">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3bd66-127">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="3bd66-127">End of client support</span></span><br/>    | <span data-ttu-id="3bd66-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3bd66-128">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3bd66-129">產品</span><span class="sxs-lookup"><span data-stu-id="3bd66-129">Product</span></span><br/>                  | <span data-ttu-id="3bd66-130">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3bd66-130">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3bd66-131">標頭</span><span class="sxs-lookup"><span data-stu-id="3bd66-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bd66-132"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="3bd66-132"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3bd66-133">IID</span><span class="sxs-lookup"><span data-stu-id="3bd66-133">IID</span></span><br/>                      | <span data-ttu-id="3bd66-134">DIID \_ IVMVirtualPCEvents 定義為 efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span><span class="sxs-lookup"><span data-stu-id="3bd66-134">DIID\_IVMVirtualPCEvents is defined as efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="3bd66-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3bd66-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bd66-136">**IVMVirtualPCEvents**</span><span class="sxs-lookup"><span data-stu-id="3bd66-136">**IVMVirtualPCEvents**</span></span>](ivmvirtualpcevents.md)
</dt> </dl>

 

