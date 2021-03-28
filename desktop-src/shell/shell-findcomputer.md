---
description: 顯示 [搜尋結果：電腦] 對話方塊。 此對話方塊會顯示指定電腦的搜尋結果。
ms.assetid: 0304b955-afde-4de4-824a-9ec9c9530360
title: 'FindComputer 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FindComputer
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3824eeb98bfac11e007d1bf7dd9f89153a7b73ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973693"
---
# <a name="shellfindcomputer-method"></a><span data-ttu-id="4f71a-104">FindComputer 方法</span><span class="sxs-lookup"><span data-stu-id="4f71a-104">Shell.FindComputer method</span></span>

<span data-ttu-id="4f71a-105">顯示 [ **搜尋結果：電腦** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="4f71a-105">Displays the **Search Results: Computers** dialog box.</span></span> <span data-ttu-id="4f71a-106">此對話方塊會顯示指定電腦的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="4f71a-106">The dialog box shows the result of the search for a specified computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f71a-107">語法</span><span class="sxs-lookup"><span data-stu-id="4f71a-107">Syntax</span></span>


```JScript
Shell.FindComputer()
```


```VB

Shell.FindComputer()
```





## <a name="parameters"></a><span data-ttu-id="4f71a-108">參數</span><span class="sxs-lookup"><span data-stu-id="4f71a-108">Parameters</span></span>

<span data-ttu-id="4f71a-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="4f71a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4f71a-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="4f71a-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="4f71a-111">JScript</span><span class="sxs-lookup"><span data-stu-id="4f71a-111">JScript</span></span>

<span data-ttu-id="4f71a-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4f71a-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="4f71a-113">VB</span><span class="sxs-lookup"><span data-stu-id="4f71a-113">VB</span></span>

<span data-ttu-id="4f71a-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4f71a-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="4f71a-115">範例</span><span class="sxs-lookup"><span data-stu-id="4f71a-115">Examples</span></span>

<span data-ttu-id="4f71a-116">下列範例顯示使用中的 **FindComputer** 。</span><span class="sxs-lookup"><span data-stu-id="4f71a-116">The following example shows **FindComputer** in use.</span></span> <span data-ttu-id="4f71a-117">此程式碼的結果與按下 [ **開始** ] 按鈕、按一下 [ **搜尋**]、按一下 [ **印表機]、[電腦] 或 [人員** ] 選項，然後按一下 **網路上的電腦** 一樣。</span><span class="sxs-lookup"><span data-stu-id="4f71a-117">The result of this code is the same as pressing the **Start** button, clicking **Search**, clicking the **Printers, computers, or people** option, then clicking **A computer on the network**.</span></span> <span data-ttu-id="4f71a-118">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="4f71a-118">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="4f71a-119">Jscript：</span><span class="sxs-lookup"><span data-stu-id="4f71a-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindComputer();
    }
</script>
```



<span data-ttu-id="4f71a-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="4f71a-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objShell.FindComputer

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="4f71a-121">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="4f71a-121">Visual Basic:</span></span>


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="4f71a-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="4f71a-122">Requirements</span></span>



| <span data-ttu-id="4f71a-123">需求</span><span class="sxs-lookup"><span data-stu-id="4f71a-123">Requirement</span></span> | <span data-ttu-id="4f71a-124">值</span><span class="sxs-lookup"><span data-stu-id="4f71a-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f71a-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4f71a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4f71a-126">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4f71a-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4f71a-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4f71a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4f71a-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4f71a-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4f71a-129">標頭</span><span class="sxs-lookup"><span data-stu-id="4f71a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f71a-130"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="4f71a-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="4f71a-131">Idl</span><span class="sxs-lookup"><span data-stu-id="4f71a-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4f71a-132"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="4f71a-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="4f71a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="4f71a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f71a-134"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="4f71a-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




