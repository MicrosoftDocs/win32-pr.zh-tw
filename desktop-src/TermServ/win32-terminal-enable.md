---
title: Enable Win32_Terminal 類別的方法
description: Enable 方法會停用或啟用終端機。
ms.assetid: f249563b-6fa0-413c-9fc7-01dd16d5c561
ms.tgt_platform: multiple
keywords:
- 啟用方法遠端桌面服務
- 啟用方法遠端桌面服務、Win32_Terminal 類別
- Win32_Terminal 類別遠端桌面服務，Enable 方法
topic_type:
- apiref
api_name:
- Win32_Terminal.Enable
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afedef572c65f249c48da850172bb9fc4d222c19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384146"
---
# <a name="enable-method-of-the-win32_terminal-class"></a><span data-ttu-id="3bf2e-106">啟用 Win32 終端機類別的方法 \_</span><span class="sxs-lookup"><span data-stu-id="3bf2e-106">Enable method of the Win32\_Terminal class</span></span>

<span data-ttu-id="3bf2e-107">**Enable** 方法會停用或啟用終端機。</span><span class="sxs-lookup"><span data-stu-id="3bf2e-107">The **Enable** method disables or enables the terminal.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bf2e-108">語法</span><span class="sxs-lookup"><span data-stu-id="3bf2e-108">Syntax</span></span>


```mof
uint32 Enable(
  [in] uint32 fEnableTerminal
);
```



## <a name="parameters"></a><span data-ttu-id="3bf2e-109">參數</span><span class="sxs-lookup"><span data-stu-id="3bf2e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bf2e-110">*fEnableTerminal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3bf2e-110">*fEnableTerminal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bf2e-111">停用或啟用終端機的旗標。</span><span class="sxs-lookup"><span data-stu-id="3bf2e-111">Flag that disables or enables the terminal.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="3bf2e-112"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="3bf2e-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="3bf2e-113">終端機已停用。</span><span class="sxs-lookup"><span data-stu-id="3bf2e-113">The terminal is disabled.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="3bf2e-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="3bf2e-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="3bf2e-115">終端機已啟用。</span><span class="sxs-lookup"><span data-stu-id="3bf2e-115">The terminal is enabled.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bf2e-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="3bf2e-116">Return value</span></span>

<span data-ttu-id="3bf2e-117">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3bf2e-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="3bf2e-118">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="3bf2e-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bf2e-119">備註</span><span class="sxs-lookup"><span data-stu-id="3bf2e-119">Remarks</span></span>

<span data-ttu-id="3bf2e-120">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="3bf2e-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3bf2e-121">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="3bf2e-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3bf2e-122">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="3bf2e-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3bf2e-123">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="3bf2e-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="3bf2e-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="3bf2e-124">Requirements</span></span>



| <span data-ttu-id="3bf2e-125">需求</span><span class="sxs-lookup"><span data-stu-id="3bf2e-125">Requirement</span></span> | <span data-ttu-id="3bf2e-126">值</span><span class="sxs-lookup"><span data-stu-id="3bf2e-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3bf2e-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3bf2e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3bf2e-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3bf2e-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3bf2e-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3bf2e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3bf2e-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3bf2e-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3bf2e-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="3bf2e-131">Namespace</span></span><br/>                | <span data-ttu-id="3bf2e-132">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="3bf2e-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="3bf2e-133">MOF</span><span class="sxs-lookup"><span data-stu-id="3bf2e-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3bf2e-134"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="3bf2e-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="3bf2e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3bf2e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3bf2e-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3bf2e-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bf2e-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3bf2e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bf2e-138">**Win32 \_ 終端機**</span><span class="sxs-lookup"><span data-stu-id="3bf2e-138">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> </dl>

 

