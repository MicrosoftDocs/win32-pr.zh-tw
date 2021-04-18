---
description: 修改虛擬機器設定。
ms.assetid: 3266bd0d-398b-4d3b-9248-e29c069aab11
title: Msvm_VirtualSystemManagementService 類別的 ModifySystemSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifySystemSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4e6bf40b3dd206affcdc014e98554bfa8f88b4c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978271"
---
# <a name="modifysystemsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="f7aa6-103">Msvm VirtualSystemManagementService 類別的 ModifySystemSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f7aa6-103">ModifySystemSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="f7aa6-104">修改虛擬機器設定。</span><span class="sxs-lookup"><span data-stu-id="f7aa6-104">Modifies virtual machine settings.</span></span> <span data-ttu-id="f7aa6-105">套用至「目前」虛擬機器設定的系統設定時，可能會修改虛擬機器實例。</span><span class="sxs-lookup"><span data-stu-id="f7aa6-105">When applied to the system settings of a "current" virtual machine configuration, as a side effect the virtual machine instance may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7aa6-106">語法</span><span class="sxs-lookup"><span data-stu-id="f7aa6-106">Syntax</span></span>


```mof
uint32 ModifySystemSettings(
  [in]  string              SystemSettings,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f7aa6-107">參數</span><span class="sxs-lookup"><span data-stu-id="f7aa6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7aa6-108">*SystemSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f7aa6-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7aa6-109">[**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)類別的內嵌實例，其中包含虛擬機器的修改後部分。</span><span class="sxs-lookup"><span data-stu-id="f7aa6-109">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that contains the modified aspects of the virtual machine.</span></span> <span data-ttu-id="f7aa6-110">**InstanceID** 屬性會識別要修改的虛擬機器設定。</span><span class="sxs-lookup"><span data-stu-id="f7aa6-110">The **InstanceID** property identifies the virtual machine setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="f7aa6-111">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f7aa6-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7aa6-112">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="f7aa6-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7aa6-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f7aa6-113">Return value</span></span>

<span data-ttu-id="f7aa6-114">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f7aa6-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="f7aa6-115">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="f7aa6-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f7aa6-116">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="f7aa6-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f7aa6-117">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="f7aa6-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f7aa6-118">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="f7aa6-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f7aa6-119">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="f7aa6-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f7aa6-120">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="f7aa6-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f7aa6-121"> (6) 的 **參數不相容**</span><span class="sxs-lookup"><span data-stu-id="f7aa6-121">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f7aa6-122">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="f7aa6-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f7aa6-123">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="f7aa6-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f7aa6-124">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="f7aa6-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="f7aa6-125">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="f7aa6-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f7aa6-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="f7aa6-126">Requirements</span></span>



| <span data-ttu-id="f7aa6-127">需求</span><span class="sxs-lookup"><span data-stu-id="f7aa6-127">Requirement</span></span> | <span data-ttu-id="f7aa6-128">值</span><span class="sxs-lookup"><span data-stu-id="f7aa6-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7aa6-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f7aa6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f7aa6-130">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f7aa6-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f7aa6-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f7aa6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f7aa6-132">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f7aa6-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f7aa6-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="f7aa6-133">Namespace</span></span><br/>                | <span data-ttu-id="f7aa6-134">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="f7aa6-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f7aa6-135">MOF</span><span class="sxs-lookup"><span data-stu-id="f7aa6-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7aa6-136"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="f7aa6-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f7aa6-137">DLL</span><span class="sxs-lookup"><span data-stu-id="f7aa6-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7aa6-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f7aa6-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f7aa6-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f7aa6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7aa6-140">**ModifyVirtualSystem (V1)**</span><span class="sxs-lookup"><span data-stu-id="f7aa6-140">**ModifyVirtualSystem (V1)**</span></span>](/previous-versions/windows/desktop/virtual/modifyvirtualsystem-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="f7aa6-141">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="f7aa6-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

