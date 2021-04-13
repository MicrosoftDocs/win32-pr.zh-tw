---
description: TakeOwnerShip WMI 類別方法會取得物件路徑中所指定之邏輯檔案的擁有權。
ms.assetid: 1112823b-0bb6-4dc0-a5c4-8d3839a47a3a
ms.tgt_platform: multiple
title: Win32_Directory 類別的 TakeOwnerShip 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c06441b7728ed8b9178e889cbd60c047f0f3a497
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510414"
---
# <a name="takeownership-method-of-the-win32_directory-class"></a><span data-ttu-id="91f09-103">Win32 目錄類別的 TakeOwnerShip 方法 \_</span><span class="sxs-lookup"><span data-stu-id="91f09-103">TakeOwnerShip method of the Win32\_Directory class</span></span>

<span data-ttu-id="91f09-104">**TakeOwnerShip** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會取得物件路徑中所指定之邏輯檔案的擁有權。</span><span class="sxs-lookup"><span data-stu-id="91f09-104">The **TakeOwnerShip** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="91f09-105">如果邏輯檔案實際上是目錄，則 **TakeOwnerShip** 會以遞迴方式運作，並取得目錄包含的所有檔案和子目錄的擁有權。</span><span class="sxs-lookup"><span data-stu-id="91f09-105">If the logical file is actually a directory, then **TakeOwnerShip** acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="91f09-106">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="91f09-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="91f09-107">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="91f09-107">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="91f09-108">語法</span><span class="sxs-lookup"><span data-stu-id="91f09-108">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="91f09-109">參數</span><span class="sxs-lookup"><span data-stu-id="91f09-109">Parameters</span></span>

<span data-ttu-id="91f09-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="91f09-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="91f09-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="91f09-111">Return value</span></span>

<span data-ttu-id="91f09-112">傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="91f09-112">Returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="91f09-113">**0**</span><span class="sxs-lookup"><span data-stu-id="91f09-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="91f09-114">要求成功。</span><span class="sxs-lookup"><span data-stu-id="91f09-114">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="91f09-115">**2**</span><span class="sxs-lookup"><span data-stu-id="91f09-115">**2**</span></span>
</dt> <dd>

<span data-ttu-id="91f09-116">存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="91f09-116">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="91f09-117">**8**</span><span class="sxs-lookup"><span data-stu-id="91f09-117">**8**</span></span>
</dt> <dd>

<span data-ttu-id="91f09-118">發生未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="91f09-118">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="91f09-119">**9**</span><span class="sxs-lookup"><span data-stu-id="91f09-119">**9**</span></span>
</dt> <dd>

<span data-ttu-id="91f09-120">指定的名稱無效。</span><span class="sxs-lookup"><span data-stu-id="91f09-120">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="91f09-121">**10**</span><span class="sxs-lookup"><span data-stu-id="91f09-121">**10**</span></span>
</dt> <dd>

<span data-ttu-id="91f09-122">指定的物件已經存在。</span><span class="sxs-lookup"><span data-stu-id="91f09-122">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="91f09-123">**11**</span><span class="sxs-lookup"><span data-stu-id="91f09-123">**11**</span></span>
</dt> <dd>

<span data-ttu-id="91f09-124">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="91f09-124">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="91f09-125">**12**</span><span class="sxs-lookup"><span data-stu-id="91f09-125">**12**</span></span>
</dt> <dd>

<span data-ttu-id="91f09-126">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="91f09-126">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="91f09-127">**13**</span><span class="sxs-lookup"><span data-stu-id="91f09-127">**13**</span></span>
</dt> <dd>

<span data-ttu-id="91f09-128">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="91f09-128">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="91f09-129">**14**</span><span class="sxs-lookup"><span data-stu-id="91f09-129">**14**</span></span>
</dt> <dd>

<span data-ttu-id="91f09-130">目錄不是空的。</span><span class="sxs-lookup"><span data-stu-id="91f09-130">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="91f09-131">**15**</span><span class="sxs-lookup"><span data-stu-id="91f09-131">**15**</span></span>
</dt> <dd>

<span data-ttu-id="91f09-132">發生共用違規。</span><span class="sxs-lookup"><span data-stu-id="91f09-132">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="91f09-133">**16**</span><span class="sxs-lookup"><span data-stu-id="91f09-133">**16**</span></span>
</dt> <dd>

<span data-ttu-id="91f09-134">指定的起始檔無效。</span><span class="sxs-lookup"><span data-stu-id="91f09-134">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="91f09-135">**17**</span><span class="sxs-lookup"><span data-stu-id="91f09-135">**17**</span></span>
</dt> <dd>

<span data-ttu-id="91f09-136">不會保留操作所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="91f09-136">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="91f09-137">**21**</span><span class="sxs-lookup"><span data-stu-id="91f09-137">**21**</span></span>
</dt> <dd>

<span data-ttu-id="91f09-138">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="91f09-138">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="91f09-139">範例</span><span class="sxs-lookup"><span data-stu-id="91f09-139">Examples</span></span>

<span data-ttu-id="91f09-140">下列 Visual Basic 腳本程式碼會呼叫 [**TakeOwnerShip**](takeownership-method-in-class-cim-directory.md) 方法來取得 C： temp 資料夾的擁有權 \\ 。</span><span class="sxs-lookup"><span data-stu-id="91f09-140">The following Visual Basic Script code calls the [**TakeOwnerShip**](takeownership-method-in-class-cim-directory.md) method to take ownership of the C:\\temp folder.</span></span>


```VB
strComputer = "." 

Set objWMIService = _
    GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 

' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod( _
    "Win32_Directory.Name='C:\\temp'", "TakeOwnerShip")

wscript.echo objOutParams.ReturnValue
```



## <a name="requirements"></a><span data-ttu-id="91f09-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="91f09-141">Requirements</span></span>



| <span data-ttu-id="91f09-142">需求</span><span class="sxs-lookup"><span data-stu-id="91f09-142">Requirement</span></span> | <span data-ttu-id="91f09-143">值</span><span class="sxs-lookup"><span data-stu-id="91f09-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91f09-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="91f09-144">Minimum supported client</span></span><br/> | <span data-ttu-id="91f09-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="91f09-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="91f09-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="91f09-146">Minimum supported server</span></span><br/> | <span data-ttu-id="91f09-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="91f09-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="91f09-148">命名空間</span><span class="sxs-lookup"><span data-stu-id="91f09-148">Namespace</span></span><br/>                | <span data-ttu-id="91f09-149">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="91f09-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="91f09-150">MOF</span><span class="sxs-lookup"><span data-stu-id="91f09-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="91f09-151"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="91f09-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="91f09-152">DLL</span><span class="sxs-lookup"><span data-stu-id="91f09-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91f09-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91f09-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91f09-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91f09-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="91f09-155">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="91f09-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="91f09-156">**Win32 \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="91f09-156">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

