---
title: Win32_TSVirtualIP 類別的 SetVirtualIPActive 方法
description: 設定 VirtualIPActive 屬性值。
ms.assetid: e485aeb1-afdf-4572-bac7-daa80d903edc
ms.tgt_platform: multiple
keywords:
- SetVirtualIPActive 方法遠端桌面服務
- SetVirtualIPActive 方法遠端桌面服務，Win32_TSVirtualIP 類別
- Win32_TSVirtualIP 類別遠端桌面服務，SetVirtualIPActive 方法
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualIPActive
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06534c967c5d86a7a19c060254b3b988ff98b17e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934572"
---
# <a name="setvirtualipactive-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="5ed96-106">Win32 TSVirtualIP 類別的 SetVirtualIPActive 方法 \_</span><span class="sxs-lookup"><span data-stu-id="5ed96-106">SetVirtualIPActive method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="5ed96-107">設定 **VirtualIPActive** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="5ed96-107">Sets the **VirtualIPActive** property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ed96-108">語法</span><span class="sxs-lookup"><span data-stu-id="5ed96-108">Syntax</span></span>


```mof
uint32 SetVirtualIPActive(
  [in] uint32 VirtualIPActive
);
```



## <a name="parameters"></a><span data-ttu-id="5ed96-109">參數</span><span class="sxs-lookup"><span data-stu-id="5ed96-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ed96-110">*VirtualIPActive* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5ed96-110">*VirtualIPActive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ed96-111">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5ed96-111">Type: **uint32**</span></span>

<span data-ttu-id="5ed96-112">指定伺服器上的 IP 虛擬化是否為作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="5ed96-112">Specifies if IP virtualization is active on the server.</span></span> <span data-ttu-id="5ed96-113">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="5ed96-113">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="5ed96-114">零</span><span class="sxs-lookup"><span data-stu-id="5ed96-114">zero</span></span>
</dt> <dd>

<span data-ttu-id="5ed96-115">IP 虛擬化未啟用。</span><span class="sxs-lookup"><span data-stu-id="5ed96-115">IP virtualization is not active.</span></span>

</dd> <dt>

<span data-ttu-id="5ed96-116">零</span><span class="sxs-lookup"><span data-stu-id="5ed96-116">nonzero</span></span>
</dt> <dd>

<span data-ttu-id="5ed96-117">IP 虛擬化處於作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="5ed96-117">IP virtualization is active.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ed96-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="5ed96-118">Return value</span></span>

<span data-ttu-id="5ed96-119">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5ed96-119">Type: **uint32**</span></span>

<span data-ttu-id="5ed96-120">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5ed96-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="5ed96-121">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="5ed96-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="5ed96-122">如果設定位於群組原則控制之下，則方法會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="5ed96-122">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ed96-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="5ed96-123">Requirements</span></span>



| <span data-ttu-id="5ed96-124">需求</span><span class="sxs-lookup"><span data-stu-id="5ed96-124">Requirement</span></span> | <span data-ttu-id="5ed96-125">值</span><span class="sxs-lookup"><span data-stu-id="5ed96-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed96-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5ed96-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5ed96-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="5ed96-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="5ed96-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5ed96-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5ed96-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5ed96-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="5ed96-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="5ed96-130">Namespace</span></span><br/>                | <span data-ttu-id="5ed96-131">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="5ed96-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="5ed96-132">MOF</span><span class="sxs-lookup"><span data-stu-id="5ed96-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ed96-133"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ed96-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ed96-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5ed96-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ed96-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ed96-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ed96-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5ed96-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ed96-137">**Win32 \_ TSVirtualIP**</span><span class="sxs-lookup"><span data-stu-id="5ed96-137">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





