---
description: 顯示 [工作列] 和 [開始功能表屬性] 對話方塊。 這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [屬性] 相同。
ms.assetid: 8E0AC08E-1132-4312-9B75-E7686B91AB02
title: 'IShellDispatch. TrayProperties 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.TrayProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5f5e22dd48b77035aab3754a4c8e3d2c414ec606
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943624"
---
# <a name="ishelldispatchtrayproperties-method"></a><span data-ttu-id="d9d92-104">IShellDispatch. TrayProperties 方法</span><span class="sxs-lookup"><span data-stu-id="d9d92-104">IShellDispatch.TrayProperties method</span></span>

<span data-ttu-id="d9d92-105">顯示 [ **工作列] 和 [開始功能表屬性** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="d9d92-105">Displays the **Taskbar and Start Menu Properties** dialog box.</span></span> <span data-ttu-id="d9d92-106">這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [ **屬性**] 相同。</span><span class="sxs-lookup"><span data-stu-id="d9d92-106">This method has the same effect as right-clicking the taskbar and selecting **Properties**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9d92-107">語法</span><span class="sxs-lookup"><span data-stu-id="d9d92-107">Syntax</span></span>


```JScript
IShellDispatch.TrayProperties()
```


```VB

IShellDispatch.TrayProperties()
```





## <a name="parameters"></a><span data-ttu-id="d9d92-108">參數</span><span class="sxs-lookup"><span data-stu-id="d9d92-108">Parameters</span></span>

<span data-ttu-id="d9d92-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d9d92-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d9d92-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="d9d92-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="d9d92-111">JScript</span><span class="sxs-lookup"><span data-stu-id="d9d92-111">JScript</span></span>

<span data-ttu-id="d9d92-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d9d92-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="d9d92-113">VB</span><span class="sxs-lookup"><span data-stu-id="d9d92-113">VB</span></span>

<span data-ttu-id="d9d92-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d9d92-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9d92-115">備註</span><span class="sxs-lookup"><span data-stu-id="d9d92-115">Remarks</span></span>

<span data-ttu-id="d9d92-116">這個方法是透過 [**TrayProperties**](shell-trayproperties.md) 方法來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="d9d92-116">This method is implemented and accessed through the [**Shell.TrayProperties**](shell-trayproperties.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="d9d92-117">範例</span><span class="sxs-lookup"><span data-stu-id="d9d92-117">Examples</span></span>

<span data-ttu-id="d9d92-118">下列範例示範如何在 JScript、VBScript 和 Visual Basic 中使用 **TrayProperties** 。</span><span class="sxs-lookup"><span data-stu-id="d9d92-118">The following examples show the use of **TrayProperties** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="d9d92-119">Jscript：</span><span class="sxs-lookup"><span data-stu-id="d9d92-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTrayPropertiesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TrayProperties();
    }
</script>
```



<span data-ttu-id="d9d92-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="d9d92-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTrayPropertiesVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TrayProperties

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="d9d92-121">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="d9d92-121">Visual Basic:</span></span>


```VB
Private Sub fnShellTrayPropertiesVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TrayProperties

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="d9d92-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="d9d92-122">Requirements</span></span>



| <span data-ttu-id="d9d92-123">需求</span><span class="sxs-lookup"><span data-stu-id="d9d92-123">Requirement</span></span> | <span data-ttu-id="d9d92-124">值</span><span class="sxs-lookup"><span data-stu-id="d9d92-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9d92-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d9d92-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d9d92-126">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d9d92-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d9d92-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d9d92-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d9d92-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d9d92-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d9d92-129">標頭</span><span class="sxs-lookup"><span data-stu-id="d9d92-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9d92-130"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="d9d92-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="d9d92-131">Idl</span><span class="sxs-lookup"><span data-stu-id="d9d92-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d9d92-132"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="d9d92-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="d9d92-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d9d92-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9d92-134"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="d9d92-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




