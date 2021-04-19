---
description: 在 Windows 網路虛擬化環境中診斷 VM 的網路連線能力。
ms.assetid: c18f48bf-1f57-4a23-a495-462afad42750
title: Msvm_VirtualSystemManagementService 類別的 DiagnoseNetworkConnection 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DiagnoseNetworkConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 70760f771e3908265a4ac70ebc1cbdf957d652c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972378"
---
# <a name="diagnosenetworkconnection-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="06c2d-103">Msvm VirtualSystemManagementService 類別的 DiagnoseNetworkConnection 方法 \_</span><span class="sxs-lookup"><span data-stu-id="06c2d-103">DiagnoseNetworkConnection method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="06c2d-104">在 Windows 網路虛擬化環境中診斷 VM 的網路連線能力。</span><span class="sxs-lookup"><span data-stu-id="06c2d-104">Diagnoses the network connectivity of a VM in a Windows Network Virtualization Environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="06c2d-105">語法</span><span class="sxs-lookup"><span data-stu-id="06c2d-105">Syntax</span></span>


```mof
uint32 DiagnoseNetworkConnection(
  [in]  Msvm_EthernetPortAllocationSettingData REF TargetNetworkAdapter,
  [in]  string                                     DiagnosticSettings,
  [out] string                                     DiagnosticInformation,
  [out] CIM_ConcreteJob                        REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="06c2d-106">參數</span><span class="sxs-lookup"><span data-stu-id="06c2d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06c2d-107">*TargetNetworkAdapter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06c2d-107">*TargetNetworkAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06c2d-108">描述目標網路介面卡的 [**Msvm \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) 參考。</span><span class="sxs-lookup"><span data-stu-id="06c2d-108">Reference to an [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) that describes the target network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="06c2d-109">*DiagnosticSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06c2d-109">*DiagnosticSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06c2d-110">要使用的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="06c2d-110">The diagnostic settings to use.</span></span>

</dd> <dt>

<span data-ttu-id="06c2d-111">*DiagnosticInformation* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="06c2d-111">*DiagnosticInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06c2d-112">成功時，傳回診斷資訊。</span><span class="sxs-lookup"><span data-stu-id="06c2d-112">On success, returns the diagnostic information.</span></span>

</dd> <dt>

<span data-ttu-id="06c2d-113">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="06c2d-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06c2d-114">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="06c2d-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06c2d-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="06c2d-115">Return value</span></span>

<span data-ttu-id="06c2d-116">成功時傳回0或 4096;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="06c2d-116">Returns a 0 or 4096 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="06c2d-117">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="06c2d-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="06c2d-118">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="06c2d-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="06c2d-119">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="06c2d-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="06c2d-120">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="06c2d-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="06c2d-121">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="06c2d-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="06c2d-122">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="06c2d-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="06c2d-123">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="06c2d-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="06c2d-124">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="06c2d-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="06c2d-125">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="06c2d-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="06c2d-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="06c2d-126">Requirements</span></span>



| <span data-ttu-id="06c2d-127">需求</span><span class="sxs-lookup"><span data-stu-id="06c2d-127">Requirement</span></span> | <span data-ttu-id="06c2d-128">值</span><span class="sxs-lookup"><span data-stu-id="06c2d-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06c2d-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="06c2d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="06c2d-130">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="06c2d-130">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="06c2d-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="06c2d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="06c2d-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="06c2d-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="06c2d-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="06c2d-133">Namespace</span></span><br/>                | <span data-ttu-id="06c2d-134">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="06c2d-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="06c2d-135">MOF</span><span class="sxs-lookup"><span data-stu-id="06c2d-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06c2d-136"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="06c2d-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="06c2d-137">DLL</span><span class="sxs-lookup"><span data-stu-id="06c2d-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06c2d-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="06c2d-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="06c2d-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06c2d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06c2d-140">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="06c2d-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

