---
description: GetOwnerSid&\# 8194;WMI 類別方法會針對此進程的擁有者，抓取 (SID) 的安全識別碼。
ms.assetid: f856b06c-8080-4145-a775-51361f741873
ms.tgt_platform: multiple
title: Win32_Process 類別的 GetOwnerSid 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetOwnerSid
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c3ed34d132d363c0ce9f83511459ec40f340a06c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970912"
---
# <a name="getownersid-method-of-the-win32_process-class"></a><span data-ttu-id="f6527-103">Win32 進程類別的 GetOwnerSid 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f6527-103">GetOwnerSid method of the Win32\_Process class</span></span>

<span data-ttu-id="f6527-104">**GetOwnerSid** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會針對此進程的擁有者，抓取 (SID) 的安全識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6527-104">The **GetOwnerSid** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method retrieves the security identifier (SID) for the owner of this process.</span></span>

<span data-ttu-id="f6527-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="f6527-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f6527-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="f6527-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f6527-107">語法</span><span class="sxs-lookup"><span data-stu-id="f6527-107">Syntax</span></span>


```mof
uint32 GetOwnerSid(
  [out] string Sid
);
```



## <a name="parameters"></a><span data-ttu-id="f6527-108">參數</span><span class="sxs-lookup"><span data-stu-id="f6527-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6527-109">*Sid* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f6527-109">*Sid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6527-110">傳回這個進程的安全識別碼描述元。</span><span class="sxs-lookup"><span data-stu-id="f6527-110">Returns the security identifier descriptor for this process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6527-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f6527-111">Return value</span></span>

<span data-ttu-id="f6527-112">傳回零 (0) 表示成功。</span><span class="sxs-lookup"><span data-stu-id="f6527-112">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="f6527-113">任何其他數字表示發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="f6527-113">Any other number indicates an error.</span></span> <span data-ttu-id="f6527-114">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="f6527-114">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f6527-115">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="f6527-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f6527-116">**成功完成** (0) </span><span class="sxs-lookup"><span data-stu-id="f6527-116">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f6527-117">**拒絕存取** (2) </span><span class="sxs-lookup"><span data-stu-id="f6527-117">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f6527-118">**許可權不足** (3) </span><span class="sxs-lookup"><span data-stu-id="f6527-118">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f6527-119">**未知的失敗** (8) </span><span class="sxs-lookup"><span data-stu-id="f6527-119">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="f6527-120"> (9) **找不到路徑**</span><span class="sxs-lookup"><span data-stu-id="f6527-120">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="f6527-121">**不正確參數** (21) </span><span class="sxs-lookup"><span data-stu-id="f6527-121">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="f6527-122">**其他** (22 4294967295) </span><span class="sxs-lookup"><span data-stu-id="f6527-122">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="f6527-123">範例</span><span class="sxs-lookup"><span data-stu-id="f6527-123">Examples</span></span>

<span data-ttu-id="f6527-124">[ [尋找遠端系統上的已登入的使用者2版](https://Gallery.TechNet.Microsoft.Com/Find-the-logged-on-users-1161bd92) ] PowerShell 程式碼範例會查詢遠端電腦，以查看已登入的使用者。</span><span class="sxs-lookup"><span data-stu-id="f6527-124">The [Find the logged on users on a remote system/s version 2](https://Gallery.TechNet.Microsoft.Com/Find-the-logged-on-users-1161bd92) PowerShell code example queries remote machines to see who is logged on.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6527-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="f6527-125">Requirements</span></span>



| <span data-ttu-id="f6527-126">需求</span><span class="sxs-lookup"><span data-stu-id="f6527-126">Requirement</span></span> | <span data-ttu-id="f6527-127">值</span><span class="sxs-lookup"><span data-stu-id="f6527-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6527-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f6527-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f6527-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f6527-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f6527-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f6527-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f6527-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6527-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f6527-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="f6527-132">Namespace</span></span><br/>                | <span data-ttu-id="f6527-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f6527-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f6527-134">MOF</span><span class="sxs-lookup"><span data-stu-id="f6527-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6527-135"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="f6527-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6527-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f6527-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6527-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6527-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6527-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f6527-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="f6527-139">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f6527-139">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f6527-140">**Win32 \_ 進程**</span><span class="sxs-lookup"><span data-stu-id="f6527-140">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 

