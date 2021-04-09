---
description: 壓縮物件路徑中指定 (或目錄) 的邏輯目錄專案檔。
ms.assetid: 4db13622-75c5-45db-8536-451059c0e477
ms.tgt_platform: multiple
title: 壓縮 Win32_Directory 類別的方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ea694c09e11e5801016a4ea85b9774448c542991
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110245"
---
# <a name="compress-method-of-the-win32_directory-class"></a><span data-ttu-id="62c71-103">壓縮 Win32 \_ 目錄類別的方法</span><span class="sxs-lookup"><span data-stu-id="62c71-103">Compress method of the Win32\_Directory class</span></span>

<span data-ttu-id="62c71-104">**壓縮** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會將邏輯目錄專案檔壓縮 (或在物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="62c71-104">The **Compress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical directory entry file (or directory) specified in the object path.</span></span>

<span data-ttu-id="62c71-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="62c71-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="62c71-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="62c71-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="62c71-107">語法</span><span class="sxs-lookup"><span data-stu-id="62c71-107">Syntax</span></span>


```mof
uint32 Compress();
```



## <a name="parameters"></a><span data-ttu-id="62c71-108">參數</span><span class="sxs-lookup"><span data-stu-id="62c71-108">Parameters</span></span>

<span data-ttu-id="62c71-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="62c71-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="62c71-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="62c71-110">Return value</span></span>

<span data-ttu-id="62c71-111">傳回值 0 (零) 如果檔案已成功壓縮，則為，而任何其他數位表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="62c71-111">Returns a value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="62c71-112">**0**</span><span class="sxs-lookup"><span data-stu-id="62c71-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="62c71-113">要求成功。</span><span class="sxs-lookup"><span data-stu-id="62c71-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="62c71-114">**2**</span><span class="sxs-lookup"><span data-stu-id="62c71-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="62c71-115">存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="62c71-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="62c71-116">**8**</span><span class="sxs-lookup"><span data-stu-id="62c71-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="62c71-117">發生未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="62c71-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="62c71-118">**9**</span><span class="sxs-lookup"><span data-stu-id="62c71-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="62c71-119">指定的名稱無效。</span><span class="sxs-lookup"><span data-stu-id="62c71-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="62c71-120">**10**</span><span class="sxs-lookup"><span data-stu-id="62c71-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="62c71-121">指定的物件已經存在。</span><span class="sxs-lookup"><span data-stu-id="62c71-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="62c71-122">**11**</span><span class="sxs-lookup"><span data-stu-id="62c71-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="62c71-123">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="62c71-123">The file system is not an NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="62c71-124">**12**</span><span class="sxs-lookup"><span data-stu-id="62c71-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="62c71-125">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="62c71-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="62c71-126">**13**</span><span class="sxs-lookup"><span data-stu-id="62c71-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="62c71-127">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="62c71-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="62c71-128">**14**</span><span class="sxs-lookup"><span data-stu-id="62c71-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="62c71-129">目錄不是空的。</span><span class="sxs-lookup"><span data-stu-id="62c71-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="62c71-130">**15**</span><span class="sxs-lookup"><span data-stu-id="62c71-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="62c71-131">發生共用違規。</span><span class="sxs-lookup"><span data-stu-id="62c71-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="62c71-132">**16**</span><span class="sxs-lookup"><span data-stu-id="62c71-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="62c71-133">指定的起始檔無效。</span><span class="sxs-lookup"><span data-stu-id="62c71-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="62c71-134">**17**</span><span class="sxs-lookup"><span data-stu-id="62c71-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="62c71-135">不會保留操作所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="62c71-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="62c71-136">**21**</span><span class="sxs-lookup"><span data-stu-id="62c71-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="62c71-137">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="62c71-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="62c71-138">備註</span><span class="sxs-lookup"><span data-stu-id="62c71-138">Remarks</span></span>

<span data-ttu-id="62c71-139">壓縮提供一種方法來釋出磁片磁碟機上的額外儲存空間，而不需要購買新硬體，也不需要移除檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="62c71-139">Compression provides a way to free additional storage space on a disk drive without purchasing new hardware and without removing files or folders.</span></span> <span data-ttu-id="62c71-140">根據硬碟的大小以及儲存在該磁片上的檔案類型而定，您或許可以復原數百 mb 的磁碟空間，因此不需要購買新的硬碟，也不需要在安裝新磁片磁碟機的情況下讓電腦離線。</span><span class="sxs-lookup"><span data-stu-id="62c71-140">Depending on the size of your hard disk and the type of files stored on that disk, you might be able to recover hundreds of megabytes of disk space and thus preclude the need to purchase a new hard drive and to take the computer offline until the new drive is installed.</span></span>

<span data-ttu-id="62c71-141">壓縮方法會壓縮指定資料夾內的所有檔案和子資料夾。</span><span class="sxs-lookup"><span data-stu-id="62c71-141">The Compress method compresses all the files and subfolders within a specified folder.</span></span> <span data-ttu-id="62c71-142">此外，此類別也包含可從資料夾中的所有檔案和子資料夾中移除壓縮的解壓縮方法。</span><span class="sxs-lookup"><span data-stu-id="62c71-142">In addition, the class also includes an Uncompress method that removes compression from all the files and subfolders in a folder.</span></span> <span data-ttu-id="62c71-143">CIM 資料檔案類別也會提供類似的方法 \_ 。</span><span class="sxs-lookup"><span data-stu-id="62c71-143">Similar methods are also provided with the CIM\_Datafile class.</span></span> <span data-ttu-id="62c71-144">這可讓您選擇性地壓縮或解壓縮資料夾中的特定檔案。</span><span class="sxs-lookup"><span data-stu-id="62c71-144">This allows you to selectively compress or uncompress specific files within a folder.</span></span>

<span data-ttu-id="62c71-145">由於壓縮 imparts 效能會稍微降低，因此不建議針對例行存取的檔案或資料夾進行存取;例如，您可能不想要壓縮資料庫檔案、記錄檔或使用者設定檔資料夾。</span><span class="sxs-lookup"><span data-stu-id="62c71-145">Because compression imparts a slight performance penalty, it is not recommended for files or folders that are accessed on a routine basis; for example, you probably do not want to compress database files, log files, or user profile folders.</span></span> <span data-ttu-id="62c71-146">更好的壓縮候選項目為不常存取的檔案和資料夾。</span><span class="sxs-lookup"><span data-stu-id="62c71-146">Better candidates for compression are files and folders that are not accessed very often.</span></span> <span data-ttu-id="62c71-147">例如，您可以撰寫腳本，以傳回一或多個月未存取之磁片磁碟機上的資料夾集合，然後壓縮每個資料夾。</span><span class="sxs-lookup"><span data-stu-id="62c71-147">For example, you might write a script to return a collection of folders on a drive that have not been accessed for a month or more and then compress each of those folders.</span></span>

<span data-ttu-id="62c71-148">壓縮資料夾所釋出的磁碟空間量會根據儲存在該資料夾中的檔案類型而有所不同。</span><span class="sxs-lookup"><span data-stu-id="62c71-148">The amount of disk space freed by compressing folders varies depending on the type of files stored in that folder.</span></span> <span data-ttu-id="62c71-149">例如，.jpg 檔案已經過壓縮，而進一步的壓縮對檔案的大小沒有太大的影響。</span><span class="sxs-lookup"><span data-stu-id="62c71-149">For example, .jpg files are already compressed, and further compression has little effect on the size of the file.</span></span> <span data-ttu-id="62c71-150">不過，其他檔案類型的節省量可能很可觀。</span><span class="sxs-lookup"><span data-stu-id="62c71-150">With other file types, however, the savings can be considerable.</span></span> <span data-ttu-id="62c71-151">例如，在 Windows 2000 測試電腦上建立新的資料夾，和 33 Microsoft Word 檔，總共占滿 15 mb 的磁碟空間 (MB) ，已複製到該資料夾。</span><span class="sxs-lookup"><span data-stu-id="62c71-151">For example, a new folder was created on a Windows 2000-based test computer, and 33 Microsoft Word documents, taking up a total of 15 megabytes (MB) of disk space, were copied into that folder.</span></span> <span data-ttu-id="62c71-152">壓縮檔時，資料夾只佔用 7 MB 的磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="62c71-152">When the documents were compressed, the folder took up only 7 MB of disk space.</span></span>

## <a name="examples"></a><span data-ttu-id="62c71-153">範例</span><span class="sxs-lookup"><span data-stu-id="62c71-153">Examples</span></span>

<span data-ttu-id="62c71-154">下列 VBScript 範例會壓縮資料夾 C： \\ 腳本。</span><span class="sxs-lookup"><span data-stu-id="62c71-154">The following VBScript sample compresses the folder C:\\Scripts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 errResults = objFolder.Compress
 Wscript.Echo errResults
Next
```



## <a name="requirements"></a><span data-ttu-id="62c71-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="62c71-155">Requirements</span></span>



| <span data-ttu-id="62c71-156">需求</span><span class="sxs-lookup"><span data-stu-id="62c71-156">Requirement</span></span> | <span data-ttu-id="62c71-157">值</span><span class="sxs-lookup"><span data-stu-id="62c71-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62c71-158">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="62c71-158">Minimum supported client</span></span><br/> | <span data-ttu-id="62c71-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62c71-159">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="62c71-160">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="62c71-160">Minimum supported server</span></span><br/> | <span data-ttu-id="62c71-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62c71-161">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="62c71-162">命名空間</span><span class="sxs-lookup"><span data-stu-id="62c71-162">Namespace</span></span><br/>                | <span data-ttu-id="62c71-163">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="62c71-163">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="62c71-164">MOF</span><span class="sxs-lookup"><span data-stu-id="62c71-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62c71-165"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="62c71-165"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="62c71-166">DLL</span><span class="sxs-lookup"><span data-stu-id="62c71-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62c71-167"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62c71-167"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62c71-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62c71-168">See also</span></span>

<dl> <dt>

<span data-ttu-id="62c71-169">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="62c71-169">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="62c71-170">**Win32 \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="62c71-170">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> <dt>

[<span data-ttu-id="62c71-171">**解壓**</span><span class="sxs-lookup"><span data-stu-id="62c71-171">**Uncompress**</span></span>](uncompress-method-in-class-win32-directory.md)
</dt> </dl>

 

