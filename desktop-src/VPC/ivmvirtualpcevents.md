---
title: 'IVMVirtualPCEvents 介面 (VPCCOMInterfaces .h) '
description: 定義 IVMVirtualPC 介面的外寄事件介面。
ms.assetid: 40ce14d8-43e4-4c72-9729-e5503d882be6
keywords:
- IVMVirtualPCEvents 介面 Virtual PC
- IVMVirtualPCEvents 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3a6fd22f75027d1424b8605e8e36e373064069
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025337"
---
# <a name="ivmvirtualpcevents-interface"></a><span data-ttu-id="8f7fe-105">IVMVirtualPCEvents 介面</span><span class="sxs-lookup"><span data-stu-id="8f7fe-105">IVMVirtualPCEvents interface</span></span>

<span data-ttu-id="8f7fe-106">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="8f7fe-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8f7fe-107">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="8f7fe-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8f7fe-108">定義 [**IVMVirtualPC**](ivmvirtualpc.md) 介面的外寄事件介面。</span><span class="sxs-lookup"><span data-stu-id="8f7fe-108">Defines the outgoing event interface for the [**IVMVirtualPC**](ivmvirtualpc.md) interface.</span></span> <span data-ttu-id="8f7fe-109">用戶端會執行這些方法來接收從 [**IVMVirtualPC**](ivmvirtualpc.md)傳送的事件。</span><span class="sxs-lookup"><span data-stu-id="8f7fe-109">The client implements these methods to receive events sent from [**IVMVirtualPC**](ivmvirtualpc.md).</span></span>

## <a name="members"></a><span data-ttu-id="8f7fe-110">成員</span><span class="sxs-lookup"><span data-stu-id="8f7fe-110">Members</span></span>

<span data-ttu-id="8f7fe-111">**IVMVirtualPCEvents** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="8f7fe-111">The **IVMVirtualPCEvents** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="8f7fe-112">**IVMVirtualPCEvents** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8f7fe-112">**IVMVirtualPCEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="8f7fe-113">方法</span><span class="sxs-lookup"><span data-stu-id="8f7fe-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8f7fe-114">方法</span><span class="sxs-lookup"><span data-stu-id="8f7fe-114">Methods</span></span>

<span data-ttu-id="8f7fe-115">**IVMVirtualPCEvents** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="8f7fe-115">The **IVMVirtualPCEvents** interface has these methods.</span></span>



| <span data-ttu-id="8f7fe-116">方法</span><span class="sxs-lookup"><span data-stu-id="8f7fe-116">Method</span></span>                                                        | <span data-ttu-id="8f7fe-117">描述</span><span class="sxs-lookup"><span data-stu-id="8f7fe-117">Description</span></span>                                                                  |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="8f7fe-118">**OnEventLogged**</span><span class="sxs-lookup"><span data-stu-id="8f7fe-118">**OnEventLogged**</span></span>](ivmvirtualpcevents-oneventlogged.md)     | <span data-ttu-id="8f7fe-119">接收 Windows Virtual PC 記錄事件的通知。</span><span class="sxs-lookup"><span data-stu-id="8f7fe-119">Receives notification that Windows Virtual PC logs an event.</span></span><br/>      |
| [<span data-ttu-id="8f7fe-120">**OnVMStateChange**</span><span class="sxs-lookup"><span data-stu-id="8f7fe-120">**OnVMStateChange**</span></span>](ivmvirtualpcevents-onvmstatechange.md) | <span data-ttu-id="8f7fe-121">收到虛擬機器的狀態已變更的通知。</span><span class="sxs-lookup"><span data-stu-id="8f7fe-121">Receives notification that a virtual machine's state has changed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8f7fe-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f7fe-122">Requirements</span></span>



| <span data-ttu-id="8f7fe-123">需求</span><span class="sxs-lookup"><span data-stu-id="8f7fe-123">Requirement</span></span> | <span data-ttu-id="8f7fe-124">值</span><span class="sxs-lookup"><span data-stu-id="8f7fe-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f7fe-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8f7fe-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8f7fe-126">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f7fe-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8f7fe-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8f7fe-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8f7fe-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="8f7fe-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8f7fe-129">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="8f7fe-129">End of client support</span></span><br/>    | <span data-ttu-id="8f7fe-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8f7fe-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8f7fe-131">產品</span><span class="sxs-lookup"><span data-stu-id="8f7fe-131">Product</span></span><br/>                  | <span data-ttu-id="8f7fe-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8f7fe-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8f7fe-133">標頭</span><span class="sxs-lookup"><span data-stu-id="8f7fe-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f7fe-134"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="8f7fe-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8f7fe-135">IID</span><span class="sxs-lookup"><span data-stu-id="8f7fe-135">IID</span></span><br/>                      | <span data-ttu-id="8f7fe-136">DIID \_ IVMVirtualPCEvents 定義為 efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span><span class="sxs-lookup"><span data-stu-id="8f7fe-136">DIID\_IVMVirtualPCEvents is defined as efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span></span><br/>        |



 

