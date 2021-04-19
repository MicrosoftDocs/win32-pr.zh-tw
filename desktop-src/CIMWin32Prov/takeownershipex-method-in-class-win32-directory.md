---
description: 取得物件路徑中指定之邏輯目錄專案檔的擁有權。 這個方法是 TakeOwnerShip 方法的擴充版本。
ms.assetid: 73726207-e885-4957-bff8-6903c4b99278
ms.tgt_platform: multiple
title: Win32_Directory 類別的 TakeOwnerShipEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2e391e942e581d0f80d46b0f59b9b273d7bff499
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977003"
---
# <a name="takeownershipex-method-of-the-win32_directory-class"></a><span data-ttu-id="43e4a-104">Win32 目錄類別的 TakeOwnerShipEx 方法 \_</span><span class="sxs-lookup"><span data-stu-id="43e4a-104">TakeOwnerShipEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="43e4a-105">**TakeOwnerShipEx** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會取得物件路徑中指定之邏輯目錄專案檔的擁有權。</span><span class="sxs-lookup"><span data-stu-id="43e4a-105">The **TakeOwnerShipEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical directory entry file specified in the object path.</span></span> <span data-ttu-id="43e4a-106">這個方法是 [**TakeOwnerShip**](takeownership-method-in-class-win32-directory.md) 方法的擴充版本。</span><span class="sxs-lookup"><span data-stu-id="43e4a-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="43e4a-107">如果邏輯檔案實際上是目錄，則此方法會以遞迴方式運作，並取得目錄包含的所有檔案和子目錄的擁有權。</span><span class="sxs-lookup"><span data-stu-id="43e4a-107">If the logical file is actually a directory, then this method acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="43e4a-108">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="43e4a-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="43e4a-109">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="43e4a-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="43e4a-110">語法</span><span class="sxs-lookup"><span data-stu-id="43e4a-110">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="43e4a-111">參數</span><span class="sxs-lookup"><span data-stu-id="43e4a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43e4a-112">*StopFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="43e4a-112">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43e4a-113">**TakeOwnerShipEx** 方法失敗之檔案或目錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="43e4a-113">Name of the file or directory where the **TakeOwnerShipEx** method failed.</span></span> <span data-ttu-id="43e4a-114">如果方法成功，則此參數為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="43e4a-114">This parameter is **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="43e4a-115">*StartFileName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="43e4a-115">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="43e4a-116">將子檔案或目錄命名為 **TakeOwnerShipEx** 的起點。</span><span class="sxs-lookup"><span data-stu-id="43e4a-116">Names the child file or directory to use as a starting point for **TakeOwnerShipEx**.</span></span> <span data-ttu-id="43e4a-117">*StartFileName* 參數通常是 *StopFileName* 參數，可指定上一個方法呼叫發生錯誤的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="43e4a-117">The *StartFileName* parameter is typically the *StopFileName* parameter that specifies the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="43e4a-118">如果這個參數是 **Null**，則會在 [**ExecMethod**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod) 呼叫中指定的檔案或目錄上執行作業。</span><span class="sxs-lookup"><span data-stu-id="43e4a-118">If this parameter is **NULL**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod) call.</span></span>

<span data-ttu-id="43e4a-119">如果使用 *StartFileName* ，則 *遞迴* 也必須設定為 true。</span><span class="sxs-lookup"><span data-stu-id="43e4a-119">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="43e4a-120">*遞迴* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="43e4a-120">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="43e4a-121">若 **為 True**，則會將擁有權變更以遞迴方式套用至 [**CIM \_ LogicalFile**](cim-logicalfile.md) 實例所指定之目錄中的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="43e4a-121">If **True**, the change of ownership is applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="43e4a-122">若為檔案實例，則會忽略 *遞迴* 輸入參數。</span><span class="sxs-lookup"><span data-stu-id="43e4a-122">For file instances, the *Recursive* input parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43e4a-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="43e4a-123">Return value</span></span>

<span data-ttu-id="43e4a-124">在成功時傳回 0 (零) 的整數值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="43e4a-124">Returns an integer value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="43e4a-125">**0**</span><span class="sxs-lookup"><span data-stu-id="43e4a-125">**0**</span></span>
</dt> <dd>

<span data-ttu-id="43e4a-126">要求成功。</span><span class="sxs-lookup"><span data-stu-id="43e4a-126">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="43e4a-127">**2**</span><span class="sxs-lookup"><span data-stu-id="43e4a-127">**2**</span></span>
</dt> <dd>

<span data-ttu-id="43e4a-128">存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="43e4a-128">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="43e4a-129">**8**</span><span class="sxs-lookup"><span data-stu-id="43e4a-129">**8**</span></span>
</dt> <dd>

<span data-ttu-id="43e4a-130">發生未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="43e4a-130">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="43e4a-131">**9**</span><span class="sxs-lookup"><span data-stu-id="43e4a-131">**9**</span></span>
</dt> <dd>

<span data-ttu-id="43e4a-132">指定的名稱無效。</span><span class="sxs-lookup"><span data-stu-id="43e4a-132">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="43e4a-133">**10**</span><span class="sxs-lookup"><span data-stu-id="43e4a-133">**10**</span></span>
</dt> <dd>

<span data-ttu-id="43e4a-134">指定的物件已經存在。</span><span class="sxs-lookup"><span data-stu-id="43e4a-134">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="43e4a-135">**11**</span><span class="sxs-lookup"><span data-stu-id="43e4a-135">**11**</span></span>
</dt> <dd>

<span data-ttu-id="43e4a-136">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="43e4a-136">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="43e4a-137">**12**</span><span class="sxs-lookup"><span data-stu-id="43e4a-137">**12**</span></span>
</dt> <dd>

<span data-ttu-id="43e4a-138">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="43e4a-138">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="43e4a-139">**13**</span><span class="sxs-lookup"><span data-stu-id="43e4a-139">**13**</span></span>
</dt> <dd>

<span data-ttu-id="43e4a-140">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="43e4a-140">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="43e4a-141">**14**</span><span class="sxs-lookup"><span data-stu-id="43e4a-141">**14**</span></span>
</dt> <dd>

<span data-ttu-id="43e4a-142">目錄不是空的。</span><span class="sxs-lookup"><span data-stu-id="43e4a-142">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="43e4a-143">**15**</span><span class="sxs-lookup"><span data-stu-id="43e4a-143">**15**</span></span>
</dt> <dd>

<span data-ttu-id="43e4a-144">發生共用違規。</span><span class="sxs-lookup"><span data-stu-id="43e4a-144">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="43e4a-145">**16**</span><span class="sxs-lookup"><span data-stu-id="43e4a-145">**16**</span></span>
</dt> <dd>

<span data-ttu-id="43e4a-146">指定的起始檔無效。</span><span class="sxs-lookup"><span data-stu-id="43e4a-146">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="43e4a-147">**17**</span><span class="sxs-lookup"><span data-stu-id="43e4a-147">**17**</span></span>
</dt> <dd>

<span data-ttu-id="43e4a-148">不會保留操作所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="43e4a-148">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="43e4a-149">**21**</span><span class="sxs-lookup"><span data-stu-id="43e4a-149">**21**</span></span>
</dt> <dd>

<span data-ttu-id="43e4a-150">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="43e4a-150">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="43e4a-151">範例</span><span class="sxs-lookup"><span data-stu-id="43e4a-151">Examples</span></span>

<span data-ttu-id="43e4a-152">下列 Visual Basic 腳本程式碼會呼叫 [**TakeOwnerShipEx**](takeownershipex-method-in-class-cim-directory.md) 方法來取得 C： temp 資料夾的擁有權 \\ 。</span><span class="sxs-lookup"><span data-stu-id="43e4a-152">The following Visual Basic Script code calls the [**TakeOwnerShipEx**](takeownershipex-method-in-class-cim-directory.md) method to take ownership of the C:\\temp folder.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")
' Obtain an InParameters object specific
' to the method.
Set objInParam = objShare.Methods_("TakeOwnerShipEx").inParameters.SpawnInstance_()

' Add the input parameters.
objInParam.Properties_.Item("Recursive") =  true

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod("Win32_Directory.Name='C:\Temp'", "TakeOwnerShipEx", objInParam)
wscript.echo objOutParams.ReturnValue
```



## <a name="requirements"></a><span data-ttu-id="43e4a-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="43e4a-153">Requirements</span></span>



| <span data-ttu-id="43e4a-154">需求</span><span class="sxs-lookup"><span data-stu-id="43e4a-154">Requirement</span></span> | <span data-ttu-id="43e4a-155">值</span><span class="sxs-lookup"><span data-stu-id="43e4a-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43e4a-156">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="43e4a-156">Minimum supported client</span></span><br/> | <span data-ttu-id="43e4a-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="43e4a-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="43e4a-158">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="43e4a-158">Minimum supported server</span></span><br/> | <span data-ttu-id="43e4a-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43e4a-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="43e4a-160">命名空間</span><span class="sxs-lookup"><span data-stu-id="43e4a-160">Namespace</span></span><br/>                | <span data-ttu-id="43e4a-161">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="43e4a-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="43e4a-162">MOF</span><span class="sxs-lookup"><span data-stu-id="43e4a-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43e4a-163"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="43e4a-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="43e4a-164">DLL</span><span class="sxs-lookup"><span data-stu-id="43e4a-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43e4a-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43e4a-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43e4a-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43e4a-166">See also</span></span>

<dl> <dt>

<span data-ttu-id="43e4a-167">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="43e4a-167">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="43e4a-168">**Win32 \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="43e4a-168">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

