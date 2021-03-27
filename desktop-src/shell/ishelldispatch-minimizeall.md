---
description: 最小化桌面上的所有視窗。 這個方法的效果與在工作列上按一下滑鼠右鍵，並選取 [將舊版系統上的所有視窗最小化]，或按一下工作列上的 [顯示桌面] 圖示。
ms.assetid: 25DD56B0-221E-44a2-9FAD-FB358ADD7FF1
title: 'IShellDispatch. MinimizeAll 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.MinimizeAll
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b8b8f20ab82a6216a03d772151f852fd9c69b917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512221"
---
# <a name="ishelldispatchminimizeall-method"></a><span data-ttu-id="758f4-104">IShellDispatch. MinimizeAll 方法</span><span class="sxs-lookup"><span data-stu-id="758f4-104">IShellDispatch.MinimizeAll method</span></span>

<span data-ttu-id="758f4-105">最小化桌面上的所有視窗。</span><span class="sxs-lookup"><span data-stu-id="758f4-105">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="758f4-106">這個方法的效果與在工作列上按一下滑鼠右鍵，並選取 [將舊版系統上的 **所有視窗最小化** ]，或按一下工作列上的 [ **顯示桌面** ] 圖示。</span><span class="sxs-lookup"><span data-stu-id="758f4-106">This method has the same effect as right-clicking the taskbar and selecting **Minimize All Windows** on older systems or clicking the **Show Desktop** icon on the taskbar.</span></span>

## <a name="syntax"></a><span data-ttu-id="758f4-107">語法</span><span class="sxs-lookup"><span data-stu-id="758f4-107">Syntax</span></span>


```JScript
IShellDispatch.MinimizeAll()
```


```VB

IShellDispatch.MinimizeAll()
```





## <a name="parameters"></a><span data-ttu-id="758f4-108">參數</span><span class="sxs-lookup"><span data-stu-id="758f4-108">Parameters</span></span>

<span data-ttu-id="758f4-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="758f4-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="758f4-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="758f4-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="758f4-111">JScript</span><span class="sxs-lookup"><span data-stu-id="758f4-111">JScript</span></span>

<span data-ttu-id="758f4-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="758f4-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="758f4-113">VB</span><span class="sxs-lookup"><span data-stu-id="758f4-113">VB</span></span>

<span data-ttu-id="758f4-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="758f4-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="758f4-115">備註</span><span class="sxs-lookup"><span data-stu-id="758f4-115">Remarks</span></span>

<span data-ttu-id="758f4-116">這個方法是透過 [**MinimizeAll**](shell-minimizeall.md) 方法來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="758f4-116">This method is implemented and accessed through the [**Shell.MinimizeAll**](shell-minimizeall.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="758f4-117">範例</span><span class="sxs-lookup"><span data-stu-id="758f4-117">Examples</span></span>

<span data-ttu-id="758f4-118">下列範例示範如何使用 **MinimizeAll** 在 JScript、VBScript 和 Visual Basic 中使用。</span><span class="sxs-lookup"><span data-stu-id="758f4-118">The following examples show the use of **MinimizeAll** in use for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="758f4-119">Jscript：</span><span class="sxs-lookup"><span data-stu-id="758f4-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellMinimizeAllJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.MinimizeAll();
    }
</script>
```



<span data-ttu-id="758f4-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="758f4-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellMinimizeAllVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.MinimizeAll

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="758f4-121">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="758f4-121">Visual Basic:</span></span>


```VB
Private Sub fnShellMinimizeAllVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.MinimizeAll

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="758f4-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="758f4-122">Requirements</span></span>



| <span data-ttu-id="758f4-123">需求</span><span class="sxs-lookup"><span data-stu-id="758f4-123">Requirement</span></span> | <span data-ttu-id="758f4-124">值</span><span class="sxs-lookup"><span data-stu-id="758f4-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="758f4-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="758f4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="758f4-126">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="758f4-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="758f4-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="758f4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="758f4-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="758f4-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="758f4-129">標頭</span><span class="sxs-lookup"><span data-stu-id="758f4-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="758f4-130"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="758f4-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="758f4-131">Idl</span><span class="sxs-lookup"><span data-stu-id="758f4-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="758f4-132"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="758f4-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="758f4-133">DLL</span><span class="sxs-lookup"><span data-stu-id="758f4-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="758f4-134"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="758f4-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="758f4-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="758f4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="758f4-136">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="758f4-136">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="758f4-137">**UndoMinimizeALL**</span><span class="sxs-lookup"><span data-stu-id="758f4-137">**UndoMinimizeALL**</span></span>](shell-undominimizeall.md)
</dt> </dl>

 

 




