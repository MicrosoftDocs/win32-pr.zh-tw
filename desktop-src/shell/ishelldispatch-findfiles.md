---
description: 顯示 [尋找：所有檔案] 對話方塊。 這與按一下 [開始] 功能表然後選取 [搜尋] 相同。
ms.assetid: 6F588D5E-5B6E-4000-BAD5-B557FB975FCA
title: 'IShellDispatch. Findfiles.ps1 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.FindFiles
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9a9ea407d0ceccfe7706ed481aa80bcda9405ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848305"
---
# <a name="ishelldispatchfindfiles-method"></a><span data-ttu-id="cb94b-104">IShellDispatch. Findfiles.ps1 方法</span><span class="sxs-lookup"><span data-stu-id="cb94b-104">IShellDispatch.FindFiles method</span></span>

<span data-ttu-id="cb94b-105">顯示 [ **尋找：所有** 檔案] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="cb94b-105">Displays the **Find: All Files** dialog box.</span></span> <span data-ttu-id="cb94b-106">這等同于按一下 [ **開始** ] 功能表，然後選取 [ **搜尋**]。</span><span class="sxs-lookup"><span data-stu-id="cb94b-106">This is the same as clicking the **Start** menu and then selecting **Search**.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb94b-107">語法</span><span class="sxs-lookup"><span data-stu-id="cb94b-107">Syntax</span></span>


```JScript
IShellDispatch.FindFiles()
```


```VB

IShellDispatch.FindFiles()
```





## <a name="parameters"></a><span data-ttu-id="cb94b-108">參數</span><span class="sxs-lookup"><span data-stu-id="cb94b-108">Parameters</span></span>

<span data-ttu-id="cb94b-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="cb94b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cb94b-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="cb94b-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="cb94b-111">JScript</span><span class="sxs-lookup"><span data-stu-id="cb94b-111">JScript</span></span>

<span data-ttu-id="cb94b-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="cb94b-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="cb94b-113">VB</span><span class="sxs-lookup"><span data-stu-id="cb94b-113">VB</span></span>

<span data-ttu-id="cb94b-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="cb94b-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb94b-115">備註</span><span class="sxs-lookup"><span data-stu-id="cb94b-115">Remarks</span></span>

<span data-ttu-id="cb94b-116">這個方法是透過 [**findfiles.ps1**](shell-findfiles.md) 方法來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="cb94b-116">This method is implemented and accessed through the [**Shell.FindFiles**](shell-findfiles.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="cb94b-117">範例</span><span class="sxs-lookup"><span data-stu-id="cb94b-117">Examples</span></span>

<span data-ttu-id="cb94b-118">下列範例示範如何在 JScript、VBScript 和 Visual Basic 中使用 **findfiles.ps1** 。</span><span class="sxs-lookup"><span data-stu-id="cb94b-118">The following examples show the use of **FindFiles** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="cb94b-119">Jscript：</span><span class="sxs-lookup"><span data-stu-id="cb94b-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindFilesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindFiles();
    }
</script>
```



<span data-ttu-id="cb94b-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="cb94b-120">VBScript:</span></span>


```VB
<script language="VBScript">
   function fnShellFindFilesVB()
       dim objShell
       
       set objShell = CreateObject("shell.application")
       objshell.FindFiles

       set objShell = nothing
   end function
</script>
```



<span data-ttu-id="cb94b-121">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="cb94b-121">Visual Basic:</span></span>


```VB
Private Sub fnShellFindFilesVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindFiles

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="cb94b-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb94b-122">Requirements</span></span>



| <span data-ttu-id="cb94b-123">需求</span><span class="sxs-lookup"><span data-stu-id="cb94b-123">Requirement</span></span> | <span data-ttu-id="cb94b-124">值</span><span class="sxs-lookup"><span data-stu-id="cb94b-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb94b-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cb94b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cb94b-126">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb94b-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cb94b-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cb94b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cb94b-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb94b-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cb94b-129">標頭</span><span class="sxs-lookup"><span data-stu-id="cb94b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb94b-130"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="cb94b-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="cb94b-131">Idl</span><span class="sxs-lookup"><span data-stu-id="cb94b-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cb94b-132"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="cb94b-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="cb94b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="cb94b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb94b-134"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="cb94b-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




