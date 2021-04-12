---
title: Win32_TSGatewayResourceGroup 類別的 SetResources 方法
description: 設定此資源群組的資源屬性。
ms.assetid: 0043ee04-26d1-4907-87cc-a15f72cb0b93
ms.tgt_platform: multiple
keywords:
- SetResources 方法遠端桌面服務
- SetResources 方法遠端桌面服務，Win32_TSGatewayResourceGroup 類別
- Win32_TSGatewayResourceGroup 類別遠端桌面服務，SetResources 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.SetResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b23f2ca14597fc7d6ce3660e6e180bf93dfd86cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384274"
---
# <a name="setresources-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="619da-106">Win32 TSGatewayResourceGroup 類別的 SetResources 方法 \_</span><span class="sxs-lookup"><span data-stu-id="619da-106">SetResources method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="619da-107">設定此資源群組的 **資源** 屬性。</span><span class="sxs-lookup"><span data-stu-id="619da-107">Sets the **Resources** property for this resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="619da-108">語法</span><span class="sxs-lookup"><span data-stu-id="619da-108">Syntax</span></span>


```mof
uint32 SetResources(
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="619da-109">參數</span><span class="sxs-lookup"><span data-stu-id="619da-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="619da-110">*資源* \[在\]</span><span class="sxs-lookup"><span data-stu-id="619da-110">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="619da-111">此資源群組中的資源清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="619da-111">Semicolon-separated list of resources in this resource group.</span></span> <span data-ttu-id="619da-112">「」 \* 表示所有資源。</span><span class="sxs-lookup"><span data-stu-id="619da-112">An "\*" means all resources.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="619da-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="619da-113">Return value</span></span>

<span data-ttu-id="619da-114">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="619da-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="619da-115">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="619da-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="619da-116">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="619da-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="619da-117">備註</span><span class="sxs-lookup"><span data-stu-id="619da-117">Remarks</span></span>

<span data-ttu-id="619da-118">如果 *resources* 參數中有多個資源，而且其中一個資源無法處理，則不會處理任何資源。</span><span class="sxs-lookup"><span data-stu-id="619da-118">If multiple resources are in the *Resources* parameter and one of the resources cannot be processed, none of the resources will be processed.</span></span>

<span data-ttu-id="619da-119">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="619da-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="619da-120">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="619da-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="619da-121">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="619da-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="619da-122">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="619da-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="619da-123">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="619da-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="619da-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="619da-124">Requirements</span></span>



| <span data-ttu-id="619da-125">需求</span><span class="sxs-lookup"><span data-stu-id="619da-125">Requirement</span></span> | <span data-ttu-id="619da-126">值</span><span class="sxs-lookup"><span data-stu-id="619da-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="619da-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="619da-127">Minimum supported client</span></span><br/> | <span data-ttu-id="619da-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="619da-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="619da-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="619da-129">Minimum supported server</span></span><br/> | <span data-ttu-id="619da-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="619da-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="619da-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="619da-131">Namespace</span></span><br/>                | <span data-ttu-id="619da-132">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="619da-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="619da-133">MOF</span><span class="sxs-lookup"><span data-stu-id="619da-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="619da-134"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="619da-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="619da-135">DLL</span><span class="sxs-lookup"><span data-stu-id="619da-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="619da-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="619da-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="619da-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="619da-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="619da-138">**Win32 \_ TSGatewayResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="619da-138">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

