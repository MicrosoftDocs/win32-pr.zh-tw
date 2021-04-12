---
title: Win32_TSGatewayResourceGroup 類別的 RemoveResources 方法
description: 移除資源群組中的資源。
ms.assetid: 5f339990-8273-4658-843e-b6b7a85808e1
ms.tgt_platform: multiple
keywords:
- RemoveResources 方法遠端桌面服務
- RemoveResources 方法遠端桌面服務，Win32_TSGatewayResourceGroup 類別
- Win32_TSGatewayResourceGroup 類別遠端桌面服務，RemoveResources 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.RemoveResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2e3d1cc1e39d8c96833fc6a371741493457a28b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385258"
---
# <a name="removeresources-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="31345-106">Win32 TSGatewayResourceGroup 類別的 RemoveResources 方法 \_</span><span class="sxs-lookup"><span data-stu-id="31345-106">RemoveResources method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="31345-107">移除資源群組中的資源。</span><span class="sxs-lookup"><span data-stu-id="31345-107">Removes resources from the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="31345-108">語法</span><span class="sxs-lookup"><span data-stu-id="31345-108">Syntax</span></span>


```mof
uint32 RemoveResources(
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="31345-109">參數</span><span class="sxs-lookup"><span data-stu-id="31345-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31345-110">*資源* \[在\]</span><span class="sxs-lookup"><span data-stu-id="31345-110">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31345-111">要移除的資源清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="31345-111">Semicolon-separated list of resources to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31345-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="31345-112">Return value</span></span>

<span data-ttu-id="31345-113">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="31345-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="31345-114">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="31345-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="31345-115">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="31345-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="31345-116">備註</span><span class="sxs-lookup"><span data-stu-id="31345-116">Remarks</span></span>

<span data-ttu-id="31345-117">如果 *resources* 參數中有多個資源，而且其中一個資源無法處理，則不會處理任何資源。</span><span class="sxs-lookup"><span data-stu-id="31345-117">If multiple resources are in the *Resources* parameter and one of the resources cannot be processed, none of the resources will be processed.</span></span>

<span data-ttu-id="31345-118">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="31345-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="31345-119">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="31345-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="31345-120">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="31345-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="31345-121">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="31345-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="31345-122">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="31345-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="31345-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="31345-123">Requirements</span></span>



| <span data-ttu-id="31345-124">需求</span><span class="sxs-lookup"><span data-stu-id="31345-124">Requirement</span></span> | <span data-ttu-id="31345-125">值</span><span class="sxs-lookup"><span data-stu-id="31345-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="31345-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="31345-126">Minimum supported client</span></span><br/> | <span data-ttu-id="31345-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="31345-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="31345-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="31345-128">Minimum supported server</span></span><br/> | <span data-ttu-id="31345-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31345-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="31345-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="31345-130">Namespace</span></span><br/>                | <span data-ttu-id="31345-131">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="31345-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="31345-132">MOF</span><span class="sxs-lookup"><span data-stu-id="31345-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31345-133"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="31345-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="31345-134">DLL</span><span class="sxs-lookup"><span data-stu-id="31345-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31345-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31345-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="31345-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31345-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31345-137">**Win32 \_ TSGatewayResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="31345-137">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

