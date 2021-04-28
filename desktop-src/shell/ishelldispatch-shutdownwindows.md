---
description: IShellDispatch. ShutdownWindows 方法-顯示關機 Windows] 對話方塊。 這與按一下 [[開始] 功能表]，然後選取 [關機] 相同。
ms.assetid: 3C4F6579-6398-4af4-8911-FE22555B0ABC
title: 'IShellDispatch. ShutdownWindows 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.ShutdownWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5146e17d17ba0f082ad2d80f91ae05c176cf44ed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100466"
---
# <a name="ishelldispatchshutdownwindows-method"></a><span data-ttu-id="a58be-104">IShellDispatch. ShutdownWindows 方法</span><span class="sxs-lookup"><span data-stu-id="a58be-104">IShellDispatch.ShutdownWindows method</span></span>

<span data-ttu-id="a58be-105">顯示 **關機 Windows** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a58be-105">Displays the **Shut Down Windows** dialog box.</span></span> <span data-ttu-id="a58be-106">這等同于按一下 [ **開始** ] 功能表，然後選取 [ **關機**]。</span><span class="sxs-lookup"><span data-stu-id="a58be-106">This is the same as clicking the **Start** menu and selecting **Shut Down**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a58be-107">語法</span><span class="sxs-lookup"><span data-stu-id="a58be-107">Syntax</span></span>


```JScript
IShellDispatch.ShutdownWindows()
```


```VB

IShellDispatch.ShutdownWindows()
```





## <a name="parameters"></a><span data-ttu-id="a58be-108">參數</span><span class="sxs-lookup"><span data-stu-id="a58be-108">Parameters</span></span>

<span data-ttu-id="a58be-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="a58be-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a58be-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="a58be-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="a58be-111">JScript</span><span class="sxs-lookup"><span data-stu-id="a58be-111">JScript</span></span>

<span data-ttu-id="a58be-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a58be-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="a58be-113">VB</span><span class="sxs-lookup"><span data-stu-id="a58be-113">VB</span></span>

<span data-ttu-id="a58be-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a58be-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a58be-115">備註</span><span class="sxs-lookup"><span data-stu-id="a58be-115">Remarks</span></span>

<span data-ttu-id="a58be-116">這個方法是透過 [**ShutdownWindows**](shell-shutdownwindows.md) 方法來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="a58be-116">This method is implemented and accessed through the [**Shell.ShutdownWindows**](shell-shutdownwindows.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="a58be-117">範例</span><span class="sxs-lookup"><span data-stu-id="a58be-117">Examples</span></span>

<span data-ttu-id="a58be-118">下列範例示範如何在 JScript、VBScript 和 Visual Basic 中使用 **ShutdownWindows** 。</span><span class="sxs-lookup"><span data-stu-id="a58be-118">The following example shows the use of **ShutdownWindows** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="a58be-119">Jscript：</span><span class="sxs-lookup"><span data-stu-id="a58be-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShutdownWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.ShutdownWindows();
    }
</script>
```



<span data-ttu-id="a58be-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="a58be-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellShutdownWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.ShutdownWindows

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="a58be-121">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="a58be-121">Visual Basic:</span></span>


```VB
Private Sub fnShellShutdownWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.ShutdownWindows

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="a58be-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="a58be-122">Requirements</span></span>



| <span data-ttu-id="a58be-123">需求</span><span class="sxs-lookup"><span data-stu-id="a58be-123">Requirement</span></span> | <span data-ttu-id="a58be-124">值</span><span class="sxs-lookup"><span data-stu-id="a58be-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a58be-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a58be-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a58be-126">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a58be-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a58be-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a58be-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a58be-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a58be-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a58be-129">標頭</span><span class="sxs-lookup"><span data-stu-id="a58be-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a58be-130"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="a58be-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="a58be-131">Idl</span><span class="sxs-lookup"><span data-stu-id="a58be-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a58be-132"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="a58be-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="a58be-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a58be-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a58be-134"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="a58be-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




