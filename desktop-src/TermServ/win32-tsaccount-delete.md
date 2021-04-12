---
title: Win32_TSAccount 類別的 Delete 方法
description: Delete 方法會刪除指定的使用者、群組或電腦帳戶。
ms.assetid: d0bb06d6-781c-4711-a59d-9ff233dd2a4c
ms.tgt_platform: multiple
keywords:
- Delete 方法遠端桌面服務
- Delete 方法遠端桌面服務，Win32_TSAccount 類別
- Win32_TSAccount 類別遠端桌面服務，Delete 方法
topic_type:
- apiref
api_name:
- Win32_TSAccount.Delete
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c6ab76ad1200fc872a3a105e74533460104d806
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385154"
---
# <a name="delete-method-of-the-win32_tsaccount-class"></a><span data-ttu-id="fecf6-106">Win32 TSAccount 類別的 Delete 方法 \_</span><span class="sxs-lookup"><span data-stu-id="fecf6-106">Delete method of the Win32\_TSAccount class</span></span>

<span data-ttu-id="fecf6-107">**Delete** 方法會刪除指定的使用者、群組或電腦帳戶。</span><span class="sxs-lookup"><span data-stu-id="fecf6-107">The **Delete** method deletes the specified user, group, or computer account.</span></span>

## <a name="syntax"></a><span data-ttu-id="fecf6-108">語法</span><span class="sxs-lookup"><span data-stu-id="fecf6-108">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="fecf6-109">參數</span><span class="sxs-lookup"><span data-stu-id="fecf6-109">Parameters</span></span>

<span data-ttu-id="fecf6-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="fecf6-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fecf6-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="fecf6-111">Return value</span></span>

<span data-ttu-id="fecf6-112">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fecf6-112">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="fecf6-113">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="fecf6-113">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="fecf6-114">備註</span><span class="sxs-lookup"><span data-stu-id="fecf6-114">Remarks</span></span>

<span data-ttu-id="fecf6-115">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="fecf6-115">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fecf6-116">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="fecf6-116">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fecf6-117">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="fecf6-117">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fecf6-118">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="fecf6-118">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="fecf6-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="fecf6-119">Requirements</span></span>



| <span data-ttu-id="fecf6-120">需求</span><span class="sxs-lookup"><span data-stu-id="fecf6-120">Requirement</span></span> | <span data-ttu-id="fecf6-121">值</span><span class="sxs-lookup"><span data-stu-id="fecf6-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fecf6-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fecf6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fecf6-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fecf6-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fecf6-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fecf6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fecf6-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fecf6-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fecf6-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="fecf6-126">Namespace</span></span><br/>                | <span data-ttu-id="fecf6-127">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="fecf6-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="fecf6-128">MOF</span><span class="sxs-lookup"><span data-stu-id="fecf6-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fecf6-129"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="fecf6-129"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="fecf6-130">DLL</span><span class="sxs-lookup"><span data-stu-id="fecf6-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fecf6-131"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fecf6-131"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fecf6-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fecf6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fecf6-133">**Win32 \_ TSAccount**</span><span class="sxs-lookup"><span data-stu-id="fecf6-133">**Win32\_TSAccount**</span></span>](win32-tsaccount.md)
</dt> </dl>

 

