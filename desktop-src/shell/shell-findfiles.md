---
description: 顯示 [尋找：所有檔案] 對話方塊。 這與按一下 [開始] 功能表，然後在 Windows XP 之前的系統中選取 [搜尋] (或其對等專案相同。
ms.assetid: cccdd3ea-b52a-4fbe-b4c5-1efc1dd6d770
title: 'Findfiles.ps1 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FindFiles
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f3e6551dc41fd8d6a040ada8000f0b46e81a5dd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194443"
---
# <a name="shellfindfiles-method"></a><span data-ttu-id="2b406-104">Findfiles.ps1 方法</span><span class="sxs-lookup"><span data-stu-id="2b406-104">Shell.FindFiles method</span></span>

<span data-ttu-id="2b406-105">顯示 [ **尋找：所有** 檔案] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="2b406-105">Displays the **Find: All Files** dialog box.</span></span> <span data-ttu-id="2b406-106">這等同于按一下 [ **開始** ] 功能表，然後選取 [ **搜尋** (] 或其對等專案（在 Windows XP 之前的系統下）。</span><span class="sxs-lookup"><span data-stu-id="2b406-106">This is the same as clicking the **Start** menu and then selecting **Search** (or its equivalent under systems earlier than Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b406-107">語法</span><span class="sxs-lookup"><span data-stu-id="2b406-107">Syntax</span></span>


```JScript
Shell.FindFiles()
```


```VB

Shell.FindFiles()
```





## <a name="parameters"></a><span data-ttu-id="2b406-108">參數</span><span class="sxs-lookup"><span data-stu-id="2b406-108">Parameters</span></span>

<span data-ttu-id="2b406-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2b406-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2b406-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="2b406-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="2b406-111">JScript</span><span class="sxs-lookup"><span data-stu-id="2b406-111">JScript</span></span>

<span data-ttu-id="2b406-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2b406-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="2b406-113">VB</span><span class="sxs-lookup"><span data-stu-id="2b406-113">VB</span></span>

<span data-ttu-id="2b406-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2b406-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="2b406-115">範例</span><span class="sxs-lookup"><span data-stu-id="2b406-115">Examples</span></span>

<span data-ttu-id="2b406-116">下列範例顯示使用中的 **findfiles.ps1** 。</span><span class="sxs-lookup"><span data-stu-id="2b406-116">The following example shows **FindFiles** in use.</span></span> <span data-ttu-id="2b406-117">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="2b406-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="2b406-118">Jscript：</span><span class="sxs-lookup"><span data-stu-id="2b406-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindFilesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.Shell_FindFiles();
    }
</script>
```



<span data-ttu-id="2b406-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="2b406-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellFindFilesVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.FindFiles

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="2b406-120">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="2b406-120">Visual Basic:</span></span>


```VB
Private Sub fnShellFindFilesVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindFiles

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="2b406-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b406-121">Requirements</span></span>



| <span data-ttu-id="2b406-122">需求</span><span class="sxs-lookup"><span data-stu-id="2b406-122">Requirement</span></span> | <span data-ttu-id="2b406-123">值</span><span class="sxs-lookup"><span data-stu-id="2b406-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b406-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2b406-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2b406-125">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b406-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2b406-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2b406-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2b406-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b406-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2b406-128">標頭</span><span class="sxs-lookup"><span data-stu-id="2b406-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b406-129"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="2b406-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="2b406-130">Idl</span><span class="sxs-lookup"><span data-stu-id="2b406-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2b406-131"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="2b406-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="2b406-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2b406-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b406-133"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="2b406-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




