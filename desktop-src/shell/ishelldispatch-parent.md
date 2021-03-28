---
description: 抓取物件，該物件表示目前物件的父系。
ms.assetid: 2FDEF8D3-3F5B-43ae-9812-83B4249D9CBB
title: 'IShellDispatch： Parent 屬性 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Parent
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 051e6f323b9663b692410d81d85e55a404e99d56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113977"
---
# <a name="ishelldispatchparent-property"></a><span data-ttu-id="c6746-103">IShellDispatch 父系屬性</span><span class="sxs-lookup"><span data-stu-id="c6746-103">IShellDispatch.Parent property</span></span>

<span data-ttu-id="c6746-104">抓取物件，該物件表示目前物件的父系。</span><span class="sxs-lookup"><span data-stu-id="c6746-104">Retrieves an object that represents the parent of the current object.</span></span>

<span data-ttu-id="c6746-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="c6746-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6746-106">語法</span><span class="sxs-lookup"><span data-stu-id="c6746-106">Syntax</span></span>


```JScript
objParent = IShellDispatch.Parent
```


```VB

Property Parent As Object
```





## <a name="property-value"></a><span data-ttu-id="c6746-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="c6746-107">Property value</span></span>

<span data-ttu-id="c6746-108">[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)型別的變數，可接收父物件。</span><span class="sxs-lookup"><span data-stu-id="c6746-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the parent object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6746-109">備註</span><span class="sxs-lookup"><span data-stu-id="c6746-109">Remarks</span></span>

<span data-ttu-id="c6746-110">這個屬性是透過 [**Shell. Parent**](shell-parent.md) 屬性來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="c6746-110">This property is implemented and accessed through the [**Shell.Parent**](shell-parent.md) property.</span></span>

## <a name="examples"></a><span data-ttu-id="c6746-111">範例</span><span class="sxs-lookup"><span data-stu-id="c6746-111">Examples</span></span>

<span data-ttu-id="c6746-112">下列範例示範如何在 JScript、VBScript 和 Visual Basic 中使用 **父代** 。</span><span class="sxs-lookup"><span data-stu-id="c6746-112">The following examples show the use of **Parent** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="c6746-113">Jscript：</span><span class="sxs-lookup"><span data-stu-id="c6746-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellParentJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objParent;

        objParent = objshell.Shell_Parent;
        if (objParent != null)
        {
            alert("Got parent property");
        }
    }
</script>
```



<span data-ttu-id="c6746-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="c6746-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellParentVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            if (not objShell is nothing) then
                dim objParent

                set objParent = objshell.Parent
                    if (not objParent is nothing) then
                        alert("Got parent property")
                    end if
                set objParent = nothing
            end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="c6746-115">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="c6746-115">Visual Basic:</span></span>


```VB
Private Sub fnShellParentVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        If (Not objShell Is Nothing) Then
            Dim objParent As Object
            
            Set objParent = objshell.Parent
                If (Not objParent Is Nothing) Then
                    Debug.Print "Got parent object"
                End If
            Set objParent = Nothing
        End If
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="c6746-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6746-116">Requirements</span></span>



| <span data-ttu-id="c6746-117">需求</span><span class="sxs-lookup"><span data-stu-id="c6746-117">Requirement</span></span> | <span data-ttu-id="c6746-118">值</span><span class="sxs-lookup"><span data-stu-id="c6746-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6746-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c6746-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c6746-120">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6746-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c6746-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c6746-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c6746-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6746-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c6746-123">標頭</span><span class="sxs-lookup"><span data-stu-id="c6746-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6746-124"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="c6746-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="c6746-125">Idl</span><span class="sxs-lookup"><span data-stu-id="c6746-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c6746-126"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c6746-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="c6746-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c6746-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6746-128"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="c6746-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
