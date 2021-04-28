---
description: ShellWindows： Count 屬性-包含集合中的專案數。
ms.assetid: 0113cc32-2197-4004-99a1-89fe10828e5f
title: 'ShellWindows： Count 屬性 (Exdisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows.Count
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b2b33dc11e6bf909043ac5391965e1ebd225d376
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103936"
---
# <a name="shellwindowscount-property"></a><span data-ttu-id="259da-103">ShellWindows Count 屬性</span><span class="sxs-lookup"><span data-stu-id="259da-103">ShellWindows.Count property</span></span>

<span data-ttu-id="259da-104">包含集合中的專案數。</span><span class="sxs-lookup"><span data-stu-id="259da-104">Contains the number of items in the collection.</span></span>

<span data-ttu-id="259da-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="259da-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="259da-106">語法</span><span class="sxs-lookup"><span data-stu-id="259da-106">Syntax</span></span>


```JScript
iCount = ShellWindows.Count
```



## <a name="property-value"></a><span data-ttu-id="259da-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="259da-107">Property value</span></span>

<span data-ttu-id="259da-108">包含 **Count** 屬性值的 **整數**。</span><span class="sxs-lookup"><span data-stu-id="259da-108">An **Integer** that contains a value for the **Count** property.</span></span>

## <a name="examples"></a><span data-ttu-id="259da-109">範例</span><span class="sxs-lookup"><span data-stu-id="259da-109">Examples</span></span>

<span data-ttu-id="259da-110">下列範例顯示使用中的 **計數** 。</span><span class="sxs-lookup"><span data-stu-id="259da-110">The following example shows **Count** in use.</span></span> <span data-ttu-id="259da-111">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="259da-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="259da-112">Jscript：</span><span class="sxs-lookup"><span data-stu-id="259da-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellWindowsCountJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objshell.Shell_Windows();
        if (objShellWindows != null)
        {
            var nCount;
            
            nCount = objShellWindows.Count;
            alert(nCount);
        }
    }
</script>
```



<span data-ttu-id="259da-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="259da-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsCountVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Shell_Windows

        if (not objShellWindows is nothing) then
            dim nCount
            nCount = objShellWindows.Count

            alert(nCount)
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="259da-114">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="259da-114">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsCountVB()
    Dim objShell         As Shell
    Dim objShellWindows  As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Shell_Windows

    If (Not objShellWindows Is Nothing) Then
        Debug.Print objShellWindows.Count
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="259da-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="259da-115">Requirements</span></span>



| <span data-ttu-id="259da-116">需求</span><span class="sxs-lookup"><span data-stu-id="259da-116">Requirement</span></span> | <span data-ttu-id="259da-117">值</span><span class="sxs-lookup"><span data-stu-id="259da-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="259da-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="259da-118">Minimum supported client</span></span><br/> | <span data-ttu-id="259da-119">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="259da-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="259da-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="259da-120">Minimum supported server</span></span><br/> | <span data-ttu-id="259da-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="259da-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="259da-122">標頭</span><span class="sxs-lookup"><span data-stu-id="259da-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="259da-123"><dt>Exdisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="259da-123"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="259da-124">DLL</span><span class="sxs-lookup"><span data-stu-id="259da-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="259da-125"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="259da-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




