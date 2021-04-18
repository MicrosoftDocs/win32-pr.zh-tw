---
title: Win32_TSVirtualIP 類別的 SetVirtualizeLoopbackAddressesEnabled 方法
description: 設定 VirtualizeLoopbackAddressesEnabled 屬性值。
ms.assetid: 84A4FF36-82B3-462A-9D2E-C15DD99524E4
ms.tgt_platform: multiple
keywords:
- SetVirtualizeLoopbackAddressesEnabled 方法遠端桌面服務
- SetVirtualizeLoopbackAddressesEnabled 方法遠端桌面服務，Win32_TSVirtualIP 類別
- Win32_TSVirtualIP 類別遠端桌面服務，SetVirtualizeLoopbackAddressesEnabled 方法
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualizeLoopbackAddressesEnabled
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed74e74a9f0fcbcd070a50743e6182649c2dca08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965287"
---
# <a name="setvirtualizeloopbackaddressesenabled-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="e3a7d-106">Win32 TSVirtualIP 類別的 SetVirtualizeLoopbackAddressesEnabled 方法 \_</span><span class="sxs-lookup"><span data-stu-id="e3a7d-106">SetVirtualizeLoopbackAddressesEnabled method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="e3a7d-107">設定 **VirtualizeLoopbackAddressesEnabled** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="e3a7d-107">Sets the **VirtualizeLoopbackAddressesEnabled** property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3a7d-108">語法</span><span class="sxs-lookup"><span data-stu-id="e3a7d-108">Syntax</span></span>


```mof
uint32 SetVirtualizeLoopbackAddressesEnabled(
  [in] uint32 VirtualizeLoopbackAddressesEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="e3a7d-109">參數</span><span class="sxs-lookup"><span data-stu-id="e3a7d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3a7d-110">*VirtualizeLoopbackAddressesEnabled* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e3a7d-110">*VirtualizeLoopbackAddressesEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3a7d-111">指定是否啟用回送位址虛擬化。</span><span class="sxs-lookup"><span data-stu-id="e3a7d-111">Specifies whether to enable loopback address virtualization.</span></span> <span data-ttu-id="e3a7d-112">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e3a7d-112">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="e3a7d-113">0</span><span class="sxs-lookup"><span data-stu-id="e3a7d-113">0</span></span>
</dt> <dd>

<span data-ttu-id="e3a7d-114">請勿啟用回送位址虛擬化。</span><span class="sxs-lookup"><span data-stu-id="e3a7d-114">Do not enable loopback address virtualization.</span></span>

</dd> <dt>

<span data-ttu-id="e3a7d-115">1</span><span class="sxs-lookup"><span data-stu-id="e3a7d-115">1</span></span>
</dt> <dd>

<span data-ttu-id="e3a7d-116">啟用回送位址虛擬化。</span><span class="sxs-lookup"><span data-stu-id="e3a7d-116">Enable loopback address virtualization.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3a7d-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="e3a7d-117">Return value</span></span>

<span data-ttu-id="e3a7d-118">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e3a7d-118">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="e3a7d-119">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="e3a7d-119">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="e3a7d-120">如果設定位於群組原則控制之下，則方法會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="e3a7d-120">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3a7d-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3a7d-121">Requirements</span></span>



| <span data-ttu-id="e3a7d-122">需求</span><span class="sxs-lookup"><span data-stu-id="e3a7d-122">Requirement</span></span> | <span data-ttu-id="e3a7d-123">值</span><span class="sxs-lookup"><span data-stu-id="e3a7d-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3a7d-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e3a7d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e3a7d-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="e3a7d-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e3a7d-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e3a7d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e3a7d-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e3a7d-127">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="e3a7d-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="e3a7d-128">Namespace</span></span><br/>                | <span data-ttu-id="e3a7d-129">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="e3a7d-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e3a7d-130">MOF</span><span class="sxs-lookup"><span data-stu-id="e3a7d-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e3a7d-131"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="e3a7d-131"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e3a7d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e3a7d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3a7d-133"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3a7d-133"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3a7d-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3a7d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3a7d-135">**Win32 \_ TSVirtualIP**</span><span class="sxs-lookup"><span data-stu-id="e3a7d-135">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





