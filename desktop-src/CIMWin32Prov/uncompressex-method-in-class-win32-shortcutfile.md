---
description: Uncompresses 邏輯快速鍵檔 (或在物件路徑中指定的目錄) 。 這個方法是解壓縮方法的擴充版本。
ms.assetid: aa1c04d1-4cce-4096-bce3-b9c61b9a4eb7
ms.tgt_platform: multiple
title: Win32_ShortcutFile 類別的 UncompressEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e07e86be3666b06063ef81c896eab6ee7a918657
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111384"
---
# <a name="uncompressex-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="c686b-104">Win32 ShortcutFile 類別的 UncompressEx 方法 \_</span><span class="sxs-lookup"><span data-stu-id="c686b-104">UncompressEx method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="c686b-105">**UncompressEx** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會 uncompresses 在物件路徑中指定的邏輯快速鍵檔 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="c686b-105">The **UncompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical shortcut file (or directory) specified in the object path.</span></span> <span data-ttu-id="c686b-106">這個方法是 [**解壓縮**](uncompress-method-in-class-win32-directory.md) 方法的擴充版本。</span><span class="sxs-lookup"><span data-stu-id="c686b-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="c686b-107">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="c686b-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c686b-108">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="c686b-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c686b-109">語法</span><span class="sxs-lookup"><span data-stu-id="c686b-109">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="c686b-110">參數</span><span class="sxs-lookup"><span data-stu-id="c686b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c686b-111">*StopFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c686b-111">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c686b-112">**UncompressEx** 方法失敗之檔案或目錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="c686b-112">Name of the file or directory where the **UncompressEx** method failed.</span></span> <span data-ttu-id="c686b-113">如果方法成功，此參數將會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="c686b-113">This parameter will be **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="c686b-114">*StartFileName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="c686b-114">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c686b-115">將子檔案或目錄命名為 **UncompressEx** 的起點。</span><span class="sxs-lookup"><span data-stu-id="c686b-115">Names the child file or directory to use as a starting point for **UncompressEx**.</span></span> <span data-ttu-id="c686b-116">*StartFileName* 參數通常是 *StopFileName* 參數，可指定上一個方法呼叫發生錯誤的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="c686b-116">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="c686b-117">如果這個參數是 **Null**，則會在 ExecMethod 呼叫中指定的檔案或目錄上執行作業。</span><span class="sxs-lookup"><span data-stu-id="c686b-117">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> <dt>

<span data-ttu-id="c686b-118">*遞迴* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="c686b-118">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c686b-119">若 **為 true**，則會將擁有權變更以遞迴方式套用至 [**CIM \_ LogicalFile**](cim-logicalfile.md) 實例所指定之目錄中的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="c686b-119">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="c686b-120">若為檔案實例，則會忽略 *遞迴* 參數。</span><span class="sxs-lookup"><span data-stu-id="c686b-120">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c686b-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="c686b-121">Return value</span></span>

<span data-ttu-id="c686b-122">如果檔案已成功解壓縮，則會傳回 0 (零) 的值，以及表示錯誤的其他任何數位。</span><span class="sxs-lookup"><span data-stu-id="c686b-122">Returns a value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="c686b-123">**0**</span><span class="sxs-lookup"><span data-stu-id="c686b-123">**0**</span></span>
</dt> <dd>

<span data-ttu-id="c686b-124">要求成功。</span><span class="sxs-lookup"><span data-stu-id="c686b-124">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="c686b-125">**2**</span><span class="sxs-lookup"><span data-stu-id="c686b-125">**2**</span></span>
</dt> <dd>

<span data-ttu-id="c686b-126">存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="c686b-126">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="c686b-127">**8**</span><span class="sxs-lookup"><span data-stu-id="c686b-127">**8**</span></span>
</dt> <dd>

<span data-ttu-id="c686b-128">發生未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="c686b-128">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="c686b-129">**9**</span><span class="sxs-lookup"><span data-stu-id="c686b-129">**9**</span></span>
</dt> <dd>

<span data-ttu-id="c686b-130">指定的名稱無效。</span><span class="sxs-lookup"><span data-stu-id="c686b-130">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c686b-131">**10**</span><span class="sxs-lookup"><span data-stu-id="c686b-131">**10**</span></span>
</dt> <dd>

<span data-ttu-id="c686b-132">指定的物件已經存在。</span><span class="sxs-lookup"><span data-stu-id="c686b-132">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="c686b-133">**11**</span><span class="sxs-lookup"><span data-stu-id="c686b-133">**11**</span></span>
</dt> <dd>

<span data-ttu-id="c686b-134">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="c686b-134">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="c686b-135">**12**</span><span class="sxs-lookup"><span data-stu-id="c686b-135">**12**</span></span>
</dt> <dd>

<span data-ttu-id="c686b-136">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="c686b-136">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="c686b-137">**13**</span><span class="sxs-lookup"><span data-stu-id="c686b-137">**13**</span></span>
</dt> <dd>

<span data-ttu-id="c686b-138">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="c686b-138">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="c686b-139">**14**</span><span class="sxs-lookup"><span data-stu-id="c686b-139">**14**</span></span>
</dt> <dd>

<span data-ttu-id="c686b-140">目錄不是空的。</span><span class="sxs-lookup"><span data-stu-id="c686b-140">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="c686b-141">**15**</span><span class="sxs-lookup"><span data-stu-id="c686b-141">**15**</span></span>
</dt> <dd>

<span data-ttu-id="c686b-142">發生共用違規。</span><span class="sxs-lookup"><span data-stu-id="c686b-142">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="c686b-143">**16**</span><span class="sxs-lookup"><span data-stu-id="c686b-143">**16**</span></span>
</dt> <dd>

<span data-ttu-id="c686b-144">指定的起始檔無效。</span><span class="sxs-lookup"><span data-stu-id="c686b-144">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c686b-145">**17**</span><span class="sxs-lookup"><span data-stu-id="c686b-145">**17**</span></span>
</dt> <dd>

<span data-ttu-id="c686b-146">不會保留操作所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="c686b-146">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="c686b-147">**21**</span><span class="sxs-lookup"><span data-stu-id="c686b-147">**21**</span></span>
</dt> <dd>

<span data-ttu-id="c686b-148">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="c686b-148">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c686b-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="c686b-149">Requirements</span></span>



| <span data-ttu-id="c686b-150">需求</span><span class="sxs-lookup"><span data-stu-id="c686b-150">Requirement</span></span> | <span data-ttu-id="c686b-151">值</span><span class="sxs-lookup"><span data-stu-id="c686b-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c686b-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c686b-152">Minimum supported client</span></span><br/> | <span data-ttu-id="c686b-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c686b-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c686b-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c686b-154">Minimum supported server</span></span><br/> | <span data-ttu-id="c686b-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c686b-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c686b-156">命名空間</span><span class="sxs-lookup"><span data-stu-id="c686b-156">Namespace</span></span><br/>                | <span data-ttu-id="c686b-157">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c686b-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c686b-158">MOF</span><span class="sxs-lookup"><span data-stu-id="c686b-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c686b-159"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="c686b-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c686b-160">DLL</span><span class="sxs-lookup"><span data-stu-id="c686b-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c686b-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c686b-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c686b-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c686b-162">See also</span></span>

<dl> <dt>

<span data-ttu-id="c686b-163">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c686b-163">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c686b-164">**Win32 \_ ShortcutFile**</span><span class="sxs-lookup"><span data-stu-id="c686b-164">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

