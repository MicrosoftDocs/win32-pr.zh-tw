---
title: Win32_TSGatewayConnectionAuthorizationPolicy 類別的 DisableClipboard 方法
description: 設定 ClipboardDisabled 屬性。 如果 DeviceRedirectionType 屬性的值為 \ 0034; 2 \ 0034;，則 ClipboardDisabled 屬性會針對透過遠端桌面閘道 (RD 閘道) 伺服器所建立的會話控制剪貼簿的重新導向。
ms.assetid: c53fc802-958b-452d-9af9-0ce89ed46079
ms.tgt_platform: multiple
keywords:
- DisableClipboard 方法遠端桌面服務
- DisableClipboard 方法遠端桌面服務，Win32_TSGatewayConnectionAuthorizationPolicy 類別
- Win32_TSGatewayConnectionAuthorizationPolicy 類別遠端桌面服務，DisableClipboard 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisableClipboard
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23ae2070a35fa31f1c9d9ad31e9e632e31c0193f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965885"
---
# <a name="disableclipboard-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="2295a-107">Win32 TSGatewayConnectionAuthorizationPolicy 類別的 DisableClipboard 方法 \_</span><span class="sxs-lookup"><span data-stu-id="2295a-107">DisableClipboard method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="2295a-108">設定 **ClipboardDisabled** 屬性。</span><span class="sxs-lookup"><span data-stu-id="2295a-108">Sets the **ClipboardDisabled** property.</span></span> <span data-ttu-id="2295a-109">如果 **DeviceRedirectionType** 屬性的值為 "2"， **ClipboardDisabled** 屬性會控制剪貼簿的重新導向，以尋找透過遠端桌面閘道 (RD 閘道) server 所建立的會話。</span><span class="sxs-lookup"><span data-stu-id="2295a-109">If the **DeviceRedirectionType** property has a value of "2", the **ClipboardDisabled** property controls redirection of the clipboard for sessions that are established through the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="2295a-110">語法</span><span class="sxs-lookup"><span data-stu-id="2295a-110">Syntax</span></span>


```mof
uint32 DisableClipboard(
  [in] boolean Disabled
);
```



## <a name="parameters"></a><span data-ttu-id="2295a-111">參數</span><span class="sxs-lookup"><span data-stu-id="2295a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2295a-112">*已停用* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2295a-112">*Disabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2295a-113">**ClipboardDisabled** 屬性的新值。</span><span class="sxs-lookup"><span data-stu-id="2295a-113">New value for the **ClipboardDisabled** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2295a-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="2295a-114">Return value</span></span>

<span data-ttu-id="2295a-115">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="2295a-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="2295a-116">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="2295a-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="2295a-117">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="2295a-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2295a-118">備註</span><span class="sxs-lookup"><span data-stu-id="2295a-118">Remarks</span></span>

<span data-ttu-id="2295a-119">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="2295a-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="2295a-120">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="2295a-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2295a-121">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="2295a-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2295a-122">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="2295a-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2295a-123">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="2295a-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2295a-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="2295a-124">Requirements</span></span>



| <span data-ttu-id="2295a-125">需求</span><span class="sxs-lookup"><span data-stu-id="2295a-125">Requirement</span></span> | <span data-ttu-id="2295a-126">值</span><span class="sxs-lookup"><span data-stu-id="2295a-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2295a-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2295a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2295a-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="2295a-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="2295a-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2295a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2295a-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2295a-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="2295a-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="2295a-131">Namespace</span></span><br/>                | <span data-ttu-id="2295a-132">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="2295a-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="2295a-133">MOF</span><span class="sxs-lookup"><span data-stu-id="2295a-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2295a-134"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="2295a-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="2295a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2295a-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2295a-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2295a-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="2295a-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2295a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2295a-138">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="2295a-138">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

