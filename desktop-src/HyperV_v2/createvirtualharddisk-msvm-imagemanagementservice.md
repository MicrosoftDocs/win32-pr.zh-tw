---
description: 建立虛擬硬碟檔案。
ms.assetid: 6c136000-1df2-4456-833c-094671408338
title: Msvm_ImageManagementService 類別的 CreateVirtualHardDisk 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.CreateVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b80a309274eb51ad7aff768898a9c3bd211f37cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988327"
---
# <a name="createvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="28dac-103">Msvm ImageManagementService 類別的 CreateVirtualHardDisk 方法 \_</span><span class="sxs-lookup"><span data-stu-id="28dac-103">CreateVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="28dac-104">建立虛擬硬碟檔案。</span><span class="sxs-lookup"><span data-stu-id="28dac-104">Creates a virtual hard disk file.</span></span>

## <a name="syntax"></a><span data-ttu-id="28dac-105">語法</span><span class="sxs-lookup"><span data-stu-id="28dac-105">Syntax</span></span>


```mof
uint32 CreateVirtualHardDisk(
  [in]  string              VirtualDiskSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="28dac-106">參數</span><span class="sxs-lookup"><span data-stu-id="28dac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28dac-107">*VirtualDiskSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="28dac-107">*VirtualDiskSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28dac-108">字串，其中包含 [**Msvm \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) 類別的內嵌實例，可用來定義要建立之虛擬硬碟的屬性。</span><span class="sxs-lookup"><span data-stu-id="28dac-108">String that contains an embedded instance of the [**Msvm\_VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) class that is used to define attributes of the virtual hard disk to be created.</span></span>

</dd> <dt>

<span data-ttu-id="28dac-109">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="28dac-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28dac-110">如果工作已完成) ，則作業 (的參考可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="28dac-110">A reference to the job (can be **Null** if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28dac-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="28dac-111">Return value</span></span>

<span data-ttu-id="28dac-112">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="28dac-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="28dac-113">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="28dac-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="28dac-114">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="28dac-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="28dac-115">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="28dac-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="28dac-116">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="28dac-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="28dac-117">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="28dac-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="28dac-118">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="28dac-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="28dac-119">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="28dac-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="28dac-120">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="28dac-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="28dac-121">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="28dac-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="28dac-122">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="28dac-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="28dac-123">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="28dac-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="28dac-124">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="28dac-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="28dac-125">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="28dac-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="28dac-126">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="28dac-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="28dac-127">備註</span><span class="sxs-lookup"><span data-stu-id="28dac-127">Remarks</span></span>

<span data-ttu-id="28dac-128">存取 [**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="28dac-128">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="28dac-129">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="28dac-129">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="28dac-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="28dac-130">Requirements</span></span>



| <span data-ttu-id="28dac-131">需求</span><span class="sxs-lookup"><span data-stu-id="28dac-131">Requirement</span></span> | <span data-ttu-id="28dac-132">值</span><span class="sxs-lookup"><span data-stu-id="28dac-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28dac-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="28dac-133">Minimum supported client</span></span><br/> | <span data-ttu-id="28dac-134">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="28dac-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="28dac-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="28dac-135">Minimum supported server</span></span><br/> | <span data-ttu-id="28dac-136">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="28dac-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="28dac-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="28dac-137">Namespace</span></span><br/>                | <span data-ttu-id="28dac-138">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="28dac-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="28dac-139">MOF</span><span class="sxs-lookup"><span data-stu-id="28dac-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="28dac-140"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="28dac-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="28dac-141">DLL</span><span class="sxs-lookup"><span data-stu-id="28dac-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28dac-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="28dac-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="28dac-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28dac-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28dac-144">**Msvm \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="28dac-144">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

