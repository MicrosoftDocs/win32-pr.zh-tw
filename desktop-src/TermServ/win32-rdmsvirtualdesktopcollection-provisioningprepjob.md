---
title: Win32_RDMSVirtualDesktopCollection 類別的 ProvisioningPrepJob 方法
description: 建立虛擬桌面布建作業。
ms.assetid: 240D4BE6-95BD-4858-8F8F-A00C92042AEF
ms.tgt_platform: multiple
keywords:
- ProvisioningPrepJob 方法遠端桌面服務
- ProvisioningPrepJob 方法遠端桌面服務，Win32_RDMSVirtualDesktopCollection 介面
- Win32_RDMSVirtualDesktopCollection 介面遠端桌面服務，ProvisioningPrepJob 方法
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningPrepJob
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9727dec0e31dd199f324ed01a4510041ba3558f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934291"
---
# <a name="provisioningprepjob-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="01239-106">Win32 RDMSVirtualDesktopCollection 類別的 ProvisioningPrepJob 方法 \_</span><span class="sxs-lookup"><span data-stu-id="01239-106">ProvisioningPrepJob method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="01239-107">建立虛擬桌面布建作業。</span><span class="sxs-lookup"><span data-stu-id="01239-107">Creates a virtual desktop provisioning job.</span></span>

## <a name="syntax"></a><span data-ttu-id="01239-108">語法</span><span class="sxs-lookup"><span data-stu-id="01239-108">Syntax</span></span>


```mof
uint32 ProvisioningPrepJob(
  [in]  string  CollectionAlias,
  [in]  string  VMHostName,
  [in]  string  VMName,
  [in]  string  ExportToLocation,
  [in]  boolean bSysPrep,
  [in]  string  MachineName,
  [in]  string  UserName,
  [in]  string  Password,
  [out] string  JobGuid
);
```



## <a name="parameters"></a><span data-ttu-id="01239-109">參數</span><span class="sxs-lookup"><span data-stu-id="01239-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01239-110">*CollectionAlias* \[在\]</span><span class="sxs-lookup"><span data-stu-id="01239-110">*CollectionAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01239-111">裝載虛擬桌面之集合的別名。</span><span class="sxs-lookup"><span data-stu-id="01239-111">The alias of the collection that hosts the virtual desktop.</span></span>

</dd> <dt>

<span data-ttu-id="01239-112">*VMHostName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="01239-112">*VMHostName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01239-113">虛擬機器主機名稱。</span><span class="sxs-lookup"><span data-stu-id="01239-113">The virtual machine host name.</span></span>

</dd> <dt>

<span data-ttu-id="01239-114">*VMName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="01239-114">*VMName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01239-115">虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="01239-115">The name of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="01239-116">*ExportToLocation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="01239-116">*ExportToLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01239-117">要匯出布建作業之位置的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="01239-117">The full path the location to export the provisioning job.</span></span>

</dd> <dt>

<span data-ttu-id="01239-118">*bSysPrep* \[在\]</span><span class="sxs-lookup"><span data-stu-id="01239-118">*bSysPrep* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01239-119">指出布建作業是否代表 Sysprep 部署。</span><span class="sxs-lookup"><span data-stu-id="01239-119">Indicates whether the provisioning job represents a Sysprep deployment.</span></span>

</dd> <dt>

<span data-ttu-id="01239-120">*MachineName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="01239-120">*MachineName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01239-121">裝載虛擬機器之電腦的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="01239-121">The machine name of the computer that hosts the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="01239-122">使用者 *名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="01239-122">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01239-123">虛擬機器的系統管理員使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="01239-123">The user name of the administrator of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="01239-124">*密碼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="01239-124">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01239-125">虛擬機器的系統管理員密碼。</span><span class="sxs-lookup"><span data-stu-id="01239-125">The password of the administrator of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="01239-126">*JobGuid* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="01239-126">*JobGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01239-127">可唯一識別布建作業的 **GUID** 。</span><span class="sxs-lookup"><span data-stu-id="01239-127">The **GUID** that uniquely identifies the provisioning job.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01239-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="01239-128">Return value</span></span>

<span data-ttu-id="01239-129">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="01239-129">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="01239-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="01239-130">Requirements</span></span>



| <span data-ttu-id="01239-131">需求</span><span class="sxs-lookup"><span data-stu-id="01239-131">Requirement</span></span> | <span data-ttu-id="01239-132">值</span><span class="sxs-lookup"><span data-stu-id="01239-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="01239-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="01239-133">Minimum supported client</span></span><br/> | <span data-ttu-id="01239-134">都不支援</span><span class="sxs-lookup"><span data-stu-id="01239-134">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="01239-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="01239-135">Minimum supported server</span></span><br/> | <span data-ttu-id="01239-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01239-136">Windows Server 2008</span></span><br/>                                                              |
| <span data-ttu-id="01239-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="01239-137">Namespace</span></span><br/>                | <span data-ttu-id="01239-138">根 \\ cimv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="01239-138">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="01239-139">MOF</span><span class="sxs-lookup"><span data-stu-id="01239-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01239-140"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="01239-140"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="01239-141">DLL</span><span class="sxs-lookup"><span data-stu-id="01239-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01239-142"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01239-142"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="01239-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="01239-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01239-144">**Win32 \_ RDMSVirtualDesktopCollection**</span><span class="sxs-lookup"><span data-stu-id="01239-144">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





