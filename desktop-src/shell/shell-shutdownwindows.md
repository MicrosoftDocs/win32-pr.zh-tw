---
description: ShutdownWindows 方法-顯示關機 Windows] 對話方塊。 這與按一下 [[開始] 功能表]，然後選取 [關機] 相同。
ms.assetid: 6fa8e2e0-a58f-4837-89f5-898cece2d80a
title: 'ShutdownWindows 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShutdownWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 2a3c0746caccb360f6f7f0156b72a57ed0a2d2b8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083666"
---
# <a name="shellshutdownwindows-method"></a><span data-ttu-id="824f9-104">ShutdownWindows 方法</span><span class="sxs-lookup"><span data-stu-id="824f9-104">Shell.ShutdownWindows method</span></span>

<span data-ttu-id="824f9-105">顯示 **關機 Windows** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="824f9-105">Displays the **Shut Down Windows** dialog box.</span></span> <span data-ttu-id="824f9-106">這等同于按一下 [ **開始** ] 功能表，然後選取 [ **關機**]。</span><span class="sxs-lookup"><span data-stu-id="824f9-106">This is the same as clicking the **Start** menu and selecting **Shut Down**.</span></span>

## <a name="syntax"></a><span data-ttu-id="824f9-107">語法</span><span class="sxs-lookup"><span data-stu-id="824f9-107">Syntax</span></span>


```JScript
iRetVal = Shell.ShutdownWindows()
```


```VB

Shell.ShutdownWindows() As Integer
```





## <a name="parameters"></a><span data-ttu-id="824f9-108">參數</span><span class="sxs-lookup"><span data-stu-id="824f9-108">Parameters</span></span>

<span data-ttu-id="824f9-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="824f9-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="824f9-110">範例</span><span class="sxs-lookup"><span data-stu-id="824f9-110">Examples</span></span>

<span data-ttu-id="824f9-111">下列範例顯示使用中的 **ShutdownWindows** 。</span><span class="sxs-lookup"><span data-stu-id="824f9-111">The following example shows **ShutdownWindows** in use.</span></span> <span data-ttu-id="824f9-112">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="824f9-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="824f9-113">Jscript：</span><span class="sxs-lookup"><span data-stu-id="824f9-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShutdownWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ShutdownWindows();
    }
</script>
```



<span data-ttu-id="824f9-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="824f9-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellShutdownWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.ShutdownWindows

        set objShell = nothing
    end function
```



<span data-ttu-id="824f9-115">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="824f9-115">Visual Basic:</span></span>


```VB
Private Sub fnShellShutdownWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.ShutdownWindows

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="824f9-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="824f9-116">Requirements</span></span>



| <span data-ttu-id="824f9-117">需求</span><span class="sxs-lookup"><span data-stu-id="824f9-117">Requirement</span></span> | <span data-ttu-id="824f9-118">值</span><span class="sxs-lookup"><span data-stu-id="824f9-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="824f9-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="824f9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="824f9-120">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="824f9-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="824f9-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="824f9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="824f9-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="824f9-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="824f9-123">標頭</span><span class="sxs-lookup"><span data-stu-id="824f9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="824f9-124"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="824f9-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="824f9-125">Idl</span><span class="sxs-lookup"><span data-stu-id="824f9-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="824f9-126"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="824f9-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="824f9-127">DLL</span><span class="sxs-lookup"><span data-stu-id="824f9-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="824f9-128"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="824f9-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




