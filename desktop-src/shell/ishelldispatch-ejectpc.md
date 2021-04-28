---
description: IShellDispatch. EjectPC 方法-從銜接站彈出電腦。 如果您的電腦支援此命令，則這與按一下 [開始] 功能表並選取 [退出電腦] 相同。
ms.assetid: 34448D82-187C-40aa-90B4-A4111B33048B
title: 'IShellDispatch. EjectPC 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.EjectPC
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ac42e1a4331a553a03bac3da50a187e06c90859c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086636"
---
# <a name="ishelldispatchejectpc-method"></a><span data-ttu-id="19336-104">IShellDispatch. EjectPC 方法</span><span class="sxs-lookup"><span data-stu-id="19336-104">IShellDispatch.EjectPC method</span></span>

<span data-ttu-id="19336-105">從其銜接站彈出電腦。</span><span class="sxs-lookup"><span data-stu-id="19336-105">Ejects the computer from its docking station.</span></span> <span data-ttu-id="19336-106">這與按一下 [ **開始** ] 功能表並選取 [ **退出** 電腦] 的方式相同，如果您的電腦支援此命令。</span><span class="sxs-lookup"><span data-stu-id="19336-106">This is the same as clicking the **Start** menu and selecting **Eject PC**, if your computer supports this command.</span></span>

## <a name="syntax"></a><span data-ttu-id="19336-107">語法</span><span class="sxs-lookup"><span data-stu-id="19336-107">Syntax</span></span>


```JScript
IShellDispatch.EjectPC()
```


```VB

IShellDispatch.EjectPC()
```





## <a name="parameters"></a><span data-ttu-id="19336-108">參數</span><span class="sxs-lookup"><span data-stu-id="19336-108">Parameters</span></span>

<span data-ttu-id="19336-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="19336-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="19336-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="19336-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="19336-111">JScript</span><span class="sxs-lookup"><span data-stu-id="19336-111">JScript</span></span>

<span data-ttu-id="19336-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="19336-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="19336-113">VB</span><span class="sxs-lookup"><span data-stu-id="19336-113">VB</span></span>

<span data-ttu-id="19336-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="19336-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="19336-115">備註</span><span class="sxs-lookup"><span data-stu-id="19336-115">Remarks</span></span>

<span data-ttu-id="19336-116">這個方法是透過 [**EjectPC**](shell-ejectpc.md) 方法來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="19336-116">This method is implemented and accessed through the [**Shell.EjectPC**](shell-ejectpc.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="19336-117">範例</span><span class="sxs-lookup"><span data-stu-id="19336-117">Examples</span></span>

<span data-ttu-id="19336-118">下列範例示範如何在 JScript、VBScript 和 Visual Basic 中使用 **EjectPC** 。</span><span class="sxs-lookup"><span data-stu-id="19336-118">The following examples show the use of **EjectPC** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="19336-119">Jscript：</span><span class="sxs-lookup"><span data-stu-id="19336-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellEjectPCJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.EjectPC();
    }
</script>
```



<span data-ttu-id="19336-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="19336-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellEjectPCVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.EjectPC

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="19336-121">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="19336-121">Visual Basic:</span></span>


```VB
Private Sub fnShellEjectPCVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.EjectPC

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="19336-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="19336-122">Requirements</span></span>



| <span data-ttu-id="19336-123">需求</span><span class="sxs-lookup"><span data-stu-id="19336-123">Requirement</span></span> | <span data-ttu-id="19336-124">值</span><span class="sxs-lookup"><span data-stu-id="19336-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19336-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="19336-125">Minimum supported client</span></span><br/> | <span data-ttu-id="19336-126">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19336-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="19336-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="19336-127">Minimum supported server</span></span><br/> | <span data-ttu-id="19336-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19336-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="19336-129">標頭</span><span class="sxs-lookup"><span data-stu-id="19336-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="19336-130"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="19336-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="19336-131">Idl</span><span class="sxs-lookup"><span data-stu-id="19336-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="19336-132"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="19336-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="19336-133">DLL</span><span class="sxs-lookup"><span data-stu-id="19336-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19336-134"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="19336-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




