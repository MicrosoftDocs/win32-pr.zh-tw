---
description: 將專案或專案複製到資料夾。
title: 'CopyHere 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.CopyHere
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 22bf1b4c-f242-4c52-b094-c5339bb35d02
ms.openlocfilehash: 1466e5d01715c0c820cbc7cd9809c51e4963ec56
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842139"
---
# <a name="foldercopyhere-method"></a><span data-ttu-id="8e692-103">CopyHere 方法</span><span class="sxs-lookup"><span data-stu-id="8e692-103">Folder.CopyHere method</span></span>

<span data-ttu-id="8e692-104">將專案或專案複製到資料夾。</span><span class="sxs-lookup"><span data-stu-id="8e692-104">Copies an item or items to a folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e692-105">語法</span><span class="sxs-lookup"><span data-stu-id="8e692-105">Syntax</span></span>


```JScript
Folder.CopyHere(
  vItem,
  [ vOptions ]
)
```



## <a name="parameters"></a><span data-ttu-id="8e692-106">參數</span><span class="sxs-lookup"><span data-stu-id="8e692-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e692-107">*vItem*</span><span class="sxs-lookup"><span data-stu-id="8e692-107">*vItem*</span></span> 
</dt> <dd>

<span data-ttu-id="8e692-108">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="8e692-108">Type: **Variant**</span></span>

<span data-ttu-id="8e692-109">要複製的專案。</span><span class="sxs-lookup"><span data-stu-id="8e692-109">The item or items to copy.</span></span> <span data-ttu-id="8e692-110">這可以是代表檔案名、 [**FolderItem**](folderitem.md) 物件或 [**FolderItems**](folderitems.md) 物件的字串。</span><span class="sxs-lookup"><span data-stu-id="8e692-110">This can be a string that represents a file name, a [**FolderItem**](folderitem.md) object, or a [**FolderItems**](folderitems.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="8e692-111">*vOptions* \[選\]</span><span class="sxs-lookup"><span data-stu-id="8e692-111">*vOptions* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8e692-112">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="8e692-112">Type: **Variant**</span></span>

<span data-ttu-id="8e692-113">複製操作的選項。</span><span class="sxs-lookup"><span data-stu-id="8e692-113">Options for the copy operation.</span></span> <span data-ttu-id="8e692-114">這個值可以是零或下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="8e692-114">This value can be zero or a combination of the following values.</span></span> <span data-ttu-id="8e692-115">這些值是根據定義來與 c + + [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa)結構的 **fFlags** 成員搭配使用的旗標。</span><span class="sxs-lookup"><span data-stu-id="8e692-115">These values are based upon flags defined for use with the **fFlags** member of the C++ [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) structure.</span></span> <span data-ttu-id="8e692-116">每個 Shell 命名空間都必須提供自己的這些旗標執行，而且每個命名空間都可以選擇忽略部分或甚至所有的旗標。</span><span class="sxs-lookup"><span data-stu-id="8e692-116">Each Shell namespace must provide its own implementation of these flags, and each namespace can choose to ignore some or even all of these flags.</span></span> <span data-ttu-id="8e692-117">這些旗標不是依 Visual Basic、VBScript 或 JScript 的名稱所定義，因此您必須自行定義，或使用其對等數值。</span><span class="sxs-lookup"><span data-stu-id="8e692-117">These flags are not defined by name for Visual Basic, VBScript, or JScript, so you must define them yourself or use their numeric equivalents.</span></span>

> [!Note]  
> <span data-ttu-id="8e692-118">在某些情況下（例如壓縮的 ( .zip) 檔），設計可能會忽略某些選項旗標。</span><span class="sxs-lookup"><span data-stu-id="8e692-118">In some cases, such as compressed (.zip) files, some option flags may be ignored by design.</span></span>

 

<dt>



 <span data-ttu-id="8e692-119">(4)</span><span class="sxs-lookup"><span data-stu-id="8e692-119">(4)</span></span>


</dt> <dd>

<span data-ttu-id="8e692-120">不要顯示進度對話方塊。</span><span class="sxs-lookup"><span data-stu-id="8e692-120">Do not display a progress dialog box.</span></span>

</dd> <dt>



 <span data-ttu-id="8e692-121">(8)</span><span class="sxs-lookup"><span data-stu-id="8e692-121">(8)</span></span>


</dt> <dd>

<span data-ttu-id="8e692-122">如果目標名稱的檔案已經存在，請將移動、複製或重新命名作業中的新名稱所要操作的檔案提供。</span><span class="sxs-lookup"><span data-stu-id="8e692-122">Give the file being operated on a new name in a move, copy, or rename operation if a file with the target name already exists.</span></span>

</dd> <dt>



 <span data-ttu-id="8e692-123">(16)</span><span class="sxs-lookup"><span data-stu-id="8e692-123">(16)</span></span>


</dt> <dd>

<span data-ttu-id="8e692-124">針對顯示的任何對話方塊，回應 [全部是]。</span><span class="sxs-lookup"><span data-stu-id="8e692-124">Respond with "Yes to All" for any dialog box that is displayed.</span></span>

</dd> <dt>



 <span data-ttu-id="8e692-125">(64)</span><span class="sxs-lookup"><span data-stu-id="8e692-125">(64)</span></span>


</dt> <dd>

<span data-ttu-id="8e692-126">盡可能保留復原資訊。</span><span class="sxs-lookup"><span data-stu-id="8e692-126">Preserve undo information, if possible.</span></span>

</dd> <dt>



 <span data-ttu-id="8e692-127"> (128) </span><span class="sxs-lookup"><span data-stu-id="8e692-127">(128)</span></span>


</dt> <dd>

<span data-ttu-id="8e692-128">只有在指定萬用字元檔案名 (時，才在檔案上執行操作。請 \* \*) 。</span><span class="sxs-lookup"><span data-stu-id="8e692-128">Perform the operation on files only if a wildcard file name (\*.\*) is specified.</span></span>

</dd> <dt>



 <span data-ttu-id="8e692-129"> (256) </span><span class="sxs-lookup"><span data-stu-id="8e692-129">(256)</span></span>


</dt> <dd>

<span data-ttu-id="8e692-130">顯示 [進度] 對話方塊，但不顯示檔案名。</span><span class="sxs-lookup"><span data-stu-id="8e692-130">Display a progress dialog box but do not show the file names.</span></span>

</dd> <dt>



 <span data-ttu-id="8e692-131"> (512) </span><span class="sxs-lookup"><span data-stu-id="8e692-131">(512)</span></span>


</dt> <dd>

<span data-ttu-id="8e692-132">如果作業需要建立新的目錄，請不要確認建立該目錄。</span><span class="sxs-lookup"><span data-stu-id="8e692-132">Do not confirm the creation of a new directory if the operation requires one to be created.</span></span>

</dd> <dt>



 <span data-ttu-id="8e692-133"> (1024) </span><span class="sxs-lookup"><span data-stu-id="8e692-133">(1024)</span></span>


</dt> <dd>

<span data-ttu-id="8e692-134">如果發生錯誤，則不顯示使用者介面。</span><span class="sxs-lookup"><span data-stu-id="8e692-134">Do not display a user interface if an error occurs.</span></span>

</dd> <dt>



 <span data-ttu-id="8e692-135"> (2048) </span><span class="sxs-lookup"><span data-stu-id="8e692-135">(2048)</span></span>


</dt> <dd>

[<span data-ttu-id="8e692-136">版本4.71。</span><span class="sxs-lookup"><span data-stu-id="8e692-136">Version 4.71.</span></span>](versions.md) <span data-ttu-id="8e692-137">請勿複製檔案的安全性屬性。</span><span class="sxs-lookup"><span data-stu-id="8e692-137">Do not copy the security attributes of the file.</span></span>

</dd> <dt>



 <span data-ttu-id="8e692-138"> (4096) </span><span class="sxs-lookup"><span data-stu-id="8e692-138">(4096)</span></span>


</dt> <dd>

<span data-ttu-id="8e692-139">只能在本機目錄中操作。</span><span class="sxs-lookup"><span data-stu-id="8e692-139">Only operate in the local directory.</span></span> <span data-ttu-id="8e692-140">請勿以遞迴方式操作子目錄。</span><span class="sxs-lookup"><span data-stu-id="8e692-140">Do not operate recursively into subdirectories.</span></span>

</dd> <dt>



 <span data-ttu-id="8e692-141"> (8192) </span><span class="sxs-lookup"><span data-stu-id="8e692-141">(8192)</span></span>


</dt> <dd>

[<span data-ttu-id="8e692-142">版本5.0。</span><span class="sxs-lookup"><span data-stu-id="8e692-142">Version 5.0.</span></span>](versions.md) <span data-ttu-id="8e692-143">請勿將連接的檔案複製為群組。</span><span class="sxs-lookup"><span data-stu-id="8e692-143">Do not copy connected files as a group.</span></span> <span data-ttu-id="8e692-144">只複製指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="8e692-144">Only copy the specified files.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e692-145">傳回值</span><span class="sxs-lookup"><span data-stu-id="8e692-145">Return value</span></span>

<span data-ttu-id="8e692-146">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8e692-146">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e692-147">備註</span><span class="sxs-lookup"><span data-stu-id="8e692-147">Remarks</span></span>

<span data-ttu-id="8e692-148">呼叫程式未提供任何通知，以指出複製已完成。</span><span class="sxs-lookup"><span data-stu-id="8e692-148">No notification is given to the calling program to indicate that the copy has completed.</span></span>

> [!Note]  
> <span data-ttu-id="8e692-149">並非所有的方法都會針對所有資料夾執行。</span><span class="sxs-lookup"><span data-stu-id="8e692-149">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="8e692-150">例如， [**ParseName**](folder-parsename.md) 方法不會針對主控台資料夾執行， (CSIDL \_ 控制項) 。</span><span class="sxs-lookup"><span data-stu-id="8e692-150">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="8e692-151">如果您嘗試呼叫未產生的方法，則會引發 0x800A01BD (decimal 445) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="8e692-151">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="8e692-152">範例</span><span class="sxs-lookup"><span data-stu-id="8e692-152">Examples</span></span>

<span data-ttu-id="8e692-153">下列範例會使用 **CopyHere** 將 Autoexec.bat 檔案從根目錄複寫到 C： \\ Windows 目錄。</span><span class="sxs-lookup"><span data-stu-id="8e692-153">The following example uses **CopyHere** to copy the Autoexec.bat file from the root directory to the C:\\Windows directory.</span></span> <span data-ttu-id="8e692-154">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="8e692-154">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="8e692-155">Jscript：</span><span class="sxs-lookup"><span data-stu-id="8e692-155">JScript:</span></span>


```JScript
<script language="JScript">
    function fnCopyHereJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            objFolder.CopyHere("C:\\AUTOEXEC.BAT");
        }
    }
 </script>
```



<span data-ttu-id="8e692-156">VBScript</span><span class="sxs-lookup"><span data-stu-id="8e692-156">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnCopyHereVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")
 
        if not objFolder is nothing then
            objFolder.CopyHere("C:\AUTOEXEC.BAT")
        end if
 
        set objShell = nothing
        set objFolder = nothing
    end function
</script>
```



<span data-ttu-id="8e692-157">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="8e692-157">Visual Basic:</span></span>


```VB
Private Sub btnCopyHere_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")
 
    If (Not objFolder Is Nothing) Then
        objFolder.CopyHere ("C:\AUTOEXEC.BAT")
    End If
 
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="8e692-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e692-158">Requirements</span></span>



| <span data-ttu-id="8e692-159">需求</span><span class="sxs-lookup"><span data-stu-id="8e692-159">Requirement</span></span> | <span data-ttu-id="8e692-160">值</span><span class="sxs-lookup"><span data-stu-id="8e692-160">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e692-161">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8e692-161">Minimum supported client</span></span><br/> | <span data-ttu-id="8e692-162">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8e692-162">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8e692-163">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8e692-163">Minimum supported server</span></span><br/> | <span data-ttu-id="8e692-164">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8e692-164">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8e692-165">標頭</span><span class="sxs-lookup"><span data-stu-id="8e692-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e692-166"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="8e692-166"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="8e692-167">Idl</span><span class="sxs-lookup"><span data-stu-id="8e692-167">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8e692-168"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="8e692-168"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="8e692-169">DLL</span><span class="sxs-lookup"><span data-stu-id="8e692-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e692-170"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="8e692-170"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e692-171">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8e692-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e692-172">**資料夾**</span><span class="sxs-lookup"><span data-stu-id="8e692-172">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




