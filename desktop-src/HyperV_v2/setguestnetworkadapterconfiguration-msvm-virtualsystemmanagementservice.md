---
description: 設定客體作業系統內的網路介面卡。
ms.assetid: 698e0c17-f8bd-433f-b982-5481f9701ba6
title: Msvm_VirtualSystemManagementService 類別的 SetGuestNetworkAdapterConfiguration 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.SetGuestNetworkAdapterConfiguration
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 02c79df7aa08faa842e2b702b4cf18944e96bdfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513356"
---
# <a name="setguestnetworkadapterconfiguration-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="b8fdf-103">Msvm VirtualSystemManagementService 類別的 SetGuestNetworkAdapterConfiguration 方法 \_</span><span class="sxs-lookup"><span data-stu-id="b8fdf-103">SetGuestNetworkAdapterConfiguration method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="b8fdf-104">設定客體作業系統內的網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="b8fdf-104">Configures the network adapters within the guest operating system.</span></span> <span data-ttu-id="b8fdf-105">這些設定參數會在與在客體作業系統內執行的 KVP Exchange 整合元件建立通訊時立即套用。</span><span class="sxs-lookup"><span data-stu-id="b8fdf-105">These configuration parameters are applied immediately upon establishing communication with the KVP Exchange integration component running within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8fdf-106">語法</span><span class="sxs-lookup"><span data-stu-id="b8fdf-106">Syntax</span></span>


```mof
uint32 SetGuestNetworkAdapterConfiguration(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 NetworkConfiguration[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="b8fdf-107">參數</span><span class="sxs-lookup"><span data-stu-id="b8fdf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8fdf-108">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="b8fdf-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8fdf-109">要設定其網路介面卡之 [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) 實例實例的參考。</span><span class="sxs-lookup"><span data-stu-id="b8fdf-109">A reference to the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance whose network adapters are to be configured.</span></span>

</dd> <dt>

<span data-ttu-id="b8fdf-110">*NetworkConfiguration* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b8fdf-110">*NetworkConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8fdf-111">[**Msvm \_ GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md)類別的內嵌實例陣列。</span><span class="sxs-lookup"><span data-stu-id="b8fdf-111">An array of embedded instances of the [**Msvm\_GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) class.</span></span> <span data-ttu-id="b8fdf-112">每個實例都會描述虛擬機器中其中一個網路介面卡的設定參數。</span><span class="sxs-lookup"><span data-stu-id="b8fdf-112">Each instance describes the configuration parameters for one of the network adapters within the virtual machine.</span></span> <span data-ttu-id="b8fdf-113">每個實例都必須指定 **DHCPEnabled** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b8fdf-113">The **DHCPEnabled** property must be specified for each instance.</span></span>

</dd> <dt>

<span data-ttu-id="b8fdf-114">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b8fdf-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8fdf-115">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="b8fdf-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8fdf-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="b8fdf-116">Return value</span></span>

<span data-ttu-id="b8fdf-117">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="b8fdf-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b8fdf-118">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="b8fdf-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b8fdf-119">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="b8fdf-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b8fdf-120">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="b8fdf-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="b8fdf-121">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="b8fdf-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="b8fdf-122">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="b8fdf-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="b8fdf-123">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="b8fdf-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="b8fdf-124">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="b8fdf-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="b8fdf-125">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="b8fdf-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="b8fdf-126">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="b8fdf-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="b8fdf-127">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="b8fdf-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="b8fdf-128">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="b8fdf-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="b8fdf-129">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="b8fdf-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="b8fdf-130">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="b8fdf-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b8fdf-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8fdf-131">Requirements</span></span>



| <span data-ttu-id="b8fdf-132">需求</span><span class="sxs-lookup"><span data-stu-id="b8fdf-132">Requirement</span></span> | <span data-ttu-id="b8fdf-133">值</span><span class="sxs-lookup"><span data-stu-id="b8fdf-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8fdf-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8fdf-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b8fdf-135">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8fdf-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b8fdf-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8fdf-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b8fdf-137">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8fdf-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b8fdf-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="b8fdf-138">Namespace</span></span><br/>                | <span data-ttu-id="b8fdf-139">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="b8fdf-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b8fdf-140">MOF</span><span class="sxs-lookup"><span data-stu-id="b8fdf-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8fdf-141"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="b8fdf-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8fdf-142">DLL</span><span class="sxs-lookup"><span data-stu-id="b8fdf-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8fdf-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b8fdf-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b8fdf-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8fdf-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8fdf-145">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="b8fdf-145">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

