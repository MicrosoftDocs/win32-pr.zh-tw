---
description: 將物件路徑中指定的邏輯快速鍵檔或目錄複寫到 FileName 參數所指定的位置。 這個方法是複製方法的擴充版本。
ms.assetid: 06b629bb-d35e-4bc2-b0e5-c6a981b6d968
ms.tgt_platform: multiple
title: Win32_ShortcutFile 類別的 CopyEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6cbf1cbb622610a01a533195752b3532b25f8959
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971136"
---
# <a name="copyex-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="49976-104">Win32 ShortcutFile 類別的 CopyEx 方法 \_</span><span class="sxs-lookup"><span data-stu-id="49976-104">CopyEx method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="49976-105">**CopyEx** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會將物件路徑中指定的邏輯快速鍵檔或目錄複寫到 *FileName* 參數所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="49976-105">The **CopyEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method copies the logical shortcut file or directory specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="49976-106">這個方法是 [**複製**](copy-method-in-class-win32-directory.md) 方法的擴充版本。</span><span class="sxs-lookup"><span data-stu-id="49976-106">This method is an extended version of the [**Copy**](copy-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="49976-107">如果需要覆寫現有的邏輯檔案，則不支援複製。</span><span class="sxs-lookup"><span data-stu-id="49976-107">A copy is not supported if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="49976-108">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="49976-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="49976-109">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="49976-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="49976-110">語法</span><span class="sxs-lookup"><span data-stu-id="49976-110">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]           string  FileName,
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="49976-111">參數</span><span class="sxs-lookup"><span data-stu-id="49976-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49976-112">*檔案名* \[在\]</span><span class="sxs-lookup"><span data-stu-id="49976-112">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49976-113"> (或目錄) 之檔案複本的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="49976-113">Fully qualified name of the copy of the file (or directory).</span></span>

<span data-ttu-id="49976-114">範例： c： \\ temp \\ newdirectory。</span><span class="sxs-lookup"><span data-stu-id="49976-114">Example: c:\\temp\\newdirectory.</span></span>

</dd> <dt>

<span data-ttu-id="49976-115">*StopFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="49976-115">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49976-116">**CopyEx** 方法失敗之檔案或目錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="49976-116">Name of the file or directory where the **CopyEx** method failed.</span></span> <span data-ttu-id="49976-117">如果方法成功，則此參數為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="49976-117">This parameter is **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="49976-118">*StartFileName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="49976-118">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="49976-119">將子檔案或目錄命名為 **CopyEx** 的起點。</span><span class="sxs-lookup"><span data-stu-id="49976-119">Names the child file or directory to use as a starting point for **CopyEx**.</span></span> <span data-ttu-id="49976-120">*StartFileName* 參數通常是 *StopFileName* 參數，可指定上一個方法呼叫發生錯誤的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="49976-120">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="49976-121">如果這個參數是 **Null**，則會在 ExecMethod 呼叫中指定的檔案或目錄上執行作業。</span><span class="sxs-lookup"><span data-stu-id="49976-121">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> <dt>

<span data-ttu-id="49976-122">*遞迴* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="49976-122">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="49976-123">若 **為 true**，則會將擁有權變更以遞迴方式套用至 [**CIM \_ LogicalFile**](cim-logicalfile.md) 實例所指定之目錄中的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="49976-123">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="49976-124">若為檔案實例，則會忽略 *遞迴* 輸入參數。</span><span class="sxs-lookup"><span data-stu-id="49976-124">For file instances, the *Recursive* input parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49976-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="49976-125">Return value</span></span>

<span data-ttu-id="49976-126">如果成功複製檔案，則傳回 0 (零) 的值，以及表示錯誤的其他任何數位。</span><span class="sxs-lookup"><span data-stu-id="49976-126">Returns a value of 0 (zero) if the file was successfully copied, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="49976-127">**0**</span><span class="sxs-lookup"><span data-stu-id="49976-127">**0**</span></span>
</dt> <dd>

<span data-ttu-id="49976-128">要求成功。</span><span class="sxs-lookup"><span data-stu-id="49976-128">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="49976-129">**2**</span><span class="sxs-lookup"><span data-stu-id="49976-129">**2**</span></span>
</dt> <dd>

<span data-ttu-id="49976-130">存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="49976-130">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="49976-131">**8**</span><span class="sxs-lookup"><span data-stu-id="49976-131">**8**</span></span>
</dt> <dd>

<span data-ttu-id="49976-132">發生未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="49976-132">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="49976-133">**9**</span><span class="sxs-lookup"><span data-stu-id="49976-133">**9**</span></span>
</dt> <dd>

<span data-ttu-id="49976-134">指定的名稱無效。</span><span class="sxs-lookup"><span data-stu-id="49976-134">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="49976-135">**10**</span><span class="sxs-lookup"><span data-stu-id="49976-135">**10**</span></span>
</dt> <dd>

<span data-ttu-id="49976-136">指定的物件已經存在。</span><span class="sxs-lookup"><span data-stu-id="49976-136">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="49976-137">**11**</span><span class="sxs-lookup"><span data-stu-id="49976-137">**11**</span></span>
</dt> <dd>

<span data-ttu-id="49976-138">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="49976-138">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="49976-139">**12**</span><span class="sxs-lookup"><span data-stu-id="49976-139">**12**</span></span>
</dt> <dd>

<span data-ttu-id="49976-140">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="49976-140">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="49976-141">**13**</span><span class="sxs-lookup"><span data-stu-id="49976-141">**13**</span></span>
</dt> <dd>

<span data-ttu-id="49976-142">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="49976-142">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="49976-143">**14**</span><span class="sxs-lookup"><span data-stu-id="49976-143">**14**</span></span>
</dt> <dd>

<span data-ttu-id="49976-144">目錄不是空的。</span><span class="sxs-lookup"><span data-stu-id="49976-144">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="49976-145">**15**</span><span class="sxs-lookup"><span data-stu-id="49976-145">**15**</span></span>
</dt> <dd>

<span data-ttu-id="49976-146">發生共用違規。</span><span class="sxs-lookup"><span data-stu-id="49976-146">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="49976-147">**16**</span><span class="sxs-lookup"><span data-stu-id="49976-147">**16**</span></span>
</dt> <dd>

<span data-ttu-id="49976-148">指定的起始檔無效。</span><span class="sxs-lookup"><span data-stu-id="49976-148">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="49976-149">**17**</span><span class="sxs-lookup"><span data-stu-id="49976-149">**17**</span></span>
</dt> <dd>

<span data-ttu-id="49976-150">不會保留操作所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="49976-150">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="49976-151">**21**</span><span class="sxs-lookup"><span data-stu-id="49976-151">**21**</span></span>
</dt> <dd>

<span data-ttu-id="49976-152">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="49976-152">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="49976-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="49976-153">Requirements</span></span>



| <span data-ttu-id="49976-154">需求</span><span class="sxs-lookup"><span data-stu-id="49976-154">Requirement</span></span> | <span data-ttu-id="49976-155">值</span><span class="sxs-lookup"><span data-stu-id="49976-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49976-156">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="49976-156">Minimum supported client</span></span><br/> | <span data-ttu-id="49976-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="49976-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="49976-158">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="49976-158">Minimum supported server</span></span><br/> | <span data-ttu-id="49976-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49976-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="49976-160">命名空間</span><span class="sxs-lookup"><span data-stu-id="49976-160">Namespace</span></span><br/>                | <span data-ttu-id="49976-161">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="49976-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="49976-162">MOF</span><span class="sxs-lookup"><span data-stu-id="49976-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="49976-163"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="49976-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="49976-164">DLL</span><span class="sxs-lookup"><span data-stu-id="49976-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49976-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49976-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49976-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49976-166">See also</span></span>

<dl> <dt>

<span data-ttu-id="49976-167">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="49976-167">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="49976-168">**Win32 \_ ShortcutFile**</span><span class="sxs-lookup"><span data-stu-id="49976-168">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

