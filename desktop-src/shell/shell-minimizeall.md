---
description: 最小化桌面上的所有視窗。
ms.assetid: 3af98a16-27d1-4c93-ac72-7c9e24e68c23
title: 'MinimizeAll 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.MinimizeAll
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 55b615cfed8813f5567b13d58648fef36aaedda3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973684"
---
# <a name="shellminimizeall-method"></a><span data-ttu-id="57490-103">MinimizeAll 方法</span><span class="sxs-lookup"><span data-stu-id="57490-103">Shell.MinimizeAll method</span></span>

<span data-ttu-id="57490-104">最小化桌面上的所有視窗。</span><span class="sxs-lookup"><span data-stu-id="57490-104">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="57490-105">這個方法的效果與在工作列上按一下滑鼠右鍵，並選取 [將舊版系統上的 **所有視窗最小化** ]，或在 windows 2000 或 windows XP 的工作列快速啟動區域中按一下 [ **顯示桌面** ] 圖示。</span><span class="sxs-lookup"><span data-stu-id="57490-105">This method has the same effect as right-clicking the taskbar and selecting **Minimize All Windows** on older systems or clicking the **Show Desktop** icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="57490-106">語法</span><span class="sxs-lookup"><span data-stu-id="57490-106">Syntax</span></span>


```JScript
iRetVal = Shell.MinimizeAll()
```


```VB

Shell.MinimizeAll() As Integer
```





## <a name="parameters"></a><span data-ttu-id="57490-107">參數</span><span class="sxs-lookup"><span data-stu-id="57490-107">Parameters</span></span>

<span data-ttu-id="57490-108">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="57490-108">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="57490-109">範例</span><span class="sxs-lookup"><span data-stu-id="57490-109">Examples</span></span>

<span data-ttu-id="57490-110">下列範例顯示使用中的 **MinimizeAll** 。</span><span class="sxs-lookup"><span data-stu-id="57490-110">The following example shows **MinimizeAll** in use.</span></span> <span data-ttu-id="57490-111">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="57490-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="57490-112">Jscript：</span><span class="sxs-lookup"><span data-stu-id="57490-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellMinimizeAllJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.MinimizeAll();
    }
</script>
```



<span data-ttu-id="57490-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="57490-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellMinimizeAllVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.MinimizeAll

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="57490-114">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="57490-114">Visual Basic:</span></span>


```VB
Private Sub fnShellMinimizeAllVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.MinimizeAll

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="57490-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="57490-115">Requirements</span></span>



| <span data-ttu-id="57490-116">需求</span><span class="sxs-lookup"><span data-stu-id="57490-116">Requirement</span></span> | <span data-ttu-id="57490-117">值</span><span class="sxs-lookup"><span data-stu-id="57490-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57490-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="57490-118">Minimum supported client</span></span><br/> | <span data-ttu-id="57490-119">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57490-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="57490-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="57490-120">Minimum supported server</span></span><br/> | <span data-ttu-id="57490-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57490-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="57490-122">標頭</span><span class="sxs-lookup"><span data-stu-id="57490-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="57490-123"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="57490-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="57490-124">Idl</span><span class="sxs-lookup"><span data-stu-id="57490-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="57490-125"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="57490-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="57490-126">DLL</span><span class="sxs-lookup"><span data-stu-id="57490-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57490-127"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="57490-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57490-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57490-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57490-129">**殼層**</span><span class="sxs-lookup"><span data-stu-id="57490-129">**Shell**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="57490-130">**UndoMinimizeALL**</span><span class="sxs-lookup"><span data-stu-id="57490-130">**UndoMinimizeALL**</span></span>](shell-undominimizeall.md)
</dt> </dl>

 

 




