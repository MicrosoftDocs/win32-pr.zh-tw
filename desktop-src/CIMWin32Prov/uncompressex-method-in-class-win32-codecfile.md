---
description: Uncompresses 邏輯編解碼器檔案 (或在物件路徑中指定的目錄) 。 這個方法是解壓縮方法的擴充版本。
ms.assetid: 257c69fa-c4f7-48be-8317-55db4b01601b
ms.tgt_platform: multiple
title: Win32_CodecFile 類別的 UncompressEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 547062a85336681b78a6081646801e78e4713e3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510691"
---
# <a name="uncompressex-method-of-the-win32_codecfile-class"></a><span data-ttu-id="2a389-104">Win32 CodecFile 類別的 UncompressEx 方法 \_</span><span class="sxs-lookup"><span data-stu-id="2a389-104">UncompressEx method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="2a389-105">**UncompressEx** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會 uncompresses 物件路徑中指定的邏輯編解碼器檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="2a389-105">The **UncompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical codec file (or directory) specified in the object path.</span></span> <span data-ttu-id="2a389-106">這個方法是 [**解壓縮**](uncompress-method-in-class-win32-directory.md) 方法的擴充版本。</span><span class="sxs-lookup"><span data-stu-id="2a389-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="2a389-107">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="2a389-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2a389-108">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="2a389-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2a389-109">語法</span><span class="sxs-lookup"><span data-stu-id="2a389-109">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="2a389-110">參數</span><span class="sxs-lookup"><span data-stu-id="2a389-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a389-111">*StopFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2a389-111">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a389-112">**UncompressEx** 方法失敗之檔案或目錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a389-112">Name of the file or directory where the **UncompressEx** method failed.</span></span> <span data-ttu-id="2a389-113">如果方法成功，此參數將會是 **null** 。</span><span class="sxs-lookup"><span data-stu-id="2a389-113">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="2a389-114">*StartFileName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="2a389-114">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2a389-115">將子檔案或目錄命名為 **UncompressEx** 的起點。 *StartFileName* 參數通常是 *StopFileName* 參數，可指定上一個方法呼叫發生錯誤的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="2a389-115">Names the child file or directory to use as a starting point for **UncompressEx**.The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="2a389-116">如果這個參數是 **Null**，則會在 **ExecMethod** 呼叫中指定的檔案或目錄上執行作業。</span><span class="sxs-lookup"><span data-stu-id="2a389-116">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

</dd> <dt>

<span data-ttu-id="2a389-117">*遞迴* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="2a389-117">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2a389-118">若 **為 true**，則會將擁有權變更以遞迴方式套用至 [**CIM \_ LogicalFile**](cim-logicalfile.md) 實例所指定之目錄中的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="2a389-118">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="2a389-119">注意：對於檔案實例， *遞迴* 輸入參數會被忽略。</span><span class="sxs-lookup"><span data-stu-id="2a389-119">Note: for file instances, the *Recursive* input parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a389-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="2a389-120">Return value</span></span>

<span data-ttu-id="2a389-121">如果成功解壓縮檔案，則傳回整數值 0 (零) ，以及表示錯誤的其他任何數位。</span><span class="sxs-lookup"><span data-stu-id="2a389-121">Returns an integer value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="2a389-122">**0**</span><span class="sxs-lookup"><span data-stu-id="2a389-122">**0**</span></span>
</dt> <dd>

<span data-ttu-id="2a389-123">要求成功。</span><span class="sxs-lookup"><span data-stu-id="2a389-123">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="2a389-124">**2**</span><span class="sxs-lookup"><span data-stu-id="2a389-124">**2**</span></span>
</dt> <dd>

<span data-ttu-id="2a389-125">存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="2a389-125">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="2a389-126">**8**</span><span class="sxs-lookup"><span data-stu-id="2a389-126">**8**</span></span>
</dt> <dd>

<span data-ttu-id="2a389-127">發生未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="2a389-127">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="2a389-128">**9**</span><span class="sxs-lookup"><span data-stu-id="2a389-128">**9**</span></span>
</dt> <dd>

<span data-ttu-id="2a389-129">指定的名稱無效。</span><span class="sxs-lookup"><span data-stu-id="2a389-129">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="2a389-130">**10**</span><span class="sxs-lookup"><span data-stu-id="2a389-130">**10**</span></span>
</dt> <dd>

<span data-ttu-id="2a389-131">指定的物件已經存在。</span><span class="sxs-lookup"><span data-stu-id="2a389-131">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="2a389-132">**11**</span><span class="sxs-lookup"><span data-stu-id="2a389-132">**11**</span></span>
</dt> <dd>

<span data-ttu-id="2a389-133">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="2a389-133">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="2a389-134">**12**</span><span class="sxs-lookup"><span data-stu-id="2a389-134">**12**</span></span>
</dt> <dd>

<span data-ttu-id="2a389-135">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="2a389-135">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="2a389-136">**13**</span><span class="sxs-lookup"><span data-stu-id="2a389-136">**13**</span></span>
</dt> <dd>

<span data-ttu-id="2a389-137">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="2a389-137">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="2a389-138">**14**</span><span class="sxs-lookup"><span data-stu-id="2a389-138">**14**</span></span>
</dt> <dd>

<span data-ttu-id="2a389-139">目錄不是空的。</span><span class="sxs-lookup"><span data-stu-id="2a389-139">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="2a389-140">**15**</span><span class="sxs-lookup"><span data-stu-id="2a389-140">**15**</span></span>
</dt> <dd>

<span data-ttu-id="2a389-141">發生共用違規。</span><span class="sxs-lookup"><span data-stu-id="2a389-141">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="2a389-142">**16**</span><span class="sxs-lookup"><span data-stu-id="2a389-142">**16**</span></span>
</dt> <dd>

<span data-ttu-id="2a389-143">指定的起始檔無效。</span><span class="sxs-lookup"><span data-stu-id="2a389-143">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="2a389-144">**17**</span><span class="sxs-lookup"><span data-stu-id="2a389-144">**17**</span></span>
</dt> <dd>

<span data-ttu-id="2a389-145">不會保留操作所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="2a389-145">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="2a389-146">**21**</span><span class="sxs-lookup"><span data-stu-id="2a389-146">**21**</span></span>
</dt> <dd>

<span data-ttu-id="2a389-147">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="2a389-147">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2a389-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a389-148">Requirements</span></span>



| <span data-ttu-id="2a389-149">需求</span><span class="sxs-lookup"><span data-stu-id="2a389-149">Requirement</span></span> | <span data-ttu-id="2a389-150">值</span><span class="sxs-lookup"><span data-stu-id="2a389-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a389-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2a389-151">Minimum supported client</span></span><br/> | <span data-ttu-id="2a389-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2a389-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2a389-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2a389-153">Minimum supported server</span></span><br/> | <span data-ttu-id="2a389-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2a389-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2a389-155">命名空間</span><span class="sxs-lookup"><span data-stu-id="2a389-155">Namespace</span></span><br/>                | <span data-ttu-id="2a389-156">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2a389-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2a389-157">MOF</span><span class="sxs-lookup"><span data-stu-id="2a389-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a389-158"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="2a389-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2a389-159">DLL</span><span class="sxs-lookup"><span data-stu-id="2a389-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a389-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a389-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a389-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a389-161">See also</span></span>

<dl> <dt>

<span data-ttu-id="2a389-162">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2a389-162">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2a389-163">**Win32 \_ CodecFile**</span><span class="sxs-lookup"><span data-stu-id="2a389-163">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

