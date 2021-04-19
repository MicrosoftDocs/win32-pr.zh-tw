---
description: 設定要在容錯移轉之後套用至虛擬機器的網路介面卡 IP 設定。
ms.assetid: a49d089e-f5dc-4bfb-9f66-2593304b9795
title: Msvm_ReplicationService 類別的 SetFailoverNetworkAdapterSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.SetFailoverNetworkAdapterSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: da5bb8c820e1dbca5103c430a7b2ce2a525a8fca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106999891"
---
# <a name="setfailovernetworkadaptersettings-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="7a7c3-103">Msvm ReplicationService 類別的 SetFailoverNetworkAdapterSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="7a7c3-103">SetFailoverNetworkAdapterSettings method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="7a7c3-104">設定要在容錯移轉之後套用至虛擬機器的網路介面卡 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="7a7c3-104">Configures the network adapter's IP settings to be applied to a virtual machine after a failover.</span></span> <span data-ttu-id="7a7c3-105">這些設定參數會在容錯移轉作業之後套用，並在與客體作業系統內執行的 KVP Exchange 整合元件建立通訊時立即套用。</span><span class="sxs-lookup"><span data-stu-id="7a7c3-105">These configuration parameters are applied after a failover operation, immediately upon establishing communication with the KVP Exchange integration component running within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a7c3-106">語法</span><span class="sxs-lookup"><span data-stu-id="7a7c3-106">Syntax</span></span>


```mof
uint32 SetFailoverNetworkAdapterSettings(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 NetworkSettings[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="7a7c3-107">參數</span><span class="sxs-lookup"><span data-stu-id="7a7c3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a7c3-108">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="7a7c3-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a7c3-109">[**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem)實例的參考，代表要設定其網路介面卡的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="7a7c3-109">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine whose network adapters are to be configured.</span></span>

</dd> <dt>

<span data-ttu-id="7a7c3-110">*NetworkSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7a7c3-110">*NetworkSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a7c3-111">[**Msvm \_ FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md)物件的內嵌實例陣列。</span><span class="sxs-lookup"><span data-stu-id="7a7c3-111">An array of embedded instances of [**Msvm\_FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md) objects.</span></span> <span data-ttu-id="7a7c3-112">每個實例都會描述虛擬機器中其中一個網路介面卡的設定參數。</span><span class="sxs-lookup"><span data-stu-id="7a7c3-112">Each instance describes the configuration parameters for one of the network adapters within the virtual machine.</span></span> <span data-ttu-id="7a7c3-113">您必須在每個實例上指定 **IPAddresses** 和 **DHCPEnabled** 屬性。</span><span class="sxs-lookup"><span data-stu-id="7a7c3-113">The **IPAddresses** and **DHCPEnabled** properties must be specified on each instance.</span></span>

</dd> <dt>

<span data-ttu-id="7a7c3-114">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7a7c3-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a7c3-115">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="7a7c3-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a7c3-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="7a7c3-116">Return value</span></span>

<span data-ttu-id="7a7c3-117">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="7a7c3-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="7a7c3-118">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="7a7c3-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7a7c3-119">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="7a7c3-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7a7c3-120">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="7a7c3-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="7a7c3-121">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="7a7c3-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="7a7c3-122">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="7a7c3-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="7a7c3-123">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="7a7c3-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="7a7c3-124">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="7a7c3-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="7a7c3-125">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="7a7c3-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="7a7c3-126">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="7a7c3-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="7a7c3-127">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="7a7c3-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="7a7c3-128">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="7a7c3-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="7a7c3-129">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="7a7c3-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="7a7c3-130">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="7a7c3-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7a7c3-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a7c3-131">Requirements</span></span>



| <span data-ttu-id="7a7c3-132">需求</span><span class="sxs-lookup"><span data-stu-id="7a7c3-132">Requirement</span></span> | <span data-ttu-id="7a7c3-133">值</span><span class="sxs-lookup"><span data-stu-id="7a7c3-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a7c3-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7a7c3-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7a7c3-135">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a7c3-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7a7c3-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7a7c3-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7a7c3-137">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a7c3-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7a7c3-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="7a7c3-138">Namespace</span></span><br/>                | <span data-ttu-id="7a7c3-139">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="7a7c3-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7a7c3-140">MOF</span><span class="sxs-lookup"><span data-stu-id="7a7c3-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a7c3-141"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="7a7c3-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7a7c3-142">DLL</span><span class="sxs-lookup"><span data-stu-id="7a7c3-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a7c3-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7a7c3-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7a7c3-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7a7c3-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a7c3-145">**InitiateFailover**</span><span class="sxs-lookup"><span data-stu-id="7a7c3-145">**InitiateFailover**</span></span>](initiatefailover-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="7a7c3-146">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="7a7c3-146">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="7a7c3-147">**RevertFailover**</span><span class="sxs-lookup"><span data-stu-id="7a7c3-147">**RevertFailover**</span></span>](revertfailover-msvm-replicationservice.md)
</dt> </dl>

 

