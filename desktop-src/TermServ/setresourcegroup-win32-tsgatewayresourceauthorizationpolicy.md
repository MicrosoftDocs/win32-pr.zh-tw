---
title: Win32_TSGatewayResourceAuthorizationPolicy 類別的 SetResourceGroup 方法
description: 設定資源群組的類型和名稱。
ms.assetid: a3dd0ffa-a39b-46f9-8317-fcc90a8afcd1
ms.tgt_platform: multiple
keywords:
- SetResourceGroup 方法遠端桌面服務
- SetResourceGroup 方法遠端桌面服務，Win32_TSGatewayResourceAuthorizationPolicy 類別
- Win32_TSGatewayResourceAuthorizationPolicy 類別遠端桌面服務，SetResourceGroup 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetResourceGroup
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d22c2ceacbbbfc40372d0f0d084cf6525f754934
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843908"
---
# <a name="setresourcegroup-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="e4fcc-106">Win32 TSGatewayResourceAuthorizationPolicy 類別的 SetResourceGroup 方法 \_</span><span class="sxs-lookup"><span data-stu-id="e4fcc-106">SetResourceGroup method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="e4fcc-107">設定資源群組的類型和名稱。</span><span class="sxs-lookup"><span data-stu-id="e4fcc-107">Sets the resource group type and name.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4fcc-108">語法</span><span class="sxs-lookup"><span data-stu-id="e4fcc-108">Syntax</span></span>


```mof
uint32 SetResourceGroup(
  [in] string ResourceGroupName,
  [in] string ResourceGroupType
);
```



## <a name="parameters"></a><span data-ttu-id="e4fcc-109">參數</span><span class="sxs-lookup"><span data-stu-id="e4fcc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4fcc-110">*ResourceGroupName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e4fcc-110">*ResourceGroupName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4fcc-111">資源群組名稱。</span><span class="sxs-lookup"><span data-stu-id="e4fcc-111">Resource group name.</span></span> <span data-ttu-id="e4fcc-112">這個值會取代現有的 **ResourceGroupName** 屬性。</span><span class="sxs-lookup"><span data-stu-id="e4fcc-112">This value replaces the existing **ResourceGroupName** property.</span></span>

</dd> <dt>

<span data-ttu-id="e4fcc-113">*ResourceGroupType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e4fcc-113">*ResourceGroupType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4fcc-114">識別資源群組的類型。</span><span class="sxs-lookup"><span data-stu-id="e4fcc-114">Identifies the type of the resource group.</span></span> <span data-ttu-id="e4fcc-115">這個值會取代現有的 **ResourceGroupType** 屬性。</span><span class="sxs-lookup"><span data-stu-id="e4fcc-115">This value replaces the existing **ResourceGroupType** property.</span></span>

<dt>

<span data-ttu-id="e4fcc-116">RG</span><span class="sxs-lookup"><span data-stu-id="e4fcc-116">"RG"</span></span>
</dt> <dd>

<span data-ttu-id="e4fcc-117">資源群組。</span><span class="sxs-lookup"><span data-stu-id="e4fcc-117">Resource group.</span></span>

</dd> <dt>

<span data-ttu-id="e4fcc-118">CG</span><span class="sxs-lookup"><span data-stu-id="e4fcc-118">"CG"</span></span>
</dt> <dd>

<span data-ttu-id="e4fcc-119">電腦群組，儲存在 Active Directory Domain Services 中。</span><span class="sxs-lookup"><span data-stu-id="e4fcc-119">Computer group, as stored in Active Directory Domain Services.</span></span>

</dd> <dt>

<span data-ttu-id="e4fcc-120">ALL</span><span class="sxs-lookup"><span data-stu-id="e4fcc-120">"ALL"</span></span>
</dt> <dd>

<span data-ttu-id="e4fcc-121">所有資源。</span><span class="sxs-lookup"><span data-stu-id="e4fcc-121">All resources.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4fcc-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="e4fcc-122">Return value</span></span>

<span data-ttu-id="e4fcc-123">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="e4fcc-123">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e4fcc-124">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="e4fcc-124">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e4fcc-125">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="e4fcc-125">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e4fcc-126">備註</span><span class="sxs-lookup"><span data-stu-id="e4fcc-126">Remarks</span></span>

<span data-ttu-id="e4fcc-127">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="e4fcc-127">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="e4fcc-128">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="e4fcc-128">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e4fcc-129">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="e4fcc-129">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e4fcc-130">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="e4fcc-130">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e4fcc-131">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="e4fcc-131">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4fcc-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="e4fcc-132">Requirements</span></span>



| <span data-ttu-id="e4fcc-133">需求</span><span class="sxs-lookup"><span data-stu-id="e4fcc-133">Requirement</span></span> | <span data-ttu-id="e4fcc-134">值</span><span class="sxs-lookup"><span data-stu-id="e4fcc-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4fcc-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e4fcc-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e4fcc-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="e4fcc-136">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e4fcc-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e4fcc-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e4fcc-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e4fcc-138">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e4fcc-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="e4fcc-139">Namespace</span></span><br/>                | <span data-ttu-id="e4fcc-140">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="e4fcc-140">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="e4fcc-141">MOF</span><span class="sxs-lookup"><span data-stu-id="e4fcc-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e4fcc-142"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="e4fcc-142"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="e4fcc-143">DLL</span><span class="sxs-lookup"><span data-stu-id="e4fcc-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4fcc-144"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4fcc-144"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="e4fcc-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e4fcc-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4fcc-146">**Win32 \_ TSGatewayResourceAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="e4fcc-146">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

