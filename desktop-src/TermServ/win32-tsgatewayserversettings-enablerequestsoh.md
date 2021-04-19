---
title: Win32_TSGatewayServerSettings 類別的 EnableRequestSOH 方法
description: EnableRequestSOH 已無法再使用。
ms.assetid: 4feb7530-cced-4ead-a1fb-679b81442bb3
ms.tgt_platform: multiple
keywords:
- EnableRequestSOH 方法遠端桌面服務
- EnableRequestSOH 方法遠端桌面服務，Win32_TSGatewayServerSettings 類別
- Win32_TSGatewayServerSettings 類別遠端桌面服務，EnableRequestSOH 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableRequestSOH
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a90ed6a3929b50d13a27ec559aab534f9e06f738
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966340"
---
# <a name="enablerequestsoh-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="fb07c-106">Win32 TSGatewayServerSettings 類別的 EnableRequestSOH 方法 \_</span><span class="sxs-lookup"><span data-stu-id="fb07c-106">EnableRequestSOH method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="fb07c-107">\[從 Windows Server 2016 無法再使用 **EnableRequestSOH** 方法。\]</span><span class="sxs-lookup"><span data-stu-id="fb07c-107">\[The **EnableRequestSOH** method is no longer available as of Windows Server 2016.\]</span></span>

<span data-ttu-id="fb07c-108">啟用或停用健康狀態聲明 (SoH) 的要求。</span><span class="sxs-lookup"><span data-stu-id="fb07c-108">Enables or disables requests for a Statement of Health (SoH).</span></span>

## <a name="syntax"></a><span data-ttu-id="fb07c-109">語法</span><span class="sxs-lookup"><span data-stu-id="fb07c-109">Syntax</span></span>


```mof
uint32 EnableRequestSOH(
  [in] boolean RequestSOH
);
```



## <a name="parameters"></a><span data-ttu-id="fb07c-110">參數</span><span class="sxs-lookup"><span data-stu-id="fb07c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb07c-111">*RequestSOH* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fb07c-111">*RequestSOH* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb07c-112">指定 **TRUE** 以啟用此功能，或指定 **FALSE** 以停用此功能。</span><span class="sxs-lookup"><span data-stu-id="fb07c-112">Specify **TRUE** to enable the feature or **FALSE** to disable the feature.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb07c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="fb07c-113">Return value</span></span>

<span data-ttu-id="fb07c-114">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="fb07c-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="fb07c-115">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="fb07c-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="fb07c-116">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="fb07c-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fb07c-117">備註</span><span class="sxs-lookup"><span data-stu-id="fb07c-117">Remarks</span></span>

<span data-ttu-id="fb07c-118">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="fb07c-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="fb07c-119">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="fb07c-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fb07c-120">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="fb07c-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fb07c-121">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="fb07c-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fb07c-122">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="fb07c-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb07c-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb07c-123">Requirements</span></span>



| <span data-ttu-id="fb07c-124">需求</span><span class="sxs-lookup"><span data-stu-id="fb07c-124">Requirement</span></span> | <span data-ttu-id="fb07c-125">值</span><span class="sxs-lookup"><span data-stu-id="fb07c-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb07c-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fb07c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fb07c-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="fb07c-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="fb07c-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fb07c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fb07c-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fb07c-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="fb07c-130">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="fb07c-130">End of server support</span></span><br/>    | <span data-ttu-id="fb07c-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fb07c-131">Windows Server 2012 R2</span></span><br/>                                                        |
| <span data-ttu-id="fb07c-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="fb07c-132">Namespace</span></span><br/>                | <span data-ttu-id="fb07c-133">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="fb07c-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="fb07c-134">MOF</span><span class="sxs-lookup"><span data-stu-id="fb07c-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb07c-135"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="fb07c-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="fb07c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="fb07c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb07c-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb07c-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="fb07c-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb07c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb07c-139">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="fb07c-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

