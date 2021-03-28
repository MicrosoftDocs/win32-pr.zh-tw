---
description: 將所有桌面視窗還原到最後一個 MinimizeAll 命令之前的相同狀態。
ms.assetid: dcedfa18-6dde-4fb8-9679-4d6ff80249e4
title: 'UndoMinimizeALL 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.UndoMinimizeALL
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4a5010e4ac6b4fca42689f7c80db50c55ab2cb4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193339"
---
# <a name="shellundominimizeall-method"></a><span data-ttu-id="89c6b-103">UndoMinimizeALL 方法</span><span class="sxs-lookup"><span data-stu-id="89c6b-103">Shell.UndoMinimizeALL method</span></span>

<span data-ttu-id="89c6b-104">將所有桌面視窗還原到最後一個 [**MinimizeAll**](shell-minimizeall.md) 命令之前的相同狀態。</span><span class="sxs-lookup"><span data-stu-id="89c6b-104">Restores all desktop windows to the same state they were in before the last [**MinimizeAll**](shell-minimizeall.md) command.</span></span> <span data-ttu-id="89c6b-105">這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [復原]，將舊版系統上的 **所有視窗最小化** ，或第二次按一下 windows 2000 或 windows XP 中工作列的 [快速啟動] 區域中的 [ **顯示桌面** ] 圖示。</span><span class="sxs-lookup"><span data-stu-id="89c6b-105">This method has the same effect as right-clicking the taskbar and selecting **Undo Minimize All Windows** on older systems or a second clicking of the **Show Desktop** icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="89c6b-106">語法</span><span class="sxs-lookup"><span data-stu-id="89c6b-106">Syntax</span></span>


```JScript
iRetVal = Shell.UndoMinimizeALL()
```


```VB

Shell.UndoMinimizeALL() As Integer
```





## <a name="parameters"></a><span data-ttu-id="89c6b-107">參數</span><span class="sxs-lookup"><span data-stu-id="89c6b-107">Parameters</span></span>

<span data-ttu-id="89c6b-108">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="89c6b-108">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="89c6b-109">範例</span><span class="sxs-lookup"><span data-stu-id="89c6b-109">Examples</span></span>

<span data-ttu-id="89c6b-110">下列範例顯示使用中的 **UndoMinimizeALL** 。</span><span class="sxs-lookup"><span data-stu-id="89c6b-110">The following example shows **UndoMinimizeALL** in use.</span></span> <span data-ttu-id="89c6b-111">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="89c6b-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="89c6b-112">Jscript：</span><span class="sxs-lookup"><span data-stu-id="89c6b-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellUndoMinimizeALLJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.UndoMinimizeALL();
    }
</script>
```



<span data-ttu-id="89c6b-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="89c6b-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellUndoMinimizeALLVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.UndoMinimizeALL

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="89c6b-114">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="89c6b-114">Visual Basic:</span></span>


```VB
Private Sub fnShellUndoMinimizeAllVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.UndoMinimizeALL

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="89c6b-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="89c6b-115">Requirements</span></span>



| <span data-ttu-id="89c6b-116">需求</span><span class="sxs-lookup"><span data-stu-id="89c6b-116">Requirement</span></span> | <span data-ttu-id="89c6b-117">值</span><span class="sxs-lookup"><span data-stu-id="89c6b-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89c6b-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="89c6b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="89c6b-119">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89c6b-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="89c6b-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="89c6b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="89c6b-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89c6b-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="89c6b-122">標頭</span><span class="sxs-lookup"><span data-stu-id="89c6b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="89c6b-123"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="89c6b-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="89c6b-124">Idl</span><span class="sxs-lookup"><span data-stu-id="89c6b-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="89c6b-125"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="89c6b-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="89c6b-126">DLL</span><span class="sxs-lookup"><span data-stu-id="89c6b-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89c6b-127"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="89c6b-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




