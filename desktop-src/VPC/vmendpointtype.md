---
title: 'VMEndpointType 列舉 (VPCCOMInterfaces) '
description: 指定端點類型。
ms.assetid: b48bd860-50dc-4c8c-b65b-69c407d4612a
keywords:
- VMEndpointType 列舉虛擬電腦
topic_type:
- apiref
api_name:
- VMEndpointType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 912eb43147af03dd2b9923c4bdb778044f40d023
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843508"
---
# <a name="vmendpointtype-enumeration"></a><span data-ttu-id="8ddda-104">VMEndpointType 列舉</span><span class="sxs-lookup"><span data-stu-id="8ddda-104">VMEndpointType enumeration</span></span>

<span data-ttu-id="8ddda-105">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="8ddda-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8ddda-106">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="8ddda-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8ddda-107">指定端點類型。</span><span class="sxs-lookup"><span data-stu-id="8ddda-107">Specifies the endpoint type.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ddda-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ddda-108">Syntax</span></span>


```C++
typedef enum  { 
  vmEndpoint_NamedPipe  = 0,
  vmEndpoint_TCPIP      = 1
} VMEndpointType;
```



## <a name="constants"></a><span data-ttu-id="8ddda-109">常數</span><span class="sxs-lookup"><span data-stu-id="8ddda-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8ddda-110"><span id="vmEndpoint_NamedPipe"></span><span id="vmendpoint_namedpipe"></span><span id="VMENDPOINT_NAMEDPIPE"></span>**vmEndpoint \_ NamedPipe**</span><span class="sxs-lookup"><span data-stu-id="8ddda-110"><span id="vmEndpoint_NamedPipe"></span><span id="vmendpoint_namedpipe"></span><span id="VMENDPOINT_NAMEDPIPE"></span>**vmEndpoint\_NamedPipe**</span></span>
</dt> <dd>

<span data-ttu-id="8ddda-111">主控制項端。</span><span class="sxs-lookup"><span data-stu-id="8ddda-111">The host side.</span></span>

</dd> <dt>

<span data-ttu-id="8ddda-112"><span id="vmEndpoint_TCPIP"></span><span id="vmendpoint_tcpip"></span><span id="VMENDPOINT_TCPIP"></span>**vmEndpoint \_ TCPIP**</span><span class="sxs-lookup"><span data-stu-id="8ddda-112"><span id="vmEndpoint_TCPIP"></span><span id="vmendpoint_tcpip"></span><span id="VMENDPOINT_TCPIP"></span>**vmEndpoint\_TCPIP**</span></span>
</dt> <dd>

<span data-ttu-id="8ddda-113">來賓端。</span><span class="sxs-lookup"><span data-stu-id="8ddda-113">The guest side.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8ddda-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ddda-114">Requirements</span></span>



| <span data-ttu-id="8ddda-115">需求</span><span class="sxs-lookup"><span data-stu-id="8ddda-115">Requirement</span></span> | <span data-ttu-id="8ddda-116">值</span><span class="sxs-lookup"><span data-stu-id="8ddda-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ddda-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8ddda-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8ddda-118">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ddda-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8ddda-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8ddda-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8ddda-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="8ddda-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8ddda-121">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="8ddda-121">End of client support</span></span><br/>    | <span data-ttu-id="8ddda-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8ddda-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8ddda-123">產品</span><span class="sxs-lookup"><span data-stu-id="8ddda-123">Product</span></span><br/>                  | <span data-ttu-id="8ddda-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8ddda-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8ddda-125">標頭</span><span class="sxs-lookup"><span data-stu-id="8ddda-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ddda-126"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="8ddda-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ddda-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ddda-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ddda-128">**IVMVirtualMachine::StartCommunicationChannel**</span><span class="sxs-lookup"><span data-stu-id="8ddda-128">**IVMVirtualMachine::StartCommunicationChannel**</span></span>](ivmvirtualmachine-startcommunicationchannel.md)
</dt> </dl>

 

