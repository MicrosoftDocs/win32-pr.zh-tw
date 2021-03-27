---
description: 建立並傳回 ShellWindows 物件。 此物件代表屬於 Shell 的所有已開啟視窗的集合。
ms.assetid: 788E2106-3534-4e22-801F-677FD02BDFE0
title: 'IShellDispatch 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Windows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: cb5f84caebf38deb27c7fb60565167793fead561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691216"
---
# <a name="ishelldispatchwindows-method"></a><span data-ttu-id="f1eeb-104">IShellDispatch 方法</span><span class="sxs-lookup"><span data-stu-id="f1eeb-104">IShellDispatch.Windows method</span></span>

<span data-ttu-id="f1eeb-105">建立並傳回 [**ShellWindows**](shellwindows.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="f1eeb-105">Creates and returns a [**ShellWindows**](shellwindows.md) object.</span></span> <span data-ttu-id="f1eeb-106">此物件代表屬於 Shell 的所有已開啟視窗的集合。</span><span class="sxs-lookup"><span data-stu-id="f1eeb-106">This object represents a collection of all of the open windows that belong to the Shell.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1eeb-107">語法</span><span class="sxs-lookup"><span data-stu-id="f1eeb-107">Syntax</span></span>


```JScript
retVal = IShellDispatch.Windows()
```


```VB

IShellDispatch.Windows() As IDispatch
```





## <a name="parameters"></a><span data-ttu-id="f1eeb-108">參數</span><span class="sxs-lookup"><span data-stu-id="f1eeb-108">Parameters</span></span>

<span data-ttu-id="f1eeb-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="f1eeb-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f1eeb-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="f1eeb-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="f1eeb-111">JScript</span><span class="sxs-lookup"><span data-stu-id="f1eeb-111">JScript</span></span>

<span data-ttu-id="f1eeb-112">類型： **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="f1eeb-112">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="f1eeb-113">[**ShellWindows**](shellwindows.md)物件的物件參考。</span><span class="sxs-lookup"><span data-stu-id="f1eeb-113">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

### <a name="vb"></a><span data-ttu-id="f1eeb-114">VB</span><span class="sxs-lookup"><span data-stu-id="f1eeb-114">VB</span></span>

<span data-ttu-id="f1eeb-115">類型： **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="f1eeb-115">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="f1eeb-116">[**ShellWindows**](shellwindows.md)物件的物件參考。</span><span class="sxs-lookup"><span data-stu-id="f1eeb-116">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1eeb-117">備註</span><span class="sxs-lookup"><span data-stu-id="f1eeb-117">Remarks</span></span>

<span data-ttu-id="f1eeb-118">這個方法是透過 [**Shell. Windows**](shell-windows.md) 方法來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="f1eeb-118">This method is implemented and accessed through the [**Shell.Windows**](shell-windows.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="f1eeb-119">範例</span><span class="sxs-lookup"><span data-stu-id="f1eeb-119">Examples</span></span>

<span data-ttu-id="f1eeb-120">下列範例會使用 **Windows** 抓取 [**ShellWindows**](shellwindows.md) 物件，並顯示它所包含的專案數計數。</span><span class="sxs-lookup"><span data-stu-id="f1eeb-120">The following examples use **Windows** to retrieve the [**ShellWindows**](shellwindows.md) object and display a count of the number of items that it contains.</span></span> <span data-ttu-id="f1eeb-121">JScript、VBScript 和 Visual Basic 會顯示使用方式。</span><span class="sxs-lookup"><span data-stu-id="f1eeb-121">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="f1eeb-122">Jscript：</span><span class="sxs-lookup"><span data-stu-id="f1eeb-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objshell.Windows();

        if (objShellWindows != null)
        {
            alert(objShellWindows.Count);
        }
    }
</script>
```



<span data-ttu-id="f1eeb-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="f1eeb-123">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Windows

        if (not objShellWindows is nothing) then
            alert(objShellWindows.Count)
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="f1eeb-124">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="f1eeb-124">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Windows

    If (Not objShellWindows Is Nothing) Then
        Debug.Print objShellWindows.Count
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="f1eeb-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1eeb-125">Requirements</span></span>



| <span data-ttu-id="f1eeb-126">需求</span><span class="sxs-lookup"><span data-stu-id="f1eeb-126">Requirement</span></span> | <span data-ttu-id="f1eeb-127">值</span><span class="sxs-lookup"><span data-stu-id="f1eeb-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1eeb-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1eeb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f1eeb-129">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1eeb-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f1eeb-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1eeb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f1eeb-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1eeb-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f1eeb-132">標頭</span><span class="sxs-lookup"><span data-stu-id="f1eeb-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1eeb-133"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="f1eeb-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f1eeb-134">Idl</span><span class="sxs-lookup"><span data-stu-id="f1eeb-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f1eeb-135"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f1eeb-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f1eeb-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f1eeb-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1eeb-137"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="f1eeb-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
