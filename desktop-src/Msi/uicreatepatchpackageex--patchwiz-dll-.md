---
description: UiCreatePatchPackageEx 函式會將套件建立檔案)  ( pcp 檔案，並產生 Windows Installer 修補套件 ( .msp 套件) 。 呼叫 Msimsp.exe 是使用 Patchwiz.dll 的建議方法。
ms.assetid: 76d9a21d-73bc-41fc-8ed0-7d7d7deff815
title: 'UiCreatePatchPackageEx (Patchwiz.dll) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac61371d1e7bf1809880c8f10a403d1730adc8e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973408"
---
# <a name="uicreatepatchpackageex-patchwizdll"></a><span data-ttu-id="cdcc3-104">UiCreatePatchPackageEx (Patchwiz.dll) </span><span class="sxs-lookup"><span data-stu-id="cdcc3-104">UiCreatePatchPackageEx (Patchwiz.dll)</span></span>

<span data-ttu-id="cdcc3-105">UiCreatePatchPackageEx 函式會將套件建立檔案)  ( pcp 檔案，並產生 Windows Installer 修補套件 ( .msp 套件) 。</span><span class="sxs-lookup"><span data-stu-id="cdcc3-105">The UiCreatePatchPackageEx function takes a package creation file (.pcp file) and generates a Windows Installer patch package (.msp package).</span></span> <span data-ttu-id="cdcc3-106">呼叫 [Msimsp.exe](msimsp-exe.md) 是使用 [Patchwiz.dll](patchwiz-dll.md)的建議方法。</span><span class="sxs-lookup"><span data-stu-id="cdcc3-106">Calling [Msimsp.exe](msimsp-exe.md) is the recommended method for using [Patchwiz.dll](patchwiz-dll.md).</span></span>

<span data-ttu-id="cdcc3-107">從 Patchwiz.dll 4.0 版開始可使用 UiCreatePatchPackageEx 函式，並擴充 [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) 函式的功能。</span><span class="sxs-lookup"><span data-stu-id="cdcc3-107">The UiCreatePatchPackageEx function is available beginning with Patchwiz.dll version 4.0 and extends the functionality of the [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) function.</span></span>

``` syntax
UINT UiCreatePatchPackageEx(
  LPCTSTR szPcpPath,              
  LPCTSTR szPatchPath,            
  LPCTSTR szLogPath,             
  HWND hwndStatus,                
  LPCTSTR szTempFolder,           
  BOOL fRemoveTempFolderContents,
  DWORD dwFlags,
  DWORD dwReserved    
);
```

## <a name="parameters"></a><span data-ttu-id="cdcc3-108">參數</span><span class="sxs-lookup"><span data-stu-id="cdcc3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdcc3-109"><span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szPcpPath*</span><span class="sxs-lookup"><span data-stu-id="cdcc3-109"><span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szPcpPath*</span></span>
</dt> <dd>

<span data-ttu-id="cdcc3-110">修補程式建立內容檔案的完整路徑 ( pcp 檔案) 。</span><span class="sxs-lookup"><span data-stu-id="cdcc3-110">Full path to the patch creation properties file (.pcp file) for this patch.</span></span>

</dd> <dt>

<span data-ttu-id="cdcc3-111"><span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szPatchPath*</span><span class="sxs-lookup"><span data-stu-id="cdcc3-111"><span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szPatchPath*</span></span>
</dt> <dd>

<span data-ttu-id="cdcc3-112">要建立之 Windows Installer 修補套件 ( .msp 檔) 的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="cdcc3-112">Full path to the Windows Installer patch package (.msp file) that is to be created.</span></span> <span data-ttu-id="cdcc3-113">這個參數可以是 **Null** 或空字串，但可能不會省略。</span><span class="sxs-lookup"><span data-stu-id="cdcc3-113">This parameter may be **NULL** or an empty string but may not be omitted.</span></span> <span data-ttu-id="cdcc3-114">如果它是 **Null** 或空字串，則函數會在 Properties 資料表中使用 PatchOutputPath 的值 [ (Patchwiz.dll)](properties-table-patchwiz-dll-.md)。</span><span class="sxs-lookup"><span data-stu-id="cdcc3-114">If it is **NULL** or an empty string, the function uses the value of PatchOutputPath in the [Properties Table (Patchwiz.dll)](properties-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="cdcc3-115"><span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szLogPath*</span><span class="sxs-lookup"><span data-stu-id="cdcc3-115"><span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szLogPath*</span></span>
</dt> <dd>

<span data-ttu-id="cdcc3-116">將附加之文字記錄檔的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="cdcc3-116">Full path to a text log file that will be appended.</span></span> <span data-ttu-id="cdcc3-117">這個參數可以是 **Null** 或空字串，但可能不會省略。</span><span class="sxs-lookup"><span data-stu-id="cdcc3-117">This parameter may be **NULL** or an empty string but may not be omitted.</span></span>

</dd> <dt>

<span data-ttu-id="cdcc3-118"><span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndStatus*</span><span class="sxs-lookup"><span data-stu-id="cdcc3-118"><span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndStatus*</span></span>
</dt> <dd>

<span data-ttu-id="cdcc3-119">顯示狀態文字之視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="cdcc3-119">Handle to a window that displays the status text.</span></span> <span data-ttu-id="cdcc3-120">這個參數可以是 **Null** 或空字串，但可能不會省略。</span><span class="sxs-lookup"><span data-stu-id="cdcc3-120">This parameter may be **NULL** or an empty string but may not be omitted.</span></span>

</dd> <dt>

<span data-ttu-id="cdcc3-121"><span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*szTempFolder*</span><span class="sxs-lookup"><span data-stu-id="cdcc3-121"><span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*szTempFolder*</span></span>
</dt> <dd>

<span data-ttu-id="cdcc3-122">暫存檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="cdcc3-122">Location for temporary files.</span></span> <span data-ttu-id="cdcc3-123">這個參數可以是 **Null** 或空字串，但可能不會省略。</span><span class="sxs-lookup"><span data-stu-id="cdcc3-123">This parameter may be **NULL** or an empty string but may not be omitted.</span></span> <span data-ttu-id="cdcc3-124">使用者必須有足夠的許可權，才能讀取和寫入此資料夾。</span><span class="sxs-lookup"><span data-stu-id="cdcc3-124">The user must have sufficient privileges to read and write to this folder.</span></span> <span data-ttu-id="cdcc3-125">預設位置為% TMP% \\ ~ pcw \_ tmp \\ .。</span><span class="sxs-lookup"><span data-stu-id="cdcc3-125">The default location is %TMP%\\~pcw\_tmp.tmp\\.</span></span>

</dd> <dt>

<span data-ttu-id="cdcc3-126"><span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*</span><span class="sxs-lookup"><span data-stu-id="cdcc3-126"><span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*</span></span>
</dt> <dd>

<span data-ttu-id="cdcc3-127">若 **為 TRUE**，則移除暫存資料夾及其所有內容（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="cdcc3-127">If **TRUE**, remove the temporary folder and all of its contents if present.</span></span> <span data-ttu-id="cdcc3-128">如果 **為 FALSE** 且資料夾存在，則函數會失敗。</span><span class="sxs-lookup"><span data-stu-id="cdcc3-128">If **FALSE**, and folder is present, the function fails.</span></span>

</dd> <dt>

<span data-ttu-id="cdcc3-129"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="cdcc3-129"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="cdcc3-130">這個參數可以設定為下列值的其中一個或組合，以指定記錄或使用者介面選項。</span><span class="sxs-lookup"><span data-stu-id="cdcc3-130">This parameter can be set to one or a combination of the following values to specify logging or user interface options.</span></span>



| <span data-ttu-id="cdcc3-131">旗標</span><span class="sxs-lookup"><span data-stu-id="cdcc3-131">Flag</span></span>            | <span data-ttu-id="cdcc3-132">值</span><span class="sxs-lookup"><span data-stu-id="cdcc3-132">Value</span></span>       | <span data-ttu-id="cdcc3-133">意義</span><span class="sxs-lookup"><span data-stu-id="cdcc3-133">Meaning</span></span>                                  |
|-----------------|-------------|------------------------------------------|
| <span data-ttu-id="cdcc3-134">LOGNONE</span><span class="sxs-lookup"><span data-stu-id="cdcc3-134">LOGNONE</span></span>         | <span data-ttu-id="cdcc3-135">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cdcc3-135">0x00000000</span></span>  | <span data-ttu-id="cdcc3-136">不將任何訊息寫入記錄檔。</span><span class="sxs-lookup"><span data-stu-id="cdcc3-136">Write no messages to the log.</span></span>            |
| <span data-ttu-id="cdcc3-137">LOGINFO</span><span class="sxs-lookup"><span data-stu-id="cdcc3-137">LOGINFO</span></span>         | <span data-ttu-id="cdcc3-138">0x00000001</span><span class="sxs-lookup"><span data-stu-id="cdcc3-138">0x00000001</span></span>  | <span data-ttu-id="cdcc3-139">將參考用訊息寫入記錄檔。</span><span class="sxs-lookup"><span data-stu-id="cdcc3-139">Write informational messages to the log.</span></span> |
| <span data-ttu-id="cdcc3-140">LOGWARN</span><span class="sxs-lookup"><span data-stu-id="cdcc3-140">LOGWARN</span></span>         | <span data-ttu-id="cdcc3-141">0x00000002</span><span class="sxs-lookup"><span data-stu-id="cdcc3-141">0x00000002</span></span>  | <span data-ttu-id="cdcc3-142">將警告寫入至記錄檔。</span><span class="sxs-lookup"><span data-stu-id="cdcc3-142">Write warnings to the log.</span></span>               |
| <span data-ttu-id="cdcc3-143">LOGERR</span><span class="sxs-lookup"><span data-stu-id="cdcc3-143">LOGERR</span></span>          | <span data-ttu-id="cdcc3-144">0x00000004</span><span class="sxs-lookup"><span data-stu-id="cdcc3-144">0x00000004</span></span>  | <span data-ttu-id="cdcc3-145">將錯誤訊息寫入至記錄檔。</span><span class="sxs-lookup"><span data-stu-id="cdcc3-145">Write error messages to the log.</span></span>         |
| <span data-ttu-id="cdcc3-146">LOGPERFMESSAGES</span><span class="sxs-lookup"><span data-stu-id="cdcc3-146">LOGPERFMESSAGES</span></span> | <span data-ttu-id="cdcc3-147">0x00000008</span><span class="sxs-lookup"><span data-stu-id="cdcc3-147">0x00000008</span></span>  | <span data-ttu-id="cdcc3-148">將效能訊息寫入至記錄檔。</span><span class="sxs-lookup"><span data-stu-id="cdcc3-148">Write performance messages to the log.</span></span>   |
| <span data-ttu-id="cdcc3-149">UINONE</span><span class="sxs-lookup"><span data-stu-id="cdcc3-149">UINONE</span></span>          | <span data-ttu-id="cdcc3-150">0x00000000f</span><span class="sxs-lookup"><span data-stu-id="cdcc3-150">0x00000000f</span></span> | <span data-ttu-id="cdcc3-151">不顯示使用者介面。</span><span class="sxs-lookup"><span data-stu-id="cdcc3-151">Do not display the user interface.</span></span>       |
| <span data-ttu-id="cdcc3-152">UIALL</span><span class="sxs-lookup"><span data-stu-id="cdcc3-152">UIALL</span></span>           | <span data-ttu-id="cdcc3-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cdcc3-153">0x00000010</span></span>  | <span data-ttu-id="cdcc3-154">顯示使用者介面。</span><span class="sxs-lookup"><span data-stu-id="cdcc3-154">Display the user interface.</span></span>              |



 

</dd> <dt>

<span data-ttu-id="cdcc3-155"><span id="dwReserved"></span><span id="dwreserved"></span><span id="DWRESERVED"></span>*>dwreserved*</span><span class="sxs-lookup"><span data-stu-id="cdcc3-155"><span id="dwReserved"></span><span id="dwreserved"></span><span id="DWRESERVED"></span>*dwReserved*</span></span>
</dt> <dd>

<span data-ttu-id="cdcc3-156">保留的。</span><span class="sxs-lookup"><span data-stu-id="cdcc3-156">Reserved.</span></span> <span data-ttu-id="cdcc3-157">此參數必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="cdcc3-157">This parameter must be set to zero.</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="cdcc3-158">傳回值</span><span class="sxs-lookup"><span data-stu-id="cdcc3-158">Return Values</span></span>

<span data-ttu-id="cdcc3-159">請參閱 UiCreatePatchPackage 傳回 [值](return-values-for-uicreatepatchpackage.md)中的資料表。</span><span class="sxs-lookup"><span data-stu-id="cdcc3-159">See the table in [Return Values for UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cdcc3-160">備註</span><span class="sxs-lookup"><span data-stu-id="cdcc3-160">Remarks</span></span>

<span data-ttu-id="cdcc3-161">如需撰寫 pcp 檔案，以及使用 [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) 來產生 Windows Installer 修補程式套件的範例，請參閱一節 [小型更新修補範例](a-small-update-patching-example.md)。</span><span class="sxs-lookup"><span data-stu-id="cdcc3-161">For an example of authoring a .pcp file and using [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) to generate a Windows Installer patch package, see the section [A Small Update Patching Example](a-small-update-patching-example.md).</span></span>

<span data-ttu-id="cdcc3-162">建立修補程式需要未壓縮的安裝映射，例如從 CD-ROM 的系統管理映射或未壓縮的安裝映射。</span><span class="sxs-lookup"><span data-stu-id="cdcc3-162">Creating a patch requires an uncompressed setup image, such as an administrative image or an uncompressed setup image from a CD-ROM.</span></span> <span data-ttu-id="cdcc3-163">[UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) 不會為封包中的檔案產生二進位修補程式。</span><span class="sxs-lookup"><span data-stu-id="cdcc3-163">[UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) does not generate binary patches for files in cabinets.</span></span>

 

 



