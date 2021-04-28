---
description: Win32_PageFile 類別的 DeleteEx 方法-刪除在物件路徑中指定 (或目錄) 的邏輯分頁檔。
ms.assetid: ea31f92a-94b9-4d4d-abd9-6c304ac5caee
ms.tgt_platform: multiple
title: Win32_PageFile 類別的 DeleteEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 34e27e80c3cfaea352ee97ad29aed0b7ca358546
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097046"
---
# <a name="deleteex-method-of-the-win32_pagefile-class"></a><span data-ttu-id="3ce00-103">Win32 \_ 分頁檔類別的 DeleteEx 方法</span><span class="sxs-lookup"><span data-stu-id="3ce00-103">DeleteEx method of the Win32\_PageFile class</span></span>

<span data-ttu-id="3ce00-104">**DeleteEx** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會刪除物件路徑中指定 (或目錄) 的邏輯分頁檔。</span><span class="sxs-lookup"><span data-stu-id="3ce00-104">The **DeleteEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes the logical paging file (or directory) specified in the object path.</span></span> <span data-ttu-id="3ce00-105">**DeleteEx** 是 [**刪除**](delete-method-in-class-win32-directory.md) 方法的擴充版本。</span><span class="sxs-lookup"><span data-stu-id="3ce00-105">**DeleteEx** is an extended version of the [**Delete**](delete-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="3ce00-106">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="3ce00-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3ce00-107">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="3ce00-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3ce00-108">語法</span><span class="sxs-lookup"><span data-stu-id="3ce00-108">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out]          string StopFileName,
  [in, optional] string StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="3ce00-109">參數</span><span class="sxs-lookup"><span data-stu-id="3ce00-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ce00-110">*StopFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3ce00-110">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ce00-111">**DeleteEx** 方法失敗之檔案或目錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ce00-111">Name of the file or directory where the **DeleteEx** method failed.</span></span> <span data-ttu-id="3ce00-112">如果方法成功，則此參數為 **null** 。</span><span class="sxs-lookup"><span data-stu-id="3ce00-112">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="3ce00-113">*StartFileName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="3ce00-113">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3ce00-114">將子檔案或目錄命名為 **DeleteEx** 的起點。</span><span class="sxs-lookup"><span data-stu-id="3ce00-114">Names the child file or directory to use as a starting point for **DeleteEx**.</span></span> <span data-ttu-id="3ce00-115">*StartFileName* 參數通常是 *StopFileName* 參數，可指定上一個方法呼叫發生錯誤的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="3ce00-115">The *StartFileName* parameter is typically the *StopFileName* parameter that specifies the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="3ce00-116">如果這個參數是 **Null**，則會在 ExecMethod 呼叫中指定的檔案或目錄上執行作業。</span><span class="sxs-lookup"><span data-stu-id="3ce00-116">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ce00-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="3ce00-117">Return value</span></span>

<span data-ttu-id="3ce00-118">如果成功刪除檔案，則傳回值為 0 (零) ，以及表示錯誤的其他任何數位。</span><span class="sxs-lookup"><span data-stu-id="3ce00-118">Returns a value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="3ce00-119">**0**</span><span class="sxs-lookup"><span data-stu-id="3ce00-119">**0**</span></span>
</dt> <dd>

<span data-ttu-id="3ce00-120">要求成功。</span><span class="sxs-lookup"><span data-stu-id="3ce00-120">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="3ce00-121">**2**</span><span class="sxs-lookup"><span data-stu-id="3ce00-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="3ce00-122">存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="3ce00-122">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="3ce00-123">**8**</span><span class="sxs-lookup"><span data-stu-id="3ce00-123">**8**</span></span>
</dt> <dd>

<span data-ttu-id="3ce00-124">發生未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="3ce00-124">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="3ce00-125">**9**</span><span class="sxs-lookup"><span data-stu-id="3ce00-125">**9**</span></span>
</dt> <dd>

<span data-ttu-id="3ce00-126">指定的名稱無效。</span><span class="sxs-lookup"><span data-stu-id="3ce00-126">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="3ce00-127">**10**</span><span class="sxs-lookup"><span data-stu-id="3ce00-127">**10**</span></span>
</dt> <dd>

<span data-ttu-id="3ce00-128">指定的物件已經存在。</span><span class="sxs-lookup"><span data-stu-id="3ce00-128">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="3ce00-129">**11**</span><span class="sxs-lookup"><span data-stu-id="3ce00-129">**11**</span></span>
</dt> <dd>

<span data-ttu-id="3ce00-130">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="3ce00-130">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="3ce00-131">**12**</span><span class="sxs-lookup"><span data-stu-id="3ce00-131">**12**</span></span>
</dt> <dd>

<span data-ttu-id="3ce00-132">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="3ce00-132">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="3ce00-133">**13**</span><span class="sxs-lookup"><span data-stu-id="3ce00-133">**13**</span></span>
</dt> <dd>

<span data-ttu-id="3ce00-134">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="3ce00-134">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="3ce00-135">**14**</span><span class="sxs-lookup"><span data-stu-id="3ce00-135">**14**</span></span>
</dt> <dd>

<span data-ttu-id="3ce00-136">目錄不是空的。</span><span class="sxs-lookup"><span data-stu-id="3ce00-136">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="3ce00-137">**15**</span><span class="sxs-lookup"><span data-stu-id="3ce00-137">**15**</span></span>
</dt> <dd>

<span data-ttu-id="3ce00-138">發生共用違規。</span><span class="sxs-lookup"><span data-stu-id="3ce00-138">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="3ce00-139">**16**</span><span class="sxs-lookup"><span data-stu-id="3ce00-139">**16**</span></span>
</dt> <dd>

<span data-ttu-id="3ce00-140">指定的起始檔無效。</span><span class="sxs-lookup"><span data-stu-id="3ce00-140">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="3ce00-141">**17**</span><span class="sxs-lookup"><span data-stu-id="3ce00-141">**17**</span></span>
</dt> <dd>

<span data-ttu-id="3ce00-142">不會保留操作所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="3ce00-142">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="3ce00-143">**21**</span><span class="sxs-lookup"><span data-stu-id="3ce00-143">**21**</span></span>
</dt> <dd>

<span data-ttu-id="3ce00-144">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="3ce00-144">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3ce00-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ce00-145">Requirements</span></span>



| <span data-ttu-id="3ce00-146">需求</span><span class="sxs-lookup"><span data-stu-id="3ce00-146">Requirement</span></span> | <span data-ttu-id="3ce00-147">值</span><span class="sxs-lookup"><span data-stu-id="3ce00-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ce00-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3ce00-148">Minimum supported client</span></span><br/> | <span data-ttu-id="3ce00-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3ce00-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3ce00-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3ce00-150">Minimum supported server</span></span><br/> | <span data-ttu-id="3ce00-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ce00-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3ce00-152">命名空間</span><span class="sxs-lookup"><span data-stu-id="3ce00-152">Namespace</span></span><br/>                | <span data-ttu-id="3ce00-153">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3ce00-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3ce00-154">MOF</span><span class="sxs-lookup"><span data-stu-id="3ce00-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ce00-155"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="3ce00-155"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ce00-156">DLL</span><span class="sxs-lookup"><span data-stu-id="3ce00-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ce00-157"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ce00-157"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ce00-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ce00-158">See also</span></span>

<dl> <dt>

<span data-ttu-id="3ce00-159">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3ce00-159">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3ce00-160">**Win32 \_ 分頁檔**</span><span class="sxs-lookup"><span data-stu-id="3ce00-160">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

