---
title: 'LB_DIR 訊息 (Winuser .h) '
description: 將名稱加入清單方塊所顯示的清單中。 訊息會新增符合指定字串和檔案屬性集的目錄和檔案的名稱。 LB \_ DIR 也可以在清單方塊中新增對應的磁碟機號。
ms.assetid: 5ec134e9-fe42-4cc0-bdea-fa5e66c218f6
keywords:
- LB_DIR message Windows 控制項
topic_type:
- apiref
api_name:
- LB_DIR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80abddbce13adec2e66824057fc5e873def306ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106001"
---
# <a name="lb_dir-message"></a><span data-ttu-id="bc965-106">LB \_ DIR 訊息</span><span class="sxs-lookup"><span data-stu-id="bc965-106">LB\_DIR message</span></span>

<span data-ttu-id="bc965-107">將名稱加入清單方塊所顯示的清單中。</span><span class="sxs-lookup"><span data-stu-id="bc965-107">Adds names to the list displayed by a list box.</span></span> <span data-ttu-id="bc965-108">訊息會新增符合指定字串和檔案屬性集的目錄和檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc965-108">The message adds the names of directories and files that match a specified string and set of file attributes.</span></span> <span data-ttu-id="bc965-109">**LB \_DIR** 也可以在清單方塊中新增對應的磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="bc965-109">**LB\_DIR** can also add mapped drive letters to the list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="bc965-110">參數</span><span class="sxs-lookup"><span data-stu-id="bc965-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc965-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bc965-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bc965-112">要加入清單方塊之檔案或目錄的屬性。</span><span class="sxs-lookup"><span data-stu-id="bc965-112">The attributes of the files or directories to be added to the list box.</span></span> <span data-ttu-id="bc965-113">這個參數可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="bc965-113">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="bc965-114">值</span><span class="sxs-lookup"><span data-stu-id="bc965-114">Value</span></span>                                                                                                                                                         | <span data-ttu-id="bc965-115">意義</span><span class="sxs-lookup"><span data-stu-id="bc965-115">Meaning</span></span>                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DDL_ARCHIVE"></span><span id="ddl_archive"></span><dl> <span data-ttu-id="bc965-116"><dt>**DDL \_ 封存**</dt></span><span class="sxs-lookup"><span data-stu-id="bc965-116"><dt>**DDL\_ARCHIVE**</dt></span></span> </dl>       | <span data-ttu-id="bc965-117">包含封存的檔案。</span><span class="sxs-lookup"><span data-stu-id="bc965-117">Includes archived files.</span></span><br/>                                                                                                            |
| <span id="DDL_DIRECTORY"></span><span id="ddl_directory"></span><dl> <span data-ttu-id="bc965-118"><dt>**DDL \_ 目錄**</dt></span><span class="sxs-lookup"><span data-stu-id="bc965-118"><dt>**DDL\_DIRECTORY**</dt></span></span> </dl> | <span data-ttu-id="bc965-119">包含子目錄。</span><span class="sxs-lookup"><span data-stu-id="bc965-119">Includes subdirectories.</span></span> <span data-ttu-id="bc965-120">子目錄名稱會以方括弧括住 (\[ \]) 。</span><span class="sxs-lookup"><span data-stu-id="bc965-120">Subdirectory names are enclosed in square brackets (\[ \]).</span></span><br/>                                                |
| <span id="DDL_DRIVES"></span><span id="ddl_drives"></span><dl> <span data-ttu-id="bc965-121"><dt>**DDL \_ 磁片磁碟機**</dt></span><span class="sxs-lookup"><span data-stu-id="bc965-121"><dt>**DDL\_DRIVES**</dt></span></span> </dl>          | <span data-ttu-id="bc965-122">所有對應的磁片磁碟機都會新增至清單中。</span><span class="sxs-lookup"><span data-stu-id="bc965-122">All mapped drives are added to the list.</span></span> <span data-ttu-id="bc965-123">磁片磁碟機會以 x 形式列出 \[ -  - \] ，其中 *x* 是磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="bc965-123">Drives are listed in the form \[-*x*-\], where *x* is the drive letter.</span></span><br/>                    |
| <span id="DDL_EXCLUSIVE"></span><span id="ddl_exclusive"></span><dl> <span data-ttu-id="bc965-124"><dt>**DDL \_ 專屬**</dt></span><span class="sxs-lookup"><span data-stu-id="bc965-124"><dt>**DDL\_EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="bc965-125">只包含具有指定屬性的檔案。</span><span class="sxs-lookup"><span data-stu-id="bc965-125">Includes only files with the specified attributes.</span></span> <span data-ttu-id="bc965-126">根據預設，即使未指定 DDL READWRITE，也會列出讀取/寫入檔案 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bc965-126">By default, read/write files are listed even if DDL\_READWRITE is not specified.</span></span><br/> |
| <span id="DDL_HIDDEN"></span><span id="ddl_hidden"></span><dl> <span data-ttu-id="bc965-127"><dt>**DDL \_ 隱藏**</dt></span><span class="sxs-lookup"><span data-stu-id="bc965-127"><dt>**DDL\_HIDDEN**</dt></span></span> </dl>          | <span data-ttu-id="bc965-128">包含隱藏的檔案。</span><span class="sxs-lookup"><span data-stu-id="bc965-128">Includes hidden files.</span></span><br/>                                                                                                              |
| <span id="DDL_READONLY"></span><span id="ddl_readonly"></span><dl> <span data-ttu-id="bc965-129"><dt>**DDL \_ READONLY**</dt></span><span class="sxs-lookup"><span data-stu-id="bc965-129"><dt>**DDL\_READONLY**</dt></span></span> </dl>    | <span data-ttu-id="bc965-130">包含唯讀檔案。</span><span class="sxs-lookup"><span data-stu-id="bc965-130">Includes read-only files.</span></span><br/>                                                                                                           |
| <span id="DDL_READWRITE"></span><span id="ddl_readwrite"></span><dl> <span data-ttu-id="bc965-131"><dt>**DDL \_ READWRITE**</dt></span><span class="sxs-lookup"><span data-stu-id="bc965-131"><dt>**DDL\_READWRITE**</dt></span></span> </dl> | <span data-ttu-id="bc965-132">包含沒有其他屬性的讀取/寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="bc965-132">Includes read/write files with no additional attributes.</span></span> <span data-ttu-id="bc965-133">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="bc965-133">This is the default setting.</span></span><br/>                                               |
| <span id="DDL_SYSTEM"></span><span id="ddl_system"></span><dl> <span data-ttu-id="bc965-134"><dt>**DDL \_ 系統**</dt></span><span class="sxs-lookup"><span data-stu-id="bc965-134"><dt>**DDL\_SYSTEM**</dt></span></span> </dl>          | <span data-ttu-id="bc965-135">包含系統檔案。</span><span class="sxs-lookup"><span data-stu-id="bc965-135">Includes system files.</span></span><br/>                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="bc965-136">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bc965-136">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bc965-137">以 null 結束的字串指標，指定絕對路徑、相對路徑或檔案名。</span><span class="sxs-lookup"><span data-stu-id="bc965-137">A pointer to the null-terminated string that specifies an absolute path, relative path, or filename.</span></span> <span data-ttu-id="bc965-138">絕對路徑可以用磁碟機號開頭 (例如 d： \) 或 UNC 名稱 (例如， \\ \\ *machinename* \\ *共用*) 。</span><span class="sxs-lookup"><span data-stu-id="bc965-138">An absolute path can begin with a drive letter (for example, d:\) or a UNC name (for example, \\\\ *machinename*\\ *sharename*).</span></span>

<span data-ttu-id="bc965-139">如果字串指定具有 *wParam* 參數所指定之屬性的檔案名或目錄，則會將檔案名或目錄加入至清單中。</span><span class="sxs-lookup"><span data-stu-id="bc965-139">If the string specifies a filename or directory that has the attributes specified by the *wParam* parameter, the filename or directory is added to the list.</span></span> <span data-ttu-id="bc965-140">如果檔案名或目錄名稱包含萬用字元 (？</span><span class="sxs-lookup"><span data-stu-id="bc965-140">If the filename or directory name contains wildcard characters (?</span></span> <span data-ttu-id="bc965-141">或 \*) ，所有符合萬用字元運算式的檔案或目錄，以及 *wParam* 參數指定的屬性都會新增至清單中。</span><span class="sxs-lookup"><span data-stu-id="bc965-141">or \*), all files or directories that match the wildcard expression and have the attributes specified by the *wParam* parameter are added to the list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc965-142">傳回值</span><span class="sxs-lookup"><span data-stu-id="bc965-142">Return value</span></span>

<span data-ttu-id="bc965-143">如果訊息成功，則傳回值是加入至清單中的最後一個名稱之以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="bc965-143">If the message succeeds, the return value is the zero-based index of the last name added to the list.</span></span>

<span data-ttu-id="bc965-144">如果發生錯誤，傳回值為 LB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="bc965-144">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="bc965-145">如果空間不足，無法儲存新的字串，則傳回值為 LB \_ ERRSPACE。</span><span class="sxs-lookup"><span data-stu-id="bc965-145">If there is insufficient space to store the new strings, the return value is LB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc965-146">備註</span><span class="sxs-lookup"><span data-stu-id="bc965-146">Remarks</span></span>

<span data-ttu-id="bc965-147">[**LB \_ INITSTORAGE**](lb-initstorage.md)訊息有助於加速初始化具有大量專案 (超過 100) 的清單方塊。</span><span class="sxs-lookup"><span data-stu-id="bc965-147">The [**LB\_INITSTORAGE**](lb-initstorage.md) message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="bc965-148">它會保留指定的記憶體數量，讓後續的 **LB \_ DIR** 訊息可以花最短的時間。</span><span class="sxs-lookup"><span data-stu-id="bc965-148">It reserves the specified amount of memory so that subsequent **LB\_DIR** messages take the shortest possible time.</span></span> <span data-ttu-id="bc965-149">您可以使用 *wParam* 和 *lParam* 參數的估計值。</span><span class="sxs-lookup"><span data-stu-id="bc965-149">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="bc965-150">如果您高估值，則會配置額外的記憶體;如果您低估了，一般配置會用於超出要求數量的專案。</span><span class="sxs-lookup"><span data-stu-id="bc965-150">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

<span data-ttu-id="bc965-151">如果 *wParam* 包含 DDL \_ 目錄旗標，而 *lParam* 指定第一層目錄的所有子目錄，例如 C： \\ TEMP \\ \* ，則清單方塊一律會包含根目錄的 ".." 專案。</span><span class="sxs-lookup"><span data-stu-id="bc965-151">If *wParam* includes the DDL\_DIRECTORY flag and *lParam* specifies all the subdirectories of a first-level directory, such as C:\\TEMP\\\*, the list box will always include a ".." entry for the root directory.</span></span> <span data-ttu-id="bc965-152">即使根目錄有隱藏的或系統屬性，而且 \_ 未指定 ddl 隱藏和 ddl 系統旗標，也是如此 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bc965-152">This is true even if the root directory has hidden or system attributes and the DDL\_HIDDEN and DDL\_SYSTEM flags are not specified.</span></span> <span data-ttu-id="bc965-153">NTFS 磁片區的根目錄具有隱藏和系統屬性。</span><span class="sxs-lookup"><span data-stu-id="bc965-153">The root directory of an NTFS volume has hidden and system attributes.</span></span>

<span data-ttu-id="bc965-154">此清單會顯示長檔名（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="bc965-154">The list displays long filenames, if any.</span></span>

<span data-ttu-id="bc965-155">若為 ANSI 應用程式，系統會使用 CP ACP 將清單方塊中的文字轉換成 Unicode \_ 。</span><span class="sxs-lookup"><span data-stu-id="bc965-155">For an ANSI application, the system converts the text in a list box to Unicode using CP\_ACP.</span></span> <span data-ttu-id="bc965-156">這可能會造成問題。</span><span class="sxs-lookup"><span data-stu-id="bc965-156">This can cause problems.</span></span> <span data-ttu-id="bc965-157">例如，在日文視窗的非 Unicode 清單方塊中，重音的羅馬字元將會出現模糊。</span><span class="sxs-lookup"><span data-stu-id="bc965-157">For example, accented Roman characters in a non-Unicode list box in Japanese Windows will come out garbled.</span></span> <span data-ttu-id="bc965-158">若要修正此問題，請將應用程式編譯為 Unicode 或使用主控描繪清單方塊。</span><span class="sxs-lookup"><span data-stu-id="bc965-158">To fix this, either compile the application as Unicode or use an owner-drawn list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc965-159">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc965-159">Requirements</span></span>



| <span data-ttu-id="bc965-160">需求</span><span class="sxs-lookup"><span data-stu-id="bc965-160">Requirement</span></span> | <span data-ttu-id="bc965-161">值</span><span class="sxs-lookup"><span data-stu-id="bc965-161">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc965-162">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bc965-162">Minimum supported client</span></span><br/> | <span data-ttu-id="bc965-163">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc965-163">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bc965-164">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bc965-164">Minimum supported server</span></span><br/> | <span data-ttu-id="bc965-165">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc965-165">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bc965-166">標頭</span><span class="sxs-lookup"><span data-stu-id="bc965-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc965-167"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="bc965-167"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc965-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc965-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc965-169">**DlgDirList**</span><span class="sxs-lookup"><span data-stu-id="bc965-169">**DlgDirList**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)
</dt> </dl>

 

 





