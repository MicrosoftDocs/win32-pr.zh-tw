---
description: 抓取虛擬機器的系統檔案大小總計。
ms.assetid: 492aa0df-1562-4d83-a0ea-43776b12c1b1
title: Msvm_VirtualSystemManagementService 類別的 GetSizeOfSystemFiles 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetSizeOfSystemFiles
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ed9fcf93093e17c2989121bf33ee5f5fbf09bab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690787"
---
# <a name="getsizeofsystemfiles-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="17824-103">Msvm VirtualSystemManagementService 類別的 GetSizeOfSystemFiles 方法 \_</span><span class="sxs-lookup"><span data-stu-id="17824-103">GetSizeOfSystemFiles method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="17824-104">抓取虛擬機器的系統檔案大小總計。</span><span class="sxs-lookup"><span data-stu-id="17824-104">Retrieves the total size of the system files of virtual machine.</span></span> <span data-ttu-id="17824-105">這些包括設定和儲存的狀態檔案。</span><span class="sxs-lookup"><span data-stu-id="17824-105">These include the configuration and saved state files.</span></span>

## <a name="syntax"></a><span data-ttu-id="17824-106">語法</span><span class="sxs-lookup"><span data-stu-id="17824-106">Syntax</span></span>


```mof
uint32 GetSizeOfSystemFiles(
  [in]  CIM_VirtualSystemSettingData REF Vssd,
  [out] uint64                           Size
);
```



## <a name="parameters"></a><span data-ttu-id="17824-107">參數</span><span class="sxs-lookup"><span data-stu-id="17824-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17824-108">*Vssd* \[在\]</span><span class="sxs-lookup"><span data-stu-id="17824-108">*Vssd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17824-109">要取出其系統檔案大小之 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) 實例的參考。</span><span class="sxs-lookup"><span data-stu-id="17824-109">A reference to the [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instance whose system files size are to be retrieved.</span></span> <span data-ttu-id="17824-110">此實例可能代表虛擬機器的目前具現化，或虛擬機器快照集的實例。</span><span class="sxs-lookup"><span data-stu-id="17824-110">This instance may represent either the current instantiation of the virtual machine, or an instance of a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="17824-111">*大小* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="17824-111">*Size* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17824-112">系統檔案的總大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="17824-112">The total size, in bytes, of system files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17824-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="17824-113">Return value</span></span>

<span data-ttu-id="17824-114">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="17824-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="17824-115">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="17824-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="17824-116">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="17824-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="17824-117">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="17824-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="17824-118">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="17824-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="17824-119">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="17824-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="17824-120">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="17824-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="17824-121">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="17824-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="17824-122">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="17824-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="17824-123">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="17824-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="17824-124">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="17824-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="17824-125">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="17824-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="17824-126">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="17824-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="17824-127">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="17824-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="17824-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="17824-128">Requirements</span></span>



| <span data-ttu-id="17824-129">需求</span><span class="sxs-lookup"><span data-stu-id="17824-129">Requirement</span></span> | <span data-ttu-id="17824-130">值</span><span class="sxs-lookup"><span data-stu-id="17824-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17824-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="17824-131">Minimum supported client</span></span><br/> | <span data-ttu-id="17824-132">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="17824-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="17824-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="17824-133">Minimum supported server</span></span><br/> | <span data-ttu-id="17824-134">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="17824-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="17824-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="17824-135">Namespace</span></span><br/>                | <span data-ttu-id="17824-136">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="17824-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="17824-137">MOF</span><span class="sxs-lookup"><span data-stu-id="17824-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17824-138"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="17824-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="17824-139">DLL</span><span class="sxs-lookup"><span data-stu-id="17824-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17824-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="17824-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="17824-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17824-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17824-142">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="17824-142">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

