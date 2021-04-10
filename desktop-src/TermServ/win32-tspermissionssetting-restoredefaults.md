---
title: 'Win32_TSPermissionsSetting 類別的 RestoreDefaults 方法 (Netfw) '
description: 還原終端機的預設許可權集合值。
ms.assetid: bdd01290-7c7c-4355-85dc-ade51b2abd94
ms.tgt_platform: multiple
keywords:
- RestoreDefaults 方法遠端桌面服務
- RestoreDefaults 方法遠端桌面服務，Win32_TSPermissionsSetting 類別
- Win32_TSPermissionsSetting 類別遠端桌面服務，RestoreDefaults 方法
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting.RestoreDefaults
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 073a8f8267ab9e7f7cbd50f15f4f3f20594d2e39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843388"
---
# <a name="restoredefaults-method-of-the-win32_tspermissionssetting-class"></a><span data-ttu-id="d0402-106">Win32 TSPermissionsSetting 類別的 RestoreDefaults 方法 \_</span><span class="sxs-lookup"><span data-stu-id="d0402-106">RestoreDefaults method of the Win32\_TSPermissionsSetting class</span></span>

<span data-ttu-id="d0402-107">**RestoreDefaults** 方法會還原終端機的預設許可權集合值。</span><span class="sxs-lookup"><span data-stu-id="d0402-107">The **RestoreDefaults** method restores the default permission set values for the terminal.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0402-108">語法</span><span class="sxs-lookup"><span data-stu-id="d0402-108">Syntax</span></span>


```mof
uint32 RestoreDefaults();
```



## <a name="parameters"></a><span data-ttu-id="d0402-109">參數</span><span class="sxs-lookup"><span data-stu-id="d0402-109">Parameters</span></span>

<span data-ttu-id="d0402-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d0402-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d0402-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d0402-111">Return value</span></span>

<span data-ttu-id="d0402-112">成功時傳回成功，否則失敗。</span><span class="sxs-lookup"><span data-stu-id="d0402-112">Returns Success on success, otherwise Failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0402-113">備註</span><span class="sxs-lookup"><span data-stu-id="d0402-113">Remarks</span></span>

<span data-ttu-id="d0402-114">預設許可權如下：</span><span class="sxs-lookup"><span data-stu-id="d0402-114">Default permissions are the following:</span></span>

-   <span data-ttu-id="d0402-115">[系統管理員]、[系統] 和 [遠端桌面] 說明小幫手帳戶都具有 [遠端桌面服務許可權](terminal-services-permissions.md)。</span><span class="sxs-lookup"><span data-stu-id="d0402-115">The Administrators, System, and Remote Desktop Help Assistant accounts have all [Remote Desktop Services Permissions](terminal-services-permissions.md).</span></span>
-   <span data-ttu-id="d0402-116">[遠端桌面使用者] 帳戶具有 [登入]、[連線]、[查詢資訊] 和 [傳送訊息] 許可權。</span><span class="sxs-lookup"><span data-stu-id="d0402-116">The Remote Desktop Users account has Logon, Connect, Query Information, and Send Message permission.</span></span>
-   <span data-ttu-id="d0402-117">本機服務和網路服務帳戶具有查詢資訊和傳送訊息許可權。</span><span class="sxs-lookup"><span data-stu-id="d0402-117">The Local Service and Network Service accounts have Query Information, and Send Message permission.</span></span>

<span data-ttu-id="d0402-118">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="d0402-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d0402-119">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="d0402-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d0402-120">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="d0402-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d0402-121">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="d0402-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0402-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0402-122">Requirements</span></span>



| <span data-ttu-id="d0402-123">需求</span><span class="sxs-lookup"><span data-stu-id="d0402-123">Requirement</span></span> | <span data-ttu-id="d0402-124">值</span><span class="sxs-lookup"><span data-stu-id="d0402-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0402-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d0402-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d0402-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0402-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d0402-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d0402-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d0402-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0402-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d0402-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="d0402-129">Namespace</span></span><br/>                | <span data-ttu-id="d0402-130">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="d0402-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d0402-131">標頭</span><span class="sxs-lookup"><span data-stu-id="d0402-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0402-132"><dt>Netfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="d0402-132"><dt>Netfw.h</dt></span></span> </dl>      |
| <span data-ttu-id="d0402-133">MOF</span><span class="sxs-lookup"><span data-stu-id="d0402-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d0402-134"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="d0402-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d0402-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d0402-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0402-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0402-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0402-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0402-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0402-138">**Win32 \_ TSPermissionsSetting**</span><span class="sxs-lookup"><span data-stu-id="d0402-138">**Win32\_TSPermissionsSetting**</span></span>](win32-tspermissionssetting.md)
</dt> </dl>

 

