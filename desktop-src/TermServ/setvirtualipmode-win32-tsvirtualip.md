---
title: Win32_TSVirtualIP 類別的 SetVirtualIPMode 方法
description: 設定 VirtualIPMode 屬性值。
ms.assetid: d4b39566-ad2a-493b-8022-c006a857043d
ms.tgt_platform: multiple
keywords:
- SetVirtualIPMode 方法遠端桌面服務
- SetVirtualIPMode 方法遠端桌面服務，Win32_TSVirtualIP 類別
- Win32_TSVirtualIP 類別遠端桌面服務，SetVirtualIPMode 方法
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualIPMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 250633f5d41f5a4a7cb06a17ba9ae45bb444a018
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106979685"
---
# <a name="setvirtualipmode-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="b11ec-106">Win32 TSVirtualIP 類別的 SetVirtualIPMode 方法 \_</span><span class="sxs-lookup"><span data-stu-id="b11ec-106">SetVirtualIPMode method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="b11ec-107">設定 **VirtualIPMode** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="b11ec-107">Sets the **VirtualIPMode** property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="b11ec-108">語法</span><span class="sxs-lookup"><span data-stu-id="b11ec-108">Syntax</span></span>


```mof
uint32 SetVirtualIPMode(
  [in] uint32 VirtualIPMode
);
```



## <a name="parameters"></a><span data-ttu-id="b11ec-109">參數</span><span class="sxs-lookup"><span data-stu-id="b11ec-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b11ec-110">*VirtualIPMode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b11ec-110">*VirtualIPMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b11ec-111">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b11ec-111">Type: **uint32**</span></span>

<span data-ttu-id="b11ec-112">指定要在伺服器上使用的 IP 虛擬化模式。</span><span class="sxs-lookup"><span data-stu-id="b11ec-112">Specifies which IP virtualization mode is being used on the server.</span></span> <span data-ttu-id="b11ec-113">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="b11ec-113">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="b11ec-114">0</span><span class="sxs-lookup"><span data-stu-id="b11ec-114">0</span></span>
</dt> <dd>

<span data-ttu-id="b11ec-115">IP 虛擬化模式為每個會話。</span><span class="sxs-lookup"><span data-stu-id="b11ec-115">The IP virtualization mode is per-session.</span></span>

</dd> <dt>

<span data-ttu-id="b11ec-116">1</span><span class="sxs-lookup"><span data-stu-id="b11ec-116">1</span></span>
</dt> <dd>

<span data-ttu-id="b11ec-117">IP 虛擬化模式為每位使用者。</span><span class="sxs-lookup"><span data-stu-id="b11ec-117">The IP virtualization mode is per-user.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b11ec-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="b11ec-118">Return value</span></span>

<span data-ttu-id="b11ec-119">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b11ec-119">Type: **uint32**</span></span>

<span data-ttu-id="b11ec-120">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b11ec-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="b11ec-121">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="b11ec-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="b11ec-122">如果設定位於群組原則控制之下，則方法會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="b11ec-122">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="b11ec-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="b11ec-123">Requirements</span></span>



| <span data-ttu-id="b11ec-124">需求</span><span class="sxs-lookup"><span data-stu-id="b11ec-124">Requirement</span></span> | <span data-ttu-id="b11ec-125">值</span><span class="sxs-lookup"><span data-stu-id="b11ec-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b11ec-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b11ec-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b11ec-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="b11ec-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="b11ec-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b11ec-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b11ec-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b11ec-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="b11ec-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="b11ec-130">Namespace</span></span><br/>                | <span data-ttu-id="b11ec-131">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="b11ec-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="b11ec-132">MOF</span><span class="sxs-lookup"><span data-stu-id="b11ec-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b11ec-133"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="b11ec-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b11ec-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b11ec-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b11ec-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b11ec-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b11ec-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b11ec-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b11ec-137">**Win32 \_ TSVirtualIP**</span><span class="sxs-lookup"><span data-stu-id="b11ec-137">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





