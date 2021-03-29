---
description: 建立並傳回新的 ShellWindows 物件，該物件為這個 ShellWindows 物件的複本。
title: 'ShellWindows._NewEnum 方法 (Exdisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows._NewEnum
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 85e84c13-62aa-4502-b642-ca55273a800d
ms.openlocfilehash: ded5ae2c337e80359c012fb63a37aa13cc43b5fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194802"
---
# <a name="shellwindows_newenum-method"></a><span data-ttu-id="38096-103">ShellWindows。 \_NewEnum 方法</span><span class="sxs-lookup"><span data-stu-id="38096-103">ShellWindows.\_NewEnum method</span></span>

<span data-ttu-id="38096-104">建立並傳回新的 [**ShellWindows**](shellwindows.md) 物件，該物件為這個 **ShellWindows** 物件的複本。</span><span class="sxs-lookup"><span data-stu-id="38096-104">Creates and returns a new [**ShellWindows**](shellwindows.md) object that is a copy of this **ShellWindows** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="38096-105">語法</span><span class="sxs-lookup"><span data-stu-id="38096-105">Syntax</span></span>


```JScript
retVal = ShellWindows._NewEnum()
```



## <a name="parameters"></a><span data-ttu-id="38096-106">參數</span><span class="sxs-lookup"><span data-stu-id="38096-106">Parameters</span></span>

<span data-ttu-id="38096-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="38096-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="38096-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="38096-108">Return value</span></span>

<span data-ttu-id="38096-109">類型： **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span><span class="sxs-lookup"><span data-stu-id="38096-109">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span></span>

<span data-ttu-id="38096-110">[**ShellWindows**](shellwindows.md)物件複製的物件參考。</span><span class="sxs-lookup"><span data-stu-id="38096-110">An object reference to the [**ShellWindows**](shellwindows.md) object copy.</span></span>

## <a name="examples"></a><span data-ttu-id="38096-111">範例</span><span class="sxs-lookup"><span data-stu-id="38096-111">Examples</span></span>

<span data-ttu-id="38096-112">下列範例顯示使用中的 **\_ NewEnum** 。</span><span class="sxs-lookup"><span data-stu-id="38096-112">The following example shows **\_NewEnum** in use.</span></span> <span data-ttu-id="38096-113">VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="38096-113">Proper usage is shown for VBScript and Visual Basic.</span></span> <span data-ttu-id="38096-114">這個方法不能與 JScript 一起使用。</span><span class="sxs-lookup"><span data-stu-id="38096-114">This method cannot be used with JScript.</span></span>

<span data-ttu-id="38096-115">VBScript</span><span class="sxs-lookup"><span data-stu-id="38096-115">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsNewEnumVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Shell_Windows

        if (not objShellWindows is nothing) then
            dim objEnumItems
            
            for each objEnumItems in objShellWindows
                alert(objEnumItems.Type)
            next
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="38096-116">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="38096-116">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsNewEnumVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Shell_Windows

    If (Not objShellWindows Is Nothing) Then
        Dim vEnumItem As Variant
        
        For Each vEnumItem In objShellWindows
            Debug.Print vEnumItem.Type
        Next vEnumItem
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="38096-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="38096-117">Requirements</span></span>



| <span data-ttu-id="38096-118">需求</span><span class="sxs-lookup"><span data-stu-id="38096-118">Requirement</span></span> | <span data-ttu-id="38096-119">值</span><span class="sxs-lookup"><span data-stu-id="38096-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38096-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="38096-120">Minimum supported client</span></span><br/> | <span data-ttu-id="38096-121">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="38096-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="38096-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="38096-122">Minimum supported server</span></span><br/> | <span data-ttu-id="38096-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="38096-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="38096-124">標頭</span><span class="sxs-lookup"><span data-stu-id="38096-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="38096-125"><dt>Exdisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="38096-125"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="38096-126">DLL</span><span class="sxs-lookup"><span data-stu-id="38096-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38096-127"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="38096-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
