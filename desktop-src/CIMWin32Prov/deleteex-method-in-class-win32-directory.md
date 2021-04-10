---
description: DeleteEx WMI 類別方法會刪除物件路徑中指定的邏輯檔案 (或目錄) 。 DeleteEx 是刪除方法的擴充版本。
ms.assetid: 6e5447c1-4d71-4a51-a1e0-b5785c13dfd2
ms.tgt_platform: multiple
title: Win32_Directory 類別的 DeleteEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ac23a4013053d252aec49b8b7be4aae62c41c8e1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936224"
---
# <a name="deleteex-method-of-the-win32_directory-class"></a><span data-ttu-id="d316b-104">Win32 目錄類別的 DeleteEx 方法 \_</span><span class="sxs-lookup"><span data-stu-id="d316b-104">DeleteEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="d316b-105">**DeleteEx** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會刪除物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="d316b-105">The **DeleteEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method will delete the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="d316b-106">**DeleteEx** 是 [**刪除**](delete-method-in-class-win32-directory.md) 方法的擴充版本。</span><span class="sxs-lookup"><span data-stu-id="d316b-106">**DeleteEx** is an extended version of the [**Delete**](delete-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="d316b-107">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="d316b-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d316b-108">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="d316b-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d316b-109">語法</span><span class="sxs-lookup"><span data-stu-id="d316b-109">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out]          string StopFileName,
  [in, optional] string StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="d316b-110">參數</span><span class="sxs-lookup"><span data-stu-id="d316b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d316b-111">*StopFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d316b-111">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d316b-112">**DeleteEx** 方法失敗之檔案或目錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="d316b-112">Name of the file or directory where the **DeleteEx** method failed.</span></span> <span data-ttu-id="d316b-113">如果方法成功，此參數將會是 **null** 。</span><span class="sxs-lookup"><span data-stu-id="d316b-113">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="d316b-114">*StartFileName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d316b-114">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d316b-115">將子檔案或目錄命名為 **DeleteEx** 的起點。</span><span class="sxs-lookup"><span data-stu-id="d316b-115">Names the child file or directory to use as a starting point for **DeleteEx**.</span></span> <span data-ttu-id="d316b-116">*StartFileName* 參數通常是 *StopFileName* 參數，可指定上一個方法呼叫發生錯誤的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="d316b-116">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="d316b-117">如果這個參數是 **Null**，則會在 ExecMethod 呼叫中指定的檔案或目錄上執行作業。</span><span class="sxs-lookup"><span data-stu-id="d316b-117">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d316b-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="d316b-118">Return value</span></span>

<span data-ttu-id="d316b-119">如果成功刪除檔案，則傳回值為 0 (零) ，以及表示錯誤的其他任何數位。</span><span class="sxs-lookup"><span data-stu-id="d316b-119">Returns a value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="d316b-120">**0**</span><span class="sxs-lookup"><span data-stu-id="d316b-120">**0**</span></span>
</dt> <dd>

<span data-ttu-id="d316b-121">要求成功。</span><span class="sxs-lookup"><span data-stu-id="d316b-121">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="d316b-122">**2**</span><span class="sxs-lookup"><span data-stu-id="d316b-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="d316b-123">存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="d316b-123">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="d316b-124">**8**</span><span class="sxs-lookup"><span data-stu-id="d316b-124">**8**</span></span>
</dt> <dd>

<span data-ttu-id="d316b-125">發生未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="d316b-125">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="d316b-126">**9**</span><span class="sxs-lookup"><span data-stu-id="d316b-126">**9**</span></span>
</dt> <dd>

<span data-ttu-id="d316b-127">指定的名稱無效。</span><span class="sxs-lookup"><span data-stu-id="d316b-127">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d316b-128">**10**</span><span class="sxs-lookup"><span data-stu-id="d316b-128">**10**</span></span>
</dt> <dd>

<span data-ttu-id="d316b-129">指定的物件已經存在。</span><span class="sxs-lookup"><span data-stu-id="d316b-129">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d316b-130">**11**</span><span class="sxs-lookup"><span data-stu-id="d316b-130">**11**</span></span>
</dt> <dd>

<span data-ttu-id="d316b-131">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="d316b-131">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="d316b-132">**12**</span><span class="sxs-lookup"><span data-stu-id="d316b-132">**12**</span></span>
</dt> <dd>

<span data-ttu-id="d316b-133">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="d316b-133">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="d316b-134">**13**</span><span class="sxs-lookup"><span data-stu-id="d316b-134">**13**</span></span>
</dt> <dd>

<span data-ttu-id="d316b-135">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="d316b-135">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="d316b-136">**14**</span><span class="sxs-lookup"><span data-stu-id="d316b-136">**14**</span></span>
</dt> <dd>

<span data-ttu-id="d316b-137">目錄不是空的。</span><span class="sxs-lookup"><span data-stu-id="d316b-137">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="d316b-138">**15**</span><span class="sxs-lookup"><span data-stu-id="d316b-138">**15**</span></span>
</dt> <dd>

<span data-ttu-id="d316b-139">發生共用違規。</span><span class="sxs-lookup"><span data-stu-id="d316b-139">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="d316b-140">**16**</span><span class="sxs-lookup"><span data-stu-id="d316b-140">**16**</span></span>
</dt> <dd>

<span data-ttu-id="d316b-141">指定的起始檔無效。</span><span class="sxs-lookup"><span data-stu-id="d316b-141">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d316b-142">**17**</span><span class="sxs-lookup"><span data-stu-id="d316b-142">**17**</span></span>
</dt> <dd>

<span data-ttu-id="d316b-143">不會保留操作所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="d316b-143">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="d316b-144">**21**</span><span class="sxs-lookup"><span data-stu-id="d316b-144">**21**</span></span>
</dt> <dd>

<span data-ttu-id="d316b-145">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="d316b-145">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d316b-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="d316b-146">Requirements</span></span>



| <span data-ttu-id="d316b-147">需求</span><span class="sxs-lookup"><span data-stu-id="d316b-147">Requirement</span></span> | <span data-ttu-id="d316b-148">值</span><span class="sxs-lookup"><span data-stu-id="d316b-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d316b-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d316b-149">Minimum supported client</span></span><br/> | <span data-ttu-id="d316b-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d316b-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d316b-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d316b-151">Minimum supported server</span></span><br/> | <span data-ttu-id="d316b-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d316b-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d316b-153">命名空間</span><span class="sxs-lookup"><span data-stu-id="d316b-153">Namespace</span></span><br/>                | <span data-ttu-id="d316b-154">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d316b-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d316b-155">MOF</span><span class="sxs-lookup"><span data-stu-id="d316b-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d316b-156"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="d316b-156"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d316b-157">DLL</span><span class="sxs-lookup"><span data-stu-id="d316b-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d316b-158"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d316b-158"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d316b-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d316b-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="d316b-160">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d316b-160">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d316b-161">**Win32 \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="d316b-161">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

