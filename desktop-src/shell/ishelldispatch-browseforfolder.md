---
description: IShellDispatch. BrowseForFolder 方法-建立一個對話方塊，讓使用者選取資料夾，然後傳回選取的資料夾資料夾物件。
ms.assetid: 578C51C1-F59B-4604-A09B-62BA61225ABB
title: 'IShellDispatch. BrowseForFolder 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.BrowseForFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ee6202c7029e2c27684e15d96dd6c38680cb0678
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086686"
---
# <a name="ishelldispatchbrowseforfolder-method"></a><span data-ttu-id="461db-103">IShellDispatch. BrowseForFolder 方法</span><span class="sxs-lookup"><span data-stu-id="461db-103">IShellDispatch.BrowseForFolder method</span></span>

<span data-ttu-id="461db-104">建立對話方塊，讓使用者選取資料夾，然後傳回選取的資料夾 [**資料夾**](folder.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="461db-104">Creates a dialog box that enables the user to select a folder and then returns the selected folder's [**Folder**](folder.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="461db-105">語法</span><span class="sxs-lookup"><span data-stu-id="461db-105">Syntax</span></span>


```JScript
retVal = IShellDispatch.BrowseForFolder(
  Hwnd,
  sTitle,
  iOptions,
  [ vRootFolder ]
)
```


```VB

IShellDispatch.BrowseForFolder( _
  ByVal Hwnd As Integer, _
  ByVal sTitle As BSTR, _
  ByVal iOptions As Integer, _
  [ ByVal vRootFolder As Variant ] _
) As FOLDER
```





## <a name="parameters"></a><span data-ttu-id="461db-106">參數</span><span class="sxs-lookup"><span data-stu-id="461db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="461db-107">*Hwnd* \[在\]</span><span class="sxs-lookup"><span data-stu-id="461db-107">*Hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="461db-108">類型： **整數**</span><span class="sxs-lookup"><span data-stu-id="461db-108">Type: **Integer**</span></span>

<span data-ttu-id="461db-109">對話方塊的父視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="461db-109">The handle to the parent window of the dialog box.</span></span> <span data-ttu-id="461db-110">此值可以是零。</span><span class="sxs-lookup"><span data-stu-id="461db-110">This value can be zero.</span></span>

</dd> <dt>

<span data-ttu-id="461db-111">*sTitle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="461db-111">*sTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="461db-112">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="461db-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="461db-113">表示在 [**流覽**] 對話方塊中顯示之標題的 **字串** 值。</span><span class="sxs-lookup"><span data-stu-id="461db-113">A **String** value that represents the title displayed inside the **Browse** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="461db-114">*microsoft.extensions.options.ioptions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="461db-114">*iOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="461db-115">類型： **整數**</span><span class="sxs-lookup"><span data-stu-id="461db-115">Type: **Integer**</span></span>

<span data-ttu-id="461db-116">**整數** 值，其中包含方法的選項。</span><span class="sxs-lookup"><span data-stu-id="461db-116">An **Integer** value that contains the options for the method.</span></span> <span data-ttu-id="461db-117">這可以是零或 [**BROWSEINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa)結構的 **ulFlags** 成員下所列的值組合。</span><span class="sxs-lookup"><span data-stu-id="461db-117">This can be zero or a combination of the values listed under the **ulFlags** member of the [**BROWSEINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) structure.</span></span>

</dd> <dt>

<span data-ttu-id="461db-118">*vRootFolder* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="461db-118">*vRootFolder* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="461db-119">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="461db-119">Type: **Variant**</span></span>

<span data-ttu-id="461db-120">要在對話方塊中使用的根資料夾。</span><span class="sxs-lookup"><span data-stu-id="461db-120">The root folder to use in the dialog box.</span></span> <span data-ttu-id="461db-121">使用者無法在樹狀結構中流覽高於此資料夾的位置。</span><span class="sxs-lookup"><span data-stu-id="461db-121">The user cannot browse higher in the tree than this folder.</span></span> <span data-ttu-id="461db-122">如果未指定此值，對話方塊中使用的根資料夾就是桌面。</span><span class="sxs-lookup"><span data-stu-id="461db-122">If this value is not specified, the root folder used in the dialog box is the desktop.</span></span> <span data-ttu-id="461db-123">這個值可以是指定資料夾路徑或其中一個 [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) 值的字串。</span><span class="sxs-lookup"><span data-stu-id="461db-123">This value can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="461db-124">請注意，在 **ShellSpecialFolderConstants** 中找到的常數名稱可以在 Visual Basic 中使用，但不能在 VBScript 或 JScript 中使用。</span><span class="sxs-lookup"><span data-stu-id="461db-124">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="461db-125">在這些情況下，必須在其位置使用數值。</span><span class="sxs-lookup"><span data-stu-id="461db-125">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="461db-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="461db-126">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="461db-127">JScript</span><span class="sxs-lookup"><span data-stu-id="461db-127">JScript</span></span>

<span data-ttu-id="461db-128">類型：**資料夾 \* \***</span><span class="sxs-lookup"><span data-stu-id="461db-128">Type: **FOLDER\*\***</span></span>

<span data-ttu-id="461db-129">所選資料夾之 [**資料夾**](folder.md) 物件的物件參考。</span><span class="sxs-lookup"><span data-stu-id="461db-129">An object reference to the selected folder's [**Folder**](folder.md) object.</span></span>

### <a name="vb"></a><span data-ttu-id="461db-130">VB</span><span class="sxs-lookup"><span data-stu-id="461db-130">VB</span></span>

<span data-ttu-id="461db-131">類型：**資料夾 \* \***</span><span class="sxs-lookup"><span data-stu-id="461db-131">Type: **FOLDER\*\***</span></span>

<span data-ttu-id="461db-132">所選資料夾之 [**資料夾**](folder.md) 物件的物件參考。</span><span class="sxs-lookup"><span data-stu-id="461db-132">An object reference to the selected folder's [**Folder**](folder.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="461db-133">備註</span><span class="sxs-lookup"><span data-stu-id="461db-133">Remarks</span></span>

<span data-ttu-id="461db-134">這個方法是透過 [**BrowseForFolder**](shell-browseforfolder.md) 方法來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="461db-134">This method is implemented and accessed through the [**Shell.BrowseForFolder**](shell-browseforfolder.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="461db-135">範例</span><span class="sxs-lookup"><span data-stu-id="461db-135">Examples</span></span>

<span data-ttu-id="461db-136">下列範例會使用 **BrowseForFolder** ，在 Windows 資料夾上顯示標題為 "Example" 的流覽視窗。</span><span class="sxs-lookup"><span data-stu-id="461db-136">The following examples use **BrowseForFolder** to display a browse window titled "Example" rooted at the Windows folder.</span></span> <span data-ttu-id="461db-137">JScript、VBScript 和 Visual Basic 會顯示使用方式。</span><span class="sxs-lookup"><span data-stu-id="461db-137">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="461db-138">Jscript：</span><span class="sxs-lookup"><span data-stu-id="461db-138">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellBrowseForFolderJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36;
        var objFolder;
        
        objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS);
        if (objFolder != null)
        {
            // Add code here.
        }
    }
</script>
```



<span data-ttu-id="461db-139">VBScript</span><span class="sxs-lookup"><span data-stu-id="461db-139">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellBrowseForFolderVB()
        dim objShell
        dim ssfWINDOWS
        dim objFolder
        
        ssfWINDOWS = 36
        set objShell = CreateObject("shell.application")
            set objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
                if (not objFolder is nothing) then
                    'Add code here.
                end if
            set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="461db-140">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="461db-140">Visual Basic:</span></span>


```VB
Private Sub fnShellBrowseForFolderVB()
    Dim objShell   As Shell
    Dim ssfWINDOWS As Long
    Dim objFolder  As Folder
    
    ssfWINDOWS = 36
    Set objShell = New Shell
        Set objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
            If (Not objFolder Is Nothing) Then
                'Add code here
            End If
        Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="461db-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="461db-141">Requirements</span></span>



| <span data-ttu-id="461db-142">需求</span><span class="sxs-lookup"><span data-stu-id="461db-142">Requirement</span></span> | <span data-ttu-id="461db-143">值</span><span class="sxs-lookup"><span data-stu-id="461db-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="461db-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="461db-144">Minimum supported client</span></span><br/> | <span data-ttu-id="461db-145">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="461db-145">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="461db-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="461db-146">Minimum supported server</span></span><br/> | <span data-ttu-id="461db-147">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="461db-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="461db-148">標頭</span><span class="sxs-lookup"><span data-stu-id="461db-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="461db-149"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="461db-149"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="461db-150">Idl</span><span class="sxs-lookup"><span data-stu-id="461db-150">IDL</span></span><br/>                      | <dl> <span data-ttu-id="461db-151"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="461db-151"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="461db-152">DLL</span><span class="sxs-lookup"><span data-stu-id="461db-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="461db-153"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="461db-153"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
