---
description: 壓縮物件路徑中指定的邏輯快速鍵檔 (或目錄)  (這個方法是壓縮方法) 的擴充版本。
ms.assetid: 1f7b6182-6ab7-4801-83a8-b57b1c78001f
ms.tgt_platform: multiple
title: Win32_ShortcutFile 類別的 CompressEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 512511b690ed6769895e9c4f9922d479d66f847e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936146"
---
# <a name="compressex-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="75f68-103">Win32 ShortcutFile 類別的 CompressEx 方法 \_</span><span class="sxs-lookup"><span data-stu-id="75f68-103">CompressEx method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="75f68-104">**CompressEx** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會壓縮物件路徑中指定 (或目錄) 的邏輯快速鍵檔 (此方法是 [**壓縮**](compress-method-in-class-win32-directory.md)方法) 的擴充版本。</span><span class="sxs-lookup"><span data-stu-id="75f68-104">The **CompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical shortcut file (or directory) specified in the object path (this method is an extended version of the [**Compress**](compress-method-in-class-win32-directory.md) method).</span></span>

<span data-ttu-id="75f68-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="75f68-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="75f68-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="75f68-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="75f68-107">語法</span><span class="sxs-lookup"><span data-stu-id="75f68-107">Syntax</span></span>


```mof
uint32 CompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="75f68-108">參數</span><span class="sxs-lookup"><span data-stu-id="75f68-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75f68-109">*StopFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="75f68-109">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75f68-110">[**CompressEx**](compressex-method-in-class-win32-directory.md)方法失敗之檔案或目錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="75f68-110">Name of the file or directory where the [**CompressEx**](compressex-method-in-class-win32-directory.md) method failed.</span></span> <span data-ttu-id="75f68-111">如果方法成功，此參數將會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="75f68-111">This parameter will be **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="75f68-112">*StartFileName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="75f68-112">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="75f68-113">將子檔案或目錄命名為 [**CompressEx**](compressex-method-in-class-win32-directory.md)的起點。</span><span class="sxs-lookup"><span data-stu-id="75f68-113">Names the child file or directory to use as a starting point for [**CompressEx**](compressex-method-in-class-win32-directory.md).</span></span> <span data-ttu-id="75f68-114">*StartFileName* 參數通常是 *StopFileName* 參數，可指定上一個方法呼叫發生錯誤的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="75f68-114">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="75f68-115">如果這個參數是 **Null**，則會在 **ExecMethod** 呼叫中指定的檔案或目錄上執行作業。</span><span class="sxs-lookup"><span data-stu-id="75f68-115">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

</dd> <dt>

<span data-ttu-id="75f68-116">*遞迴* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="75f68-116">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="75f68-117">若 **為 true**，則會將擁有權變更以遞迴方式套用至 [**CIM \_ LogicalFile**](cim-logicalfile.md) 實例所指定之目錄中的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="75f68-117">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="75f68-118">若為檔案實例，則會忽略 *遞迴* 參數。</span><span class="sxs-lookup"><span data-stu-id="75f68-118">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75f68-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="75f68-119">Return value</span></span>

<span data-ttu-id="75f68-120">傳回值 0 (零) 如果檔案已成功壓縮，則為，而任何其他數位表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="75f68-120">Returns a value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="75f68-121">**0**</span><span class="sxs-lookup"><span data-stu-id="75f68-121">**0**</span></span>
</dt> <dd>

<span data-ttu-id="75f68-122">要求成功。</span><span class="sxs-lookup"><span data-stu-id="75f68-122">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="75f68-123">**2**</span><span class="sxs-lookup"><span data-stu-id="75f68-123">**2**</span></span>
</dt> <dd>

<span data-ttu-id="75f68-124">存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="75f68-124">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="75f68-125">**8**</span><span class="sxs-lookup"><span data-stu-id="75f68-125">**8**</span></span>
</dt> <dd>

<span data-ttu-id="75f68-126">發生未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="75f68-126">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="75f68-127">**9**</span><span class="sxs-lookup"><span data-stu-id="75f68-127">**9**</span></span>
</dt> <dd>

<span data-ttu-id="75f68-128">指定的名稱無效。</span><span class="sxs-lookup"><span data-stu-id="75f68-128">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="75f68-129">**10**</span><span class="sxs-lookup"><span data-stu-id="75f68-129">**10**</span></span>
</dt> <dd>

<span data-ttu-id="75f68-130">指定的物件已經存在。</span><span class="sxs-lookup"><span data-stu-id="75f68-130">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="75f68-131">**11**</span><span class="sxs-lookup"><span data-stu-id="75f68-131">**11**</span></span>
</dt> <dd>

<span data-ttu-id="75f68-132">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="75f68-132">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="75f68-133">**12**</span><span class="sxs-lookup"><span data-stu-id="75f68-133">**12**</span></span>
</dt> <dd>

<span data-ttu-id="75f68-134">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="75f68-134">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="75f68-135">**13**</span><span class="sxs-lookup"><span data-stu-id="75f68-135">**13**</span></span>
</dt> <dd>

<span data-ttu-id="75f68-136">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="75f68-136">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="75f68-137">**14**</span><span class="sxs-lookup"><span data-stu-id="75f68-137">**14**</span></span>
</dt> <dd>

<span data-ttu-id="75f68-138">目錄不是空的。</span><span class="sxs-lookup"><span data-stu-id="75f68-138">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="75f68-139">**15**</span><span class="sxs-lookup"><span data-stu-id="75f68-139">**15**</span></span>
</dt> <dd>

<span data-ttu-id="75f68-140">發生共用違規。</span><span class="sxs-lookup"><span data-stu-id="75f68-140">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="75f68-141">**16**</span><span class="sxs-lookup"><span data-stu-id="75f68-141">**16**</span></span>
</dt> <dd>

<span data-ttu-id="75f68-142">指定的起始檔無效。</span><span class="sxs-lookup"><span data-stu-id="75f68-142">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="75f68-143">**17**</span><span class="sxs-lookup"><span data-stu-id="75f68-143">**17**</span></span>
</dt> <dd>

<span data-ttu-id="75f68-144">不會保留操作所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="75f68-144">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="75f68-145">**21**</span><span class="sxs-lookup"><span data-stu-id="75f68-145">**21**</span></span>
</dt> <dd>

<span data-ttu-id="75f68-146">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="75f68-146">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="75f68-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="75f68-147">Requirements</span></span>



| <span data-ttu-id="75f68-148">需求</span><span class="sxs-lookup"><span data-stu-id="75f68-148">Requirement</span></span> | <span data-ttu-id="75f68-149">值</span><span class="sxs-lookup"><span data-stu-id="75f68-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75f68-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="75f68-150">Minimum supported client</span></span><br/> | <span data-ttu-id="75f68-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="75f68-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="75f68-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="75f68-152">Minimum supported server</span></span><br/> | <span data-ttu-id="75f68-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75f68-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="75f68-154">命名空間</span><span class="sxs-lookup"><span data-stu-id="75f68-154">Namespace</span></span><br/>                | <span data-ttu-id="75f68-155">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="75f68-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="75f68-156">MOF</span><span class="sxs-lookup"><span data-stu-id="75f68-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75f68-157"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="75f68-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="75f68-158">DLL</span><span class="sxs-lookup"><span data-stu-id="75f68-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75f68-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75f68-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75f68-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75f68-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="75f68-161">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="75f68-161">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="75f68-162">**Win32 \_ ShortcutFile**</span><span class="sxs-lookup"><span data-stu-id="75f68-162">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

