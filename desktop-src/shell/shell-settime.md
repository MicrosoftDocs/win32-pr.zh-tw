---
description: 顯示 [日期和時間屬性] 對話方塊。 這個方法的效果與以滑鼠右鍵按一下工作列狀態區域中的時鐘，然後選取 [調整日期/時間]。
ms.assetid: 01694607-3fc2-4d0d-ba48-5bdbb40da000
title: 'SetTime 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.SetTime
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b610effe87bd9e4ab33a6e8396e90f79e7bbbe9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973253"
---
# <a name="shellsettime-method"></a><span data-ttu-id="fa813-104">SetTime 方法</span><span class="sxs-lookup"><span data-stu-id="fa813-104">Shell.SetTime method</span></span>

<span data-ttu-id="fa813-105">顯示 [ **日期和時間屬性** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="fa813-105">Displays the **Date and Time Properties** dialog box.</span></span> <span data-ttu-id="fa813-106">這個方法的效果與以滑鼠右鍵按一下工作列狀態區域中的時鐘，然後選取 [ **調整日期/時間**]。</span><span class="sxs-lookup"><span data-stu-id="fa813-106">This method has the same effect as right-clicking the clock in the taskbar status area and selecting **Adjust Date/Time**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa813-107">語法</span><span class="sxs-lookup"><span data-stu-id="fa813-107">Syntax</span></span>


```JScript
iRetVal = Shell.SetTime()
```


```VB

Shell.SetTime() As Integer
```





## <a name="parameters"></a><span data-ttu-id="fa813-108">參數</span><span class="sxs-lookup"><span data-stu-id="fa813-108">Parameters</span></span>

<span data-ttu-id="fa813-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="fa813-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="fa813-110">範例</span><span class="sxs-lookup"><span data-stu-id="fa813-110">Examples</span></span>

<span data-ttu-id="fa813-111">下列範例顯示使用中的 **SetTime** 。</span><span class="sxs-lookup"><span data-stu-id="fa813-111">The following example shows **SetTime** in use.</span></span> <span data-ttu-id="fa813-112">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="fa813-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="fa813-113">Jscript：</span><span class="sxs-lookup"><span data-stu-id="fa813-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellSetTimeJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.SetTime();
    }
</script>
```



<span data-ttu-id="fa813-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="fa813-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellSetTimeVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.SetTime
 
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="fa813-115">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="fa813-115">Visual Basic:</span></span>


```VB
Private Sub fnShellSetTimeVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.SetTime
 
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="fa813-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa813-116">Requirements</span></span>



| <span data-ttu-id="fa813-117">需求</span><span class="sxs-lookup"><span data-stu-id="fa813-117">Requirement</span></span> | <span data-ttu-id="fa813-118">值</span><span class="sxs-lookup"><span data-stu-id="fa813-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa813-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa813-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fa813-120">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa813-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fa813-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa813-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fa813-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa813-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fa813-123">標頭</span><span class="sxs-lookup"><span data-stu-id="fa813-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa813-124"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="fa813-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="fa813-125">Idl</span><span class="sxs-lookup"><span data-stu-id="fa813-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fa813-126"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="fa813-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="fa813-127">DLL</span><span class="sxs-lookup"><span data-stu-id="fa813-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa813-128"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="fa813-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




