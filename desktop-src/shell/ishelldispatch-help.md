---
description: 顯示 [Windows 說明及支援] 視窗。 這個方法與按一下 [[開始] 功能表]，並選取 [說明及支援] 的效果相同。
ms.assetid: 9460C87E-6703-4df6-A84C-8D394E0E6703
title: 'IShellDispatch： Help 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Help
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b58bcc97748cecf6ab4064ecccf3ba5bbe190b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972421"
---
# <a name="ishelldispatchhelp-method"></a><span data-ttu-id="42007-104">IShellDispatch. Help 方法</span><span class="sxs-lookup"><span data-stu-id="42007-104">IShellDispatch.Help method</span></span>

<span data-ttu-id="42007-105">顯示 [Windows 說明及支援] 視窗。</span><span class="sxs-lookup"><span data-stu-id="42007-105">Displays the Windows Help and Support window.</span></span> <span data-ttu-id="42007-106">這個方法與按一下 [ **開始** ] 功能表並選取 [說明 **及支援**] 的效果相同。</span><span class="sxs-lookup"><span data-stu-id="42007-106">This method has the same effect as clicking the **Start** menu and selecting **Help and Support**.</span></span>

## <a name="syntax"></a><span data-ttu-id="42007-107">語法</span><span class="sxs-lookup"><span data-stu-id="42007-107">Syntax</span></span>


```JScript
IShellDispatch.Help()
```


```VB

IShellDispatch.Help()
```





## <a name="parameters"></a><span data-ttu-id="42007-108">參數</span><span class="sxs-lookup"><span data-stu-id="42007-108">Parameters</span></span>

<span data-ttu-id="42007-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="42007-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="42007-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="42007-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="42007-111">JScript</span><span class="sxs-lookup"><span data-stu-id="42007-111">JScript</span></span>

<span data-ttu-id="42007-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="42007-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="42007-113">VB</span><span class="sxs-lookup"><span data-stu-id="42007-113">VB</span></span>

<span data-ttu-id="42007-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="42007-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="42007-115">備註</span><span class="sxs-lookup"><span data-stu-id="42007-115">Remarks</span></span>

<span data-ttu-id="42007-116">這個方法是透過 [**Shell. Help**](shell-help.md) 方法來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="42007-116">This method is implemented and accessed through the [**Shell.Help**](shell-help.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="42007-117">範例</span><span class="sxs-lookup"><span data-stu-id="42007-117">Examples</span></span>

<span data-ttu-id="42007-118">下列範例示範 **如何** 使用 JScript、VBScript 和 Visual Basic 中的說明。</span><span class="sxs-lookup"><span data-stu-id="42007-118">The following examples show the use of **Help** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="42007-119">Jscript：</span><span class="sxs-lookup"><span data-stu-id="42007-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellHelpJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Help();
    }
</script>
```



<span data-ttu-id="42007-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="42007-120">VBScript:</span></span>


```VB
 <script language="VBScript">
    function fnShellHelpVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.Help

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="42007-121">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="42007-121">Visual Basic:</span></span>


```VB
Private Sub fnShellHelpVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.Help

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="42007-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="42007-122">Requirements</span></span>



| <span data-ttu-id="42007-123">需求</span><span class="sxs-lookup"><span data-stu-id="42007-123">Requirement</span></span> | <span data-ttu-id="42007-124">值</span><span class="sxs-lookup"><span data-stu-id="42007-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42007-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="42007-125">Minimum supported client</span></span><br/> | <span data-ttu-id="42007-126">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42007-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="42007-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="42007-127">Minimum supported server</span></span><br/> | <span data-ttu-id="42007-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42007-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="42007-129">標頭</span><span class="sxs-lookup"><span data-stu-id="42007-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="42007-130"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="42007-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="42007-131">Idl</span><span class="sxs-lookup"><span data-stu-id="42007-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="42007-132"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="42007-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="42007-133">DLL</span><span class="sxs-lookup"><span data-stu-id="42007-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42007-134"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="42007-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




