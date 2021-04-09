---
description: 在 Windows 網路虛擬化環境中測試 VM 的網路連線能力。
ms.assetid: 37d4c34d-406e-4c52-afce-b0eef754eeb3
title: Msvm_VirtualSystemManagementService 類別的 TestNetworkConnection 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.TestNetworkConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e8f15faacb1b8ad683b1ea9abfa9b91f5c376dab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112284"
---
# <a name="testnetworkconnection-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="24a1f-103">Msvm VirtualSystemManagementService 類別的 TestNetworkConnection 方法 \_</span><span class="sxs-lookup"><span data-stu-id="24a1f-103">TestNetworkConnection method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="24a1f-104">在 Windows 網路虛擬化環境中測試 VM 的網路連線能力。</span><span class="sxs-lookup"><span data-stu-id="24a1f-104">Tests the network connectivity of a VM in a Windows network virtualization environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="24a1f-105">語法</span><span class="sxs-lookup"><span data-stu-id="24a1f-105">Syntax</span></span>


```mof
uint32 TestNetworkConnection(
  [in]  Msvm_EthernetPortAllocationSettingData REF TargetNetworkAdapter,
  [in]  boolean                                    IsSender,
  [in]  string                                     SenderIP,
  [in]  string                                     ReceiverIP,
  [in]  string                                     ReceiverMac,
  [in]  uint32                                     IsolationId,
  [in]  uint32                                     SequenceNumber,
  [out] uint32                                     RoundTripTime,
  [out] CIM_ConcreteJob                        REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="24a1f-106">參數</span><span class="sxs-lookup"><span data-stu-id="24a1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24a1f-107">*TargetNetworkAdapter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="24a1f-107">*TargetNetworkAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24a1f-108">描述目標網路介面卡的 [**Msvm \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) 參考。</span><span class="sxs-lookup"><span data-stu-id="24a1f-108">Reference to a [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) describing the target network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="24a1f-109">*IsSender* \[在\]</span><span class="sxs-lookup"><span data-stu-id="24a1f-109">*IsSender* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24a1f-110">指出是否要在傳送者端或接收者叫用此方法。</span><span class="sxs-lookup"><span data-stu-id="24a1f-110">Indicates whether this method is being invoked at the sender or the receiver.</span></span>

</dd> <dt>

<span data-ttu-id="24a1f-111">*SenderIP* \[在\]</span><span class="sxs-lookup"><span data-stu-id="24a1f-111">*SenderIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24a1f-112">寄件者 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="24a1f-112">The sender IP address.</span></span>

</dd> <dt>

<span data-ttu-id="24a1f-113">*ReceiverIP* \[在\]</span><span class="sxs-lookup"><span data-stu-id="24a1f-113">*ReceiverIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24a1f-114">寄件者 Mac 位址。</span><span class="sxs-lookup"><span data-stu-id="24a1f-114">The sender Mac address.</span></span>

</dd> <dt>

<span data-ttu-id="24a1f-115">*ReceiverMac* \[在\]</span><span class="sxs-lookup"><span data-stu-id="24a1f-115">*ReceiverMac* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24a1f-116">寄件者 Mac 位址。</span><span class="sxs-lookup"><span data-stu-id="24a1f-116">The sender Mac address.</span></span>

</dd> <dt>

<span data-ttu-id="24a1f-117">*IsolationId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="24a1f-117">*IsolationId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24a1f-118">隔離識別碼。</span><span class="sxs-lookup"><span data-stu-id="24a1f-118">The Isolation ID.</span></span>

</dd> <dt>

<span data-ttu-id="24a1f-119">*SequenceNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="24a1f-119">*SequenceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24a1f-120">隔離識別碼。</span><span class="sxs-lookup"><span data-stu-id="24a1f-120">The Isolation ID.</span></span>

</dd> <dt>

<span data-ttu-id="24a1f-121">*RoundTripTime* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="24a1f-121">*RoundTripTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24a1f-122">來回行程時間。</span><span class="sxs-lookup"><span data-stu-id="24a1f-122">The round trip time.</span></span>

</dd> <dt>

<span data-ttu-id="24a1f-123">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="24a1f-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24a1f-124">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="24a1f-124">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24a1f-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="24a1f-125">Return value</span></span>

<span data-ttu-id="24a1f-126">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="24a1f-126">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="24a1f-127">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="24a1f-127">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="24a1f-128">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="24a1f-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="24a1f-129">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="24a1f-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="24a1f-130">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="24a1f-130">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="24a1f-131">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="24a1f-131">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="24a1f-132">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="24a1f-132">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="24a1f-133">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="24a1f-133">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="24a1f-134">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="24a1f-134">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="24a1f-135">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="24a1f-135">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="24a1f-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="24a1f-136">Requirements</span></span>



| <span data-ttu-id="24a1f-137">需求</span><span class="sxs-lookup"><span data-stu-id="24a1f-137">Requirement</span></span> | <span data-ttu-id="24a1f-138">值</span><span class="sxs-lookup"><span data-stu-id="24a1f-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24a1f-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="24a1f-139">Minimum supported client</span></span><br/> | <span data-ttu-id="24a1f-140">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="24a1f-140">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="24a1f-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="24a1f-141">Minimum supported server</span></span><br/> | <span data-ttu-id="24a1f-142">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="24a1f-142">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="24a1f-143">命名空間</span><span class="sxs-lookup"><span data-stu-id="24a1f-143">Namespace</span></span><br/>                | <span data-ttu-id="24a1f-144">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="24a1f-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="24a1f-145">MOF</span><span class="sxs-lookup"><span data-stu-id="24a1f-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24a1f-146"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="24a1f-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="24a1f-147">DLL</span><span class="sxs-lookup"><span data-stu-id="24a1f-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24a1f-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="24a1f-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="24a1f-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="24a1f-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24a1f-150">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="24a1f-150">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

