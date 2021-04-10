---
description: 取得物件路徑中指定的邏輯分頁檔擁有權。 這個方法是 TakeOwnerShip 方法的擴充版本。
ms.assetid: 6c359910-713a-441e-b2e1-949929c07e93
ms.tgt_platform: multiple
title: Win32_PageFile 類別的 TakeOwnerShipEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5b0f4662b4884da227a64768cc29bce4c615f8f7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187600"
---
# <a name="takeownershipex-method-of-the-win32_pagefile-class"></a><span data-ttu-id="8f3a1-104">Win32 \_ 分頁檔類別的 TakeOwnerShipEx 方法</span><span class="sxs-lookup"><span data-stu-id="8f3a1-104">TakeOwnerShipEx method of the Win32\_PageFile class</span></span>

<span data-ttu-id="8f3a1-105">**TakeOwnerShipEx** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會取得物件路徑中指定之邏輯分頁檔的擁有權。</span><span class="sxs-lookup"><span data-stu-id="8f3a1-105">The **TakeOwnerShipEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical paging file specified in the object path.</span></span> <span data-ttu-id="8f3a1-106">這個方法是 [**TakeOwnerShip**](takeownership-method-in-class-win32-directory.md) 方法的擴充版本。</span><span class="sxs-lookup"><span data-stu-id="8f3a1-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="8f3a1-107">如果邏輯檔案實際上是目錄，則此方法會以遞迴方式運作，並取得目錄包含的所有檔案和子目錄的擁有權。</span><span class="sxs-lookup"><span data-stu-id="8f3a1-107">If the logical file is actually a directory, then this method acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="8f3a1-108">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="8f3a1-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8f3a1-109">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="8f3a1-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8f3a1-110">語法</span><span class="sxs-lookup"><span data-stu-id="8f3a1-110">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="8f3a1-111">參數</span><span class="sxs-lookup"><span data-stu-id="8f3a1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f3a1-112">*StopFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8f3a1-112">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f3a1-113">**TakeOwnerShipEx** 方法失敗之檔案或目錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f3a1-113">Name of the file or directory where the **TakeOwnerShipEx** method failed.</span></span> <span data-ttu-id="8f3a1-114">如果方法成功，此參數將會是 **null** 。</span><span class="sxs-lookup"><span data-stu-id="8f3a1-114">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="8f3a1-115">*StartFileName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="8f3a1-115">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8f3a1-116">將子檔案或目錄命名為 **TakeOwnerShipEx** 的起點。 *StartFileName* 參數通常是 *StopFileName* 參數，可指定上一個方法呼叫發生錯誤的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="8f3a1-116">Names the child file or directory to use as a starting point for **TakeOwnerShipEx**.The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="8f3a1-117">如果這個參數是 **Null**，則會在 ExecMethod 呼叫中指定的檔案或目錄上執行作業。</span><span class="sxs-lookup"><span data-stu-id="8f3a1-117">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> <dt>

<span data-ttu-id="8f3a1-118">*遞迴* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="8f3a1-118">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8f3a1-119">若 **為 true**，則會將擁有權的變更以遞迴方式套用至 [**CIM \_ LogicalFile**](cim-logicalfile.md) 實例所指定之目錄中的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="8f3a1-119">If **true**, the change of ownership will be applied recursively to the files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="8f3a1-120">若為檔案實例，則會忽略 *遞迴* 參數。</span><span class="sxs-lookup"><span data-stu-id="8f3a1-120">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f3a1-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="8f3a1-121">Return value</span></span>

<span data-ttu-id="8f3a1-122">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="8f3a1-122">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="8f3a1-123">**0**</span><span class="sxs-lookup"><span data-stu-id="8f3a1-123">**0**</span></span>
</dt> <dd>

<span data-ttu-id="8f3a1-124">要求成功。</span><span class="sxs-lookup"><span data-stu-id="8f3a1-124">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="8f3a1-125">**2**</span><span class="sxs-lookup"><span data-stu-id="8f3a1-125">**2**</span></span>
</dt> <dd>

<span data-ttu-id="8f3a1-126">存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="8f3a1-126">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="8f3a1-127">**8**</span><span class="sxs-lookup"><span data-stu-id="8f3a1-127">**8**</span></span>
</dt> <dd>

<span data-ttu-id="8f3a1-128">發生未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="8f3a1-128">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="8f3a1-129">**9**</span><span class="sxs-lookup"><span data-stu-id="8f3a1-129">**9**</span></span>
</dt> <dd>

<span data-ttu-id="8f3a1-130">指定的名稱無效。</span><span class="sxs-lookup"><span data-stu-id="8f3a1-130">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="8f3a1-131">**10**</span><span class="sxs-lookup"><span data-stu-id="8f3a1-131">**10**</span></span>
</dt> <dd>

<span data-ttu-id="8f3a1-132">指定的物件已經存在。</span><span class="sxs-lookup"><span data-stu-id="8f3a1-132">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="8f3a1-133">**11**</span><span class="sxs-lookup"><span data-stu-id="8f3a1-133">**11**</span></span>
</dt> <dd>

<span data-ttu-id="8f3a1-134">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="8f3a1-134">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="8f3a1-135">**12**</span><span class="sxs-lookup"><span data-stu-id="8f3a1-135">**12**</span></span>
</dt> <dd>

<span data-ttu-id="8f3a1-136">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="8f3a1-136">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="8f3a1-137">**13**</span><span class="sxs-lookup"><span data-stu-id="8f3a1-137">**13**</span></span>
</dt> <dd>

<span data-ttu-id="8f3a1-138">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="8f3a1-138">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="8f3a1-139">**14**</span><span class="sxs-lookup"><span data-stu-id="8f3a1-139">**14**</span></span>
</dt> <dd>

<span data-ttu-id="8f3a1-140">目錄不是空的。</span><span class="sxs-lookup"><span data-stu-id="8f3a1-140">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="8f3a1-141">**15**</span><span class="sxs-lookup"><span data-stu-id="8f3a1-141">**15**</span></span>
</dt> <dd>

<span data-ttu-id="8f3a1-142">發生共用違規。</span><span class="sxs-lookup"><span data-stu-id="8f3a1-142">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="8f3a1-143">**16**</span><span class="sxs-lookup"><span data-stu-id="8f3a1-143">**16**</span></span>
</dt> <dd>

<span data-ttu-id="8f3a1-144">指定的起始檔無效。</span><span class="sxs-lookup"><span data-stu-id="8f3a1-144">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="8f3a1-145">**17**</span><span class="sxs-lookup"><span data-stu-id="8f3a1-145">**17**</span></span>
</dt> <dd>

<span data-ttu-id="8f3a1-146">不會保留操作所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="8f3a1-146">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="8f3a1-147">**21**</span><span class="sxs-lookup"><span data-stu-id="8f3a1-147">**21**</span></span>
</dt> <dd>

<span data-ttu-id="8f3a1-148">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="8f3a1-148">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8f3a1-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f3a1-149">Requirements</span></span>



| <span data-ttu-id="8f3a1-150">需求</span><span class="sxs-lookup"><span data-stu-id="8f3a1-150">Requirement</span></span> | <span data-ttu-id="8f3a1-151">值</span><span class="sxs-lookup"><span data-stu-id="8f3a1-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f3a1-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8f3a1-152">Minimum supported client</span></span><br/> | <span data-ttu-id="8f3a1-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f3a1-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8f3a1-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8f3a1-154">Minimum supported server</span></span><br/> | <span data-ttu-id="8f3a1-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f3a1-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8f3a1-156">命名空間</span><span class="sxs-lookup"><span data-stu-id="8f3a1-156">Namespace</span></span><br/>                | <span data-ttu-id="8f3a1-157">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8f3a1-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8f3a1-158">MOF</span><span class="sxs-lookup"><span data-stu-id="8f3a1-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f3a1-159"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f3a1-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f3a1-160">DLL</span><span class="sxs-lookup"><span data-stu-id="8f3a1-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f3a1-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f3a1-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f3a1-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f3a1-162">See also</span></span>

<dl> <dt>

<span data-ttu-id="8f3a1-163">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8f3a1-163">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8f3a1-164">**Win32 \_ 分頁檔**</span><span class="sxs-lookup"><span data-stu-id="8f3a1-164">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

