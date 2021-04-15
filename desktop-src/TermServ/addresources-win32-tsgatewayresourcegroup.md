---
title: Win32_TSGatewayResourceGroup 類別的 AddResources 方法
description: 將資源新增至資源群組。
ms.assetid: 3210b468-6b82-4edb-ac8b-95f66a7b9328
ms.tgt_platform: multiple
keywords:
- AddResources 方法遠端桌面服務
- AddResources 方法遠端桌面服務，Win32_TSGatewayResourceGroup 類別
- Win32_TSGatewayResourceGroup 類別遠端桌面服務，AddResources 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.AddResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a37498accf76b28f16e0de45565916c18ab8d9dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508364"
---
# <a name="addresources-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="e2afa-106">Win32 TSGatewayResourceGroup 類別的 AddResources 方法 \_</span><span class="sxs-lookup"><span data-stu-id="e2afa-106">AddResources method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="e2afa-107">將資源新增至資源群組。</span><span class="sxs-lookup"><span data-stu-id="e2afa-107">Adds resources to the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2afa-108">語法</span><span class="sxs-lookup"><span data-stu-id="e2afa-108">Syntax</span></span>


```mof
uint32 AddResources(
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="e2afa-109">參數</span><span class="sxs-lookup"><span data-stu-id="e2afa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2afa-110">*資源* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e2afa-110">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2afa-111">要新增至資源群組的資源清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="e2afa-111">Semicolon-separated list of resources to be added to the resource group.</span></span> <span data-ttu-id="e2afa-112">「」 \* 表示所有資源。</span><span class="sxs-lookup"><span data-stu-id="e2afa-112">An "\*" means all resources.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2afa-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e2afa-113">Return value</span></span>

<span data-ttu-id="e2afa-114">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="e2afa-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e2afa-115">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="e2afa-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e2afa-116">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="e2afa-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e2afa-117">備註</span><span class="sxs-lookup"><span data-stu-id="e2afa-117">Remarks</span></span>

<span data-ttu-id="e2afa-118">如果 *resources* 參數中有多個資源，而且其中一個資源無法處理，則不會處理任何資源。</span><span class="sxs-lookup"><span data-stu-id="e2afa-118">If multiple resources are in the *Resources* parameter and one of the resources cannot be processed, none of the resources will be processed.</span></span>

<span data-ttu-id="e2afa-119">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="e2afa-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="e2afa-120">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="e2afa-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e2afa-121">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="e2afa-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e2afa-122">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="e2afa-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e2afa-123">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="e2afa-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2afa-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2afa-124">Requirements</span></span>



| <span data-ttu-id="e2afa-125">需求</span><span class="sxs-lookup"><span data-stu-id="e2afa-125">Requirement</span></span> | <span data-ttu-id="e2afa-126">值</span><span class="sxs-lookup"><span data-stu-id="e2afa-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2afa-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e2afa-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e2afa-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="e2afa-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e2afa-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e2afa-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e2afa-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2afa-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e2afa-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="e2afa-131">Namespace</span></span><br/>                | <span data-ttu-id="e2afa-132">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="e2afa-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="e2afa-133">MOF</span><span class="sxs-lookup"><span data-stu-id="e2afa-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2afa-134"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2afa-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2afa-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e2afa-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2afa-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2afa-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="e2afa-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2afa-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2afa-138">**Win32 \_ TSGatewayResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="e2afa-138">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

