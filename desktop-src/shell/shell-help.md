---
description: 顯示 Windows 說明及支援中心。 這個方法與按一下 [[開始] 功能表]，並選取 [說明及支援] 的效果相同。
ms.assetid: fc13fef8-dac8-4c59-936d-8da0e63e06d4
title: 'Shell. Help 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Help
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: bfb4e9b3272355c41d13526d2e526515ff65d42b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192810"
---
# <a name="shellhelp-method"></a><span data-ttu-id="ef987-104">Shell. Help 方法</span><span class="sxs-lookup"><span data-stu-id="ef987-104">Shell.Help method</span></span>

<span data-ttu-id="ef987-105">顯示 Windows 說明及支援中心。</span><span class="sxs-lookup"><span data-stu-id="ef987-105">Displays the Windows Help and Support Center.</span></span> <span data-ttu-id="ef987-106">這個方法與按一下 [ **開始** ] 功能表並選取 [說明 **及支援**] 的效果相同。</span><span class="sxs-lookup"><span data-stu-id="ef987-106">This method has the same effect as clicking the **Start** menu and selecting **Help and Support**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef987-107">語法</span><span class="sxs-lookup"><span data-stu-id="ef987-107">Syntax</span></span>


```JScript
Shell.Help()
```


```VB

Shell.Help()
```





## <a name="parameters"></a><span data-ttu-id="ef987-108">參數</span><span class="sxs-lookup"><span data-stu-id="ef987-108">Parameters</span></span>

<span data-ttu-id="ef987-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="ef987-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ef987-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="ef987-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="ef987-111">JScript</span><span class="sxs-lookup"><span data-stu-id="ef987-111">JScript</span></span>

<span data-ttu-id="ef987-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ef987-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="ef987-113">VB</span><span class="sxs-lookup"><span data-stu-id="ef987-113">VB</span></span>

<span data-ttu-id="ef987-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ef987-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="ef987-115">範例</span><span class="sxs-lookup"><span data-stu-id="ef987-115">Examples</span></span>

<span data-ttu-id="ef987-116">下列 **範例顯示使用** 說明。</span><span class="sxs-lookup"><span data-stu-id="ef987-116">The following example shows **Help** in use.</span></span> <span data-ttu-id="ef987-117">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="ef987-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="ef987-118">Jscript：</span><span class="sxs-lookup"><span data-stu-id="ef987-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellHelpJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.Help();
    }
</script>
```



<span data-ttu-id="ef987-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="ef987-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellHelpVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.Help

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="ef987-120">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="ef987-120">Visual Basic:</span></span>


```VB
Private Sub fnShellHelpVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.Help

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="ef987-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="ef987-121">Requirements</span></span>



| <span data-ttu-id="ef987-122">需求</span><span class="sxs-lookup"><span data-stu-id="ef987-122">Requirement</span></span> | <span data-ttu-id="ef987-123">值</span><span class="sxs-lookup"><span data-stu-id="ef987-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef987-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ef987-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ef987-125">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef987-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ef987-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ef987-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ef987-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef987-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ef987-128">標頭</span><span class="sxs-lookup"><span data-stu-id="ef987-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef987-129"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="ef987-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="ef987-130">Idl</span><span class="sxs-lookup"><span data-stu-id="ef987-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ef987-131"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="ef987-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="ef987-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ef987-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef987-133"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="ef987-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




