---
description: 向使用者顯示 [執行] 對話方塊。 這個方法的效果與按一下 [開始] 功能表並選取 [執行] 相同。
ms.assetid: bb984777-e09f-41e6-8359-51c5291654f7
title: 'FileRun 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FileRun
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ebccf11ea21fdd4ceba2563a6110c1eb2494947b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973700"
---
# <a name="shellfilerun-method"></a><span data-ttu-id="af53f-104">FileRun 方法</span><span class="sxs-lookup"><span data-stu-id="af53f-104">Shell.FileRun method</span></span>

<span data-ttu-id="af53f-105">向使用者顯示 [ **執行** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="af53f-105">Displays the **Run** dialog to the user.</span></span> <span data-ttu-id="af53f-106">這個方法與按一下 [ **開始** ] 功能表並選取 [ **執行**] 的效果相同。</span><span class="sxs-lookup"><span data-stu-id="af53f-106">This method has the same effect as clicking the **Start** menu and selecting **Run**.</span></span>

## <a name="syntax"></a><span data-ttu-id="af53f-107">語法</span><span class="sxs-lookup"><span data-stu-id="af53f-107">Syntax</span></span>


```JScript
Shell.FileRun()
```


```VB

Shell.FileRun()
```





## <a name="parameters"></a><span data-ttu-id="af53f-108">參數</span><span class="sxs-lookup"><span data-stu-id="af53f-108">Parameters</span></span>

<span data-ttu-id="af53f-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="af53f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="af53f-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="af53f-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="af53f-111">JScript</span><span class="sxs-lookup"><span data-stu-id="af53f-111">JScript</span></span>

<span data-ttu-id="af53f-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="af53f-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="af53f-113">VB</span><span class="sxs-lookup"><span data-stu-id="af53f-113">VB</span></span>

<span data-ttu-id="af53f-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="af53f-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="af53f-115">範例</span><span class="sxs-lookup"><span data-stu-id="af53f-115">Examples</span></span>

<span data-ttu-id="af53f-116">下列範例顯示使用中的 **FileRun** 。</span><span class="sxs-lookup"><span data-stu-id="af53f-116">The following example shows **FileRun** in use.</span></span> <span data-ttu-id="af53f-117">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="af53f-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="af53f-118">Jscript：</span><span class="sxs-lookup"><span data-stu-id="af53f-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFileRunJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FileRun();
    }
</script>
```



<span data-ttu-id="af53f-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="af53f-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellFileRunVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.FileRun

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="af53f-120">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="af53f-120">Visual Basic:</span></span>


```VB
Private Sub fnShellFileRunVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FileRun

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="af53f-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="af53f-121">Requirements</span></span>



| <span data-ttu-id="af53f-122">需求</span><span class="sxs-lookup"><span data-stu-id="af53f-122">Requirement</span></span> | <span data-ttu-id="af53f-123">值</span><span class="sxs-lookup"><span data-stu-id="af53f-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af53f-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="af53f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="af53f-125">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af53f-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="af53f-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="af53f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="af53f-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af53f-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="af53f-128">標頭</span><span class="sxs-lookup"><span data-stu-id="af53f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="af53f-129"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="af53f-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="af53f-130">Idl</span><span class="sxs-lookup"><span data-stu-id="af53f-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="af53f-131"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="af53f-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="af53f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="af53f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af53f-133"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="af53f-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




