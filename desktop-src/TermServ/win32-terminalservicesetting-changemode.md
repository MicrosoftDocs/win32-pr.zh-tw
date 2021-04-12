---
title: Win32_TerminalServiceSetting 類別的 ChangeMode 方法
description: ChangeMode 方法會設定目前遠端桌面工作階段主機 (RD 工作階段主機) server 的授權類型。
ms.assetid: 293483ee-51ce-4cd4-ba13-6c7c02bbdbbf
ms.tgt_platform: multiple
keywords:
- ChangeMode 方法遠端桌面服務
- ChangeMode 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，ChangeMode 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.ChangeMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 880fcab8aa68e49c6b3c00278b90635686de6168
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384546"
---
# <a name="changemode-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="39017-106">Win32 TerminalServiceSetting 類別的 ChangeMode 方法 \_</span><span class="sxs-lookup"><span data-stu-id="39017-106">ChangeMode method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="39017-107">**ChangeMode** 方法會設定目前遠端桌面工作階段主機 (RD 工作階段主機) server 的授權類型。</span><span class="sxs-lookup"><span data-stu-id="39017-107">The **ChangeMode** method sets the licensing type of the current Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="39017-108">語法</span><span class="sxs-lookup"><span data-stu-id="39017-108">Syntax</span></span>


```mof
uint32 ChangeMode(
  [in] uint32 LicensingType
);
```



## <a name="parameters"></a><span data-ttu-id="39017-109">參數</span><span class="sxs-lookup"><span data-stu-id="39017-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39017-110">*LicensingType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="39017-110">*LicensingType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39017-111">要根據 RD 工作階段主機伺服器模式設定的授權類型。</span><span class="sxs-lookup"><span data-stu-id="39017-111">The licensing type to set based on the RD Session Host server mode.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="39017-112"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="39017-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="39017-113">個人 RD 工作階段主機 server。</span><span class="sxs-lookup"><span data-stu-id="39017-113">Personal RD Session Host server.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="39017-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="39017-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="39017-115">用於系統管理的遠端桌面。</span><span class="sxs-lookup"><span data-stu-id="39017-115">Remote desktop for administration.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="39017-116"><span id="2"></span>**二級**</span><span class="sxs-lookup"><span data-stu-id="39017-116"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="39017-117">每一裝置/每基座。</span><span class="sxs-lookup"><span data-stu-id="39017-117">Per device/per seat.</span></span> <span data-ttu-id="39017-118">適用于應用程式伺服器。</span><span class="sxs-lookup"><span data-stu-id="39017-118">Valid for application servers.</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="39017-119"><span id="4"></span>**億**</span><span class="sxs-lookup"><span data-stu-id="39017-119"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="39017-120">每個使用者。</span><span class="sxs-lookup"><span data-stu-id="39017-120">Per User.</span></span> <span data-ttu-id="39017-121">適用于應用程式伺服器。</span><span class="sxs-lookup"><span data-stu-id="39017-121">Valid for application servers.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39017-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="39017-122">Return value</span></span>

<span data-ttu-id="39017-123">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="39017-123">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="39017-124">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="39017-124">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="39017-125">備註</span><span class="sxs-lookup"><span data-stu-id="39017-125">Remarks</span></span>

<span data-ttu-id="39017-126">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="39017-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="39017-127">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="39017-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="39017-128">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="39017-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="39017-129">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="39017-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="39017-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="39017-130">Requirements</span></span>



| <span data-ttu-id="39017-131">需求</span><span class="sxs-lookup"><span data-stu-id="39017-131">Requirement</span></span> | <span data-ttu-id="39017-132">值</span><span class="sxs-lookup"><span data-stu-id="39017-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39017-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="39017-133">Minimum supported client</span></span><br/> | <span data-ttu-id="39017-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39017-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="39017-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="39017-135">Minimum supported server</span></span><br/> | <span data-ttu-id="39017-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39017-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="39017-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="39017-137">Namespace</span></span><br/>                | <span data-ttu-id="39017-138">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="39017-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="39017-139">MOF</span><span class="sxs-lookup"><span data-stu-id="39017-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39017-140"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="39017-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="39017-141">DLL</span><span class="sxs-lookup"><span data-stu-id="39017-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39017-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39017-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39017-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39017-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39017-144">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="39017-144">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

