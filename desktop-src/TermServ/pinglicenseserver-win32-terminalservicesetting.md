---
title: Win32_TerminalServiceSetting 類別的 PingLicenseServer 方法
description: PingLicenseServer 已無法再使用。
ms.assetid: d2a9f273-1ff9-4391-889b-a3b9c9f95c3b
ms.tgt_platform: multiple
keywords:
- PingLicenseServer 方法遠端桌面服務
- PingLicenseServer 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，PingLicenseServer 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.PingLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fe7277b3130c88c1aec7716c1a3bf560b81db64
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384574"
---
# <a name="pinglicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="92c38-106">Win32 TerminalServiceSetting 類別的 PingLicenseServer 方法 \_</span><span class="sxs-lookup"><span data-stu-id="92c38-106">PingLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="92c38-107">\[**PingLicenseServer** 不再適用于 Windows Server 2008 R2。\]</span><span class="sxs-lookup"><span data-stu-id="92c38-107">\[**PingLicenseServer** is no longer available for use as of Windows Server 2008 R2.\]</span></span>

<span data-ttu-id="92c38-108">**Windows Server 2008：** Ping 授權伺服器以判斷它是否為有效的授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="92c38-108">**Windows Server 2008:** Pings the license server to determine if it is a valid license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="92c38-109">語法</span><span class="sxs-lookup"><span data-stu-id="92c38-109">Syntax</span></span>


```mof
uint32 PingLicenseServer(
  [in] string ServerName
);
```



## <a name="parameters"></a><span data-ttu-id="92c38-110">參數</span><span class="sxs-lookup"><span data-stu-id="92c38-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92c38-111">*ServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="92c38-111">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92c38-112">授權伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="92c38-112">Name of the license server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92c38-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="92c38-113">Return value</span></span>

<dl> <dt>

<span data-ttu-id="92c38-114">**S \_ 確定**</span><span class="sxs-lookup"><span data-stu-id="92c38-114">**S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="92c38-115">伺服器是有效的授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="92c38-115">The server is a valid license server.</span></span>

</dd> <dt>

<span data-ttu-id="92c38-116">**S \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="92c38-116">**S\_FALSE**</span></span>
</dt> <dd>

<span data-ttu-id="92c38-117">授權伺服器無效。</span><span class="sxs-lookup"><span data-stu-id="92c38-117">The license server is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="92c38-118">備註</span><span class="sxs-lookup"><span data-stu-id="92c38-118">Remarks</span></span>

<span data-ttu-id="92c38-119">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="92c38-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="92c38-120">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="92c38-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="92c38-121">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="92c38-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="92c38-122">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="92c38-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="92c38-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="92c38-123">Requirements</span></span>



| <span data-ttu-id="92c38-124">需求</span><span class="sxs-lookup"><span data-stu-id="92c38-124">Requirement</span></span> | <span data-ttu-id="92c38-125">值</span><span class="sxs-lookup"><span data-stu-id="92c38-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92c38-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="92c38-126">Minimum supported client</span></span><br/> | <span data-ttu-id="92c38-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="92c38-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="92c38-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="92c38-128">Minimum supported server</span></span><br/> | <span data-ttu-id="92c38-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92c38-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="92c38-130">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="92c38-130">End of client support</span></span><br/>    | <span data-ttu-id="92c38-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="92c38-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="92c38-132">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="92c38-132">End of server support</span></span><br/>    | <span data-ttu-id="92c38-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92c38-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="92c38-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="92c38-134">Namespace</span></span><br/>                | <span data-ttu-id="92c38-135">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="92c38-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="92c38-136">MOF</span><span class="sxs-lookup"><span data-stu-id="92c38-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92c38-137"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="92c38-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="92c38-138">DLL</span><span class="sxs-lookup"><span data-stu-id="92c38-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92c38-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92c38-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92c38-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="92c38-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92c38-141">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="92c38-141">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

