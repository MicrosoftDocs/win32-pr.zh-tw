---
description: 垂直並排顯示桌面上的所有視窗。 這個方法的效果與在工作列上按一下滑鼠右鍵，然後垂直選取 [並排顯示視窗] 效果相同。
ms.assetid: 7d0f6dbe-b5a6-431b-954f-7ef2c62c68ea
title: 'TileVertically 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.TileVertically
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8ecea9df2bcbb2e410841231ed7eca170872e015
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973676"
---
# <a name="shelltilevertically-method"></a><span data-ttu-id="48050-104">TileVertically 方法</span><span class="sxs-lookup"><span data-stu-id="48050-104">Shell.TileVertically method</span></span>

<span data-ttu-id="48050-105">垂直並排顯示桌面上的所有視窗。</span><span class="sxs-lookup"><span data-stu-id="48050-105">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="48050-106">這個方法的效果與在工作列上按一下滑鼠右鍵，然後垂直選取 [ **並排顯示視窗**] 效果相同。</span><span class="sxs-lookup"><span data-stu-id="48050-106">This method has the same effect as right-clicking the taskbar and selecting **Tile Windows Vertically**.</span></span>

## <a name="syntax"></a><span data-ttu-id="48050-107">語法</span><span class="sxs-lookup"><span data-stu-id="48050-107">Syntax</span></span>


```JScript
iRetVal = Shell.TileVertically()
```


```VB

Shell.TileVertically() As Integer
```





## <a name="parameters"></a><span data-ttu-id="48050-108">參數</span><span class="sxs-lookup"><span data-stu-id="48050-108">Parameters</span></span>

<span data-ttu-id="48050-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="48050-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="48050-110">範例</span><span class="sxs-lookup"><span data-stu-id="48050-110">Examples</span></span>

<span data-ttu-id="48050-111">下列範例顯示使用中的 **TileVertically** 。</span><span class="sxs-lookup"><span data-stu-id="48050-111">The following example shows **TileVertically** in use.</span></span> <span data-ttu-id="48050-112">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="48050-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="48050-113">Jscript：</span><span class="sxs-lookup"><span data-stu-id="48050-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTileVerticallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TileVertically();
    }
</script>
```



<span data-ttu-id="48050-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="48050-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTileVerticallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.TileVertically

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="48050-115">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="48050-115">Visual Basic:</span></span>


```VB
Private Sub fnShellTileVerticallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.TileVertically

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="48050-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="48050-116">Requirements</span></span>



| <span data-ttu-id="48050-117">需求</span><span class="sxs-lookup"><span data-stu-id="48050-117">Requirement</span></span> | <span data-ttu-id="48050-118">值</span><span class="sxs-lookup"><span data-stu-id="48050-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48050-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="48050-119">Minimum supported client</span></span><br/> | <span data-ttu-id="48050-120">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48050-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="48050-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="48050-121">Minimum supported server</span></span><br/> | <span data-ttu-id="48050-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48050-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="48050-123">標頭</span><span class="sxs-lookup"><span data-stu-id="48050-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="48050-124"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="48050-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="48050-125">Idl</span><span class="sxs-lookup"><span data-stu-id="48050-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="48050-126"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="48050-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="48050-127">DLL</span><span class="sxs-lookup"><span data-stu-id="48050-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48050-128"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="48050-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




