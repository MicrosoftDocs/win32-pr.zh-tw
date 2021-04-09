---
title: Win32_RdvhManagement 類別的 RdvCreateUserDiskTemplate 方法
description: 使用指定的最大大小，在指定的位置建立使用者磁片範本。
ms.assetid: b8ca8b8c-58fd-44fc-9a88-5d7d41ef96a2
ms.tgt_platform: multiple
keywords:
- RdvCreateUserDiskTemplate 方法遠端桌面服務
- RdvCreateUserDiskTemplate 方法遠端桌面服務，Win32_RdvhManagement 類別
- Win32_RdvhManagement 類別遠端桌面服務，RdvCreateUserDiskTemplate 方法
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvCreateUserDiskTemplate
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cdc7fec869fa4ffde9ac0a5a724f73b04b84351
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686354"
---
# <a name="rdvcreateuserdisktemplate-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="cd969-106">Win32 RdvhManagement 類別的 RdvCreateUserDiskTemplate 方法 \_</span><span class="sxs-lookup"><span data-stu-id="cd969-106">RdvCreateUserDiskTemplate method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="cd969-107">使用指定的最大大小，在指定的位置建立使用者磁片範本。</span><span class="sxs-lookup"><span data-stu-id="cd969-107">Creates a user disk template, with the specified maximum size, at the specified location.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd969-108">語法</span><span class="sxs-lookup"><span data-stu-id="cd969-108">Syntax</span></span>


```mof
uint32 RdvCreateUserDiskTemplate(
  [in] string UserDisksStorageUrl,
  [in] uint32 UserDiskMaxSizeInGB
);
```



## <a name="parameters"></a><span data-ttu-id="cd969-109">參數</span><span class="sxs-lookup"><span data-stu-id="cd969-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd969-110">*UserDisksStorageUrl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cd969-110">*UserDisksStorageUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd969-111">使用者磁片儲存體的位置。</span><span class="sxs-lookup"><span data-stu-id="cd969-111">Location of the user disk storage.</span></span>

</dd> <dt>

<span data-ttu-id="cd969-112">*UserDiskMaxSizeInGB* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cd969-112">*UserDiskMaxSizeInGB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd969-113">使用者磁片的大小上限（以 GB 為單位）。</span><span class="sxs-lookup"><span data-stu-id="cd969-113">Maximum size of the user disk, in GB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd969-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="cd969-114">Return value</span></span>

<span data-ttu-id="cd969-115">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="cd969-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="cd969-116">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="cd969-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd969-117">備註</span><span class="sxs-lookup"><span data-stu-id="cd969-117">Remarks</span></span>

<span data-ttu-id="cd969-118">使用此範本建立的所有使用者磁片，其大小上限會與範本相同。</span><span class="sxs-lookup"><span data-stu-id="cd969-118">All user disks created using this template will have the same maximum size as the template.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd969-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd969-119">Requirements</span></span>



| <span data-ttu-id="cd969-120">需求</span><span class="sxs-lookup"><span data-stu-id="cd969-120">Requirement</span></span> | <span data-ttu-id="cd969-121">值</span><span class="sxs-lookup"><span data-stu-id="cd969-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd969-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cd969-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cd969-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="cd969-123">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="cd969-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cd969-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cd969-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cd969-125">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="cd969-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="cd969-126">Namespace</span></span><br/>                | <span data-ttu-id="cd969-127">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="cd969-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="cd969-128">MOF</span><span class="sxs-lookup"><span data-stu-id="cd969-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd969-129"><dt>TSVmHost mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd969-129"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="cd969-130">DLL</span><span class="sxs-lookup"><span data-stu-id="cd969-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd969-131"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd969-131"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd969-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cd969-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd969-133">**Win32 \_ RdvhManagement**</span><span class="sxs-lookup"><span data-stu-id="cd969-133">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





