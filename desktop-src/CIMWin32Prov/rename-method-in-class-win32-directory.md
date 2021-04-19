---
description: 重新命名物件路徑中指定的目錄專案檔。
ms.assetid: 8bfe1b69-5f93-4408-a742-f03a9cb16bfe
ms.tgt_platform: multiple
title: Win32_Directory 類別的重新命名方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 874151e1ff8c9feca375df3eb441665863d1070d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973561"
---
# <a name="rename-method-of-the-win32_directory-class"></a><span data-ttu-id="5d099-103">Win32 目錄類別的重新命名方法 \_</span><span class="sxs-lookup"><span data-stu-id="5d099-103">Rename method of the Win32\_Directory class</span></span>

<span data-ttu-id="5d099-104">**重新命名** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會重新命名物件路徑中指定的目錄專案檔。</span><span class="sxs-lookup"><span data-stu-id="5d099-104">The **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renames the directory entry file specified in the object path.</span></span> <span data-ttu-id="5d099-105">如果目的地是在另一個磁片磁碟機上，或需要覆寫現有的邏輯檔案，則不支援重新命名。</span><span class="sxs-lookup"><span data-stu-id="5d099-105">A rename is not supported if the destination is on another drive or if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="5d099-106">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="5d099-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5d099-107">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="5d099-107">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5d099-108">語法</span><span class="sxs-lookup"><span data-stu-id="5d099-108">Syntax</span></span>


```mof
uint32 Rename(
   string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="5d099-109">參數</span><span class="sxs-lookup"><span data-stu-id="5d099-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d099-110">*FileName*</span><span class="sxs-lookup"><span data-stu-id="5d099-110">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="5d099-111">檔案 (或目錄) 的完整新名稱。</span><span class="sxs-lookup"><span data-stu-id="5d099-111">Fully qualified new name of the file (or directory).</span></span> <span data-ttu-id="5d099-112">範例： c： \\ temp \\newfile.txt。</span><span class="sxs-lookup"><span data-stu-id="5d099-112">Example: c:\\temp\\newfile.txt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d099-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5d099-113">Return value</span></span>

<span data-ttu-id="5d099-114">如果成功重新命名檔案，則傳回值為 0 (零) ，以及表示錯誤的其他任何數位。</span><span class="sxs-lookup"><span data-stu-id="5d099-114">Returns a value of 0 (zero) if the file was successfully renamed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="5d099-115">**0**</span><span class="sxs-lookup"><span data-stu-id="5d099-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="5d099-116">要求成功。</span><span class="sxs-lookup"><span data-stu-id="5d099-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="5d099-117">**2**</span><span class="sxs-lookup"><span data-stu-id="5d099-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="5d099-118">存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="5d099-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="5d099-119">**8**</span><span class="sxs-lookup"><span data-stu-id="5d099-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="5d099-120">發生未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="5d099-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="5d099-121">**9**</span><span class="sxs-lookup"><span data-stu-id="5d099-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="5d099-122">指定的名稱無效。</span><span class="sxs-lookup"><span data-stu-id="5d099-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5d099-123">**10**</span><span class="sxs-lookup"><span data-stu-id="5d099-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="5d099-124">指定的物件已經存在。</span><span class="sxs-lookup"><span data-stu-id="5d099-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="5d099-125">**11**</span><span class="sxs-lookup"><span data-stu-id="5d099-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="5d099-126">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="5d099-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="5d099-127">**12**</span><span class="sxs-lookup"><span data-stu-id="5d099-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="5d099-128">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="5d099-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="5d099-129">**13**</span><span class="sxs-lookup"><span data-stu-id="5d099-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="5d099-130">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="5d099-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="5d099-131">**14**</span><span class="sxs-lookup"><span data-stu-id="5d099-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="5d099-132">目錄不是空的。</span><span class="sxs-lookup"><span data-stu-id="5d099-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="5d099-133">**15**</span><span class="sxs-lookup"><span data-stu-id="5d099-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="5d099-134">發生共用違規。</span><span class="sxs-lookup"><span data-stu-id="5d099-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="5d099-135">**16**</span><span class="sxs-lookup"><span data-stu-id="5d099-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="5d099-136">指定的起始檔無效。</span><span class="sxs-lookup"><span data-stu-id="5d099-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5d099-137">**17**</span><span class="sxs-lookup"><span data-stu-id="5d099-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="5d099-138">不會保留操作所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="5d099-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="5d099-139">**21**</span><span class="sxs-lookup"><span data-stu-id="5d099-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="5d099-140">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="5d099-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d099-141">備註</span><span class="sxs-lookup"><span data-stu-id="5d099-141">Remarks</span></span>

<span data-ttu-id="5d099-142">若要重新命名資料夾，請先系結至有問題的資料夾，然後呼叫重新命名方法。</span><span class="sxs-lookup"><span data-stu-id="5d099-142">To rename a folder, first bind to the folder in question and then call the Rename method.</span></span> <span data-ttu-id="5d099-143">作為方法的唯一參數，以完整路徑名稱傳遞資料夾的新名稱。</span><span class="sxs-lookup"><span data-stu-id="5d099-143">As the sole parameter to the method, pass the new name for the folder as a complete path name.</span></span> <span data-ttu-id="5d099-144">例如，如果 C： script 記錄備份中的 \\ 資料夾 \\ 要重新命名為 \\ c： \\ scripts \\ Archive，您必須傳遞 c： script \\ \\ archive 作為完整的資料夾名稱。</span><span class="sxs-lookup"><span data-stu-id="5d099-144">For example, if the folder in the C:\\Scripts\\Logs\\Backup is to be renamed C:\\Scripts\\Archive, you must pass C:\\Scripts\\Archive as the complete folder name.</span></span> <span data-ttu-id="5d099-145">只傳遞資料夾名稱-封存-會導致不正確路徑錯誤。</span><span class="sxs-lookup"><span data-stu-id="5d099-145">Passing only the folder name - Archive - results in an Invalid path error.</span></span>

<span data-ttu-id="5d099-146">Win32 \_ 目錄類別不提供移動資料夾的逐步方法。</span><span class="sxs-lookup"><span data-stu-id="5d099-146">The Win32\_Directory class does not provide a one-step method for moving folders.</span></span> <span data-ttu-id="5d099-147">相反地，移動資料夾通常包含兩個步驟：</span><span class="sxs-lookup"><span data-stu-id="5d099-147">Instead, moving a folder generally involves two steps:</span></span>

<dl> 1. <span data-ttu-id="5d099-148">將資料夾複製到新位置</span><span class="sxs-lookup"><span data-stu-id="5d099-148">Copying the folder to its new location</span></span>  
2. <span data-ttu-id="5d099-149">正在刪除原始檔案夾</span><span class="sxs-lookup"><span data-stu-id="5d099-149">Deleting the original folder</span></span>  
</dl>

<span data-ttu-id="5d099-150">這項雙步驟程式的唯一例外，就是將資料夾移至相同磁片磁碟機上的新位置。</span><span class="sxs-lookup"><span data-stu-id="5d099-150">The one exception to this two-step process involves moving a folder to a new location on the same drive.</span></span> <span data-ttu-id="5d099-151">例如，假設您想要將 C： \\ Temp 移至 c： \\ 編寫 \\ 暫存檔案封存 \\ 的腳本。</span><span class="sxs-lookup"><span data-stu-id="5d099-151">For example, suppose you want to move C:\\Temp to C:\\Scripts\\Temporary Files\\Archive.</span></span> <span data-ttu-id="5d099-152">只要目前的位置和新的位置都在相同的磁片磁碟機上，只要呼叫 Rename 方法並傳遞新的位置做為方法參數，就可以移動資料夾。</span><span class="sxs-lookup"><span data-stu-id="5d099-152">As long as the current location and the new location are on the same drive, you can move the folder by simply calling the Rename method and passing the new location as the method parameter.</span></span> <span data-ttu-id="5d099-153">這種方法可以有效地讓您在單一步驟中移動資料夾。</span><span class="sxs-lookup"><span data-stu-id="5d099-153">This approach effectively allows you to move the folder in a single step.</span></span> <span data-ttu-id="5d099-154">但是，如果目前磁片磁碟機和新磁片磁碟機不同，腳本就會失敗。</span><span class="sxs-lookup"><span data-stu-id="5d099-154">However, the script fails if the current drive and the new drive are different.</span></span> <span data-ttu-id="5d099-155">嘗試將 C： temp 重新命名 \\ 為 D： \\ temp 失敗，並出現「磁片磁碟機不相同」錯誤。</span><span class="sxs-lookup"><span data-stu-id="5d099-155">An attempt to rename C:\\Temp to D:\\Temp fails with a "Drive not the same" error.</span></span>

## <a name="examples"></a><span data-ttu-id="5d099-156">範例</span><span class="sxs-lookup"><span data-stu-id="5d099-156">Examples</span></span>

<span data-ttu-id="5d099-157">下列程式碼會從 TechNet 資源庫上 [使用 WMI VBScript 範例移動資料夾](https://Gallery.TechNet.Microsoft.Com/f4f9643c-d7ed-4f54-b155-c6515396431f) ，使用重新命名方法將資料夾 c： \\ 腳本移至 c： \\ Admins 檔封存 \\ \\ \\ VBScript。</span><span class="sxs-lookup"><span data-stu-id="5d099-157">The following code, from the [Move a Folder Using WMI](https://Gallery.TechNet.Microsoft.Com/f4f9643c-d7ed-4f54-b155-c6515396431f) VBScript sample on TechNet Gallery, uses the Rename method to move the folder C:\\Scripts to C:\\Admins\\Documents\\Archive\\VBScript.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colFolders = objWMIService.ExecQuery _ 
    ("Select * from Win32_Directory where name = 'c:\\Scripts'") 
 
For Each objFolder in colFolders 
    errResults = objFolder.Rename("C:\Admins\Documents\Archive\VBScript") 
Next
```



## <a name="requirements"></a><span data-ttu-id="5d099-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d099-158">Requirements</span></span>



| <span data-ttu-id="5d099-159">需求</span><span class="sxs-lookup"><span data-stu-id="5d099-159">Requirement</span></span> | <span data-ttu-id="5d099-160">值</span><span class="sxs-lookup"><span data-stu-id="5d099-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d099-161">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5d099-161">Minimum supported client</span></span><br/> | <span data-ttu-id="5d099-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5d099-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5d099-163">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5d099-163">Minimum supported server</span></span><br/> | <span data-ttu-id="5d099-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5d099-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5d099-165">命名空間</span><span class="sxs-lookup"><span data-stu-id="5d099-165">Namespace</span></span><br/>                | <span data-ttu-id="5d099-166">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5d099-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5d099-167">MOF</span><span class="sxs-lookup"><span data-stu-id="5d099-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d099-168"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="5d099-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5d099-169">DLL</span><span class="sxs-lookup"><span data-stu-id="5d099-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d099-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d099-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d099-171">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d099-171">See also</span></span>

<dl> <dt>

<span data-ttu-id="5d099-172">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5d099-172">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5d099-173">**Win32 \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="5d099-173">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

