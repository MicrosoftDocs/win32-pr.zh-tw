---
description: IShellDispatch4. ToggleDesktop 方法-顯示或隱藏桌面。
title: 'IShellDispatch4. ToggleDesktop 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.ToggleDesktop
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 60199e18-b8da-48a6-b316-e7f07ff44b78
ms.openlocfilehash: b635408ed8a44b8bb0d27e52c167470f80f61b18
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116816"
---
# <a name="ishelldispatch4toggledesktop-method"></a><span data-ttu-id="822d0-103">IShellDispatch4. ToggleDesktop 方法</span><span class="sxs-lookup"><span data-stu-id="822d0-103">IShellDispatch4.ToggleDesktop method</span></span>

<span data-ttu-id="822d0-104">顯示或隱藏桌面。</span><span class="sxs-lookup"><span data-stu-id="822d0-104">Displays or hides the desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="822d0-105">語法</span><span class="sxs-lookup"><span data-stu-id="822d0-105">Syntax</span></span>


```JScript
IShellDispatch4.ToggleDesktop()
```


```VB

IShellDispatch4.ToggleDesktop()
```





## <a name="parameters"></a><span data-ttu-id="822d0-106">參數</span><span class="sxs-lookup"><span data-stu-id="822d0-106">Parameters</span></span>

<span data-ttu-id="822d0-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="822d0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="822d0-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="822d0-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="822d0-109">JScript</span><span class="sxs-lookup"><span data-stu-id="822d0-109">JScript</span></span>

<span data-ttu-id="822d0-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="822d0-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="822d0-111">VB</span><span class="sxs-lookup"><span data-stu-id="822d0-111">VB</span></span>

<span data-ttu-id="822d0-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="822d0-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="822d0-113">備註</span><span class="sxs-lookup"><span data-stu-id="822d0-113">Remarks</span></span>

<span data-ttu-id="822d0-114">這個方法的效果與工作列上的 [ **顯示桌面** ] 按鈕相同。</span><span class="sxs-lookup"><span data-stu-id="822d0-114">This method has the same effect as the **Show Desktop** button on the taskbar.</span></span> <span data-ttu-id="822d0-115">它會隱藏所有開啟的視窗以顯示桌面，或顯示所有開啟的視窗來隱藏桌面。</span><span class="sxs-lookup"><span data-stu-id="822d0-115">It either hides all open windows to show the desktop or it hides the desktop by showing all open windows.</span></span> <span data-ttu-id="822d0-116">**ToggleDesktop** 方法不會顯示使用者介面，它只會叫用切換動作。</span><span class="sxs-lookup"><span data-stu-id="822d0-116">The **ToggleDesktop** method does not display a user interface, it just invokes the toggle action.</span></span>

## <a name="examples"></a><span data-ttu-id="822d0-117">範例</span><span class="sxs-lookup"><span data-stu-id="822d0-117">Examples</span></span>

<span data-ttu-id="822d0-118">下列範例示範如何適當地使用 JScript、VBScript 和 Visual Basic 的 **ToggleDesktop** 。</span><span class="sxs-lookup"><span data-stu-id="822d0-118">The following examples show the proper use of **ToggleDesktop** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="822d0-119">Jscript：</span><span class="sxs-lookup"><span data-stu-id="822d0-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch4ToggleDesktopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ToggleDesktop();
    }
</script>
```



<span data-ttu-id="822d0-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="822d0-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIShellDispatch4ToggleDesktopVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            objShell.ToggleDesktop
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="822d0-121">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="822d0-121">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4ToggleDesktopVB()
    Dim objShell As Shell
            
    Set objShell = New Shell
        objShell.ToggleDesktop
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="822d0-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="822d0-122">Requirements</span></span>



| <span data-ttu-id="822d0-123">需求</span><span class="sxs-lookup"><span data-stu-id="822d0-123">Requirement</span></span> | <span data-ttu-id="822d0-124">值</span><span class="sxs-lookup"><span data-stu-id="822d0-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="822d0-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="822d0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="822d0-126">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="822d0-126">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="822d0-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="822d0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="822d0-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="822d0-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="822d0-129">標頭</span><span class="sxs-lookup"><span data-stu-id="822d0-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="822d0-130"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="822d0-130"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="822d0-131">Idl</span><span class="sxs-lookup"><span data-stu-id="822d0-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="822d0-132"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="822d0-132"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="822d0-133">DLL</span><span class="sxs-lookup"><span data-stu-id="822d0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="822d0-134"><dt>Shell32.dll (6.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="822d0-134"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




