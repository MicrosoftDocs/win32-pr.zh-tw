---
title: Win32_TSGatewayResourceGroup 類別的 SetName 方法
description: 設定資源群組的名稱屬性。
ms.assetid: 2c2fe1b6-5826-490e-aec2-479a0191e215
ms.tgt_platform: multiple
keywords:
- SetName 方法遠端桌面服務
- SetName 方法遠端桌面服務，Win32_TSGatewayResourceGroup 類別
- Win32_TSGatewayResourceGroup 類別遠端桌面服務，SetName 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.SetName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac9ea16eb82896bb8fad67fff7ed849308100726
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843580"
---
# <a name="setname-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="61122-106">Win32 TSGatewayResourceGroup 類別的 SetName 方法 \_</span><span class="sxs-lookup"><span data-stu-id="61122-106">SetName method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="61122-107">設定資源群組的 **名稱** 屬性。</span><span class="sxs-lookup"><span data-stu-id="61122-107">Sets the **Name** property for the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="61122-108">語法</span><span class="sxs-lookup"><span data-stu-id="61122-108">Syntax</span></span>


```mof
uint32 SetName(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="61122-109">參數</span><span class="sxs-lookup"><span data-stu-id="61122-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61122-110">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="61122-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61122-111">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="61122-111">Name of the resource group.</span></span> <span data-ttu-id="61122-112">名稱必須為64個字元或更少，) 會忽略唯一的 (大小寫，且不能包含下列保留字元：</span><span class="sxs-lookup"><span data-stu-id="61122-112">The name must be 64 characters or less, unique (case is ignored), and cannot contain the following reserved characters:</span></span>

<span data-ttu-id="61122-113"><> ：;" / \\ \| ?</span><span class="sxs-lookup"><span data-stu-id="61122-113"><> : ; " / \\ \| ?</span></span> <span data-ttu-id="61122-114">\*\[TAB\]</span><span class="sxs-lookup"><span data-stu-id="61122-114">\* \[TAB\]</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61122-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="61122-115">Return value</span></span>

<span data-ttu-id="61122-116">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="61122-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="61122-117">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="61122-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="61122-118">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="61122-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="61122-119">備註</span><span class="sxs-lookup"><span data-stu-id="61122-119">Remarks</span></span>

<span data-ttu-id="61122-120">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="61122-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="61122-121">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="61122-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="61122-122">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="61122-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="61122-123">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="61122-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="61122-124">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="61122-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="61122-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="61122-125">Requirements</span></span>



| <span data-ttu-id="61122-126">需求</span><span class="sxs-lookup"><span data-stu-id="61122-126">Requirement</span></span> | <span data-ttu-id="61122-127">值</span><span class="sxs-lookup"><span data-stu-id="61122-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="61122-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="61122-128">Minimum supported client</span></span><br/> | <span data-ttu-id="61122-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="61122-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="61122-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="61122-130">Minimum supported server</span></span><br/> | <span data-ttu-id="61122-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61122-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="61122-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="61122-132">Namespace</span></span><br/>                | <span data-ttu-id="61122-133">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="61122-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="61122-134">MOF</span><span class="sxs-lookup"><span data-stu-id="61122-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61122-135"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="61122-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="61122-136">DLL</span><span class="sxs-lookup"><span data-stu-id="61122-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61122-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61122-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="61122-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61122-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61122-139">**Win32 \_ TSGatewayResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="61122-139">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

