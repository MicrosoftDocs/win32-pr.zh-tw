---
description: 顯示 [日期和時間] 對話方塊。 這個方法的效果與以滑鼠右鍵按一下工作列狀態區域中的時鐘，然後選取 [調整日期/時間]。
ms.assetid: D4B949F6-5508-4624-9706-491184703DC6
title: 'IShellDispatch. SetTime 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.SetTime
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9c9e687ea89cad4715aeacf72a2a33792fba9f7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848303"
---
# <a name="ishelldispatchsettime-method"></a><span data-ttu-id="b4fd1-104">IShellDispatch. SetTime 方法</span><span class="sxs-lookup"><span data-stu-id="b4fd1-104">IShellDispatch.SetTime method</span></span>

<span data-ttu-id="b4fd1-105">顯示 [ **日期和時間** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="b4fd1-105">Displays the **Date and Time** dialog box.</span></span> <span data-ttu-id="b4fd1-106">這個方法的效果與以滑鼠右鍵按一下工作列狀態區域中的時鐘，然後選取 [ **調整日期/時間**]。</span><span class="sxs-lookup"><span data-stu-id="b4fd1-106">This method has the same effect as right-clicking the clock in the taskbar status area and selecting **Adjust date/time**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4fd1-107">語法</span><span class="sxs-lookup"><span data-stu-id="b4fd1-107">Syntax</span></span>


```JScript
IShellDispatch.SetTime()
```


```VB

IShellDispatch.SetTime()
```





## <a name="parameters"></a><span data-ttu-id="b4fd1-108">參數</span><span class="sxs-lookup"><span data-stu-id="b4fd1-108">Parameters</span></span>

<span data-ttu-id="b4fd1-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="b4fd1-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b4fd1-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="b4fd1-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="b4fd1-111">JScript</span><span class="sxs-lookup"><span data-stu-id="b4fd1-111">JScript</span></span>

<span data-ttu-id="b4fd1-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b4fd1-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="b4fd1-113">VB</span><span class="sxs-lookup"><span data-stu-id="b4fd1-113">VB</span></span>

<span data-ttu-id="b4fd1-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b4fd1-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4fd1-115">備註</span><span class="sxs-lookup"><span data-stu-id="b4fd1-115">Remarks</span></span>

<span data-ttu-id="b4fd1-116">這個方法是透過 [**SetTime**](shell-settime.md) 方法來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="b4fd1-116">This method is implemented and accessed through the [**Shell.SetTime**](shell-settime.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="b4fd1-117">範例</span><span class="sxs-lookup"><span data-stu-id="b4fd1-117">Examples</span></span>

<span data-ttu-id="b4fd1-118">下列範例示範如何在 JScript、VBScript 和 Visual Basic 中使用 **SetTime** 。</span><span class="sxs-lookup"><span data-stu-id="b4fd1-118">The following examples show the use of **SetTime** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="b4fd1-119">Jscript：</span><span class="sxs-lookup"><span data-stu-id="b4fd1-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellSetTimeJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.SetTime();
    }
</script>
```



<span data-ttu-id="b4fd1-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="b4fd1-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellSetTimeVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.SetTime
 
        set objShell = nothing
    end function
```



<span data-ttu-id="b4fd1-121">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="b4fd1-121">Visual Basic:</span></span>


```VB
Private Sub fnShellSetTimeVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.SetTime
 
    Set objShell = Nothing
```



## <a name="requirements"></a><span data-ttu-id="b4fd1-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="b4fd1-122">Requirements</span></span>



| <span data-ttu-id="b4fd1-123">需求</span><span class="sxs-lookup"><span data-stu-id="b4fd1-123">Requirement</span></span> | <span data-ttu-id="b4fd1-124">值</span><span class="sxs-lookup"><span data-stu-id="b4fd1-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4fd1-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b4fd1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b4fd1-126">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b4fd1-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b4fd1-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b4fd1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b4fd1-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b4fd1-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b4fd1-129">標頭</span><span class="sxs-lookup"><span data-stu-id="b4fd1-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4fd1-130"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="b4fd1-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b4fd1-131">Idl</span><span class="sxs-lookup"><span data-stu-id="b4fd1-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b4fd1-132"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="b4fd1-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b4fd1-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b4fd1-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4fd1-134"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="b4fd1-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




