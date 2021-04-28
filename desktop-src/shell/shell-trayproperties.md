---
description: TrayProperties 方法-顯示 [工作列] 和 [開始功能表屬性] 對話方塊。 這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [屬性] 相同。
ms.assetid: 0d82d847-9e6f-461e-b938-fe8fd49a636f
title: 'TrayProperties 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.TrayProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e09f6833fbf07c99fdbce9c02b020bcbb5361408
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104096"
---
# <a name="shelltrayproperties-method"></a><span data-ttu-id="d3810-104">TrayProperties 方法</span><span class="sxs-lookup"><span data-stu-id="d3810-104">Shell.TrayProperties method</span></span>

<span data-ttu-id="d3810-105">顯示 [ **工作列] 和 [開始功能表屬性** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="d3810-105">Displays the **Taskbar and Start Menu Properties** dialog box.</span></span> <span data-ttu-id="d3810-106">這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [ **屬性**] 相同。</span><span class="sxs-lookup"><span data-stu-id="d3810-106">This method has the same effect as right-clicking the taskbar and selecting **Properties**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3810-107">語法</span><span class="sxs-lookup"><span data-stu-id="d3810-107">Syntax</span></span>


```JScript
iRetVal = Shell.TrayProperties()
```


```VB

Shell.TrayProperties() As Integer
```





## <a name="parameters"></a><span data-ttu-id="d3810-108">參數</span><span class="sxs-lookup"><span data-stu-id="d3810-108">Parameters</span></span>

<span data-ttu-id="d3810-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d3810-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="d3810-110">範例</span><span class="sxs-lookup"><span data-stu-id="d3810-110">Examples</span></span>

<span data-ttu-id="d3810-111">下列範例顯示使用中的 **TrayProperties** 。</span><span class="sxs-lookup"><span data-stu-id="d3810-111">The following example shows **TrayProperties** in use.</span></span> <span data-ttu-id="d3810-112">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="d3810-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="d3810-113">Jscript：</span><span class="sxs-lookup"><span data-stu-id="d3810-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTrayPropertiesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TrayProperties();
    }
</script>
```



<span data-ttu-id="d3810-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="d3810-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTrayPropertiesVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.TrayProperties

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="d3810-115">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="d3810-115">Visual Basic:</span></span>


```VB
Private Sub fnShellTrayPropertiesVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.TrayProperties

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="d3810-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3810-116">Requirements</span></span>



| <span data-ttu-id="d3810-117">需求</span><span class="sxs-lookup"><span data-stu-id="d3810-117">Requirement</span></span> | <span data-ttu-id="d3810-118">值</span><span class="sxs-lookup"><span data-stu-id="d3810-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3810-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d3810-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d3810-120">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3810-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d3810-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d3810-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d3810-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3810-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d3810-123">標頭</span><span class="sxs-lookup"><span data-stu-id="d3810-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3810-124"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="d3810-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="d3810-125">Idl</span><span class="sxs-lookup"><span data-stu-id="d3810-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d3810-126"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="d3810-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="d3810-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d3810-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3810-128"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="d3810-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




