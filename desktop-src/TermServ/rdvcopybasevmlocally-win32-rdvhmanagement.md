---
title: Win32_RdvhManagement 類別的 RdvCopyBaseVmLocally 方法
description: 將本地基礎虛擬機器複製到指定的遠端桌面虛擬化 (RDV) 主機伺服器。
ms.assetid: 13c0c629-42c6-4689-9740-f13f31688e42
ms.tgt_platform: multiple
keywords:
- RdvCopyBaseVmLocally 方法遠端桌面服務
- RdvCopyBaseVmLocally 方法遠端桌面服務，Win32_RdvhManagement 類別
- Win32_RdvhManagement 類別遠端桌面服務，RdvCopyBaseVmLocally 方法
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvCopyBaseVmLocally
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d96e01038a4b41edcf32a6a5a9b353403fa6021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385170"
---
# <a name="rdvcopybasevmlocally-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="bca9b-106">Win32 RdvhManagement 類別的 RdvCopyBaseVmLocally 方法 \_</span><span class="sxs-lookup"><span data-stu-id="bca9b-106">RdvCopyBaseVmLocally method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="bca9b-107">將本地基礎虛擬機器複製到指定的遠端桌面虛擬化 (RDV) 主機伺服器。</span><span class="sxs-lookup"><span data-stu-id="bca9b-107">Copies a local base virtual machine to a specified remote desktop virtualization (RDV) host server.</span></span>

## <a name="syntax"></a><span data-ttu-id="bca9b-108">語法</span><span class="sxs-lookup"><span data-stu-id="bca9b-108">Syntax</span></span>


```mof
uint32 RdvCopyBaseVmLocally(
  [in] string BaseVmLocation,
  [in] string FarmName,
  [in] string GoldCacheLocation
);
```



## <a name="parameters"></a><span data-ttu-id="bca9b-109">參數</span><span class="sxs-lookup"><span data-stu-id="bca9b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bca9b-110">*BaseVmLocation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bca9b-110">*BaseVmLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bca9b-111">基礎虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="bca9b-111">The base virtual machine location.</span></span>

</dd> <dt>

<span data-ttu-id="bca9b-112">*FarmName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bca9b-112">*FarmName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bca9b-113">要複製的主機伺服器陣列的名稱。</span><span class="sxs-lookup"><span data-stu-id="bca9b-113">The name of the host farm to copy to.</span></span>

</dd> <dt>

<span data-ttu-id="bca9b-114">*GoldCacheLocation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bca9b-114">*GoldCacheLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bca9b-115">金級快取位置。</span><span class="sxs-lookup"><span data-stu-id="bca9b-115">The gold cache location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bca9b-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="bca9b-116">Return value</span></span>

<span data-ttu-id="bca9b-117">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="bca9b-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="bca9b-118">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="bca9b-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="bca9b-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="bca9b-119">Requirements</span></span>



| <span data-ttu-id="bca9b-120">需求</span><span class="sxs-lookup"><span data-stu-id="bca9b-120">Requirement</span></span> | <span data-ttu-id="bca9b-121">值</span><span class="sxs-lookup"><span data-stu-id="bca9b-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="bca9b-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bca9b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bca9b-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="bca9b-123">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="bca9b-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bca9b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bca9b-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bca9b-125">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="bca9b-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="bca9b-126">Namespace</span></span><br/>                | <span data-ttu-id="bca9b-127">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="bca9b-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="bca9b-128">MOF</span><span class="sxs-lookup"><span data-stu-id="bca9b-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bca9b-129"><dt>TSVmHost mof</dt></span><span class="sxs-lookup"><span data-stu-id="bca9b-129"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="bca9b-130">DLL</span><span class="sxs-lookup"><span data-stu-id="bca9b-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bca9b-131"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bca9b-131"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bca9b-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bca9b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bca9b-133">**Win32 \_ RdvhManagement**</span><span class="sxs-lookup"><span data-stu-id="bca9b-133">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





