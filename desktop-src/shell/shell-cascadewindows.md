---
description: 將桌面上的所有視窗都串聯在一起。 這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [串聯視窗] 相同。
ms.assetid: f73d2066-4626-455b-8ee6-f7004cc9e699
title: 'CascadeWindows 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.CascadeWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 751182ec53e0495021f4a6e2fad355c2c700ad66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513605"
---
# <a name="shellcascadewindows-method"></a><span data-ttu-id="45dae-104">CascadeWindows 方法</span><span class="sxs-lookup"><span data-stu-id="45dae-104">Shell.CascadeWindows method</span></span>

<span data-ttu-id="45dae-105">將桌面上的所有視窗都串聯在一起。</span><span class="sxs-lookup"><span data-stu-id="45dae-105">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="45dae-106">這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [串聯 **視窗**] 相同。</span><span class="sxs-lookup"><span data-stu-id="45dae-106">This method has the same effect as right-clicking the taskbar and selecting **Cascade Windows**.</span></span>

## <a name="syntax"></a><span data-ttu-id="45dae-107">語法</span><span class="sxs-lookup"><span data-stu-id="45dae-107">Syntax</span></span>


```JScript
Shell.CascadeWindows()
```


```VB

Shell.CascadeWindows()
```





## <a name="parameters"></a><span data-ttu-id="45dae-108">參數</span><span class="sxs-lookup"><span data-stu-id="45dae-108">Parameters</span></span>

<span data-ttu-id="45dae-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="45dae-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="45dae-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="45dae-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="45dae-111">JScript</span><span class="sxs-lookup"><span data-stu-id="45dae-111">JScript</span></span>

<span data-ttu-id="45dae-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="45dae-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="45dae-113">VB</span><span class="sxs-lookup"><span data-stu-id="45dae-113">VB</span></span>

<span data-ttu-id="45dae-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="45dae-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="45dae-115">範例</span><span class="sxs-lookup"><span data-stu-id="45dae-115">Examples</span></span>

<span data-ttu-id="45dae-116">下列範例顯示使用中的 **CascadeWindows** 。</span><span class="sxs-lookup"><span data-stu-id="45dae-116">The following example shows **CascadeWindows** in use.</span></span> <span data-ttu-id="45dae-117">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="45dae-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="45dae-118">Jscript：</span><span class="sxs-lookup"><span data-stu-id="45dae-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellCascadeWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.CascadeWindows();
    }
</script>
```



<span data-ttu-id="45dae-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="45dae-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellCascadeWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.CascadeWindows
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="45dae-120">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="45dae-120">Visual Basic:</span></span>


```VB
Private Sub fnShellCascadeWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.CascadeWindows
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="45dae-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="45dae-121">Requirements</span></span>



| <span data-ttu-id="45dae-122">需求</span><span class="sxs-lookup"><span data-stu-id="45dae-122">Requirement</span></span> | <span data-ttu-id="45dae-123">值</span><span class="sxs-lookup"><span data-stu-id="45dae-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45dae-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="45dae-124">Minimum supported client</span></span><br/> | <span data-ttu-id="45dae-125">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="45dae-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="45dae-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="45dae-126">Minimum supported server</span></span><br/> | <span data-ttu-id="45dae-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="45dae-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="45dae-128">標頭</span><span class="sxs-lookup"><span data-stu-id="45dae-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="45dae-129"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="45dae-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="45dae-130">Idl</span><span class="sxs-lookup"><span data-stu-id="45dae-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="45dae-131"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="45dae-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="45dae-132">DLL</span><span class="sxs-lookup"><span data-stu-id="45dae-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45dae-133"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="45dae-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




