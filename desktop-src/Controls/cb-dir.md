---
title: 'CB_DIR 訊息 (Winuser .h) '
description: 將名稱新增至下拉式方塊所顯示的清單。 訊息會新增符合指定字串和檔案屬性集的目錄和檔案的名稱。 CB \_ DIR 也可以將對應的磁碟機號新增至清單。
ms.assetid: 6082d12c-0af4-4a99-98c0-6a98d171f4d8
keywords:
- CB_DIR message Windows 控制項
topic_type:
- apiref
api_name:
- CB_DIR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98cbea5bb88614d5606dd3d5cb165be59f632556
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843576"
---
# <a name="cb_dir-message"></a><span data-ttu-id="a8900-106">CB \_ DIR 訊息</span><span class="sxs-lookup"><span data-stu-id="a8900-106">CB\_DIR message</span></span>

<span data-ttu-id="a8900-107">將名稱新增至下拉式方塊所顯示的清單。</span><span class="sxs-lookup"><span data-stu-id="a8900-107">Adds names to the list displayed by the combo box.</span></span> <span data-ttu-id="a8900-108">訊息會新增符合指定字串和檔案屬性集的目錄和檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="a8900-108">The message adds the names of directories and files that match a specified string and set of file attributes.</span></span> <span data-ttu-id="a8900-109">**CB \_DIR** 也可以將對應的磁碟機號新增至清單。</span><span class="sxs-lookup"><span data-stu-id="a8900-109">**CB\_DIR** can also add mapped drive letters to the list.</span></span>

## <a name="parameters"></a><span data-ttu-id="a8900-110">參數</span><span class="sxs-lookup"><span data-stu-id="a8900-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8900-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a8900-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8900-112">要加入至下拉式方塊之檔案或目錄的屬性。</span><span class="sxs-lookup"><span data-stu-id="a8900-112">The attributes of the files or directories to be added to the combo box.</span></span> <span data-ttu-id="a8900-113">這個參數可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="a8900-113">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="a8900-114">值</span><span class="sxs-lookup"><span data-stu-id="a8900-114">Value</span></span>                                                                                                                                                         | <span data-ttu-id="a8900-115">意義</span><span class="sxs-lookup"><span data-stu-id="a8900-115">Meaning</span></span>                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DDL_ARCHIVE"></span><span id="ddl_archive"></span><dl> <span data-ttu-id="a8900-116"><dt>**DDL \_ 封存**</dt></span><span class="sxs-lookup"><span data-stu-id="a8900-116"><dt>**DDL\_ARCHIVE**</dt></span></span> </dl>       | <span data-ttu-id="a8900-117">包含封存的檔案。</span><span class="sxs-lookup"><span data-stu-id="a8900-117">Includes archived files.</span></span><br/>                                                                                                            |
| <span id="DDL_DIRECTORY"></span><span id="ddl_directory"></span><dl> <span data-ttu-id="a8900-118"><dt>**DDL \_ 目錄**</dt></span><span class="sxs-lookup"><span data-stu-id="a8900-118"><dt>**DDL\_DIRECTORY**</dt></span></span> </dl> | <span data-ttu-id="a8900-119">包含子目錄，以方括弧括住 (\[ \]) 。</span><span class="sxs-lookup"><span data-stu-id="a8900-119">Includes subdirectories, which are enclosed in square brackets (\[ \]).</span></span><br/>                                                             |
| <span id="DDL_DRIVES"></span><span id="ddl_drives"></span><dl> <span data-ttu-id="a8900-120"><dt>**DDL \_ 磁片磁碟機**</dt></span><span class="sxs-lookup"><span data-stu-id="a8900-120"><dt>**DDL\_DRIVES**</dt></span></span> </dl>          | <span data-ttu-id="a8900-121">所有對應的磁片磁碟機都會新增至清單中。</span><span class="sxs-lookup"><span data-stu-id="a8900-121">All mapped drives are added to the list.</span></span> <span data-ttu-id="a8900-122">磁片磁碟機會以 x 形式列出 \[ -  - \] ，其中 *x* 是磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="a8900-122">Drives are listed in the form \[-*x*-\], where *x* is the drive letter.</span></span><br/>                    |
| <span id="DDL_EXCLUSIVE"></span><span id="ddl_exclusive"></span><dl> <span data-ttu-id="a8900-123"><dt>**DDL \_ 專屬**</dt></span><span class="sxs-lookup"><span data-stu-id="a8900-123"><dt>**DDL\_EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="a8900-124">只包含具有指定屬性的檔案。</span><span class="sxs-lookup"><span data-stu-id="a8900-124">Includes only files with the specified attributes.</span></span> <span data-ttu-id="a8900-125">根據預設，即使未指定 DDL READWRITE，也會列出讀取/寫入檔案 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a8900-125">By default, read/write files are listed even if DDL\_READWRITE is not specified.</span></span><br/> |
| <span id="DDL_HIDDEN"></span><span id="ddl_hidden"></span><dl> <span data-ttu-id="a8900-126"><dt>**DDL \_ 隱藏**</dt></span><span class="sxs-lookup"><span data-stu-id="a8900-126"><dt>**DDL\_HIDDEN**</dt></span></span> </dl>          | <span data-ttu-id="a8900-127">包含隱藏的檔案。</span><span class="sxs-lookup"><span data-stu-id="a8900-127">Includes hidden files.</span></span><br/>                                                                                                              |
| <span id="DDL_READONLY"></span><span id="ddl_readonly"></span><dl> <span data-ttu-id="a8900-128"><dt>**DDL \_ READONLY**</dt></span><span class="sxs-lookup"><span data-stu-id="a8900-128"><dt>**DDL\_READONLY**</dt></span></span> </dl>    | <span data-ttu-id="a8900-129">包含唯讀檔案。</span><span class="sxs-lookup"><span data-stu-id="a8900-129">Includes read-only files.</span></span><br/>                                                                                                           |
| <span id="DDL_READWRITE"></span><span id="ddl_readwrite"></span><dl> <span data-ttu-id="a8900-130"><dt>**DDL \_ READWRITE**</dt></span><span class="sxs-lookup"><span data-stu-id="a8900-130"><dt>**DDL\_READWRITE**</dt></span></span> </dl> | <span data-ttu-id="a8900-131">包含沒有其他屬性的讀取/寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="a8900-131">Includes read/write files with no additional attributes.</span></span> <span data-ttu-id="a8900-132">此為預設值。</span><span class="sxs-lookup"><span data-stu-id="a8900-132">This is the default.</span></span><br/>                                                       |
| <span id="DDL_SYSTEM"></span><span id="ddl_system"></span><dl> <span data-ttu-id="a8900-133"><dt>**DDL \_ 系統**</dt></span><span class="sxs-lookup"><span data-stu-id="a8900-133"><dt>**DDL\_SYSTEM**</dt></span></span> </dl>          | <span data-ttu-id="a8900-134">包含系統檔案。</span><span class="sxs-lookup"><span data-stu-id="a8900-134">Includes system files.</span></span><br/>                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="a8900-135">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8900-135">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8900-136">**LPCTSTR** 指標，指向以 null 終止的字串，這個字串會指定絕對路徑、相對路徑或檔案名。</span><span class="sxs-lookup"><span data-stu-id="a8900-136">An **LPCTSTR** pointer to a null-terminated string that specifies an absolute path, relative path, or file name.</span></span> <span data-ttu-id="a8900-137">絕對路徑可以用磁碟機號開頭 (例如 d： \) 或 UNC 名稱 (例如， \\ \\ *machinename* \\ *共用*) 。</span><span class="sxs-lookup"><span data-stu-id="a8900-137">An absolute path can begin with a drive letter (for example, d:\) or a UNC name (for example, \\\\*machinename*\\*sharename*).</span></span> <span data-ttu-id="a8900-138">如果字串指定具有 *wParam* 參數所指定之屬性的檔案名或目錄，則會將檔案名或目錄加入至清單中。</span><span class="sxs-lookup"><span data-stu-id="a8900-138">If the string specifies a file name or directory that has the attributes specified by the *wParam* parameter, the file name or directory is added to the list.</span></span> <span data-ttu-id="a8900-139">如果檔案名或目錄名稱中包含萬用字元 (？</span><span class="sxs-lookup"><span data-stu-id="a8900-139">If the file name or directory name contains wildcard characters (?</span></span> <span data-ttu-id="a8900-140">或 \*) ，所有符合萬用字元運算式的檔案或目錄，以及 *wParam* 參數指定的屬性，都會新增至下拉式方塊中顯示的清單。</span><span class="sxs-lookup"><span data-stu-id="a8900-140">or \*), all files or directories that match the wildcard expression and have the attributes specified by the *wParam* parameter are added to the list displayed in the combo box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8900-141">傳回值</span><span class="sxs-lookup"><span data-stu-id="a8900-141">Return value</span></span>

<span data-ttu-id="a8900-142">如果訊息成功，則傳回值是加入至清單中的最後一個名稱之以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="a8900-142">If the message succeeds, the return value is the zero-based index of the last name added to the list.</span></span>

<span data-ttu-id="a8900-143">如果發生錯誤，傳回值會是 CB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="a8900-143">If an error occurs, the return value is CB\_ERR.</span></span> <span data-ttu-id="a8900-144">如果空間不足，無法儲存新的字串，則傳回值為 CB \_ ERRSPACE。</span><span class="sxs-lookup"><span data-stu-id="a8900-144">If there is insufficient space to store the new strings, the return value is CB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8900-145">備註</span><span class="sxs-lookup"><span data-stu-id="a8900-145">Remarks</span></span>

<span data-ttu-id="a8900-146">如果 *wParam* 包含 DDL \_ 目錄旗標，而 *lParam* 指定第一層目錄的所有子目錄，例如 C： \\ TEMP \\ \* ，則清單方塊一律會包含根目錄的 ".." 專案。</span><span class="sxs-lookup"><span data-stu-id="a8900-146">If *wParam* includes the DDL\_DIRECTORY flag and *lParam* specifies all the subdirectories of a first-level directory, such as C:\\TEMP\\\*, the list box will always include a ".." entry for the root directory.</span></span> <span data-ttu-id="a8900-147">即使根目錄有隱藏的或系統屬性，而且 \_ 未指定 ddl 隱藏和 ddl 系統旗標，也是如此 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a8900-147">This is true even if the root directory has hidden or system attributes and the DDL\_HIDDEN and DDL\_SYSTEM flags are not specified.</span></span> <span data-ttu-id="a8900-148">NTFS 磁片區的根目錄具有隱藏和系統屬性。</span><span class="sxs-lookup"><span data-stu-id="a8900-148">The root directory of an NTFS volume has hidden and system attributes.</span></span>

<span data-ttu-id="a8900-149">此清單會顯示長檔名（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="a8900-149">The list displays long file names, if any.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8900-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8900-150">Requirements</span></span>



| <span data-ttu-id="a8900-151">需求</span><span class="sxs-lookup"><span data-stu-id="a8900-151">Requirement</span></span> | <span data-ttu-id="a8900-152">值</span><span class="sxs-lookup"><span data-stu-id="a8900-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8900-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a8900-153">Minimum supported client</span></span><br/> | <span data-ttu-id="a8900-154">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8900-154">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a8900-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a8900-155">Minimum supported server</span></span><br/> | <span data-ttu-id="a8900-156">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8900-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a8900-157">標頭</span><span class="sxs-lookup"><span data-stu-id="a8900-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8900-158"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="a8900-158"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8900-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8900-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="a8900-160">**參考**</span><span class="sxs-lookup"><span data-stu-id="a8900-160">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a8900-161">**CB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="a8900-161">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="a8900-162">**CB \_ INSERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="a8900-162">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="a8900-163">**DlgDirListComboBox**</span><span class="sxs-lookup"><span data-stu-id="a8900-163">**DlgDirListComboBox**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dlgdirlistcomboboxa)
</dt> </dl>

 

 





