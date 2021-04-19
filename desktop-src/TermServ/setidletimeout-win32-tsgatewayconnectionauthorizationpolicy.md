---
title: Win32_TSGatewayConnectionAuthorizationPolicy 類別的 SetIdleTimeout 方法
description: 設定 IdleTimeout 屬性。
ms.assetid: 162224dd-e4d4-483f-9ec4-b87731bc5014
ms.tgt_platform: multiple
keywords:
- SetIdleTimeout 方法遠端桌面服務
- SetIdleTimeout 方法遠端桌面服務，Win32_TSGatewayConnectionAuthorizationPolicy 類別
- Win32_TSGatewayConnectionAuthorizationPolicy 類別遠端桌面服務，SetIdleTimeout 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetIdleTimeout
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c166311477dc9de94ca6c9614e14ac98907b406
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969625"
---
# <a name="setidletimeout-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="10aa6-106">Win32 TSGatewayConnectionAuthorizationPolicy 類別的 SetIdleTimeout 方法 \_</span><span class="sxs-lookup"><span data-stu-id="10aa6-106">SetIdleTimeout method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="10aa6-107">設定 **IdleTimeout** 屬性。</span><span class="sxs-lookup"><span data-stu-id="10aa6-107">Sets the **IdleTimeout** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="10aa6-108">語法</span><span class="sxs-lookup"><span data-stu-id="10aa6-108">Syntax</span></span>


```mof
uint32 SetIdleTimeout(
  [in] uint32 IdleTimeout
);
```



## <a name="parameters"></a><span data-ttu-id="10aa6-109">參數</span><span class="sxs-lookup"><span data-stu-id="10aa6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10aa6-110">*IdleTimeout* \[在\]</span><span class="sxs-lookup"><span data-stu-id="10aa6-110">*IdleTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10aa6-111">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="10aa6-111">Type: **uint32**</span></span>

<span data-ttu-id="10aa6-112">新的超時值（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="10aa6-112">The new timeout value, in minutes.</span></span> <span data-ttu-id="10aa6-113">值為0表示沒有任何超時時間。</span><span class="sxs-lookup"><span data-stu-id="10aa6-113">A value of 0 means there is no timeout.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10aa6-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="10aa6-114">Return value</span></span>

<span data-ttu-id="10aa6-115">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="10aa6-115">Type: **uint32**</span></span>

<span data-ttu-id="10aa6-116">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="10aa6-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="10aa6-117">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="10aa6-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="10aa6-118">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="10aa6-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="10aa6-119">備註</span><span class="sxs-lookup"><span data-stu-id="10aa6-119">Remarks</span></span>

<span data-ttu-id="10aa6-120">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="10aa6-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="10aa6-121">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="10aa6-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="10aa6-122">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="10aa6-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="10aa6-123">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="10aa6-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="10aa6-124">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="10aa6-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="10aa6-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="10aa6-125">Requirements</span></span>



| <span data-ttu-id="10aa6-126">需求</span><span class="sxs-lookup"><span data-stu-id="10aa6-126">Requirement</span></span> | <span data-ttu-id="10aa6-127">值</span><span class="sxs-lookup"><span data-stu-id="10aa6-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="10aa6-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10aa6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="10aa6-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="10aa6-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="10aa6-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10aa6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="10aa6-131">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="10aa6-131">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="10aa6-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="10aa6-132">Namespace</span></span><br/>                | <span data-ttu-id="10aa6-133">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="10aa6-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="10aa6-134">MOF</span><span class="sxs-lookup"><span data-stu-id="10aa6-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10aa6-135"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="10aa6-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="10aa6-136">DLL</span><span class="sxs-lookup"><span data-stu-id="10aa6-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10aa6-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10aa6-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="10aa6-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10aa6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10aa6-139">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="10aa6-139">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

