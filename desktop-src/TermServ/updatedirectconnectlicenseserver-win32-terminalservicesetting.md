---
title: Win32_TerminalServiceSetting 類別的 UpdateDirectConnectLicenseServer 方法
description: UpdateDirectConnectLicenseServer 已無法再使用。
ms.assetid: 0b6e0dba-e23b-4c8d-8021-93d802501359
ms.tgt_platform: multiple
keywords:
- UpdateDirectConnectLicenseServer 方法遠端桌面服務
- UpdateDirectConnectLicenseServer 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，UpdateDirectConnectLicenseServer 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.UpdateDirectConnectLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2249dd00b44955a4e2712b8b7bf746793e89d57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968561"
---
# <a name="updatedirectconnectlicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="2d944-106">Win32 TerminalServiceSetting 類別的 UpdateDirectConnectLicenseServer 方法 \_</span><span class="sxs-lookup"><span data-stu-id="2d944-106">UpdateDirectConnectLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="2d944-107">\[**UpdateDirectConnectLicenseServer** 不再適用于 Windows Server 2008 R2。\]</span><span class="sxs-lookup"><span data-stu-id="2d944-107">\[**UpdateDirectConnectLicenseServer** is no longer available for use as of Windows Server 2008 R2.\]</span></span>

<span data-ttu-id="2d944-108">**Windows Server 2008：** 更新探索授權伺服器的清單。</span><span class="sxs-lookup"><span data-stu-id="2d944-108">**Windows Server 2008:** Updates the list of discovery license servers.</span></span> <span data-ttu-id="2d944-109">伺服器清單會以分號分隔 ( ";") 。</span><span class="sxs-lookup"><span data-stu-id="2d944-109">The server list is delimited by semicolons (";").</span></span>

## <a name="syntax"></a><span data-ttu-id="2d944-110">語法</span><span class="sxs-lookup"><span data-stu-id="2d944-110">Syntax</span></span>


```mof
uint32 UpdateDirectConnectLicenseServer(
  [in] string LicenseServerList
);
```



## <a name="parameters"></a><span data-ttu-id="2d944-111">參數</span><span class="sxs-lookup"><span data-stu-id="2d944-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d944-112">*LicenseServerList* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2d944-112">*LicenseServerList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d944-113">授權伺服器的清單。</span><span class="sxs-lookup"><span data-stu-id="2d944-113">List of license servers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d944-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="2d944-114">Return value</span></span>

<span data-ttu-id="2d944-115">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2d944-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="2d944-116">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="2d944-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d944-117">備註</span><span class="sxs-lookup"><span data-stu-id="2d944-117">Remarks</span></span>

<span data-ttu-id="2d944-118">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="2d944-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2d944-119">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="2d944-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2d944-120">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="2d944-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2d944-121">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="2d944-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2d944-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d944-122">Requirements</span></span>



| <span data-ttu-id="2d944-123">需求</span><span class="sxs-lookup"><span data-stu-id="2d944-123">Requirement</span></span> | <span data-ttu-id="2d944-124">值</span><span class="sxs-lookup"><span data-stu-id="2d944-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d944-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2d944-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2d944-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="2d944-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="2d944-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2d944-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2d944-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2d944-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2d944-129">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="2d944-129">End of client support</span></span><br/>    | <span data-ttu-id="2d944-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="2d944-130">None supported</span></span><br/>                                                               |
| <span data-ttu-id="2d944-131">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="2d944-131">End of server support</span></span><br/>    | <span data-ttu-id="2d944-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2d944-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2d944-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="2d944-133">Namespace</span></span><br/>                | <span data-ttu-id="2d944-134">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="2d944-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="2d944-135">MOF</span><span class="sxs-lookup"><span data-stu-id="2d944-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d944-136"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="2d944-136"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d944-137">DLL</span><span class="sxs-lookup"><span data-stu-id="2d944-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d944-138"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d944-138"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d944-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d944-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d944-140">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="2d944-140">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

