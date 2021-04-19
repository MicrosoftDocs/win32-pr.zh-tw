---
description: 重新命名物件路徑中指定的分頁檔。
ms.assetid: 6a98e05f-337e-4224-a847-f01913031b20
ms.tgt_platform: multiple
title: Win32_PageFile 類別的重新命名方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c9ba8162cd115a567e9e9010420c558061fed08
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971301"
---
# <a name="rename-method-of-the-win32_pagefile-class"></a><span data-ttu-id="fd641-103">Win32 分頁檔類別的重新命名方法 \_</span><span class="sxs-lookup"><span data-stu-id="fd641-103">Rename method of the Win32\_PageFile class</span></span>

<span data-ttu-id="fd641-104">**重新命名** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會重新命名物件路徑中指定的分頁檔。</span><span class="sxs-lookup"><span data-stu-id="fd641-104">The **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renames the paging file specified in the object path.</span></span> <span data-ttu-id="fd641-105">如果目的地是在另一個磁片磁碟機上，或需要覆寫現有的邏輯檔案，則不支援重新命名。</span><span class="sxs-lookup"><span data-stu-id="fd641-105">A rename is not supported if the destination is on another drive or if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="fd641-106">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="fd641-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="fd641-107">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="fd641-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="fd641-108">語法</span><span class="sxs-lookup"><span data-stu-id="fd641-108">Syntax</span></span>


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="fd641-109">參數</span><span class="sxs-lookup"><span data-stu-id="fd641-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd641-110">*檔案名* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fd641-110">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd641-111">檔案 (或目錄) 的完整新名稱。</span><span class="sxs-lookup"><span data-stu-id="fd641-111">Fully qualified new name of the file (or directory).</span></span>

<span data-ttu-id="fd641-112">範例： c： \\ temp \\newfile.txt</span><span class="sxs-lookup"><span data-stu-id="fd641-112">Example: c:\\temp\\newfile.txt</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd641-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="fd641-113">Return value</span></span>

<span data-ttu-id="fd641-114">如果成功重新命名檔案，則傳回值為 0 (零) ，以及表示錯誤的其他任何數位。</span><span class="sxs-lookup"><span data-stu-id="fd641-114">Returns a value of 0 (zero) if the file was successfully renamed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="fd641-115">**0**</span><span class="sxs-lookup"><span data-stu-id="fd641-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="fd641-116">要求成功。</span><span class="sxs-lookup"><span data-stu-id="fd641-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="fd641-117">**2**</span><span class="sxs-lookup"><span data-stu-id="fd641-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="fd641-118">存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="fd641-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="fd641-119">**8**</span><span class="sxs-lookup"><span data-stu-id="fd641-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="fd641-120">發生未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="fd641-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="fd641-121">**9**</span><span class="sxs-lookup"><span data-stu-id="fd641-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="fd641-122">指定的名稱無效。</span><span class="sxs-lookup"><span data-stu-id="fd641-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="fd641-123">**10**</span><span class="sxs-lookup"><span data-stu-id="fd641-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="fd641-124">指定的物件已經存在。</span><span class="sxs-lookup"><span data-stu-id="fd641-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="fd641-125">**11**</span><span class="sxs-lookup"><span data-stu-id="fd641-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="fd641-126">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="fd641-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="fd641-127">**12**</span><span class="sxs-lookup"><span data-stu-id="fd641-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="fd641-128">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="fd641-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="fd641-129">**13**</span><span class="sxs-lookup"><span data-stu-id="fd641-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="fd641-130">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="fd641-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="fd641-131">**14**</span><span class="sxs-lookup"><span data-stu-id="fd641-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="fd641-132">目錄不是空的。</span><span class="sxs-lookup"><span data-stu-id="fd641-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="fd641-133">**15**</span><span class="sxs-lookup"><span data-stu-id="fd641-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="fd641-134">發生共用違規。</span><span class="sxs-lookup"><span data-stu-id="fd641-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="fd641-135">**16**</span><span class="sxs-lookup"><span data-stu-id="fd641-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="fd641-136">指定的起始檔無效。</span><span class="sxs-lookup"><span data-stu-id="fd641-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="fd641-137">**17**</span><span class="sxs-lookup"><span data-stu-id="fd641-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="fd641-138">不會保留操作所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="fd641-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="fd641-139">**21**</span><span class="sxs-lookup"><span data-stu-id="fd641-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="fd641-140">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="fd641-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd641-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd641-141">Requirements</span></span>



| <span data-ttu-id="fd641-142">需求</span><span class="sxs-lookup"><span data-stu-id="fd641-142">Requirement</span></span> | <span data-ttu-id="fd641-143">值</span><span class="sxs-lookup"><span data-stu-id="fd641-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd641-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fd641-144">Minimum supported client</span></span><br/> | <span data-ttu-id="fd641-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd641-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fd641-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fd641-146">Minimum supported server</span></span><br/> | <span data-ttu-id="fd641-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd641-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fd641-148">命名空間</span><span class="sxs-lookup"><span data-stu-id="fd641-148">Namespace</span></span><br/>                | <span data-ttu-id="fd641-149">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fd641-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fd641-150">MOF</span><span class="sxs-lookup"><span data-stu-id="fd641-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd641-151"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd641-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd641-152">DLL</span><span class="sxs-lookup"><span data-stu-id="fd641-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd641-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd641-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd641-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd641-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="fd641-155">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fd641-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="fd641-156">**Win32 \_ 分頁檔**</span><span class="sxs-lookup"><span data-stu-id="fd641-156">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

