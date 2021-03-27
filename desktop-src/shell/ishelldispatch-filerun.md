---
description: 向使用者顯示 [執行] 對話方塊。
ms.assetid: BC7C4C26-593D-4467-A2AA-4F2DF835C989
title: 'IShellDispatch. FileRun 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.FileRun
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 56806edf06d334d90ad038886d955c00876f8f0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691224"
---
# <a name="ishelldispatchfilerun-method"></a><span data-ttu-id="b013c-103">IShellDispatch. FileRun 方法</span><span class="sxs-lookup"><span data-stu-id="b013c-103">IShellDispatch.FileRun method</span></span>

<span data-ttu-id="b013c-104">向使用者顯示 [ **執行** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="b013c-104">Displays the **Run** dialog to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="b013c-105">語法</span><span class="sxs-lookup"><span data-stu-id="b013c-105">Syntax</span></span>


```JScript
IShellDispatch.FileRun()
```


```VB

IShellDispatch.FileRun()
```





## <a name="parameters"></a><span data-ttu-id="b013c-106">參數</span><span class="sxs-lookup"><span data-stu-id="b013c-106">Parameters</span></span>

<span data-ttu-id="b013c-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="b013c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b013c-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="b013c-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="b013c-109">JScript</span><span class="sxs-lookup"><span data-stu-id="b013c-109">JScript</span></span>

<span data-ttu-id="b013c-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b013c-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="b013c-111">VB</span><span class="sxs-lookup"><span data-stu-id="b013c-111">VB</span></span>

<span data-ttu-id="b013c-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b013c-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b013c-113">備註</span><span class="sxs-lookup"><span data-stu-id="b013c-113">Remarks</span></span>

<span data-ttu-id="b013c-114">這個方法是透過 [**FileRun**](shell-filerun.md) 方法來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="b013c-114">This method is implemented and accessed through the [**Shell.FileRun**](shell-filerun.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="b013c-115">範例</span><span class="sxs-lookup"><span data-stu-id="b013c-115">Examples</span></span>

<span data-ttu-id="b013c-116">下列範例示範如何在 JScript、VBScript 和 Visual Basic 中使用 **FileRun** 。</span><span class="sxs-lookup"><span data-stu-id="b013c-116">The following examples show the use of **FileRun** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="b013c-117">Jscript：</span><span class="sxs-lookup"><span data-stu-id="b013c-117">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFileRunJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.FileRun();
    }
</script>
```



<span data-ttu-id="b013c-118">VBScript</span><span class="sxs-lookup"><span data-stu-id="b013c-118">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellFileRunVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.FileRun

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="b013c-119">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="b013c-119">Visual Basic:</span></span>


```VB
Private Sub fnShellFileRunVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.FileRun

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="b013c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="b013c-120">Requirements</span></span>



| <span data-ttu-id="b013c-121">需求</span><span class="sxs-lookup"><span data-stu-id="b013c-121">Requirement</span></span> | <span data-ttu-id="b013c-122">值</span><span class="sxs-lookup"><span data-stu-id="b013c-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b013c-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b013c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b013c-124">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b013c-124">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b013c-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b013c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b013c-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b013c-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b013c-127">標頭</span><span class="sxs-lookup"><span data-stu-id="b013c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b013c-128"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="b013c-128"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b013c-129">Idl</span><span class="sxs-lookup"><span data-stu-id="b013c-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b013c-130"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="b013c-130"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b013c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b013c-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b013c-132"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="b013c-132"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




