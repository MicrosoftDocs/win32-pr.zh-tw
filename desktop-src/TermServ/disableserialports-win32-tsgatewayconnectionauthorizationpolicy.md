---
title: Win32_TSGatewayConnectionAuthorizationPolicy 類別的 DisableSerialPorts 方法
description: 設定 SerialPortsDisabled 屬性。
ms.assetid: 95c027e3-f76d-4335-84ac-93a1c3718e66
ms.tgt_platform: multiple
keywords:
- DisableSerialPorts 方法遠端桌面服務
- DisableSerialPorts 方法遠端桌面服務，Win32_TSGatewayConnectionAuthorizationPolicy 類別
- Win32_TSGatewayConnectionAuthorizationPolicy 類別遠端桌面服務，DisableSerialPorts 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisableSerialPorts
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a4f6941f8bc98d7f8e424a984922ad1f6631c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685636"
---
# <a name="disableserialports-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="a54f7-106">Win32 TSGatewayConnectionAuthorizationPolicy 類別的 DisableSerialPorts 方法 \_</span><span class="sxs-lookup"><span data-stu-id="a54f7-106">DisableSerialPorts method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="a54f7-107">設定 **SerialPortsDisabled** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a54f7-107">Sets the **SerialPortsDisabled** property.</span></span> <span data-ttu-id="a54f7-108">如果 **DeviceRedirectionType** 屬性的值為 "2"， **SerialPortsDisabled** 屬性就會針對透過遠端桌面閘道 (RD 閘道) 伺服器所建立的會話，控制序列埠的重新導向。</span><span class="sxs-lookup"><span data-stu-id="a54f7-108">If the **DeviceRedirectionType** property has a value of "2", the **SerialPortsDisabled** property controls redirection of the serial ports for sessions that are established through the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="a54f7-109">語法</span><span class="sxs-lookup"><span data-stu-id="a54f7-109">Syntax</span></span>


```mof
uint32 DisableSerialPorts(
  [in] boolean Disabled
);
```



## <a name="parameters"></a><span data-ttu-id="a54f7-110">參數</span><span class="sxs-lookup"><span data-stu-id="a54f7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a54f7-111">*已停用* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a54f7-111">*Disabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a54f7-112">**SerialPortsDisabled** 屬性的新值。</span><span class="sxs-lookup"><span data-stu-id="a54f7-112">New value for the **SerialPortsDisabled** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a54f7-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a54f7-113">Return value</span></span>

<span data-ttu-id="a54f7-114">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="a54f7-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="a54f7-115">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="a54f7-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="a54f7-116">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="a54f7-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a54f7-117">備註</span><span class="sxs-lookup"><span data-stu-id="a54f7-117">Remarks</span></span>

<span data-ttu-id="a54f7-118">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="a54f7-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="a54f7-119">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="a54f7-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a54f7-120">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="a54f7-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a54f7-121">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="a54f7-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a54f7-122">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="a54f7-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a54f7-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="a54f7-123">Requirements</span></span>



| <span data-ttu-id="a54f7-124">需求</span><span class="sxs-lookup"><span data-stu-id="a54f7-124">Requirement</span></span> | <span data-ttu-id="a54f7-125">值</span><span class="sxs-lookup"><span data-stu-id="a54f7-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a54f7-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a54f7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a54f7-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="a54f7-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="a54f7-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a54f7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a54f7-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a54f7-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a54f7-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="a54f7-130">Namespace</span></span><br/>                | <span data-ttu-id="a54f7-131">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="a54f7-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="a54f7-132">MOF</span><span class="sxs-lookup"><span data-stu-id="a54f7-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a54f7-133"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="a54f7-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="a54f7-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a54f7-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a54f7-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a54f7-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="a54f7-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a54f7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a54f7-137">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="a54f7-137">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

