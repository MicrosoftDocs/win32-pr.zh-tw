---
title: Win32_TSGatewayConnectionAuthorizationPolicy 類別的 SetSecureIdAllowed 方法
description: 這個方法是保留供日後使用。
ms.assetid: 9f49e69a-c004-4e3e-b238-69865e3bf00b
ms.tgt_platform: multiple
keywords:
- SetSecureIdAllowed 方法遠端桌面服務
- SetSecureIdAllowed 方法遠端桌面服務，Win32_TSGatewayConnectionAuthorizationPolicy 類別
- Win32_TSGatewayConnectionAuthorizationPolicy 類別遠端桌面服務，SetSecureIdAllowed 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetSecureIdAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70e61c158a7dfcafb6d1d5ac66833e42284b818d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968365"
---
# <a name="setsecureidallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="c9cbc-106">Win32 TSGatewayConnectionAuthorizationPolicy 類別的 SetSecureIdAllowed 方法 \_</span><span class="sxs-lookup"><span data-stu-id="c9cbc-106">SetSecureIdAllowed method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="c9cbc-107">這個方法是保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="c9cbc-107">This method is reserved for future use.</span></span>

<span data-ttu-id="c9cbc-108">設定 **SecureIdAllowed** 屬性，這會保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="c9cbc-108">Sets the **SecureIdAllowed** property, which is reserved for future use.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9cbc-109">語法</span><span class="sxs-lookup"><span data-stu-id="c9cbc-109">Syntax</span></span>


```mof
uint32 SetSecureIdAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a><span data-ttu-id="c9cbc-110">參數</span><span class="sxs-lookup"><span data-stu-id="c9cbc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9cbc-111">*允許* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c9cbc-111">*Allowed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9cbc-112">新的 **SecureIdAllowed** 值。</span><span class="sxs-lookup"><span data-stu-id="c9cbc-112">New **SecureIdAllowed** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9cbc-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c9cbc-113">Return value</span></span>

<span data-ttu-id="c9cbc-114">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="c9cbc-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="c9cbc-115">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="c9cbc-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="c9cbc-116">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="c9cbc-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c9cbc-117">備註</span><span class="sxs-lookup"><span data-stu-id="c9cbc-117">Remarks</span></span>

<span data-ttu-id="c9cbc-118">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="c9cbc-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="c9cbc-119">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="c9cbc-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c9cbc-120">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="c9cbc-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c9cbc-121">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="c9cbc-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c9cbc-122">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="c9cbc-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9cbc-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9cbc-123">Requirements</span></span>



| <span data-ttu-id="c9cbc-124">需求</span><span class="sxs-lookup"><span data-stu-id="c9cbc-124">Requirement</span></span> | <span data-ttu-id="c9cbc-125">值</span><span class="sxs-lookup"><span data-stu-id="c9cbc-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9cbc-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c9cbc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c9cbc-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="c9cbc-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="c9cbc-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c9cbc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c9cbc-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9cbc-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c9cbc-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="c9cbc-130">Namespace</span></span><br/>                | <span data-ttu-id="c9cbc-131">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="c9cbc-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="c9cbc-132">MOF</span><span class="sxs-lookup"><span data-stu-id="c9cbc-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9cbc-133"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9cbc-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="c9cbc-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c9cbc-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9cbc-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9cbc-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="c9cbc-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9cbc-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9cbc-137">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="c9cbc-137">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

