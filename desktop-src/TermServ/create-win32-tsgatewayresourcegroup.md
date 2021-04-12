---
title: Win32_TSGatewayResourceGroup 類別的 Create 方法
description: 建立資源群組。
ms.assetid: 715e6086-1c7d-4b20-983a-3ab98e875ca5
ms.tgt_platform: multiple
keywords:
- 建立方法遠端桌面服務
- 建立方法遠端桌面服務、Win32_TSGatewayResourceGroup 類別
- Win32_TSGatewayResourceGroup 類別遠端桌面服務，Create 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d9c5179967c143faa36763b7a2aabb8849d2f13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024760"
---
# <a name="create-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="57619-106">Win32 TSGatewayResourceGroup 類別的 Create 方法 \_</span><span class="sxs-lookup"><span data-stu-id="57619-106">Create method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="57619-107">建立資源群組。</span><span class="sxs-lookup"><span data-stu-id="57619-107">Creates a resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="57619-108">語法</span><span class="sxs-lookup"><span data-stu-id="57619-108">Syntax</span></span>


```mof
uint32 Create(
  [in] string Name,
  [in] string Description,
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="57619-109">參數</span><span class="sxs-lookup"><span data-stu-id="57619-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57619-110">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="57619-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57619-111">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="57619-111">Name of the resource group.</span></span>

</dd> <dt>

<span data-ttu-id="57619-112">*描述* \[在\]</span><span class="sxs-lookup"><span data-stu-id="57619-112">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57619-113">資源群組的描述。</span><span class="sxs-lookup"><span data-stu-id="57619-113">Description of the resource group.</span></span>

</dd> <dt>

<span data-ttu-id="57619-114">*資源* \[在\]</span><span class="sxs-lookup"><span data-stu-id="57619-114">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57619-115">此資源群組中的資源清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="57619-115">Semicolon-separated list of resources in this resource group.</span></span> <span data-ttu-id="57619-116">「」 \* 表示所有資源。</span><span class="sxs-lookup"><span data-stu-id="57619-116">An "\*" means all resources.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57619-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="57619-117">Return value</span></span>

<span data-ttu-id="57619-118">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="57619-118">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="57619-119">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="57619-119">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="57619-120">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="57619-120">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="57619-121">備註</span><span class="sxs-lookup"><span data-stu-id="57619-121">Remarks</span></span>

<span data-ttu-id="57619-122">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="57619-122">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="57619-123">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="57619-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="57619-124">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="57619-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="57619-125">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="57619-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="57619-126">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="57619-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="57619-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="57619-127">Requirements</span></span>



| <span data-ttu-id="57619-128">需求</span><span class="sxs-lookup"><span data-stu-id="57619-128">Requirement</span></span> | <span data-ttu-id="57619-129">值</span><span class="sxs-lookup"><span data-stu-id="57619-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="57619-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="57619-130">Minimum supported client</span></span><br/> | <span data-ttu-id="57619-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="57619-131">None supported</span></span><br/>                                                                |
| <span data-ttu-id="57619-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="57619-132">Minimum supported server</span></span><br/> | <span data-ttu-id="57619-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="57619-133">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="57619-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="57619-134">Namespace</span></span><br/>                | <span data-ttu-id="57619-135">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="57619-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="57619-136">MOF</span><span class="sxs-lookup"><span data-stu-id="57619-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="57619-137"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="57619-137"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="57619-138">DLL</span><span class="sxs-lookup"><span data-stu-id="57619-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57619-139"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57619-139"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="57619-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57619-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57619-141">**Win32 \_ TSGatewayResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="57619-141">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

