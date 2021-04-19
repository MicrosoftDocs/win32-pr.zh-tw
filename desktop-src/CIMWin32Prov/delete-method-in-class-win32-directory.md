---
description: Delete WMI 類別方法會刪除物件路徑中指定的邏輯檔案 (或目錄) 。
ms.assetid: 5663b8a8-3089-475b-8a36-454a7315bfca
ms.tgt_platform: multiple
title: Win32_Directory 類別的 Delete 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 843583698c11c1b9ad8f08e83aa6e4b894b55db8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970938"
---
# <a name="delete-method-of-the-win32_directory-class"></a><span data-ttu-id="4767b-103">Win32 目錄類別的 Delete 方法 \_</span><span class="sxs-lookup"><span data-stu-id="4767b-103">Delete method of the Win32\_Directory class</span></span>

<span data-ttu-id="4767b-104">**Delete** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會刪除物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="4767b-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method will delete the logical file (or directory) specified in the object path.</span></span>

<span data-ttu-id="4767b-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="4767b-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4767b-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="4767b-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4767b-107">語法</span><span class="sxs-lookup"><span data-stu-id="4767b-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="4767b-108">參數</span><span class="sxs-lookup"><span data-stu-id="4767b-108">Parameters</span></span>

<span data-ttu-id="4767b-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="4767b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4767b-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="4767b-110">Return value</span></span>

<span data-ttu-id="4767b-111">如果成功刪除檔案，則傳回值為 0 (零) ，以及表示錯誤的其他任何數位。</span><span class="sxs-lookup"><span data-stu-id="4767b-111">Returns a value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="4767b-112">**0**</span><span class="sxs-lookup"><span data-stu-id="4767b-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="4767b-113">要求成功。</span><span class="sxs-lookup"><span data-stu-id="4767b-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="4767b-114">**2**</span><span class="sxs-lookup"><span data-stu-id="4767b-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="4767b-115">存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="4767b-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="4767b-116">**8**</span><span class="sxs-lookup"><span data-stu-id="4767b-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="4767b-117">發生未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="4767b-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="4767b-118">**9**</span><span class="sxs-lookup"><span data-stu-id="4767b-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="4767b-119">指定的名稱無效。</span><span class="sxs-lookup"><span data-stu-id="4767b-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="4767b-120">**10**</span><span class="sxs-lookup"><span data-stu-id="4767b-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="4767b-121">指定的物件已經存在。</span><span class="sxs-lookup"><span data-stu-id="4767b-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="4767b-122">**11**</span><span class="sxs-lookup"><span data-stu-id="4767b-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="4767b-123">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="4767b-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="4767b-124">**12**</span><span class="sxs-lookup"><span data-stu-id="4767b-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="4767b-125">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="4767b-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="4767b-126">**13**</span><span class="sxs-lookup"><span data-stu-id="4767b-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="4767b-127">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="4767b-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="4767b-128">**14**</span><span class="sxs-lookup"><span data-stu-id="4767b-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="4767b-129">目錄不是空的。</span><span class="sxs-lookup"><span data-stu-id="4767b-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="4767b-130">**15**</span><span class="sxs-lookup"><span data-stu-id="4767b-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="4767b-131">發生共用違規。</span><span class="sxs-lookup"><span data-stu-id="4767b-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="4767b-132">**16**</span><span class="sxs-lookup"><span data-stu-id="4767b-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="4767b-133">指定的起始檔無效。</span><span class="sxs-lookup"><span data-stu-id="4767b-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="4767b-134">**17**</span><span class="sxs-lookup"><span data-stu-id="4767b-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="4767b-135">不會保留操作所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="4767b-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="4767b-136">**21**</span><span class="sxs-lookup"><span data-stu-id="4767b-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="4767b-137">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="4767b-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4767b-138">備註</span><span class="sxs-lookup"><span data-stu-id="4767b-138">Remarks</span></span>

<span data-ttu-id="4767b-139">資料夾不一定是檔案系統的永久新增專案。</span><span class="sxs-lookup"><span data-stu-id="4767b-139">Folders are not necessarily permanent additions to a file system.</span></span> <span data-ttu-id="4767b-140">在某個時間點，可能需要刪除資料夾，可能是因為已不再需要資料夾，因為電腦的角色已變更，或因為錯誤地建立資料夾。</span><span class="sxs-lookup"><span data-stu-id="4767b-140">At some point, folders might need to be deleted, perhaps because they are no longer required, because the role of the computer has changed, or because the folders were created by mistake.</span></span>

<span data-ttu-id="4767b-141">刪除可讓您刪除資料夾：您只需系結至有問題的資料夾，然後呼叫 Delete 方法。</span><span class="sxs-lookup"><span data-stu-id="4767b-141">Delete allows you to delete folders: you simply bind to the folder in question and then call the Delete method.</span></span> <span data-ttu-id="4767b-142">呼叫 Delete 方法之後，就會從檔案系統中永久移除資料夾;它不會傳送至資源回收筒。</span><span class="sxs-lookup"><span data-stu-id="4767b-142">After the Delete method is called, the folder is permanently removed from the file system; it is not sent to the Recycle Bin.</span></span> <span data-ttu-id="4767b-143">此外，也不會有確認通知 ( 「您確定要刪除此資料夾嗎？」發出 ) 。</span><span class="sxs-lookup"><span data-stu-id="4767b-143">In addition, no confirmation notice ("Are you sure you want to delete this folder?") is issued.</span></span> <span data-ttu-id="4767b-144">相反地，會立即移除資料夾。</span><span class="sxs-lookup"><span data-stu-id="4767b-144">Instead, the folder is immediately removed.</span></span>

<span data-ttu-id="4767b-145">您無法使用 FileSystemObject 刪除唯讀資料夾;不過，這可以使用 WMI 來完成。</span><span class="sxs-lookup"><span data-stu-id="4767b-145">You cannot delete read-only folders using the FileSystemObject; however, this can be done using WMI.</span></span> <span data-ttu-id="4767b-146">如果您的腳本使用 WMI，而您不想要移除唯讀資料夾，您必須先使用 [可讀取] 屬性來檢查資料夾狀態，再加以刪除。</span><span class="sxs-lookup"><span data-stu-id="4767b-146">If your script uses WMI and you do not want to remove a read-only folder, you must use the Readable property to check the folder status before deleting it.</span></span>

## <a name="examples"></a><span data-ttu-id="4767b-147">範例</span><span class="sxs-lookup"><span data-stu-id="4767b-147">Examples</span></span>

<span data-ttu-id="4767b-148">下列 VBScript 程式碼範例會刪除資料夾 C： \\ 腳本。</span><span class="sxs-lookup"><span data-stu-id="4767b-148">The following VBScript code sample deletes the folder C:\\Scripts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 errResults = objFolder.Delete
 Wscript.Echo errResults
Next
```



## <a name="requirements"></a><span data-ttu-id="4767b-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="4767b-149">Requirements</span></span>



| <span data-ttu-id="4767b-150">需求</span><span class="sxs-lookup"><span data-stu-id="4767b-150">Requirement</span></span> | <span data-ttu-id="4767b-151">值</span><span class="sxs-lookup"><span data-stu-id="4767b-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4767b-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4767b-152">Minimum supported client</span></span><br/> | <span data-ttu-id="4767b-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4767b-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4767b-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4767b-154">Minimum supported server</span></span><br/> | <span data-ttu-id="4767b-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4767b-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4767b-156">命名空間</span><span class="sxs-lookup"><span data-stu-id="4767b-156">Namespace</span></span><br/>                | <span data-ttu-id="4767b-157">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4767b-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4767b-158">MOF</span><span class="sxs-lookup"><span data-stu-id="4767b-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4767b-159"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="4767b-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4767b-160">DLL</span><span class="sxs-lookup"><span data-stu-id="4767b-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4767b-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4767b-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4767b-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4767b-162">See also</span></span>

<dl> <dt>

<span data-ttu-id="4767b-163">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4767b-163">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4767b-164">**Win32 \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="4767b-164">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

