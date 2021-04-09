---
description: 將物件路徑中指定的邏輯目錄專案檔或目錄複寫到輸入參數所指定的位置。
ms.assetid: 038e23d7-71db-4db6-8fb1-e84e972510c9
ms.tgt_platform: multiple
title: Win32_Directory 類別的 Copy 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 25568167d9532303a7cbee794757bc674a378b39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110808"
---
# <a name="copy-method-of-the-win32_directory-class"></a><span data-ttu-id="f1631-103">Win32 目錄類別的 Copy 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f1631-103">Copy method of the Win32\_Directory class</span></span>

<span data-ttu-id="f1631-104">**複製** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會將物件路徑中指定的邏輯目錄專案檔或目錄複寫到輸入參數所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="f1631-104">The **Copy** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method copies the logical directory entry file or directory specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="f1631-105">如果需要覆寫現有的邏輯檔案，則不支援複製。</span><span class="sxs-lookup"><span data-stu-id="f1631-105">A copy is not supported if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="f1631-106">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="f1631-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f1631-107">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="f1631-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f1631-108">語法</span><span class="sxs-lookup"><span data-stu-id="f1631-108">Syntax</span></span>


```mof
uint32 Copy(
   string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="f1631-109">參數</span><span class="sxs-lookup"><span data-stu-id="f1631-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1631-110">*FileName*</span><span class="sxs-lookup"><span data-stu-id="f1631-110">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="f1631-111"> (或目錄) 之檔案複本的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="f1631-111">Fully qualified name of the copy of the file (or directory).</span></span> <span data-ttu-id="f1631-112">範例： c： \\ temp \\ newdirectory</span><span class="sxs-lookup"><span data-stu-id="f1631-112">Example: c:\\temp\\newdirectory</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1631-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f1631-113">Return value</span></span>

<span data-ttu-id="f1631-114">如果成功複製檔案，則傳回 0 (零) 的值，以及表示錯誤的其他任何數位。</span><span class="sxs-lookup"><span data-stu-id="f1631-114">Returns a value of 0 (zero) if the file was successfully copied, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="f1631-115">**0**</span><span class="sxs-lookup"><span data-stu-id="f1631-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="f1631-116">要求成功。</span><span class="sxs-lookup"><span data-stu-id="f1631-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="f1631-117">**2**</span><span class="sxs-lookup"><span data-stu-id="f1631-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="f1631-118">存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="f1631-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="f1631-119">**8**</span><span class="sxs-lookup"><span data-stu-id="f1631-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="f1631-120">發生未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="f1631-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="f1631-121">**9**</span><span class="sxs-lookup"><span data-stu-id="f1631-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="f1631-122">指定的名稱無效。</span><span class="sxs-lookup"><span data-stu-id="f1631-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f1631-123">**10**</span><span class="sxs-lookup"><span data-stu-id="f1631-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="f1631-124">指定的物件已經存在。</span><span class="sxs-lookup"><span data-stu-id="f1631-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f1631-125">**11**</span><span class="sxs-lookup"><span data-stu-id="f1631-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="f1631-126">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="f1631-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="f1631-127">**12**</span><span class="sxs-lookup"><span data-stu-id="f1631-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="f1631-128">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="f1631-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="f1631-129">**13**</span><span class="sxs-lookup"><span data-stu-id="f1631-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="f1631-130">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="f1631-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="f1631-131">**14**</span><span class="sxs-lookup"><span data-stu-id="f1631-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="f1631-132">目錄不是空的。</span><span class="sxs-lookup"><span data-stu-id="f1631-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="f1631-133">**15**</span><span class="sxs-lookup"><span data-stu-id="f1631-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="f1631-134">發生共用違規。</span><span class="sxs-lookup"><span data-stu-id="f1631-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="f1631-135">**16**</span><span class="sxs-lookup"><span data-stu-id="f1631-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="f1631-136">指定的起始檔無效。</span><span class="sxs-lookup"><span data-stu-id="f1631-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f1631-137">**17**</span><span class="sxs-lookup"><span data-stu-id="f1631-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="f1631-138">不會保留操作所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="f1631-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="f1631-139">**21**</span><span class="sxs-lookup"><span data-stu-id="f1631-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="f1631-140">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="f1631-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1631-141">備註</span><span class="sxs-lookup"><span data-stu-id="f1631-141">Remarks</span></span>

<span data-ttu-id="f1631-142">資料夾通常需要從一個位置複製到另一個位置。</span><span class="sxs-lookup"><span data-stu-id="f1631-142">Folders often need to be copied from one location to another.</span></span> <span data-ttu-id="f1631-143">例如，您可以將資料夾從一部伺服器複製到另一部伺服器，以建立該資料夾的備份複本。</span><span class="sxs-lookup"><span data-stu-id="f1631-143">For example, you might copy a folder from one server to another to create a backup copy of that folder.</span></span> <span data-ttu-id="f1631-144">或者，您可能會有需要複製到使用者工作站的 [範本] 資料夾，或是應該複製到所有 DNS 伺服器的 [腳本] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="f1631-144">Or you might have a templates folder that needs to be copied to user workstations, or a scripts folder that should be copied to all of your DNS servers.</span></span>

<span data-ttu-id="f1631-145">Win32 \_ 目錄複寫方法可讓您在同一部 (電腦上將資料夾從一個位置複製到另一個位置，例如，將資料夾從磁片磁碟機 C 複製到磁片磁碟機 D) 或在遠端電腦上。</span><span class="sxs-lookup"><span data-stu-id="f1631-145">The Win32\_Directory Copy method enables you to copy a folder from one location to another, either on the same computer (for example, copying a folder from drive C to drive D) or on a remote computer.</span></span> <span data-ttu-id="f1631-146">若要複製資料夾，您可以傳回要複製之資料夾的實例，然後呼叫 Copy 方法，以參數的方式傳遞新資料夾複本的目標位置。</span><span class="sxs-lookup"><span data-stu-id="f1631-146">To copy a folder, you return an instance of the folder to be copied and then call the Copy method, passing as a parameter the target location for the new copy of the folder.</span></span> <span data-ttu-id="f1631-147">例如，這行程式碼會將資料夾複製到磁片磁碟機 F 上的 Scripts 資料夾：</span><span class="sxs-lookup"><span data-stu-id="f1631-147">For example, this line of code copies a folder to the Scripts folder on drive F:</span></span>

`objFolder.Copy("F:\Scripts")`

<span data-ttu-id="f1631-148">執行複製方法時，WMI 不會覆寫現有的資料夾。</span><span class="sxs-lookup"><span data-stu-id="f1631-148">WMI will not overwrite an existing folder when executing the Copy method.</span></span> <span data-ttu-id="f1631-149">這表示，如果目的地資料夾存在，則複製作業會失敗。</span><span class="sxs-lookup"><span data-stu-id="f1631-149">This means that the copy operation fails if the destination folder exists.</span></span> <span data-ttu-id="f1631-150">例如，假設您有一個名為 Scripts 的資料夾，而且您嘗試將該資料夾複製到名為「 \\ \\ atl-fs-01 封存」的遠端共用 \\ 。</span><span class="sxs-lookup"><span data-stu-id="f1631-150">For example, suppose you have a folder named Scripts and you attempt to copy that folder to a remote share named \\\\atl-fs-01\\archive.</span></span> <span data-ttu-id="f1631-151">如果該共用上已有名稱為 Scripts 的資料夾，複製作業會失敗。</span><span class="sxs-lookup"><span data-stu-id="f1631-151">If a folder named Scripts already exists on that share, the copy operation fails.</span></span>

## <a name="examples"></a><span data-ttu-id="f1631-152">範例</span><span class="sxs-lookup"><span data-stu-id="f1631-152">Examples</span></span>

<span data-ttu-id="f1631-153">從 [使用 WMI 複製資料夾](https://Gallery.TechNet.Microsoft.Com/71b8f517-0240-42a2-be5c-e5a3921604d2)中取得的下列程式碼範例會使用複製方法，將資料夾 C： \\ 腳本複製到 D： \\ Archive。</span><span class="sxs-lookup"><span data-stu-id="f1631-153">The followng code sample, taken from the [Copy a Folder Using WMI](https://Gallery.TechNet.Microsoft.Com/71b8f517-0240-42a2-be5c-e5a3921604d2), uses the Copy method to copy the folder C:\\Scripts to D:\\Archive.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colFolders = objWMIService.ExecQuery( _ 
    "Select * from Win32_Directory where Name = 'c:\\Scripts'") 
 
For Each objFolder in colFolders 
    errResults  = objFolder.Copy("D:\Archive") 
Next
```



## <a name="requirements"></a><span data-ttu-id="f1631-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1631-154">Requirements</span></span>



| <span data-ttu-id="f1631-155">需求</span><span class="sxs-lookup"><span data-stu-id="f1631-155">Requirement</span></span> | <span data-ttu-id="f1631-156">值</span><span class="sxs-lookup"><span data-stu-id="f1631-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1631-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1631-157">Minimum supported client</span></span><br/> | <span data-ttu-id="f1631-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f1631-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f1631-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1631-159">Minimum supported server</span></span><br/> | <span data-ttu-id="f1631-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1631-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f1631-161">命名空間</span><span class="sxs-lookup"><span data-stu-id="f1631-161">Namespace</span></span><br/>                | <span data-ttu-id="f1631-162">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f1631-162">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f1631-163">MOF</span><span class="sxs-lookup"><span data-stu-id="f1631-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1631-164"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1631-164"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1631-165">DLL</span><span class="sxs-lookup"><span data-stu-id="f1631-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1631-166"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1631-166"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1631-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1631-167">See also</span></span>

<dl> <dt>

<span data-ttu-id="f1631-168">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f1631-168">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f1631-169">**Win32 \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="f1631-169">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

