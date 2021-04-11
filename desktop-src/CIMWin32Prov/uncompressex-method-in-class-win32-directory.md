---
description: Uncompresses 邏輯目錄專案檔 (或在物件路徑中指定的目錄) 。 這個方法是解壓縮方法的擴充版本。
ms.assetid: cd18d8b7-ab63-475c-a3a6-79611c9e032d
ms.tgt_platform: multiple
title: Win32_Directory 類別的 UncompressEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a0fd02d0757745199249d64fa08d73f8b5ec65a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111385"
---
# <a name="uncompressex-method-of-the-win32_directory-class"></a><span data-ttu-id="c44fd-104">Win32 目錄類別的 UncompressEx 方法 \_</span><span class="sxs-lookup"><span data-stu-id="c44fd-104">UncompressEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="c44fd-105">**UncompressEx** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會 uncompresses 邏輯目錄專案檔， (或在物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="c44fd-105">The **UncompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical directory entry file (or directory) specified in the object path.</span></span> <span data-ttu-id="c44fd-106">這個方法是 [**解壓縮**](uncompress-method-in-class-win32-directory.md) 方法的擴充版本。</span><span class="sxs-lookup"><span data-stu-id="c44fd-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="c44fd-107">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="c44fd-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c44fd-108">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="c44fd-108">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c44fd-109">語法</span><span class="sxs-lookup"><span data-stu-id="c44fd-109">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="c44fd-110">參數</span><span class="sxs-lookup"><span data-stu-id="c44fd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c44fd-111">*StopFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c44fd-111">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c44fd-112">**UncompressEx** 方法失敗的檔案/目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="c44fd-112">Name of the file/directory where the **UncompressEx** method failed.</span></span> <span data-ttu-id="c44fd-113">如果方法成功，此參數將會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="c44fd-113">This parameter will be **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="c44fd-114">*StartFileName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="c44fd-114">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c44fd-115">將子檔案/目錄命名為 **UncompressEx** 的起點。</span><span class="sxs-lookup"><span data-stu-id="c44fd-115">Names the child file/directory to use as a starting point for **UncompressEx**.</span></span> <span data-ttu-id="c44fd-116">*StartFileName* 參數通常是 *StopFileName* 參數，可指定上一個方法呼叫發生錯誤的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="c44fd-116">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="c44fd-117">如果這個參數是 **Null**，則會在 ExecMethod 呼叫中指定的檔案或目錄上執行作業。</span><span class="sxs-lookup"><span data-stu-id="c44fd-117">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

<span data-ttu-id="c44fd-118">如果使用 *StartFileName* ，則 *遞迴* 也必須設定為 true。</span><span class="sxs-lookup"><span data-stu-id="c44fd-118">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="c44fd-119">*遞迴* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="c44fd-119">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c44fd-120">若 **為 true**，則會將擁有權變更以遞迴方式套用至 [**CIM \_ LogicalFile**](cim-logicalfile.md) 實例所指定之目錄中的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="c44fd-120">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="c44fd-121">注意：對於檔案實例， *遞迴* 輸入參數會被忽略。</span><span class="sxs-lookup"><span data-stu-id="c44fd-121">Note: for file instances, the *Recursive* input parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c44fd-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="c44fd-122">Return value</span></span>

<span data-ttu-id="c44fd-123">如果成功解壓縮檔案，則傳回值為 0 (零) ，以及表示錯誤的其他任何數位。</span><span class="sxs-lookup"><span data-stu-id="c44fd-123">Returns an value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="c44fd-124">**0**</span><span class="sxs-lookup"><span data-stu-id="c44fd-124">**0**</span></span>
</dt> <dd>

<span data-ttu-id="c44fd-125">要求成功。</span><span class="sxs-lookup"><span data-stu-id="c44fd-125">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="c44fd-126">**2**</span><span class="sxs-lookup"><span data-stu-id="c44fd-126">**2**</span></span>
</dt> <dd>

<span data-ttu-id="c44fd-127">存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="c44fd-127">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="c44fd-128">**8**</span><span class="sxs-lookup"><span data-stu-id="c44fd-128">**8**</span></span>
</dt> <dd>

<span data-ttu-id="c44fd-129">發生未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="c44fd-129">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="c44fd-130">**9**</span><span class="sxs-lookup"><span data-stu-id="c44fd-130">**9**</span></span>
</dt> <dd>

<span data-ttu-id="c44fd-131">指定的名稱無效。</span><span class="sxs-lookup"><span data-stu-id="c44fd-131">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c44fd-132">**10**</span><span class="sxs-lookup"><span data-stu-id="c44fd-132">**10**</span></span>
</dt> <dd>

<span data-ttu-id="c44fd-133">指定的物件已經存在。</span><span class="sxs-lookup"><span data-stu-id="c44fd-133">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="c44fd-134">**11**</span><span class="sxs-lookup"><span data-stu-id="c44fd-134">**11**</span></span>
</dt> <dd>

<span data-ttu-id="c44fd-135">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="c44fd-135">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="c44fd-136">**12**</span><span class="sxs-lookup"><span data-stu-id="c44fd-136">**12**</span></span>
</dt> <dd>

<span data-ttu-id="c44fd-137">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="c44fd-137">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="c44fd-138">**13**</span><span class="sxs-lookup"><span data-stu-id="c44fd-138">**13**</span></span>
</dt> <dd>

<span data-ttu-id="c44fd-139">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="c44fd-139">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="c44fd-140">**14**</span><span class="sxs-lookup"><span data-stu-id="c44fd-140">**14**</span></span>
</dt> <dd>

<span data-ttu-id="c44fd-141">目錄不是空的。</span><span class="sxs-lookup"><span data-stu-id="c44fd-141">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="c44fd-142">**15**</span><span class="sxs-lookup"><span data-stu-id="c44fd-142">**15**</span></span>
</dt> <dd>

<span data-ttu-id="c44fd-143">發生共用違規。</span><span class="sxs-lookup"><span data-stu-id="c44fd-143">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="c44fd-144">**16**</span><span class="sxs-lookup"><span data-stu-id="c44fd-144">**16**</span></span>
</dt> <dd>

<span data-ttu-id="c44fd-145">指定的起始檔無效。</span><span class="sxs-lookup"><span data-stu-id="c44fd-145">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c44fd-146">**17**</span><span class="sxs-lookup"><span data-stu-id="c44fd-146">**17**</span></span>
</dt> <dd>

<span data-ttu-id="c44fd-147">不會保留操作所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="c44fd-147">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="c44fd-148">**21**</span><span class="sxs-lookup"><span data-stu-id="c44fd-148">**21**</span></span>
</dt> <dd>

<span data-ttu-id="c44fd-149">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="c44fd-149">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c44fd-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="c44fd-150">Requirements</span></span>



| <span data-ttu-id="c44fd-151">需求</span><span class="sxs-lookup"><span data-stu-id="c44fd-151">Requirement</span></span> | <span data-ttu-id="c44fd-152">值</span><span class="sxs-lookup"><span data-stu-id="c44fd-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c44fd-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c44fd-153">Minimum supported client</span></span><br/> | <span data-ttu-id="c44fd-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c44fd-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c44fd-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c44fd-155">Minimum supported server</span></span><br/> | <span data-ttu-id="c44fd-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c44fd-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c44fd-157">命名空間</span><span class="sxs-lookup"><span data-stu-id="c44fd-157">Namespace</span></span><br/>                | <span data-ttu-id="c44fd-158">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c44fd-158">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c44fd-159">MOF</span><span class="sxs-lookup"><span data-stu-id="c44fd-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c44fd-160"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="c44fd-160"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c44fd-161">DLL</span><span class="sxs-lookup"><span data-stu-id="c44fd-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c44fd-162"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c44fd-162"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c44fd-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c44fd-163">See also</span></span>

<dl> <dt>

<span data-ttu-id="c44fd-164">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c44fd-164">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c44fd-165">**Win32 \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="c44fd-165">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

