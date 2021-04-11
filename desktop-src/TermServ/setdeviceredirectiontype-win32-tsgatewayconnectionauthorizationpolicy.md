---
title: Win32_TSGatewayConnectionAuthorizationPolicy 類別的 SetDeviceRedirectionType 方法
description: 設定 DeviceRedirectionType 屬性，它會控制要重新導向的裝置。
ms.assetid: d97a0a7d-a08e-4703-b0f0-ba5d20688dc8
ms.tgt_platform: multiple
keywords:
- SetDeviceRedirectionType 方法遠端桌面服務
- SetDeviceRedirectionType 方法遠端桌面服務，Win32_TSGatewayConnectionAuthorizationPolicy 類別
- Win32_TSGatewayConnectionAuthorizationPolicy 類別遠端桌面服務，SetDeviceRedirectionType 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetDeviceRedirectionType
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98b369e0b6031aa503e2f7f55860d004f63b7f93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934293"
---
# <a name="setdeviceredirectiontype-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="0d207-106">Win32 TSGatewayConnectionAuthorizationPolicy 類別的 SetDeviceRedirectionType 方法 \_</span><span class="sxs-lookup"><span data-stu-id="0d207-106">SetDeviceRedirectionType method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="0d207-107">設定 **DeviceRedirectionType** 屬性，它會控制要重新導向的裝置。</span><span class="sxs-lookup"><span data-stu-id="0d207-107">Sets the **DeviceRedirectionType** property, which controls which devices will be redirected.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d207-108">語法</span><span class="sxs-lookup"><span data-stu-id="0d207-108">Syntax</span></span>


```mof
uint32 SetDeviceRedirectionType(
  [in] uint32 DeviceRedirectionType
);
```



## <a name="parameters"></a><span data-ttu-id="0d207-109">參數</span><span class="sxs-lookup"><span data-stu-id="0d207-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d207-110">*DeviceRedirectionType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0d207-110">*DeviceRedirectionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d207-111">裝置重新導向類型。</span><span class="sxs-lookup"><span data-stu-id="0d207-111">The device redirection type.</span></span>

<dt>

<span data-ttu-id="0d207-112">0</span><span class="sxs-lookup"><span data-stu-id="0d207-112">0</span></span>
</dt> <dd>

<span data-ttu-id="0d207-113">將會重新導向所有裝置。</span><span class="sxs-lookup"><span data-stu-id="0d207-113">All devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="0d207-114">1</span><span class="sxs-lookup"><span data-stu-id="0d207-114">1</span></span>
</dt> <dd>

<span data-ttu-id="0d207-115">將不會重新導向任何裝置。</span><span class="sxs-lookup"><span data-stu-id="0d207-115">No devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="0d207-116">2</span><span class="sxs-lookup"><span data-stu-id="0d207-116">2</span></span>
</dt> <dd>

<span data-ttu-id="0d207-117">將不會重新導向指定的裝置。</span><span class="sxs-lookup"><span data-stu-id="0d207-117">Specified devices will not be redirected.</span></span> <span data-ttu-id="0d207-118">**DiskDrivesDisabled**、 **PrintersDisabled**、 **SerialPortsDisabled**、 **ClipboardDisabled** 和 **PlugAndPlayDevicesDisabled** 屬性控制哪些裝置將不會被重新導向。</span><span class="sxs-lookup"><span data-stu-id="0d207-118">The **DiskDrivesDisabled**, **PrintersDisabled**, **SerialPortsDisabled**, **ClipboardDisabled**, and **PlugAndPlayDevicesDisabled** properties control which devices will not be redirected.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d207-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="0d207-119">Return value</span></span>

<span data-ttu-id="0d207-120">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="0d207-120">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="0d207-121">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="0d207-121">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="0d207-122">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="0d207-122">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0d207-123">備註</span><span class="sxs-lookup"><span data-stu-id="0d207-123">Remarks</span></span>

<span data-ttu-id="0d207-124">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="0d207-124">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="0d207-125">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="0d207-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0d207-126">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="0d207-126">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0d207-127">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="0d207-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0d207-128">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="0d207-128">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d207-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d207-129">Requirements</span></span>



| <span data-ttu-id="0d207-130">需求</span><span class="sxs-lookup"><span data-stu-id="0d207-130">Requirement</span></span> | <span data-ttu-id="0d207-131">值</span><span class="sxs-lookup"><span data-stu-id="0d207-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d207-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0d207-132">Minimum supported client</span></span><br/> | <span data-ttu-id="0d207-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="0d207-133">None supported</span></span><br/>                                                                |
| <span data-ttu-id="0d207-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0d207-134">Minimum supported server</span></span><br/> | <span data-ttu-id="0d207-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d207-135">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="0d207-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="0d207-136">Namespace</span></span><br/>                | <span data-ttu-id="0d207-137">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="0d207-137">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="0d207-138">MOF</span><span class="sxs-lookup"><span data-stu-id="0d207-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d207-139"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d207-139"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d207-140">DLL</span><span class="sxs-lookup"><span data-stu-id="0d207-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d207-141"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d207-141"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="0d207-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d207-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d207-143">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="0d207-143">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

