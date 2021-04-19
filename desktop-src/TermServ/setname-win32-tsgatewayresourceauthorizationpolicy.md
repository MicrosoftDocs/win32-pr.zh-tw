---
title: Win32_TSGatewayResourceAuthorizationPolicy 類別的 SetName 方法
description: 將遠端桌面資源授權原則的 [名稱] 屬性設定 (RD \ 160;RAP) 。
ms.assetid: 3a652ece-11fe-4aa7-913d-39ef96ab1633
ms.tgt_platform: multiple
keywords:
- SetName 方法遠端桌面服務
- SetName 方法遠端桌面服務，Win32_TSGatewayResourceAuthorizationPolicy 類別
- Win32_TSGatewayResourceAuthorizationPolicy 類別遠端桌面服務，SetName 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c7e595472302d97e91026b3a84dc466e248ef5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968161"
---
# <a name="setname-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="1aa37-106">Win32 TSGatewayResourceAuthorizationPolicy 類別的 SetName 方法 \_</span><span class="sxs-lookup"><span data-stu-id="1aa37-106">SetName method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="1aa37-107">將遠端桌面資源授權原則的 [ **名稱** ] 屬性設定為 (RD RAP) 。</span><span class="sxs-lookup"><span data-stu-id="1aa37-107">Sets the **Name** property for the Remote Desktop resource authorization policy (RD RAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="1aa37-108">語法</span><span class="sxs-lookup"><span data-stu-id="1aa37-108">Syntax</span></span>


```mof
uint32 SetName(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="1aa37-109">參數</span><span class="sxs-lookup"><span data-stu-id="1aa37-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1aa37-110">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1aa37-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1aa37-111">RD RAP 的名稱。</span><span class="sxs-lookup"><span data-stu-id="1aa37-111">Name of the RD RAP.</span></span> <span data-ttu-id="1aa37-112">名稱必須為64個字元或更少，) 會忽略唯一的 (大小寫，且不能包含下列保留字元：</span><span class="sxs-lookup"><span data-stu-id="1aa37-112">The name must be 64 characters or less, unique (case is ignored), and cannot contain the following reserved characters:</span></span>

<span data-ttu-id="1aa37-113"><> ：;" / \\ \| ?</span><span class="sxs-lookup"><span data-stu-id="1aa37-113"><> : ; " / \\ \| ?</span></span> <span data-ttu-id="1aa37-114">\*\[TAB\]</span><span class="sxs-lookup"><span data-stu-id="1aa37-114">\* \[TAB\]</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1aa37-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="1aa37-115">Return value</span></span>

<span data-ttu-id="1aa37-116">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="1aa37-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="1aa37-117">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="1aa37-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="1aa37-118">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="1aa37-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1aa37-119">備註</span><span class="sxs-lookup"><span data-stu-id="1aa37-119">Remarks</span></span>

<span data-ttu-id="1aa37-120">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="1aa37-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="1aa37-121">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="1aa37-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1aa37-122">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="1aa37-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1aa37-123">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="1aa37-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1aa37-124">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="1aa37-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1aa37-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="1aa37-125">Requirements</span></span>



| <span data-ttu-id="1aa37-126">需求</span><span class="sxs-lookup"><span data-stu-id="1aa37-126">Requirement</span></span> | <span data-ttu-id="1aa37-127">值</span><span class="sxs-lookup"><span data-stu-id="1aa37-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1aa37-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1aa37-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1aa37-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="1aa37-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="1aa37-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1aa37-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1aa37-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1aa37-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="1aa37-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="1aa37-132">Namespace</span></span><br/>                | <span data-ttu-id="1aa37-133">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="1aa37-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="1aa37-134">MOF</span><span class="sxs-lookup"><span data-stu-id="1aa37-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1aa37-135"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="1aa37-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="1aa37-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1aa37-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1aa37-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1aa37-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="1aa37-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1aa37-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1aa37-139">**Win32 \_ TSGatewayResourceAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="1aa37-139">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

