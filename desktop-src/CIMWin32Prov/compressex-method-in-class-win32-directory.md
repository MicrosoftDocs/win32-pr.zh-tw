---
description: 壓縮 (或物件路徑中指定的目錄) 的邏輯目錄專案檔， (這個方法是壓縮方法) 的擴充版本。
ms.assetid: 6b6e559c-4ca6-49d4-b255-5e1511fdf2e2
ms.tgt_platform: multiple
title: Win32_Directory 類別的 CompressEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3ee300919efa388d27ae9d594bc2b6c27def88e6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998432"
---
# <a name="compressex-method-of-the-win32_directory-class"></a><span data-ttu-id="15084-103">Win32 目錄類別的 CompressEx 方法 \_</span><span class="sxs-lookup"><span data-stu-id="15084-103">CompressEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="15084-104">**CompressEx** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會將邏輯目錄專案檔壓縮 (或物件路徑中指定的目錄)  (這個方法是 [**壓縮**](compress-method-in-class-win32-directory.md)方法) 的擴充版本。</span><span class="sxs-lookup"><span data-stu-id="15084-104">The **CompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical directory entry file (or directory) specified in the object path (this method is an extended version of the [**Compress**](compress-method-in-class-win32-directory.md) method).</span></span>

<span data-ttu-id="15084-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="15084-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="15084-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="15084-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="15084-107">語法</span><span class="sxs-lookup"><span data-stu-id="15084-107">Syntax</span></span>


```mof
uint32 CompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="15084-108">參數</span><span class="sxs-lookup"><span data-stu-id="15084-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15084-109">*StopFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="15084-109">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15084-110">**CompressEx** 方法失敗之檔案或目錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="15084-110">Name of the file or directory where the **CompressEx** method failed.</span></span> <span data-ttu-id="15084-111">如果方法成功，此參數將會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="15084-111">This parameter will be **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="15084-112">*StartFileName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="15084-112">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="15084-113">將子檔案或目錄命名為 **CompressEx** 的起點。</span><span class="sxs-lookup"><span data-stu-id="15084-113">Names the child file or directory to use as a starting point for **CompressEx**.</span></span> <span data-ttu-id="15084-114">*StartFileName* 參數通常是 *StopFileName* 參數，可指定上一個方法呼叫發生錯誤的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="15084-114">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="15084-115">如果這個參數是 **Null**，則會在 **ExecMethod** 呼叫中指定的檔案或目錄上執行作業。</span><span class="sxs-lookup"><span data-stu-id="15084-115">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

<span data-ttu-id="15084-116">如果使用 *StartFileName* ，則 *遞迴* 也必須設定為 true。</span><span class="sxs-lookup"><span data-stu-id="15084-116">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="15084-117">*遞迴* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="15084-117">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="15084-118">若 **為 true**，則會將擁有權變更以遞迴方式套用至 [**CIM \_ LogicalFile**](cim-logicalfile.md) 實例所指定之目錄中的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="15084-118">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="15084-119">若為檔案實例，則會忽略 *遞迴* 輸入參數。</span><span class="sxs-lookup"><span data-stu-id="15084-119">For file instances, the *Recursive* input parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15084-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="15084-120">Return value</span></span>

<span data-ttu-id="15084-121">傳回值 0 (零) 如果檔案已成功壓縮，則為，而任何其他數位表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="15084-121">Returns a value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="15084-122">**0**</span><span class="sxs-lookup"><span data-stu-id="15084-122">**0**</span></span>
</dt> <dd>

<span data-ttu-id="15084-123">要求成功。</span><span class="sxs-lookup"><span data-stu-id="15084-123">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="15084-124">**2**</span><span class="sxs-lookup"><span data-stu-id="15084-124">**2**</span></span>
</dt> <dd>

<span data-ttu-id="15084-125">存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="15084-125">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="15084-126">**8**</span><span class="sxs-lookup"><span data-stu-id="15084-126">**8**</span></span>
</dt> <dd>

<span data-ttu-id="15084-127">發生未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="15084-127">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="15084-128">**9**</span><span class="sxs-lookup"><span data-stu-id="15084-128">**9**</span></span>
</dt> <dd>

<span data-ttu-id="15084-129">指定的名稱無效。</span><span class="sxs-lookup"><span data-stu-id="15084-129">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="15084-130">**10**</span><span class="sxs-lookup"><span data-stu-id="15084-130">**10**</span></span>
</dt> <dd>

<span data-ttu-id="15084-131">指定的物件已經存在。</span><span class="sxs-lookup"><span data-stu-id="15084-131">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="15084-132">**11**</span><span class="sxs-lookup"><span data-stu-id="15084-132">**11**</span></span>
</dt> <dd>

<span data-ttu-id="15084-133">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="15084-133">The file system is not an NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="15084-134">**12**</span><span class="sxs-lookup"><span data-stu-id="15084-134">**12**</span></span>
</dt> <dd>

<span data-ttu-id="15084-135">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="15084-135">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="15084-136">**13**</span><span class="sxs-lookup"><span data-stu-id="15084-136">**13**</span></span>
</dt> <dd>

<span data-ttu-id="15084-137">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="15084-137">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="15084-138">**14**</span><span class="sxs-lookup"><span data-stu-id="15084-138">**14**</span></span>
</dt> <dd>

<span data-ttu-id="15084-139">目錄不是空的。</span><span class="sxs-lookup"><span data-stu-id="15084-139">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="15084-140">**15**</span><span class="sxs-lookup"><span data-stu-id="15084-140">**15**</span></span>
</dt> <dd>

<span data-ttu-id="15084-141">發生共用違規。</span><span class="sxs-lookup"><span data-stu-id="15084-141">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="15084-142">**16**</span><span class="sxs-lookup"><span data-stu-id="15084-142">**16**</span></span>
</dt> <dd>

<span data-ttu-id="15084-143">指定的起始檔無效。</span><span class="sxs-lookup"><span data-stu-id="15084-143">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="15084-144">**17**</span><span class="sxs-lookup"><span data-stu-id="15084-144">**17**</span></span>
</dt> <dd>

<span data-ttu-id="15084-145">不會保留操作所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="15084-145">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="15084-146">**21**</span><span class="sxs-lookup"><span data-stu-id="15084-146">**21**</span></span>
</dt> <dd>

<span data-ttu-id="15084-147">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="15084-147">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="15084-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="15084-148">Requirements</span></span>



| <span data-ttu-id="15084-149">需求</span><span class="sxs-lookup"><span data-stu-id="15084-149">Requirement</span></span> | <span data-ttu-id="15084-150">值</span><span class="sxs-lookup"><span data-stu-id="15084-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15084-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="15084-151">Minimum supported client</span></span><br/> | <span data-ttu-id="15084-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15084-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="15084-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="15084-153">Minimum supported server</span></span><br/> | <span data-ttu-id="15084-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15084-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="15084-155">命名空間</span><span class="sxs-lookup"><span data-stu-id="15084-155">Namespace</span></span><br/>                | <span data-ttu-id="15084-156">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="15084-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="15084-157">MOF</span><span class="sxs-lookup"><span data-stu-id="15084-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15084-158"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="15084-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="15084-159">DLL</span><span class="sxs-lookup"><span data-stu-id="15084-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15084-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15084-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15084-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15084-161">See also</span></span>

<dl> <dt>

<span data-ttu-id="15084-162">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="15084-162">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="15084-163">**Win32 \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="15084-163">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

