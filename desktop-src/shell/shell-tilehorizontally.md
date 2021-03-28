---
description: 以水準方式並排顯示桌面上的所有視窗。 這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [水準並排顯示視窗] 效果相同。
ms.assetid: b0e06766-1bd4-4744-81f3-139b018aa72c
title: 'TileHorizontally 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.TileHorizontally
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e295d0a7847afc0cb405f3ab9141e54ae424e9e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193340"
---
# <a name="shelltilehorizontally-method"></a><span data-ttu-id="5195c-104">TileHorizontally 方法</span><span class="sxs-lookup"><span data-stu-id="5195c-104">Shell.TileHorizontally method</span></span>

<span data-ttu-id="5195c-105">以水準方式並排顯示桌面上的所有視窗。</span><span class="sxs-lookup"><span data-stu-id="5195c-105">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="5195c-106">這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [ **水準並排顯示視窗**] 效果相同。</span><span class="sxs-lookup"><span data-stu-id="5195c-106">This method has the same effect as right-clicking the taskbar and selecting **Tile Windows Horizontally**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5195c-107">語法</span><span class="sxs-lookup"><span data-stu-id="5195c-107">Syntax</span></span>


```JScript
iRetVal = Shell.TileHorizontally()
```


```VB

Shell.TileHorizontally() As Integer
```





## <a name="parameters"></a><span data-ttu-id="5195c-108">參數</span><span class="sxs-lookup"><span data-stu-id="5195c-108">Parameters</span></span>

<span data-ttu-id="5195c-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="5195c-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="5195c-110">範例</span><span class="sxs-lookup"><span data-stu-id="5195c-110">Examples</span></span>

<span data-ttu-id="5195c-111">下列範例顯示使用中的 **TileHorizontally** 。</span><span class="sxs-lookup"><span data-stu-id="5195c-111">The following example shows **TileHorizontally** in use.</span></span> <span data-ttu-id="5195c-112">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="5195c-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="5195c-113">Jscript：</span><span class="sxs-lookup"><span data-stu-id="5195c-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTileHorizontallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TileHorizontally();
    }
</script>
```



<span data-ttu-id="5195c-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="5195c-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTileHorizontallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.TileHorizontally

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="5195c-115">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="5195c-115">Visual Basic:</span></span>


```VB
Private Sub fnShellTileHorizontallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.TileHorizontally

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="5195c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="5195c-116">Requirements</span></span>



| <span data-ttu-id="5195c-117">需求</span><span class="sxs-lookup"><span data-stu-id="5195c-117">Requirement</span></span> | <span data-ttu-id="5195c-118">值</span><span class="sxs-lookup"><span data-stu-id="5195c-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5195c-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5195c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5195c-120">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5195c-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5195c-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5195c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5195c-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5195c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5195c-123">標頭</span><span class="sxs-lookup"><span data-stu-id="5195c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5195c-124"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="5195c-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="5195c-125">Idl</span><span class="sxs-lookup"><span data-stu-id="5195c-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5195c-126"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="5195c-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="5195c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="5195c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5195c-128"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="5195c-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




