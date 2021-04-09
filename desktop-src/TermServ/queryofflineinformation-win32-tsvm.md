---
title: Win32_TSVm 類別的 QueryOfflineInformation 方法
description: )  (的虛擬桌面伺服器的屬性，但是只有在伺服器離線時，才會加以抓取。
ms.assetid: f6ce74cb-a4a4-4e05-a0a7-bac0b7f52c45
ms.tgt_platform: multiple
keywords:
- QueryOfflineInformation 方法遠端桌面服務
- QueryOfflineInformation 方法遠端桌面服務，Win32_TSVm 類別
- Win32_TSVm 類別遠端桌面服務，QueryOfflineInformation 方法
topic_type:
- apiref
api_name:
- Win32_TSVm.QueryOfflineInformation
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4750ebdb82b08ae1ed0350e1ac448d9aca4003b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843844"
---
# <a name="queryofflineinformation-method-of-the-win32_tsvm-class"></a><span data-ttu-id="5b2b3-106">Win32 TSVm 類別的 QueryOfflineInformation 方法 \_</span><span class="sxs-lookup"><span data-stu-id="5b2b3-106">QueryOfflineInformation method of the Win32\_TSVm class</span></span>

<span data-ttu-id="5b2b3-107">)  (的虛擬桌面伺服器的屬性，但是只有在伺服器離線時，才會加以抓取。</span><span class="sxs-lookup"><span data-stu-id="5b2b3-107">Retrieves the properties of the current virtual desktop server (VDS), but only when the server is offline.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b2b3-108">語法</span><span class="sxs-lookup"><span data-stu-id="5b2b3-108">Syntax</span></span>


```mof
uint32 QueryOfflineInformation(
  [out] string  Build,
  [out] string  CurrentVersion,
  [out] string  InstallationType,
  [out] string  EditionId,
  [out] string  SysPrepImageState,
  [out] string  SysPrepMode,
  [out] sint32  ProcArch,
  [out] boolean fIsVmbusCapable,
  [out] boolean fIsRdvIcInstalled
);
```



## <a name="parameters"></a><span data-ttu-id="5b2b3-109">參數</span><span class="sxs-lookup"><span data-stu-id="5b2b3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b2b3-110">*組建* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5b2b3-110">*Build* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b2b3-111">成功時，會傳回 VDS 的組建版本。</span><span class="sxs-lookup"><span data-stu-id="5b2b3-111">On a success, returns the build version of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="5b2b3-112">*CurrentVersion* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5b2b3-112">*CurrentVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b2b3-113">成功時，會傳回 VDS 的目前版本。</span><span class="sxs-lookup"><span data-stu-id="5b2b3-113">On a success, returns the current version of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="5b2b3-114">*InstallationType* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5b2b3-114">*InstallationType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b2b3-115">成功時，會傳回 VDS 的安裝類型。</span><span class="sxs-lookup"><span data-stu-id="5b2b3-115">On a success, returns the installation type of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="5b2b3-116">*EditionId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5b2b3-116">*EditionId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b2b3-117">成功時，會傳回 VDS 的版本識別碼。</span><span class="sxs-lookup"><span data-stu-id="5b2b3-117">On a success, returns the edition ID of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="5b2b3-118">*SysPrepImageState* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5b2b3-118">*SysPrepImageState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b2b3-119">成功時，會傳回 VDS 的系統準備映射狀態。</span><span class="sxs-lookup"><span data-stu-id="5b2b3-119">On success, returns the system prep image state of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="5b2b3-120">*SysPrepMode* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5b2b3-120">*SysPrepMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b2b3-121">成功時，會傳回 VDS 的系統準備模式。</span><span class="sxs-lookup"><span data-stu-id="5b2b3-121">On a success, returns the system prep mode of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="5b2b3-122">*ProcArch* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5b2b3-122">*ProcArch* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b2b3-123">成功時，會傳回表示處理器架構的值。</span><span class="sxs-lookup"><span data-stu-id="5b2b3-123">On a success, returns a value indicating the processor architecture.</span></span>

<dt>

<span data-ttu-id="5b2b3-124">0</span><span class="sxs-lookup"><span data-stu-id="5b2b3-124">0</span></span>
</dt> <dd>

<span data-ttu-id="5b2b3-125">x86</span><span class="sxs-lookup"><span data-stu-id="5b2b3-125">x86</span></span>

</dd> <dt>

<span data-ttu-id="5b2b3-126">1</span><span class="sxs-lookup"><span data-stu-id="5b2b3-126">1</span></span>
</dt> <dd>

<span data-ttu-id="5b2b3-127">amd64</span><span class="sxs-lookup"><span data-stu-id="5b2b3-127">amd64</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5b2b3-128">*fIsVmbusCapable* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5b2b3-128">*fIsVmbusCapable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b2b3-129">成功時，會指出系統是否支援 VMBus。</span><span class="sxs-lookup"><span data-stu-id="5b2b3-129">on a success, indicates whether the system is VMBus-capable.</span></span>

</dd> <dt>

<span data-ttu-id="5b2b3-130">*fIsRdvIcInstalled* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5b2b3-130">*fIsRdvIcInstalled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b2b3-131">成功時，表示是否已安裝 RDVIC。</span><span class="sxs-lookup"><span data-stu-id="5b2b3-131">On a success, indicates if RDVIC is installed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b2b3-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="5b2b3-132">Return value</span></span>

<span data-ttu-id="5b2b3-133">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5b2b3-133">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="5b2b3-134">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="5b2b3-134">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b2b3-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b2b3-135">Requirements</span></span>



| <span data-ttu-id="5b2b3-136">需求</span><span class="sxs-lookup"><span data-stu-id="5b2b3-136">Requirement</span></span> | <span data-ttu-id="5b2b3-137">值</span><span class="sxs-lookup"><span data-stu-id="5b2b3-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b2b3-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5b2b3-138">Minimum supported client</span></span><br/> | <span data-ttu-id="5b2b3-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="5b2b3-139">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="5b2b3-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5b2b3-140">Minimum supported server</span></span><br/> | <span data-ttu-id="5b2b3-141">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5b2b3-141">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="5b2b3-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="5b2b3-142">Namespace</span></span><br/>                | <span data-ttu-id="5b2b3-143">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="5b2b3-143">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="5b2b3-144">MOF</span><span class="sxs-lookup"><span data-stu-id="5b2b3-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b2b3-145"><dt>TSVmHost mof</dt></span><span class="sxs-lookup"><span data-stu-id="5b2b3-145"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="5b2b3-146">DLL</span><span class="sxs-lookup"><span data-stu-id="5b2b3-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b2b3-147"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b2b3-147"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b2b3-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b2b3-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b2b3-149">**Win32 \_ TSVm**</span><span class="sxs-lookup"><span data-stu-id="5b2b3-149">**Win32\_TSVm**</span></span>](win32-tsvm.md)
</dt> </dl>

 

 





