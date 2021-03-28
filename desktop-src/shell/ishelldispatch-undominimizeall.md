---
description: 將所有桌面視窗還原到最後一個 MinimizeAll 命令之前的狀態。
ms.assetid: 32BDE544-C4FF-4a64-99AF-F8960AEC4690
title: 'IShellDispatch. UndoMinimizeALL 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.UndoMinimizeALL
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1b11fdd7a0a82a11baa20b0f3a63a31a8a46b701
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512216"
---
# <a name="ishelldispatchundominimizeall-method"></a><span data-ttu-id="9e1fa-103">IShellDispatch. UndoMinimizeALL 方法</span><span class="sxs-lookup"><span data-stu-id="9e1fa-103">IShellDispatch.UndoMinimizeALL method</span></span>

<span data-ttu-id="9e1fa-104">將所有桌面視窗還原到最後一個 [**MinimizeAll**](shell-minimizeall.md) 命令之前的狀態。</span><span class="sxs-lookup"><span data-stu-id="9e1fa-104">Restores all desktop windows to the state they were in before the last [**MinimizeAll**](shell-minimizeall.md) command.</span></span> <span data-ttu-id="9e1fa-105">這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [ **復原最小化** 舊系統上的所有 Windows (]) 或第二次按一下工作列中的 [ **顯示桌面** ] 圖示。</span><span class="sxs-lookup"><span data-stu-id="9e1fa-105">This method has the same effect as right-clicking the taskbar and selecting **Undo Minimize All Windows** (on older systems) or a second clicking of the **Show Desktop** icon in the taskbar.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e1fa-106">語法</span><span class="sxs-lookup"><span data-stu-id="9e1fa-106">Syntax</span></span>


```JScript
IShellDispatch.UndoMinimizeALL()
```


```VB

IShellDispatch.UndoMinimizeALL()
```





## <a name="parameters"></a><span data-ttu-id="9e1fa-107">參數</span><span class="sxs-lookup"><span data-stu-id="9e1fa-107">Parameters</span></span>

<span data-ttu-id="9e1fa-108">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="9e1fa-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9e1fa-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="9e1fa-109">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="9e1fa-110">JScript</span><span class="sxs-lookup"><span data-stu-id="9e1fa-110">JScript</span></span>

<span data-ttu-id="9e1fa-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9e1fa-111">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="9e1fa-112">VB</span><span class="sxs-lookup"><span data-stu-id="9e1fa-112">VB</span></span>

<span data-ttu-id="9e1fa-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9e1fa-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e1fa-114">備註</span><span class="sxs-lookup"><span data-stu-id="9e1fa-114">Remarks</span></span>

<span data-ttu-id="9e1fa-115">這個方法是透過 [**UndoMinimizeAll**](./shell-undominimizeall.md) 方法來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="9e1fa-115">This method is implemented and accessed through the [**Shell.UndoMinimizeAll**](./shell-undominimizeall.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="9e1fa-116">範例</span><span class="sxs-lookup"><span data-stu-id="9e1fa-116">Examples</span></span>

<span data-ttu-id="9e1fa-117">下列範例示範如何在 JScript、VBScript 和 Visual Basic 中使用 **UndoMinimizeALL** 。</span><span class="sxs-lookup"><span data-stu-id="9e1fa-117">The following examples show the use of **UndoMinimizeALL** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="9e1fa-118">Jscript：</span><span class="sxs-lookup"><span data-stu-id="9e1fa-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellUndoMinimizeALLJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.UndoMinimizeALL();
    }
</script>
```



<span data-ttu-id="9e1fa-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="9e1fa-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellUndoMinimizeALLVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.UndoMinimizeALL

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="9e1fa-120">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="9e1fa-120">Visual Basic:</span></span>


```VB
Private Sub fnShellUndoMinimizeAllVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.UndoMinimizeALL

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="9e1fa-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="9e1fa-121">Requirements</span></span>



| <span data-ttu-id="9e1fa-122">需求</span><span class="sxs-lookup"><span data-stu-id="9e1fa-122">Requirement</span></span> | <span data-ttu-id="9e1fa-123">值</span><span class="sxs-lookup"><span data-stu-id="9e1fa-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e1fa-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9e1fa-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9e1fa-125">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9e1fa-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9e1fa-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9e1fa-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9e1fa-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9e1fa-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9e1fa-128">標頭</span><span class="sxs-lookup"><span data-stu-id="9e1fa-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e1fa-129"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="9e1fa-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="9e1fa-130">Idl</span><span class="sxs-lookup"><span data-stu-id="9e1fa-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9e1fa-131"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="9e1fa-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="9e1fa-132">DLL</span><span class="sxs-lookup"><span data-stu-id="9e1fa-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e1fa-133"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="9e1fa-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
