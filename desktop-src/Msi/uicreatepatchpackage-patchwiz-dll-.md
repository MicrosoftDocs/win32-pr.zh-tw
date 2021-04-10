---
description: UiCreatePatchPackage 函式會將套件建立檔案)  ( pcp 檔案，並產生 Windows Installer 修補套件 ( .msp 套件) 。
ms.assetid: 77fedb80-b664-417d-879b-846e74cc4c23
title: 'UiCreatePatchPackage (Patchwiz.dll) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bcda07d74ffc32c76809037d9ac90cf11ea25c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847682"
---
# <a name="uicreatepatchpackage-patchwizdll"></a><span data-ttu-id="9c760-103">UiCreatePatchPackage (Patchwiz.dll) </span><span class="sxs-lookup"><span data-stu-id="9c760-103">UiCreatePatchPackage (Patchwiz.dll)</span></span>

<span data-ttu-id="9c760-104">UiCreatePatchPackage 函式會將套件建立檔案)  ( pcp 檔案，並產生 Windows Installer 修補套件 ( .msp 套件) 。</span><span class="sxs-lookup"><span data-stu-id="9c760-104">The UiCreatePatchPackage function takes a package creation file (.pcp file) and generates a Windows Installer patch package (.msp package).</span></span> <span data-ttu-id="9c760-105">呼叫 [Msimsp.exe](msimsp-exe.md) 是使用 [Patchwiz.dll](patchwiz-dll.md)的建議方法。</span><span class="sxs-lookup"><span data-stu-id="9c760-105">Calling [Msimsp.exe](msimsp-exe.md) is the recommended method for using [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="9c760-106">[UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md)函式可在4.0 版的 Patchwiz.dll 中取得，並擴充 UiCreatePatchPackage 函式的功能。</span><span class="sxs-lookup"><span data-stu-id="9c760-106">The [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function is available in version 4.0 of Patchwiz.dll and extends the functionality of the UiCreatePatchPackage function.</span></span>

``` syntax
UINT UiCreatePatchPackage(
  LPCTSTR szPcpPath,              
  LPCTSTR szPatchPath,            
  LPCTSTR szLogPath,             
  HWND hwndStatus,                
  LPCTSTR szTempFolder,           
  Bool fRemoveTempFolderContents  
);
```

## <a name="parameters"></a><span data-ttu-id="9c760-107">參數</span><span class="sxs-lookup"><span data-stu-id="9c760-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c760-108"><span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szPcpPath*</span><span class="sxs-lookup"><span data-stu-id="9c760-108"><span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szPcpPath*</span></span>
</dt> <dd>

<span data-ttu-id="9c760-109">修補程式建立內容檔案的完整路徑 ( pcp 檔案) 。</span><span class="sxs-lookup"><span data-stu-id="9c760-109">Full path to the patch creation properties file (.pcp file) for this patch.</span></span>

</dd> <dt>

<span data-ttu-id="9c760-110"><span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szPatchPath*</span><span class="sxs-lookup"><span data-stu-id="9c760-110"><span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szPatchPath*</span></span>
</dt> <dd>

<span data-ttu-id="9c760-111">要建立之 Windows Installer 修補套件 ( .msp 檔) 的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="9c760-111">Full path to the Windows Installer patch package (.msp file) that is to be created.</span></span> <span data-ttu-id="9c760-112">這個參數可以是 **Null** 或空字串，但可能不會省略。</span><span class="sxs-lookup"><span data-stu-id="9c760-112">This parameter may be **NULL** or an empty string but may not be omitted.</span></span> <span data-ttu-id="9c760-113">如果它是 **Null** 或空字串，則函數會在 Properties 資料表中使用 PatchOutputPath 的值 [ (Patchwiz.dll)](properties-table-patchwiz-dll-.md)。</span><span class="sxs-lookup"><span data-stu-id="9c760-113">If it is **NULL** or an empty string, the function uses the value of PatchOutputPath in the [Properties Table (Patchwiz.dll)](properties-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c760-114"><span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szLogPath*</span><span class="sxs-lookup"><span data-stu-id="9c760-114"><span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szLogPath*</span></span>
</dt> <dd>

<span data-ttu-id="9c760-115">將附加之文字記錄檔的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="9c760-115">Full path to a text log file that will be appended.</span></span> <span data-ttu-id="9c760-116">這個參數可以是 **Null** 或空字串，但可能不會省略。</span><span class="sxs-lookup"><span data-stu-id="9c760-116">This parameter may be **NULL** or an empty string but may not be omitted.</span></span>

</dd> <dt>

<span data-ttu-id="9c760-117"><span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndStatus*</span><span class="sxs-lookup"><span data-stu-id="9c760-117"><span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndStatus*</span></span>
</dt> <dd>

<span data-ttu-id="9c760-118">顯示狀態文字之視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="9c760-118">Handle to a window that displays the status text.</span></span> <span data-ttu-id="9c760-119">這個參數可以是 **Null** 或空字串，但可能不會省略。</span><span class="sxs-lookup"><span data-stu-id="9c760-119">This parameter may be **NULL** or an empty string but may not be omitted.</span></span>

</dd> <dt>

<span data-ttu-id="9c760-120"><span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*szTempFolder*</span><span class="sxs-lookup"><span data-stu-id="9c760-120"><span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*szTempFolder*</span></span>
</dt> <dd>

<span data-ttu-id="9c760-121">暫存檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="9c760-121">Location for temporary files.</span></span> <span data-ttu-id="9c760-122">這個參數可以是 **Null** 或空字串，但可能不會省略。</span><span class="sxs-lookup"><span data-stu-id="9c760-122">This parameter may be **NULL** or an empty string but may not be omitted.</span></span> <span data-ttu-id="9c760-123">預設位置為% TMP% \\ ~ pcw \_ tmp \\ .。</span><span class="sxs-lookup"><span data-stu-id="9c760-123">The default location is %TMP%\\~pcw\_tmp.tmp\\.</span></span>

</dd> <dt>

<span data-ttu-id="9c760-124"><span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*</span><span class="sxs-lookup"><span data-stu-id="9c760-124"><span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*</span></span>
</dt> <dd>

<span data-ttu-id="9c760-125">若 **為 TRUE**，則移除暫存資料夾及其所有內容（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="9c760-125">If **TRUE**, remove the temporary folder and all of its contents if present.</span></span> <span data-ttu-id="9c760-126">如果 **為 FALSE** 且資料夾存在，則函數會失敗。</span><span class="sxs-lookup"><span data-stu-id="9c760-126">If **FALSE**, and folder is present, the function fails.</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="9c760-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="9c760-127">Return Values</span></span>

<span data-ttu-id="9c760-128">請參閱 UiCreatePatchPackage 傳回 [值](return-values-for-uicreatepatchpackage.md)中的資料表。</span><span class="sxs-lookup"><span data-stu-id="9c760-128">See the table in [Return Values for UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9c760-129">備註</span><span class="sxs-lookup"><span data-stu-id="9c760-129">Remarks</span></span>

<span data-ttu-id="9c760-130">如需撰寫 pcp 檔案，以及使用 UiCreatePatchPackage 來產生 Windows Installer 修補程式套件的範例，請參閱一節 [小型更新修補範例](a-small-update-patching-example.md)。</span><span class="sxs-lookup"><span data-stu-id="9c760-130">For an example of authoring a .pcp file and using UiCreatePatchPackage to generate a Windows Installer patch package, see the section [A Small Update Patching Example](a-small-update-patching-example.md).</span></span>

<span data-ttu-id="9c760-131">建立修補程式需要未壓縮的安裝映射，例如從 CD-ROM 的系統管理映射或未壓縮的安裝映射。</span><span class="sxs-lookup"><span data-stu-id="9c760-131">Creating a patch requires an uncompressed setup image, such as an administrative image or an uncompressed setup image from a CD-ROM.</span></span> <span data-ttu-id="9c760-132">UiCreatePatchPackage 不會為封包中的檔案產生二進位修補程式。</span><span class="sxs-lookup"><span data-stu-id="9c760-132">UiCreatePatchPackage does not generate binary patches for files in cabinets.</span></span>

 

 



