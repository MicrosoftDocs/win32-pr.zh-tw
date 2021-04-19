---
description: 設定虛擬機器的複寫授權專案。
ms.assetid: 39b6b0c4-5515-4863-9038-4c37421abe65
title: Msvm_ReplicationService 類別的 SetAuthorizationEntry 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.SetAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 03b2c2c37a38e957a1b560e2314845abf204ee01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978957"
---
# <a name="setauthorizationentry-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="6cca9-103">Msvm ReplicationService 類別的 SetAuthorizationEntry 方法 \_</span><span class="sxs-lookup"><span data-stu-id="6cca9-103">SetAuthorizationEntry method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="6cca9-104">設定虛擬機器的複寫授權專案。</span><span class="sxs-lookup"><span data-stu-id="6cca9-104">Sets the replication authorization entry for a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cca9-105">語法</span><span class="sxs-lookup"><span data-stu-id="6cca9-105">Syntax</span></span>


```mof
uint32 SetAuthorizationEntry(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 AuthorizationEntry,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6cca9-106">參數</span><span class="sxs-lookup"><span data-stu-id="6cca9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cca9-107">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="6cca9-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cca9-108">[**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem)實例的參考，代表要設定其授權專案的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6cca9-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine to set the authorization entry for.</span></span>

</dd> <dt>

<span data-ttu-id="6cca9-109">*AuthorizationEntry* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6cca9-109">*AuthorizationEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cca9-110">[**Msvm \_ ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md)類別實例的字串表示，定義要用於虛擬機器的授權專案。</span><span class="sxs-lookup"><span data-stu-id="6cca9-110">A string representation of an instance of the [**Msvm\_ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) class that defines the authorization entry to be used for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="6cca9-111">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6cca9-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6cca9-112">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="6cca9-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cca9-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="6cca9-113">Return value</span></span>

<span data-ttu-id="6cca9-114">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="6cca9-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="6cca9-115">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="6cca9-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6cca9-116">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="6cca9-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6cca9-117">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="6cca9-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="6cca9-118">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="6cca9-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="6cca9-119">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="6cca9-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="6cca9-120">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="6cca9-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="6cca9-121">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="6cca9-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="6cca9-122">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="6cca9-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="6cca9-123">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="6cca9-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="6cca9-124">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="6cca9-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="6cca9-125">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="6cca9-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="6cca9-126">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="6cca9-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="6cca9-127">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="6cca9-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="6cca9-128">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="6cca9-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6cca9-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="6cca9-129">Requirements</span></span>



| <span data-ttu-id="6cca9-130">需求</span><span class="sxs-lookup"><span data-stu-id="6cca9-130">Requirement</span></span> | <span data-ttu-id="6cca9-131">值</span><span class="sxs-lookup"><span data-stu-id="6cca9-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cca9-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6cca9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6cca9-133">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6cca9-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6cca9-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6cca9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6cca9-135">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6cca9-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6cca9-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="6cca9-136">Namespace</span></span><br/>                | <span data-ttu-id="6cca9-137">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="6cca9-137">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6cca9-138">MOF</span><span class="sxs-lookup"><span data-stu-id="6cca9-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6cca9-139"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="6cca9-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6cca9-140">DLL</span><span class="sxs-lookup"><span data-stu-id="6cca9-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6cca9-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6cca9-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6cca9-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6cca9-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cca9-143">**AddAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="6cca9-143">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="6cca9-144">**ModifyAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="6cca9-144">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="6cca9-145">**RemoveAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="6cca9-145">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="6cca9-146">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="6cca9-146">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

