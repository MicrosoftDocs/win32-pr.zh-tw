---
description: 從伺服器的共用資源清單中刪除共用名稱，中斷與共用資源的連接。
ms.assetid: 175f9c0e-0017-4a86-8e05-ad78e2c93c11
ms.tgt_platform: multiple
title: Win32_Share 類別的 Delete 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2048ba9dac91b139888f27c037d64849de8a4ee8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110805"
---
# <a name="delete-method-of-the-win32_share-class"></a><span data-ttu-id="af732-103">Win32 共用類別的 Delete 方法 \_</span><span class="sxs-lookup"><span data-stu-id="af732-103">Delete method of the Win32\_Share class</span></span>

<span data-ttu-id="af732-104">**Delete** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會從伺服器的共用資源清單中刪除共用名稱，中斷與共用資源的連接。</span><span class="sxs-lookup"><span data-stu-id="af732-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes a share name from a server's list of shared resources, disconnecting connections to the shared resource.</span></span>

<span data-ttu-id="af732-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="af732-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="af732-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="af732-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="af732-107">語法</span><span class="sxs-lookup"><span data-stu-id="af732-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="af732-108">參數</span><span class="sxs-lookup"><span data-stu-id="af732-108">Parameters</span></span>

<span data-ttu-id="af732-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="af732-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="af732-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="af732-110">Return value</span></span>

<span data-ttu-id="af732-111">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="af732-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="af732-112">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="af732-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="af732-113">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="af732-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="af732-114">**成功** (0) </span><span class="sxs-lookup"><span data-stu-id="af732-114">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="af732-115">**拒絕存取** (2) </span><span class="sxs-lookup"><span data-stu-id="af732-115">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="af732-116">**未知的失敗** (8) </span><span class="sxs-lookup"><span data-stu-id="af732-116">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="af732-117">**不正確名稱** (9) </span><span class="sxs-lookup"><span data-stu-id="af732-117">**Invalid name** (9)</span></span>
</dt> <dt>

<span data-ttu-id="af732-118">**層級** (10) 無效</span><span class="sxs-lookup"><span data-stu-id="af732-118">**Invalid level** (10)</span></span>
</dt> <dt>

<span data-ttu-id="af732-119">**不正確參數** (21) </span><span class="sxs-lookup"><span data-stu-id="af732-119">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="af732-120">**重複的共用** (22) </span><span class="sxs-lookup"><span data-stu-id="af732-120">**Duplicate share** (22)</span></span>
</dt> <dt>

<span data-ttu-id="af732-121">重新 **導向路徑** (23) </span><span class="sxs-lookup"><span data-stu-id="af732-121">**Redirected path** (23)</span></span>
</dt> <dt>

<span data-ttu-id="af732-122">**未知的裝置或目錄** (24) </span><span class="sxs-lookup"><span data-stu-id="af732-122">**Unknown device or directory** (24)</span></span>
</dt> <dt>

<span data-ttu-id="af732-123">**找不到網路名稱** (25) </span><span class="sxs-lookup"><span data-stu-id="af732-123">**Net name not found** (25)</span></span>
</dt> <dt>

<span data-ttu-id="af732-124">**其他** (26 4294967295) </span><span class="sxs-lookup"><span data-stu-id="af732-124">**Other** (26 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="af732-125">備註</span><span class="sxs-lookup"><span data-stu-id="af732-125">Remarks</span></span>

<span data-ttu-id="af732-126">**Delete** 方法是物件方法，用於類別的實例。</span><span class="sxs-lookup"><span data-stu-id="af732-126">The **Delete** method is an object method and is used on an instance of a class.</span></span>

<span data-ttu-id="af732-127">只有 Administrators 或 Account Operators 本機群組的成員，或是具有通訊、列印或伺服器操作員群組成員資格的成員，才能夠成功執行方法。</span><span class="sxs-lookup"><span data-stu-id="af732-127">Only members of the Administrators or Account Operators local group or those with Communication, Print, or Server operator group membership can successfully execute the method.</span></span> <span data-ttu-id="af732-128">列印操作員只能刪除印表機佇列。</span><span class="sxs-lookup"><span data-stu-id="af732-128">The Print operator can delete only printer queues.</span></span> <span data-ttu-id="af732-129">通訊運算子只能刪除通訊裝置佇列。</span><span class="sxs-lookup"><span data-stu-id="af732-129">The Communication operator can delete only communication-device queues.</span></span>

## <a name="examples"></a><span data-ttu-id="af732-130">範例</span><span class="sxs-lookup"><span data-stu-id="af732-130">Examples</span></span>

<span data-ttu-id="af732-131">下列 VBScript 程式碼範例會刪除指定的共用。</span><span class="sxs-lookup"><span data-stu-id="af732-131">The following VBScript code sample deletes the specified share.</span></span>


```VB
On Error Resume Next

ComputerName = InputBox("Enter the computer name:", "Delete Share", "localhost")

SName = InputBox("Enter the name of the share:", "Delete Share")



Set Shares = GetObject("winmgmts:\\" & ComputerName & _
 "\root\cimv2").ExecQuery("SELECT * FROM Win32_Share WHERE name = '" & SName & "'")



For Each Share in Shares
 Share.Delete()
Next
```



<span data-ttu-id="af732-132">下列 PowerShell 程式碼範例會刪除空白的共用。</span><span class="sxs-lookup"><span data-stu-id="af732-132">The following PowerShell code sample deletes blank shares.</span></span>


```PowerShell
$Shares = Get-WMIObject Win32_Share | Where {$_.Name -eq ""}

Foreach ($Share in $Shares) {
   $Share.Delete()
}
"{0} blank shares found and removed" -f $shares.count
```



## <a name="requirements"></a><span data-ttu-id="af732-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="af732-133">Requirements</span></span>



| <span data-ttu-id="af732-134">需求</span><span class="sxs-lookup"><span data-stu-id="af732-134">Requirement</span></span> | <span data-ttu-id="af732-135">值</span><span class="sxs-lookup"><span data-stu-id="af732-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af732-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="af732-136">Minimum supported client</span></span><br/> | <span data-ttu-id="af732-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="af732-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="af732-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="af732-138">Minimum supported server</span></span><br/> | <span data-ttu-id="af732-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af732-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="af732-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="af732-140">Namespace</span></span><br/>                | <span data-ttu-id="af732-141">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="af732-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="af732-142">MOF</span><span class="sxs-lookup"><span data-stu-id="af732-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af732-143"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="af732-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="af732-144">DLL</span><span class="sxs-lookup"><span data-stu-id="af732-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af732-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af732-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af732-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af732-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="af732-147">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="af732-147">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="af732-148">**Win32 \_ 共用**</span><span class="sxs-lookup"><span data-stu-id="af732-148">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

