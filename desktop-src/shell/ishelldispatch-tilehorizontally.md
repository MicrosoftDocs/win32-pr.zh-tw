---
description: 以水準方式並排顯示桌面上的所有視窗。 這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [顯示視窗堆疊]。
ms.assetid: 85785510-6B75-450a-A9BB-6C3B4F6194E2
title: 'IShellDispatch. TileHorizontally 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.TileHorizontally
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 06491f797de4a9fcb5c431d85cff71fbc78d605c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113976"
---
# <a name="ishelldispatchtilehorizontally-method"></a><span data-ttu-id="9a507-104">IShellDispatch. TileHorizontally 方法</span><span class="sxs-lookup"><span data-stu-id="9a507-104">IShellDispatch.TileHorizontally method</span></span>

<span data-ttu-id="9a507-105">以水準方式並排顯示桌面上的所有視窗。</span><span class="sxs-lookup"><span data-stu-id="9a507-105">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="9a507-106">這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [ **顯示視窗堆疊**]。</span><span class="sxs-lookup"><span data-stu-id="9a507-106">This method has the same effect as right-clicking the taskbar and selecting **Show windows stacked**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a507-107">語法</span><span class="sxs-lookup"><span data-stu-id="9a507-107">Syntax</span></span>


```JScript
IShellDispatch.TileHorizontally()
```


```VB

IShellDispatch.TileHorizontally()
```





## <a name="parameters"></a><span data-ttu-id="9a507-108">參數</span><span class="sxs-lookup"><span data-stu-id="9a507-108">Parameters</span></span>

<span data-ttu-id="9a507-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="9a507-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9a507-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="9a507-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="9a507-111">JScript</span><span class="sxs-lookup"><span data-stu-id="9a507-111">JScript</span></span>

<span data-ttu-id="9a507-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9a507-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="9a507-113">VB</span><span class="sxs-lookup"><span data-stu-id="9a507-113">VB</span></span>

<span data-ttu-id="9a507-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9a507-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a507-115">備註</span><span class="sxs-lookup"><span data-stu-id="9a507-115">Remarks</span></span>

<span data-ttu-id="9a507-116">這個方法是透過 [**TileHorizontally**](shell-tilehorizontally.md) 方法來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="9a507-116">This method is implemented and accessed through the [**Shell.TileHorizontally**](shell-tilehorizontally.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="9a507-117">範例</span><span class="sxs-lookup"><span data-stu-id="9a507-117">Examples</span></span>

<span data-ttu-id="9a507-118">下列範例示範如何在 JScript、VBScript 和 Visual Basic 中使用 **TileHorizontally** 。</span><span class="sxs-lookup"><span data-stu-id="9a507-118">The following example shows the use of **TileHorizontally** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="9a507-119">Jscript：</span><span class="sxs-lookup"><span data-stu-id="9a507-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTileHorizontallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TileHorizontally();
    }
</script>
```



<span data-ttu-id="9a507-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="9a507-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTileHorizontallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TileHorizontally

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="9a507-121">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="9a507-121">Visual Basic:</span></span>


```VB
Private Sub fnShellTileHorizontallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TileHorizontally

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="9a507-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a507-122">Requirements</span></span>



| <span data-ttu-id="9a507-123">需求</span><span class="sxs-lookup"><span data-stu-id="9a507-123">Requirement</span></span> | <span data-ttu-id="9a507-124">值</span><span class="sxs-lookup"><span data-stu-id="9a507-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a507-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9a507-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9a507-126">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9a507-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9a507-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9a507-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9a507-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9a507-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9a507-129">標頭</span><span class="sxs-lookup"><span data-stu-id="9a507-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a507-130"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="9a507-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="9a507-131">Idl</span><span class="sxs-lookup"><span data-stu-id="9a507-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9a507-132"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="9a507-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="9a507-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9a507-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a507-134"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="9a507-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




