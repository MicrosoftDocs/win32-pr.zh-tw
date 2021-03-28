---
description: 將桌面上的所有視窗都串聯在一起。 這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [串聯視窗] 相同。
ms.assetid: 6A957D70-D6A3-4485-8DF3-7FD2C6DEFF78
title: 'IShellDispatch. CascadeWindows 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.CascadeWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4252e4df579bc73e9f082630f9f98b83e3b57f47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113984"
---
# <a name="ishelldispatchcascadewindows-method"></a><span data-ttu-id="deaa6-104">IShellDispatch. CascadeWindows 方法</span><span class="sxs-lookup"><span data-stu-id="deaa6-104">IShellDispatch.CascadeWindows method</span></span>

<span data-ttu-id="deaa6-105">將桌面上的所有視窗都串聯在一起。</span><span class="sxs-lookup"><span data-stu-id="deaa6-105">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="deaa6-106">這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [串聯 **視窗**] 相同。</span><span class="sxs-lookup"><span data-stu-id="deaa6-106">This method has the same effect as right-clicking the taskbar and selecting **Cascade windows**.</span></span>

## <a name="syntax"></a><span data-ttu-id="deaa6-107">語法</span><span class="sxs-lookup"><span data-stu-id="deaa6-107">Syntax</span></span>


```JScript
IShellDispatch.CascadeWindows()
```


```VB

IShellDispatch.CascadeWindows()
```





## <a name="parameters"></a><span data-ttu-id="deaa6-108">參數</span><span class="sxs-lookup"><span data-stu-id="deaa6-108">Parameters</span></span>

<span data-ttu-id="deaa6-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="deaa6-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="deaa6-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="deaa6-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="deaa6-111">JScript</span><span class="sxs-lookup"><span data-stu-id="deaa6-111">JScript</span></span>

<span data-ttu-id="deaa6-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="deaa6-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="deaa6-113">VB</span><span class="sxs-lookup"><span data-stu-id="deaa6-113">VB</span></span>

<span data-ttu-id="deaa6-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="deaa6-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="deaa6-115">備註</span><span class="sxs-lookup"><span data-stu-id="deaa6-115">Remarks</span></span>

<span data-ttu-id="deaa6-116">這個方法是透過 [**CascadeWindows**](shell-cascadewindows.md) 方法來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="deaa6-116">This method is implemented and accessed through the [**Shell.CascadeWindows**](shell-cascadewindows.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="deaa6-117">範例</span><span class="sxs-lookup"><span data-stu-id="deaa6-117">Examples</span></span>

<span data-ttu-id="deaa6-118">下列範例示範如何在 JScript、VBScript 和 Visual Basic 中使用 **CascadeWindows** 。</span><span class="sxs-lookup"><span data-stu-id="deaa6-118">The following examples show the use of **CascadeWindows** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="deaa6-119">Jscript：</span><span class="sxs-lookup"><span data-stu-id="deaa6-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellCascadeWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.CascadeWindows();
    }
</script>
```



<span data-ttu-id="deaa6-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="deaa6-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellCascadeWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.CascadeWindows
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="deaa6-121">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="deaa6-121">Visual Basic:</span></span>


```VB
Private Sub fnShellCascadeWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.CascadeWindows
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="deaa6-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="deaa6-122">Requirements</span></span>



| <span data-ttu-id="deaa6-123">需求</span><span class="sxs-lookup"><span data-stu-id="deaa6-123">Requirement</span></span> | <span data-ttu-id="deaa6-124">值</span><span class="sxs-lookup"><span data-stu-id="deaa6-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="deaa6-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="deaa6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="deaa6-126">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="deaa6-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="deaa6-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="deaa6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="deaa6-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="deaa6-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="deaa6-129">標頭</span><span class="sxs-lookup"><span data-stu-id="deaa6-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="deaa6-130"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="deaa6-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="deaa6-131">Idl</span><span class="sxs-lookup"><span data-stu-id="deaa6-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="deaa6-132"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="deaa6-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="deaa6-133">DLL</span><span class="sxs-lookup"><span data-stu-id="deaa6-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="deaa6-134"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="deaa6-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




