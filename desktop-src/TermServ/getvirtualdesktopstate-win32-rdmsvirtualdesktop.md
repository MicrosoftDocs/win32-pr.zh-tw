---
title: Win32_RDMSVirtualDesktop 類別的 GetVirtualDesktopState 方法
description: 捕獲虛擬桌面的狀態。
ms.assetid: 176096ba-2b5f-428c-9216-02e3e97be64e
ms.tgt_platform: multiple
keywords:
- GetVirtualDesktopState 方法遠端桌面服務
- GetVirtualDesktopState 方法遠端桌面服務，Win32_RDMSVirtualDesktop 類別
- Win32_RDMSVirtualDesktop 類別遠端桌面服務，GetVirtualDesktopState 方法
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetVirtualDesktopState
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 674e9646f0f41166fbfdc9e4ad35df697023329a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106996575"
---
# <a name="getvirtualdesktopstate-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="9e0ac-106">Win32 RDMSVirtualDesktop 類別的 GetVirtualDesktopState 方法 \_</span><span class="sxs-lookup"><span data-stu-id="9e0ac-106">GetVirtualDesktopState method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="9e0ac-107">捕獲虛擬桌面的狀態。</span><span class="sxs-lookup"><span data-stu-id="9e0ac-107">Retrieves the state of the virtual desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e0ac-108">語法</span><span class="sxs-lookup"><span data-stu-id="9e0ac-108">Syntax</span></span>


```mof
uint32 GetVirtualDesktopState(
  [out] uint32 VMState
);
```



## <a name="parameters"></a><span data-ttu-id="9e0ac-109">參數</span><span class="sxs-lookup"><span data-stu-id="9e0ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e0ac-110">*VMState* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9e0ac-110">*VMState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e0ac-111">接收值，指出虛擬機器的狀態。</span><span class="sxs-lookup"><span data-stu-id="9e0ac-111">Receives a value that indicates the state of the virtual machine.</span></span>

<span data-ttu-id="9e0ac-112">這個參數可以設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="9e0ac-112">This parameter can bet set to one of the following values:</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9e0ac-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0 (預設) ) </span><span class="sxs-lookup"><span data-stu-id="9e0ac-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0 (Default))</span></span>


</dt> <dd>

<span data-ttu-id="9e0ac-114">無法判斷虛擬機器的狀態。</span><span class="sxs-lookup"><span data-stu-id="9e0ac-114">The state of the virtual machine could not be determined.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9e0ac-115"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="9e0ac-115"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9e0ac-116">虛擬機器未執行。</span><span class="sxs-lookup"><span data-stu-id="9e0ac-116">The virtual machine is running.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9e0ac-117"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="9e0ac-117"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9e0ac-118">虛擬機器已關閉。</span><span class="sxs-lookup"><span data-stu-id="9e0ac-118">The virtual machine is turned off.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="9e0ac-119"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (32768) </span><span class="sxs-lookup"><span data-stu-id="9e0ac-119"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="9e0ac-120">虛擬機器已暫停。</span><span class="sxs-lookup"><span data-stu-id="9e0ac-120">The virtual machine is paused.</span></span>

</dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="9e0ac-121"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>已 **暫** 止 (32769) </span><span class="sxs-lookup"><span data-stu-id="9e0ac-121"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (32769)</span></span>


</dt> <dd>

<span data-ttu-id="9e0ac-122">虛擬機器處於儲存狀態。</span><span class="sxs-lookup"><span data-stu-id="9e0ac-122">The virtual machine is in a saved state.</span></span>

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9e0ac-123"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**啟動** (32770) </span><span class="sxs-lookup"><span data-stu-id="9e0ac-123"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (32770)</span></span>


</dt> <dd>

<span data-ttu-id="9e0ac-124">虛擬機器正在啟動。</span><span class="sxs-lookup"><span data-stu-id="9e0ac-124">The virtual machine is starting.</span></span>

</dd> <dt>

<span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>

<span data-ttu-id="9e0ac-125"><span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>**正在儲存** (32773) </span><span class="sxs-lookup"><span data-stu-id="9e0ac-125"><span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>**Saving** (32773)</span></span>


</dt> <dd>

<span data-ttu-id="9e0ac-126">虛擬機器正在儲存其狀態。</span><span class="sxs-lookup"><span data-stu-id="9e0ac-126">The virtual machine is saving its state.</span></span>

</dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9e0ac-127"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (32774) </span><span class="sxs-lookup"><span data-stu-id="9e0ac-127"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (32774)</span></span>


</dt> <dd>

<span data-ttu-id="9e0ac-128">虛擬機器正在關閉。</span><span class="sxs-lookup"><span data-stu-id="9e0ac-128">The virtual machine is turning off.</span></span>

</dd> <dt>

<span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>

<span data-ttu-id="9e0ac-129"><span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>**暫停** (32776) </span><span class="sxs-lookup"><span data-stu-id="9e0ac-129"><span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>**Pausing** (32776)</span></span>


</dt> <dd>

<span data-ttu-id="9e0ac-130">虛擬機器正在暫停。</span><span class="sxs-lookup"><span data-stu-id="9e0ac-130">The virtual machine is pausing.</span></span>

</dd> <dt>

<span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>

<span data-ttu-id="9e0ac-131"><span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>**繼續** (32777) </span><span class="sxs-lookup"><span data-stu-id="9e0ac-131"><span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>**Resuming** (32777)</span></span>


</dt> <dd>

<span data-ttu-id="9e0ac-132">虛擬機器正在從暫停狀態繼續。</span><span class="sxs-lookup"><span data-stu-id="9e0ac-132">The virtual machine is resuming from a paused state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e0ac-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="9e0ac-133">Return value</span></span>

<span data-ttu-id="9e0ac-134">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9e0ac-134">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e0ac-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="9e0ac-135">Requirements</span></span>



| <span data-ttu-id="9e0ac-136">需求</span><span class="sxs-lookup"><span data-stu-id="9e0ac-136">Requirement</span></span> | <span data-ttu-id="9e0ac-137">值</span><span class="sxs-lookup"><span data-stu-id="9e0ac-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e0ac-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9e0ac-138">Minimum supported client</span></span><br/> | <span data-ttu-id="9e0ac-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="9e0ac-139">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="9e0ac-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9e0ac-140">Minimum supported server</span></span><br/> | <span data-ttu-id="9e0ac-141">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9e0ac-141">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="9e0ac-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="9e0ac-142">Namespace</span></span><br/>                | <span data-ttu-id="9e0ac-143">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="9e0ac-143">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="9e0ac-144">MOF</span><span class="sxs-lookup"><span data-stu-id="9e0ac-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e0ac-145"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="9e0ac-145"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="9e0ac-146">DLL</span><span class="sxs-lookup"><span data-stu-id="9e0ac-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e0ac-147"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e0ac-147"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="9e0ac-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9e0ac-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e0ac-149">**Win32 \_ RDMSVirtualDesktop**</span><span class="sxs-lookup"><span data-stu-id="9e0ac-149">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





