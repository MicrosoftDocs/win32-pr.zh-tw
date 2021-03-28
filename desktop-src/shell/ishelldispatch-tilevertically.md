---
description: 垂直並排顯示桌面上的所有視窗。 這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [並排顯示視窗]。
ms.assetid: 63CB7E20-48E6-4cfe-B0BA-0D28A7B151BD
title: 'IShellDispatch. TileVertically 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.TileVertically
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 42f98ae99814495029c67d41b05e86182c6b8b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972412"
---
# <a name="ishelldispatchtilevertically-method"></a><span data-ttu-id="c8214-104">IShellDispatch. TileVertically 方法</span><span class="sxs-lookup"><span data-stu-id="c8214-104">IShellDispatch.TileVertically method</span></span>

<span data-ttu-id="c8214-105">垂直並排顯示桌面上的所有視窗。</span><span class="sxs-lookup"><span data-stu-id="c8214-105">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="c8214-106">這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [並排 **顯示視窗**]。</span><span class="sxs-lookup"><span data-stu-id="c8214-106">This method has the same effect as right-clicking the taskbar and selecting **Show windows side by side**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8214-107">語法</span><span class="sxs-lookup"><span data-stu-id="c8214-107">Syntax</span></span>


```JScript
IShellDispatch.TileVertically()
```


```VB

IShellDispatch.TileVertically()
```





## <a name="parameters"></a><span data-ttu-id="c8214-108">參數</span><span class="sxs-lookup"><span data-stu-id="c8214-108">Parameters</span></span>

<span data-ttu-id="c8214-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c8214-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c8214-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="c8214-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="c8214-111">JScript</span><span class="sxs-lookup"><span data-stu-id="c8214-111">JScript</span></span>

<span data-ttu-id="c8214-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c8214-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="c8214-113">VB</span><span class="sxs-lookup"><span data-stu-id="c8214-113">VB</span></span>

<span data-ttu-id="c8214-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c8214-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8214-115">備註</span><span class="sxs-lookup"><span data-stu-id="c8214-115">Remarks</span></span>

<span data-ttu-id="c8214-116">這個方法是透過 [**TileVertically**](shell-tilevertically.md) 方法來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="c8214-116">This method is implemented and accessed through the [**Shell.TileVertically**](shell-tilevertically.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="c8214-117">範例</span><span class="sxs-lookup"><span data-stu-id="c8214-117">Examples</span></span>

<span data-ttu-id="c8214-118">下列範例示範如何在 JScript、VBScript 和 Visual Basic 中使用 **TileVertically** 。</span><span class="sxs-lookup"><span data-stu-id="c8214-118">The following examples show the use of **TileVertically** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="c8214-119">Jscript：</span><span class="sxs-lookup"><span data-stu-id="c8214-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTileVerticallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TileVertically();
    }
</script>
```



<span data-ttu-id="c8214-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="c8214-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTileVerticallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TileVertically

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="c8214-121">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="c8214-121">Visual Basic:</span></span>


```VB
Private Sub fnShellTileVerticallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TileVertically

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="c8214-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8214-122">Requirements</span></span>



| <span data-ttu-id="c8214-123">需求</span><span class="sxs-lookup"><span data-stu-id="c8214-123">Requirement</span></span> | <span data-ttu-id="c8214-124">值</span><span class="sxs-lookup"><span data-stu-id="c8214-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8214-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c8214-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c8214-126">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8214-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c8214-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c8214-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c8214-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8214-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c8214-129">標頭</span><span class="sxs-lookup"><span data-stu-id="c8214-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8214-130"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="c8214-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="c8214-131">Idl</span><span class="sxs-lookup"><span data-stu-id="c8214-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c8214-132"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c8214-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="c8214-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c8214-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8214-134"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="c8214-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




