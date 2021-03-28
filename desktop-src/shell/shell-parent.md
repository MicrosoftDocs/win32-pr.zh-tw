---
description: 取得物件，表示目前物件的父系。
ms.assetid: 76c2f72c-5ef6-4f2c-bdfc-62ced6dbc504
title: 'Shell. Parent 屬性 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Parent
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a121e4f87be1163429156f22dfe7bd55f1345f43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973257"
---
# <a name="shellparent-property"></a><span data-ttu-id="85331-103">Shell. Parent 屬性</span><span class="sxs-lookup"><span data-stu-id="85331-103">Shell.Parent property</span></span>

<span data-ttu-id="85331-104">取得物件，表示目前物件的父系。</span><span class="sxs-lookup"><span data-stu-id="85331-104">Gets an object that represents the parent of the current object.</span></span>

<span data-ttu-id="85331-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="85331-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="85331-106">語法</span><span class="sxs-lookup"><span data-stu-id="85331-106">Syntax</span></span>


```JScript
objParent = Shell.Parent
```


```VB

Property Parent As Object
```





## <a name="property-value"></a><span data-ttu-id="85331-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="85331-107">Property value</span></span>

<span data-ttu-id="85331-108">[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)型別的變數，可接收父物件。</span><span class="sxs-lookup"><span data-stu-id="85331-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the parent object.</span></span>

## <a name="examples"></a><span data-ttu-id="85331-109">範例</span><span class="sxs-lookup"><span data-stu-id="85331-109">Examples</span></span>

<span data-ttu-id="85331-110">下列範例示範如何適當地使用 JScript、VBScript 和 Visual Basic 的 **父系** 。</span><span class="sxs-lookup"><span data-stu-id="85331-110">The following example shows the proper use of **Parent** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="85331-111">Jscript：</span><span class="sxs-lookup"><span data-stu-id="85331-111">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellParentJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objParent;

        objParent = objShell.Parent;
        if (objParent != null)
        {
            alert("Got parent property");
        }
    }
</script>
```



<span data-ttu-id="85331-112">VBScript</span><span class="sxs-lookup"><span data-stu-id="85331-112">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellParentVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            if (not objShell is nothing) then
                dim objParent

                set objParent = objShell.Parent
                    if (not objParent is nothing) then
                        alert("Got parent property")
                    end if
                set objParent = nothing
            end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="85331-113">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="85331-113">Visual Basic:</span></span>


```VB
Private Sub fnShellParentVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        If (Not objShell Is Nothing) Then
            Dim objParent As Object
            
            Set objParent = objShell.Parent
                If (Not objParent Is Nothing) Then
                    Debug.Print "Got parent object"
                End If
            Set objParent = Nothing
        End If
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="85331-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="85331-114">Requirements</span></span>



| <span data-ttu-id="85331-115">需求</span><span class="sxs-lookup"><span data-stu-id="85331-115">Requirement</span></span> | <span data-ttu-id="85331-116">值</span><span class="sxs-lookup"><span data-stu-id="85331-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85331-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="85331-117">Minimum supported client</span></span><br/> | <span data-ttu-id="85331-118">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85331-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="85331-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="85331-119">Minimum supported server</span></span><br/> | <span data-ttu-id="85331-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85331-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="85331-121">標頭</span><span class="sxs-lookup"><span data-stu-id="85331-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="85331-122"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="85331-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="85331-123">Idl</span><span class="sxs-lookup"><span data-stu-id="85331-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="85331-124"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="85331-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="85331-125">DLL</span><span class="sxs-lookup"><span data-stu-id="85331-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85331-126"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="85331-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
