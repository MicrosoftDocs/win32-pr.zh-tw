---
description: Shell. Windows 方法-建立並傳回 ShellWindows 物件。 此物件代表屬於 Shell 的所有已開啟視窗的集合。
title: 'Shell. Windows 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Windows
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ffa6311c-8bbe-45c4-9b06-069779d2306d
ms.openlocfilehash: bbe8ed55865322fc7436959fd80b478baa3c0b40
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842609"
---
# <a name="shellwindows-method"></a><span data-ttu-id="3e7c2-104">Shell. Windows 方法</span><span class="sxs-lookup"><span data-stu-id="3e7c2-104">Shell.Windows method</span></span>

<span data-ttu-id="3e7c2-105">建立並傳回 [**ShellWindows**](shellwindows.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="3e7c2-105">Creates and returns a [**ShellWindows**](shellwindows.md) object.</span></span> <span data-ttu-id="3e7c2-106">此物件代表屬於 Shell 的所有已開啟視窗的集合。</span><span class="sxs-lookup"><span data-stu-id="3e7c2-106">This object represents a collection of all of the open windows that belong to the Shell.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e7c2-107">語法</span><span class="sxs-lookup"><span data-stu-id="3e7c2-107">Syntax</span></span>


```JScript
retVal = Shell.Windows()
```


```VB

Shell.Windows() As IDispatch
```





## <a name="parameters"></a><span data-ttu-id="3e7c2-108">參數</span><span class="sxs-lookup"><span data-stu-id="3e7c2-108">Parameters</span></span>

<span data-ttu-id="3e7c2-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="3e7c2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3e7c2-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="3e7c2-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="3e7c2-111">JScript</span><span class="sxs-lookup"><span data-stu-id="3e7c2-111">JScript</span></span>

<span data-ttu-id="3e7c2-112">類型： **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="3e7c2-112">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="3e7c2-113">[**ShellWindows**](shellwindows.md)物件的物件參考。</span><span class="sxs-lookup"><span data-stu-id="3e7c2-113">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

### <a name="vb"></a><span data-ttu-id="3e7c2-114">VB</span><span class="sxs-lookup"><span data-stu-id="3e7c2-114">VB</span></span>

<span data-ttu-id="3e7c2-115">類型： **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="3e7c2-115">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="3e7c2-116">[**ShellWindows**](shellwindows.md)物件的物件參考。</span><span class="sxs-lookup"><span data-stu-id="3e7c2-116">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="3e7c2-117">範例</span><span class="sxs-lookup"><span data-stu-id="3e7c2-117">Examples</span></span>

<span data-ttu-id="3e7c2-118">下列範例會使用 **Windows** 來取出 [**ShellWindows**](shellwindows.md) 物件，並顯示其包含的專案數目計數。</span><span class="sxs-lookup"><span data-stu-id="3e7c2-118">The following example uses **Windows** to retrieve the [**ShellWindows**](shellwindows.md) object and display a count of the number of items that it contains.</span></span> <span data-ttu-id="3e7c2-119">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="3e7c2-119">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="3e7c2-120">Jscript：</span><span class="sxs-lookup"><span data-stu-id="3e7c2-120">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objShell.Windows();

        if (objShellWindows != null)
        {
            var Shell = new ActiveXObject("WScript.Shell");
            Shell.Popup(objShellWindows.Count);
        }
    }
</script>
```



<span data-ttu-id="3e7c2-121">VBScript</span><span class="sxs-lookup"><span data-stu-id="3e7c2-121">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsVBS()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objShell.Windows

        if (not objShellWindows is nothing) then
            WScript.Echo objShellWindows.Count
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="3e7c2-122">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="3e7c2-122">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objShell.Windows

    If (Not objShellWindows Is Nothing) Then
        Debug.Print objShellWindows.Count
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="3e7c2-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e7c2-123">Requirements</span></span>



| <span data-ttu-id="3e7c2-124">需求</span><span class="sxs-lookup"><span data-stu-id="3e7c2-124">Requirement</span></span> | <span data-ttu-id="3e7c2-125">值</span><span class="sxs-lookup"><span data-stu-id="3e7c2-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e7c2-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3e7c2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3e7c2-127">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3e7c2-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3e7c2-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3e7c2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3e7c2-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3e7c2-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3e7c2-130">標頭</span><span class="sxs-lookup"><span data-stu-id="3e7c2-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e7c2-131"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="3e7c2-131"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="3e7c2-132">Idl</span><span class="sxs-lookup"><span data-stu-id="3e7c2-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3e7c2-133"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="3e7c2-133"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="3e7c2-134">DLL</span><span class="sxs-lookup"><span data-stu-id="3e7c2-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e7c2-135"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="3e7c2-135"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
