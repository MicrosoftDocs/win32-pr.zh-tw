---
description: 顯示 [搜尋結果：電腦] 對話方塊。 此對話方塊會顯示指定電腦的搜尋結果。
ms.assetid: 9B687A8A-BB29-49a0-8AE3-11A75FAF3257
title: 'IShellDispatch. FindComputer 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.FindComputer
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3ad928b6860a85126a714a08f3bc3df9d4aff67c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972428"
---
# <a name="ishelldispatchfindcomputer-method"></a><span data-ttu-id="aa9de-104">IShellDispatch. FindComputer 方法</span><span class="sxs-lookup"><span data-stu-id="aa9de-104">IShellDispatch.FindComputer method</span></span>

<span data-ttu-id="aa9de-105">顯示 [ **搜尋結果：電腦** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="aa9de-105">Displays the **Search Results: Computers** dialog box.</span></span> <span data-ttu-id="aa9de-106">此對話方塊會顯示指定電腦的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="aa9de-106">The dialog box shows the result of the search for a specified computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa9de-107">語法</span><span class="sxs-lookup"><span data-stu-id="aa9de-107">Syntax</span></span>


```JScript
IShellDispatch.FindComputer()
```


```VB

IShellDispatch.FindComputer()
```





## <a name="parameters"></a><span data-ttu-id="aa9de-108">參數</span><span class="sxs-lookup"><span data-stu-id="aa9de-108">Parameters</span></span>

<span data-ttu-id="aa9de-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="aa9de-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aa9de-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="aa9de-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="aa9de-111">JScript</span><span class="sxs-lookup"><span data-stu-id="aa9de-111">JScript</span></span>

<span data-ttu-id="aa9de-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="aa9de-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="aa9de-113">VB</span><span class="sxs-lookup"><span data-stu-id="aa9de-113">VB</span></span>

<span data-ttu-id="aa9de-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="aa9de-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa9de-115">備註</span><span class="sxs-lookup"><span data-stu-id="aa9de-115">Remarks</span></span>

<span data-ttu-id="aa9de-116">這個方法是透過 [**FindComputer**](shell-findcomputer.md) 方法來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="aa9de-116">This method is implemented and accessed through the [**Shell.FindComputer**](shell-findcomputer.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="aa9de-117">範例</span><span class="sxs-lookup"><span data-stu-id="aa9de-117">Examples</span></span>

<span data-ttu-id="aa9de-118">下列範例示範如何在 JScript、VBScript 和 Visual Basic 中使用 **FindComputer** 。</span><span class="sxs-lookup"><span data-stu-id="aa9de-118">The following examples show the use of **FindComputer** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="aa9de-119">Jscript：</span><span class="sxs-lookup"><span data-stu-id="aa9de-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.FindComputer();
    }
</script>
```



<span data-ttu-id="aa9de-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="aa9de-120">VBScript:</span></span>


```VB
 <script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objshell.FindComputer

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="aa9de-121">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="aa9de-121">Visual Basic:</span></span>


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="aa9de-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa9de-122">Requirements</span></span>



| <span data-ttu-id="aa9de-123">需求</span><span class="sxs-lookup"><span data-stu-id="aa9de-123">Requirement</span></span> | <span data-ttu-id="aa9de-124">值</span><span class="sxs-lookup"><span data-stu-id="aa9de-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa9de-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aa9de-125">Minimum supported client</span></span><br/> | <span data-ttu-id="aa9de-126">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aa9de-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="aa9de-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aa9de-127">Minimum supported server</span></span><br/> | <span data-ttu-id="aa9de-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aa9de-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="aa9de-129">標頭</span><span class="sxs-lookup"><span data-stu-id="aa9de-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa9de-130"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="aa9de-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="aa9de-131">Idl</span><span class="sxs-lookup"><span data-stu-id="aa9de-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="aa9de-132"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="aa9de-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="aa9de-133">DLL</span><span class="sxs-lookup"><span data-stu-id="aa9de-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa9de-134"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="aa9de-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




