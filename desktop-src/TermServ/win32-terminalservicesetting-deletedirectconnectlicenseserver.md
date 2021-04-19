---
title: Win32_TerminalServiceSetting 類別的 DeleteDirectConnectLicenseServer 方法
description: DeleteDirectConnectLicenseServer 已無法再使用。
ms.assetid: 190316ab-b8ed-4102-8346-42603d6451e6
ms.tgt_platform: multiple
keywords:
- DeleteDirectConnectLicenseServer 方法遠端桌面服務
- DeleteDirectConnectLicenseServer 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，DeleteDirectConnectLicenseServer 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.DeleteDirectConnectLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1929ee4294040e80ec9bb633bd70d4709b3e56b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968378"
---
# <a name="deletedirectconnectlicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="c4bf8-106">Win32 TerminalServiceSetting 類別的 DeleteDirectConnectLicenseServer 方法 \_</span><span class="sxs-lookup"><span data-stu-id="c4bf8-106">DeleteDirectConnectLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="c4bf8-107">\[**DeleteDirectConnectLicenseServer** 不再適用于 Windows Server 2008 R2。\]</span><span class="sxs-lookup"><span data-stu-id="c4bf8-107">\[**DeleteDirectConnectLicenseServer** is no longer available for use as of Windows Server 2008 R2.\]</span></span>

<span data-ttu-id="c4bf8-108">**Windows Server 2008：** 從登錄中移除授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="c4bf8-108">**Windows Server 2008:** Removes a license server from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4bf8-109">語法</span><span class="sxs-lookup"><span data-stu-id="c4bf8-109">Syntax</span></span>


```mof
uint32 DeleteDirectConnectLicenseServer(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a><span data-ttu-id="c4bf8-110">參數</span><span class="sxs-lookup"><span data-stu-id="c4bf8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4bf8-111">*LicenseServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c4bf8-111">*LicenseServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4bf8-112">要移除之授權伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4bf8-112">Name of the license server to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4bf8-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c4bf8-113">Return value</span></span>

<span data-ttu-id="c4bf8-114">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c4bf8-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="c4bf8-115">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="c4bf8-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4bf8-116">備註</span><span class="sxs-lookup"><span data-stu-id="c4bf8-116">Remarks</span></span>

<span data-ttu-id="c4bf8-117">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="c4bf8-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c4bf8-118">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="c4bf8-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c4bf8-119">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="c4bf8-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c4bf8-120">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="c4bf8-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4bf8-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4bf8-121">Requirements</span></span>



| <span data-ttu-id="c4bf8-122">需求</span><span class="sxs-lookup"><span data-stu-id="c4bf8-122">Requirement</span></span> | <span data-ttu-id="c4bf8-123">值</span><span class="sxs-lookup"><span data-stu-id="c4bf8-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4bf8-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c4bf8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c4bf8-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="c4bf8-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="c4bf8-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c4bf8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c4bf8-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4bf8-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c4bf8-128">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="c4bf8-128">End of client support</span></span><br/>    | <span data-ttu-id="c4bf8-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="c4bf8-129">None supported</span></span><br/>                                                               |
| <span data-ttu-id="c4bf8-130">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="c4bf8-130">End of server support</span></span><br/>    | <span data-ttu-id="c4bf8-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4bf8-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c4bf8-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="c4bf8-132">Namespace</span></span><br/>                | <span data-ttu-id="c4bf8-133">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="c4bf8-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c4bf8-134">MOF</span><span class="sxs-lookup"><span data-stu-id="c4bf8-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4bf8-135"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="c4bf8-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4bf8-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c4bf8-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4bf8-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4bf8-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4bf8-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c4bf8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4bf8-139">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="c4bf8-139">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

