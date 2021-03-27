---
description: 將專案或專案移至此資料夾。
ms.assetid: 07723dc1-5d9d-4f32-ab18-52617b0988c4
title: 'MoveHere 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.MoveHere
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: da6590d63f4a3c79252e25f3625c0ee75b146b6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689267"
---
# <a name="foldermovehere-method"></a><span data-ttu-id="0615f-103">MoveHere 方法</span><span class="sxs-lookup"><span data-stu-id="0615f-103">Folder.MoveHere method</span></span>

<span data-ttu-id="0615f-104">將專案或專案移至此資料夾。</span><span class="sxs-lookup"><span data-stu-id="0615f-104">Moves an item or items to this folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="0615f-105">語法</span><span class="sxs-lookup"><span data-stu-id="0615f-105">Syntax</span></span>


```JScript
Folder.MoveHere(
  vItem,
  [ vOptions ]
)
```



## <a name="parameters"></a><span data-ttu-id="0615f-106">參數</span><span class="sxs-lookup"><span data-stu-id="0615f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0615f-107">*vItem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0615f-107">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0615f-108">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="0615f-108">Type: **Variant**</span></span>

<span data-ttu-id="0615f-109">要移動的專案。</span><span class="sxs-lookup"><span data-stu-id="0615f-109">The item or items to move.</span></span> <span data-ttu-id="0615f-110">這可以是代表檔案名、 [**FolderItem**](folderitem.md) 物件或 [**FolderItems**](folderitems.md) 物件的字串。</span><span class="sxs-lookup"><span data-stu-id="0615f-110">This can be a string that represents a file name, a [**FolderItem**](folderitem.md) object, or a [**FolderItems**](folderitems.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="0615f-111">*vOptions* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="0615f-111">*vOptions* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0615f-112">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="0615f-112">Type: **Variant**</span></span>

<span data-ttu-id="0615f-113">移動操作的選項。</span><span class="sxs-lookup"><span data-stu-id="0615f-113">Options for the move operation.</span></span> <span data-ttu-id="0615f-114">這個值可以是零或下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="0615f-114">This value can be zero or a combination of the following values.</span></span> <span data-ttu-id="0615f-115">這些值是根據定義來與 c + + [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa)結構的 **fFlags** 成員搭配使用的旗標。</span><span class="sxs-lookup"><span data-stu-id="0615f-115">These values are based upon flags defined for use with the **fFlags** member of the C++ [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) structure.</span></span> <span data-ttu-id="0615f-116">這些旗標並未定義為 Visual Basic、VBScript 或 JScript 的定義，因此您必須自行定義它們或使用其對等數值。</span><span class="sxs-lookup"><span data-stu-id="0615f-116">These flags are not defined as such for Visual Basic, VBScript, or JScript, so you must define them yourself or use their numeric equivalents.</span></span>

<dt>



 <span data-ttu-id="0615f-117">(4)</span><span class="sxs-lookup"><span data-stu-id="0615f-117">(4)</span></span>


</dt> <dd>

<span data-ttu-id="0615f-118">不要顯示進度對話方塊。</span><span class="sxs-lookup"><span data-stu-id="0615f-118">Do not display a progress dialog box.</span></span>

</dd> <dt>



 <span data-ttu-id="0615f-119">(8)</span><span class="sxs-lookup"><span data-stu-id="0615f-119">(8)</span></span>


</dt> <dd>

<span data-ttu-id="0615f-120">如果目標名稱的檔案已經存在，請將移動、複製或重新命名作業中的新名稱所要操作的檔案提供。</span><span class="sxs-lookup"><span data-stu-id="0615f-120">Give the file being operated on a new name in a move, copy, or rename operation if a file with the target name already exists.</span></span>

</dd> <dt>



 <span data-ttu-id="0615f-121">(16)</span><span class="sxs-lookup"><span data-stu-id="0615f-121">(16)</span></span>


</dt> <dd>

<span data-ttu-id="0615f-122">針對顯示的任何對話方塊，回應 [全部是]。</span><span class="sxs-lookup"><span data-stu-id="0615f-122">Respond with "Yes to All" for any dialog box that is displayed.</span></span>

</dd> <dt>



 <span data-ttu-id="0615f-123">(64)</span><span class="sxs-lookup"><span data-stu-id="0615f-123">(64)</span></span>


</dt> <dd>

<span data-ttu-id="0615f-124">盡可能保留復原資訊。</span><span class="sxs-lookup"><span data-stu-id="0615f-124">Preserve undo information, if possible.</span></span>

</dd> <dt>



 <span data-ttu-id="0615f-125"> (128) </span><span class="sxs-lookup"><span data-stu-id="0615f-125">(128)</span></span>


</dt> <dd>

<span data-ttu-id="0615f-126">只有在指定萬用字元檔案名 (時，才在檔案上執行操作。請 \* \*) 。</span><span class="sxs-lookup"><span data-stu-id="0615f-126">Perform the operation on files only if a wildcard file name (\*.\*) is specified.</span></span>

</dd> <dt>



 <span data-ttu-id="0615f-127"> (256) </span><span class="sxs-lookup"><span data-stu-id="0615f-127">(256)</span></span>


</dt> <dd>

<span data-ttu-id="0615f-128">顯示 [進度] 對話方塊，但不顯示檔案名。</span><span class="sxs-lookup"><span data-stu-id="0615f-128">Display a progress dialog box but do not show the file names.</span></span>

</dd> <dt>



 <span data-ttu-id="0615f-129"> (512) </span><span class="sxs-lookup"><span data-stu-id="0615f-129">(512)</span></span>


</dt> <dd>

<span data-ttu-id="0615f-130">如果作業需要建立新的目錄，請不要確認建立該目錄。</span><span class="sxs-lookup"><span data-stu-id="0615f-130">Do not confirm the creation of a new directory if the operation requires one to be created.</span></span>

</dd> <dt>



 <span data-ttu-id="0615f-131"> (1024) </span><span class="sxs-lookup"><span data-stu-id="0615f-131">(1024)</span></span>


</dt> <dd>

<span data-ttu-id="0615f-132">如果發生錯誤，則不顯示使用者介面。</span><span class="sxs-lookup"><span data-stu-id="0615f-132">Do not display a user interface if an error occurs.</span></span>

</dd> <dt>



 <span data-ttu-id="0615f-133"> (2048) </span><span class="sxs-lookup"><span data-stu-id="0615f-133">(2048)</span></span>


</dt> <dd>

[<span data-ttu-id="0615f-134">版本4.71。</span><span class="sxs-lookup"><span data-stu-id="0615f-134">Version 4.71.</span></span>](versions.md) <span data-ttu-id="0615f-135">請勿複製檔案的安全性屬性。</span><span class="sxs-lookup"><span data-stu-id="0615f-135">Do not copy the security attributes of the file.</span></span>

</dd> <dt>



 <span data-ttu-id="0615f-136"> (4096) </span><span class="sxs-lookup"><span data-stu-id="0615f-136">(4096)</span></span>


</dt> <dd>

<span data-ttu-id="0615f-137">只能在本機目錄中操作。</span><span class="sxs-lookup"><span data-stu-id="0615f-137">Only operate in the local directory.</span></span> <span data-ttu-id="0615f-138">請勿以遞迴方式操作子目錄。</span><span class="sxs-lookup"><span data-stu-id="0615f-138">Do not operate recursively into subdirectories.</span></span>

</dd> <dt>



 <span data-ttu-id="0615f-139"> (9182) </span><span class="sxs-lookup"><span data-stu-id="0615f-139">(9182)</span></span>


</dt> <dd>

[<span data-ttu-id="0615f-140">版本5.0。</span><span class="sxs-lookup"><span data-stu-id="0615f-140">Version 5.0.</span></span>](versions.md) <span data-ttu-id="0615f-141">請勿將連接的檔案移動為群組。</span><span class="sxs-lookup"><span data-stu-id="0615f-141">Do not move connected files as a group.</span></span> <span data-ttu-id="0615f-142">只移動指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="0615f-142">Only move the specified files.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0615f-143">傳回值</span><span class="sxs-lookup"><span data-stu-id="0615f-143">Return value</span></span>

<span data-ttu-id="0615f-144">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0615f-144">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0615f-145">備註</span><span class="sxs-lookup"><span data-stu-id="0615f-145">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0615f-146">並非所有的方法都會針對所有資料夾執行。</span><span class="sxs-lookup"><span data-stu-id="0615f-146">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="0615f-147">例如， [**ParseName**](folder-parsename.md) 方法不會針對主控台資料夾執行， (CSIDL \_ 控制項) 。</span><span class="sxs-lookup"><span data-stu-id="0615f-147">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="0615f-148">如果您嘗試呼叫未產生的方法，則會引發 0x800A01BD (decimal 445) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="0615f-148">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="0615f-149">範例</span><span class="sxs-lookup"><span data-stu-id="0615f-149">Examples</span></span>

<span data-ttu-id="0615f-150">下列範例會使用 **MoveHere** 將檔案 Temp.txt 從 c 磁片磁碟機的根目錄移至 c： \\ Windows 資料夾。</span><span class="sxs-lookup"><span data-stu-id="0615f-150">The following example uses **MoveHere** to move the file Temp.txt from the root directory of the C drive to the C:\\Windows folder.</span></span> <span data-ttu-id="0615f-151">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="0615f-151">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="0615f-152">Jscript：</span><span class="sxs-lookup"><span data-stu-id="0615f-152">JScript:</span></span>


```JScript
<script language="JScript">
    var FOF_NOCONFIRMATION = 16;

    function fnFolderObjectMoveHereJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            objFolder.MoveHere ("C:\\temp.txt", FOF_NOCONFIRMATION);
        }
    }
</script>
```



<span data-ttu-id="0615f-153">VBScript</span><span class="sxs-lookup"><span data-stu-id="0615f-153">VBScript:</span></span>


```VB
<script language="VBScript">
    private const FOF_NOCONFIRMATION = 16
    
    function fnFolderObjectMoveHereVB()
        dim objShell
        dim objFolder

        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            objFolder.MoveHere "C:\temp.txt", FOF_NOCONFIRMATION
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="0615f-154">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="0615f-154">Visual Basic:</span></span>


```VB
Private Const FOF_NOCONFIRMATION = &H10

Private Sub btnMoveHere_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        objFolder.MoveHere "c:\temp.txt", FOF_NOCONFIRMATION
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="0615f-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="0615f-155">Requirements</span></span>



| <span data-ttu-id="0615f-156">需求</span><span class="sxs-lookup"><span data-stu-id="0615f-156">Requirement</span></span> | <span data-ttu-id="0615f-157">值</span><span class="sxs-lookup"><span data-stu-id="0615f-157">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0615f-158">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0615f-158">Minimum supported client</span></span><br/> | <span data-ttu-id="0615f-159">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0615f-159">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0615f-160">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0615f-160">Minimum supported server</span></span><br/> | <span data-ttu-id="0615f-161">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0615f-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0615f-162">標頭</span><span class="sxs-lookup"><span data-stu-id="0615f-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="0615f-163"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="0615f-163"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="0615f-164">Idl</span><span class="sxs-lookup"><span data-stu-id="0615f-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0615f-165"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="0615f-165"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="0615f-166">DLL</span><span class="sxs-lookup"><span data-stu-id="0615f-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0615f-167"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="0615f-167"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




