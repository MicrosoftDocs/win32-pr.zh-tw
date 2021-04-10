---
title: Win32_TSGatewayServerSettings 類別的 TSGStoreAdminMsg 方法
description: 更新閘道伺服器的系統管理訊息。
ms.assetid: 84e5b967-12fd-47a7-93e4-2550c15c4491
ms.tgt_platform: multiple
keywords:
- TSGStoreAdminMsg 方法遠端桌面服務
- TSGStoreAdminMsg 方法遠端桌面服務，Win32_TSGatewayServerSettings 類別
- Win32_TSGatewayServerSettings 類別遠端桌面服務，TSGStoreAdminMsg 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.TSGStoreAdminMsg
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 398a027d28970b28b4a1e7db37b5fbfee06e881e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843692"
---
# <a name="tsgstoreadminmsg-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="ffe86-106">Win32 TSGatewayServerSettings 類別的 TSGStoreAdminMsg 方法 \_</span><span class="sxs-lookup"><span data-stu-id="ffe86-106">TSGStoreAdminMsg method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="ffe86-107">更新閘道伺服器的系統管理訊息。</span><span class="sxs-lookup"><span data-stu-id="ffe86-107">Updates the administrative message for the gateway server.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffe86-108">語法</span><span class="sxs-lookup"><span data-stu-id="ffe86-108">Syntax</span></span>


```mof
uint32 TSGStoreAdminMsg(
  [in] string TSGAdmMsg,
  [in] string MsgStartTime,
  [in] string MsgEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="ffe86-109">參數</span><span class="sxs-lookup"><span data-stu-id="ffe86-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffe86-110">*TSGAdmMsg* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ffe86-110">*TSGAdmMsg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffe86-111">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ffe86-111">Type: **string**</span></span>

<span data-ttu-id="ffe86-112">系統管理郵件內文。</span><span class="sxs-lookup"><span data-stu-id="ffe86-112">The administrative message text.</span></span>

</dd> <dt>

<span data-ttu-id="ffe86-113">*MsgStartTime* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ffe86-113">*MsgStartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffe86-114">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ffe86-114">Type: **string**</span></span>

<span data-ttu-id="ffe86-115">管理訊息開始時間。</span><span class="sxs-lookup"><span data-stu-id="ffe86-115">The administrative message start time.</span></span>

</dd> <dt>

<span data-ttu-id="ffe86-116">*MsgEndTime* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ffe86-116">*MsgEndTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffe86-117">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ffe86-117">Type: **string**</span></span>

<span data-ttu-id="ffe86-118">系統管理訊息的結束時間。</span><span class="sxs-lookup"><span data-stu-id="ffe86-118">The administrative message end time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffe86-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="ffe86-119">Return value</span></span>

<span data-ttu-id="ffe86-120">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ffe86-120">Type: **uint32**</span></span>

<span data-ttu-id="ffe86-121">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="ffe86-121">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="ffe86-122">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="ffe86-122">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="ffe86-123">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="ffe86-123">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ffe86-124">備註</span><span class="sxs-lookup"><span data-stu-id="ffe86-124">Remarks</span></span>

<span data-ttu-id="ffe86-125">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="ffe86-125">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="ffe86-126">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="ffe86-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ffe86-127">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="ffe86-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ffe86-128">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="ffe86-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ffe86-129">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="ffe86-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ffe86-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="ffe86-130">Requirements</span></span>



| <span data-ttu-id="ffe86-131">需求</span><span class="sxs-lookup"><span data-stu-id="ffe86-131">Requirement</span></span> | <span data-ttu-id="ffe86-132">值</span><span class="sxs-lookup"><span data-stu-id="ffe86-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffe86-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ffe86-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ffe86-134">都不支援</span><span class="sxs-lookup"><span data-stu-id="ffe86-134">None supported</span></span><br/>                                                                |
| <span data-ttu-id="ffe86-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ffe86-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ffe86-136">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ffe86-136">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="ffe86-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="ffe86-137">Namespace</span></span><br/>                | <span data-ttu-id="ffe86-138">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="ffe86-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="ffe86-139">MOF</span><span class="sxs-lookup"><span data-stu-id="ffe86-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ffe86-140"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="ffe86-140"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="ffe86-141">DLL</span><span class="sxs-lookup"><span data-stu-id="ffe86-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffe86-142"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffe86-142"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="ffe86-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ffe86-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffe86-144">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="ffe86-144">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

