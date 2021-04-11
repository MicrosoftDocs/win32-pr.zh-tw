---
title: Win32_TerminalServiceSetting 類別的 AddDirectConnectLicenseServer 方法
description: AddDirectConnectLicenseServer 已無法再使用。
ms.assetid: 7920fd28-0fa3-4f96-bec3-d9e37c97920c
ms.tgt_platform: multiple
keywords:
- AddDirectConnectLicenseServer 方法遠端桌面服務
- AddDirectConnectLicenseServer 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，AddDirectConnectLicenseServer 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.AddDirectConnectLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be9bba23f5c0bfc69b4c8d7951ab38eac6690b84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385157"
---
# <a name="adddirectconnectlicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="73836-106">Win32 TerminalServiceSetting 類別的 AddDirectConnectLicenseServer 方法 \_</span><span class="sxs-lookup"><span data-stu-id="73836-106">AddDirectConnectLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="73836-107">\[**AddDirectConnectLicenseServer** 不再適用于 Windows Server 2008 R2。\]</span><span class="sxs-lookup"><span data-stu-id="73836-107">\[**AddDirectConnectLicenseServer** is no longer available for use as of Windows Server 2008 R2.\]</span></span>

<span data-ttu-id="73836-108">**Windows Server 2008：** 設定新的授權伺服器，並將授權伺服器新增至登錄，藉由遠端桌面工作階段主機 (RD 工作階段主機) 伺服器來進行探索。</span><span class="sxs-lookup"><span data-stu-id="73836-108">**Windows Server 2008:** Configures a new license server and adds the license server to the registry for discovery by Remote Desktop Session Host (RD Session Host) servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="73836-109">語法</span><span class="sxs-lookup"><span data-stu-id="73836-109">Syntax</span></span>


```mof
uint32 AddDirectConnectLicenseServer(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a><span data-ttu-id="73836-110">參數</span><span class="sxs-lookup"><span data-stu-id="73836-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73836-111">*LicenseServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="73836-111">*LicenseServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73836-112">要新增之授權伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="73836-112">Name of the license server to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73836-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="73836-113">Return value</span></span>

<span data-ttu-id="73836-114">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="73836-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="73836-115">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="73836-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="73836-116">備註</span><span class="sxs-lookup"><span data-stu-id="73836-116">Remarks</span></span>

<span data-ttu-id="73836-117">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="73836-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="73836-118">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="73836-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="73836-119">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="73836-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="73836-120">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="73836-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="73836-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="73836-121">Requirements</span></span>



| <span data-ttu-id="73836-122">需求</span><span class="sxs-lookup"><span data-stu-id="73836-122">Requirement</span></span> | <span data-ttu-id="73836-123">值</span><span class="sxs-lookup"><span data-stu-id="73836-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73836-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73836-124">Minimum supported client</span></span><br/> | <span data-ttu-id="73836-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="73836-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="73836-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73836-126">Minimum supported server</span></span><br/> | <span data-ttu-id="73836-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="73836-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="73836-128">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="73836-128">End of client support</span></span><br/>    | <span data-ttu-id="73836-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="73836-129">None supported</span></span><br/>                                                               |
| <span data-ttu-id="73836-130">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="73836-130">End of server support</span></span><br/>    | <span data-ttu-id="73836-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="73836-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="73836-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="73836-132">Namespace</span></span><br/>                | <span data-ttu-id="73836-133">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="73836-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="73836-134">MOF</span><span class="sxs-lookup"><span data-stu-id="73836-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73836-135"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="73836-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="73836-136">DLL</span><span class="sxs-lookup"><span data-stu-id="73836-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73836-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73836-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73836-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73836-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73836-139">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="73836-139">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

