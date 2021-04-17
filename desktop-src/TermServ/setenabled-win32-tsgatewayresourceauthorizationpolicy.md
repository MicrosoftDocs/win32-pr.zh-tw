---
title: Win32_TSGatewayResourceAuthorizationPolicy 類別的 SetEnabled 方法
description: 啟用或停用遠端桌面資源授權原則 (RD \ 160;藉由設定 Enabled 屬性來) RAP。
ms.assetid: ee5830ba-36a1-4f28-a902-be5867439ada
ms.tgt_platform: multiple
keywords:
- SetEnabled 方法遠端桌面服務
- SetEnabled 方法遠端桌面服務，Win32_TSGatewayResourceAuthorizationPolicy 類別
- Win32_TSGatewayResourceAuthorizationPolicy 類別遠端桌面服務，SetEnabled 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0de7c4e013690a5d5e8ffd6b235a42ea43c445ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466737"
---
# <a name="setenabled-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="5d0e3-106">Win32 TSGatewayResourceAuthorizationPolicy 類別的 SetEnabled 方法 \_</span><span class="sxs-lookup"><span data-stu-id="5d0e3-106">SetEnabled method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="5d0e3-107">藉由設定 **Enabled** 屬性，啟用或停用遠端桌面資源授權原則 (RD RAP) 。</span><span class="sxs-lookup"><span data-stu-id="5d0e3-107">Enables or disables the Remote Desktop resource authorization policy (RD RAP) by setting the **Enabled** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d0e3-108">語法</span><span class="sxs-lookup"><span data-stu-id="5d0e3-108">Syntax</span></span>


```mof
uint32 SetEnabled(
  [in] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="5d0e3-109">參數</span><span class="sxs-lookup"><span data-stu-id="5d0e3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d0e3-110">*已啟用* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5d0e3-110">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d0e3-111">若 **為 True**，將會啟用 RD RAP。</span><span class="sxs-lookup"><span data-stu-id="5d0e3-111">If **True**, the RD RAP will be enabled.</span></span> <span data-ttu-id="5d0e3-112">如果 **為 False**，則會停用 RD RAP。</span><span class="sxs-lookup"><span data-stu-id="5d0e3-112">If **False**, the RD RAP will be disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d0e3-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5d0e3-113">Return value</span></span>

<span data-ttu-id="5d0e3-114">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="5d0e3-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="5d0e3-115">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="5d0e3-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="5d0e3-116">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="5d0e3-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5d0e3-117">備註</span><span class="sxs-lookup"><span data-stu-id="5d0e3-117">Remarks</span></span>

<span data-ttu-id="5d0e3-118">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="5d0e3-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="5d0e3-119">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="5d0e3-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5d0e3-120">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="5d0e3-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5d0e3-121">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="5d0e3-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5d0e3-122">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="5d0e3-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d0e3-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d0e3-123">Requirements</span></span>



| <span data-ttu-id="5d0e3-124">需求</span><span class="sxs-lookup"><span data-stu-id="5d0e3-124">Requirement</span></span> | <span data-ttu-id="5d0e3-125">值</span><span class="sxs-lookup"><span data-stu-id="5d0e3-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d0e3-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5d0e3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5d0e3-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="5d0e3-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="5d0e3-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5d0e3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5d0e3-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5d0e3-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="5d0e3-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="5d0e3-130">Namespace</span></span><br/>                | <span data-ttu-id="5d0e3-131">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="5d0e3-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="5d0e3-132">MOF</span><span class="sxs-lookup"><span data-stu-id="5d0e3-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d0e3-133"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="5d0e3-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="5d0e3-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5d0e3-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d0e3-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d0e3-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="5d0e3-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d0e3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d0e3-137">**Win32 \_ TSGatewayResourceAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="5d0e3-137">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

