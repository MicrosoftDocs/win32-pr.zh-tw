---
description: 在 Windows 檔案總管視窗中開啟指定的資料夾。
ms.assetid: a788a3c4-f316-4fae-9294-3872eee8f46a
title: 'Shell。探索方法 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Explore
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 00b597aea0121e5f87f51886e8019a1130a20584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945007"
---
# <a name="shellexplore-method"></a><span data-ttu-id="242eb-103">Shell. 探索方法</span><span class="sxs-lookup"><span data-stu-id="242eb-103">Shell.Explore method</span></span>

<span data-ttu-id="242eb-104">在 Windows 檔案總管視窗中開啟指定的資料夾。</span><span class="sxs-lookup"><span data-stu-id="242eb-104">Opens a specified folder in a Windows Explorer window.</span></span>

## <a name="syntax"></a><span data-ttu-id="242eb-105">語法</span><span class="sxs-lookup"><span data-stu-id="242eb-105">Syntax</span></span>


```JScript
Shell.Explore(
  vDir
)
```


```VB

Shell.Explore( _
  ByVal vDir As Variant _
)
```





## <a name="parameters"></a><span data-ttu-id="242eb-106">參數</span><span class="sxs-lookup"><span data-stu-id="242eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="242eb-107">*vDir* \[在\]</span><span class="sxs-lookup"><span data-stu-id="242eb-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="242eb-108">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="242eb-108">Type: **Variant**</span></span>

<span data-ttu-id="242eb-109">要顯示的資料夾。</span><span class="sxs-lookup"><span data-stu-id="242eb-109">The folder to be displayed.</span></span> <span data-ttu-id="242eb-110">這可以是指定資料夾路徑或其中一個 [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) 值的字串。</span><span class="sxs-lookup"><span data-stu-id="242eb-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="242eb-111">請注意，在 **ShellSpecialFolderConstants** 中找到的常數名稱可以在 Visual Basic 中使用，但不能在 VBScript 或 JScript 中使用。</span><span class="sxs-lookup"><span data-stu-id="242eb-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="242eb-112">在這些情況下，必須在其位置使用數值。</span><span class="sxs-lookup"><span data-stu-id="242eb-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="242eb-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="242eb-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="242eb-114">JScript</span><span class="sxs-lookup"><span data-stu-id="242eb-114">JScript</span></span>

<span data-ttu-id="242eb-115">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="242eb-115">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="242eb-116">VB</span><span class="sxs-lookup"><span data-stu-id="242eb-116">VB</span></span>

<span data-ttu-id="242eb-117">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="242eb-117">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="242eb-118">範例</span><span class="sxs-lookup"><span data-stu-id="242eb-118">Examples</span></span>

<span data-ttu-id="242eb-119">下列範例示範如何使用 **探索** 。</span><span class="sxs-lookup"><span data-stu-id="242eb-119">The following example shows **Explore** in use.</span></span> <span data-ttu-id="242eb-120">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="242eb-120">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="242eb-121">Jscript：</span><span class="sxs-lookup"><span data-stu-id="242eb-121">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellExploreJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.Explore("C:\\");
    }
</script>]]>
```



<span data-ttu-id="242eb-122">VBScript</span><span class="sxs-lookup"><span data-stu-id="242eb-122">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellExploreVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objShell.Explore(ssfWINDOWS)

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="242eb-123">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="242eb-123">Visual Basic:</span></span>


```VB
Private Sub fnShellExploreVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.Explore (ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="242eb-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="242eb-124">Requirements</span></span>



| <span data-ttu-id="242eb-125">需求</span><span class="sxs-lookup"><span data-stu-id="242eb-125">Requirement</span></span> | <span data-ttu-id="242eb-126">值</span><span class="sxs-lookup"><span data-stu-id="242eb-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="242eb-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="242eb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="242eb-128">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="242eb-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="242eb-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="242eb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="242eb-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="242eb-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="242eb-131">標頭</span><span class="sxs-lookup"><span data-stu-id="242eb-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="242eb-132"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="242eb-132"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="242eb-133">Idl</span><span class="sxs-lookup"><span data-stu-id="242eb-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="242eb-134"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="242eb-134"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="242eb-135">DLL</span><span class="sxs-lookup"><span data-stu-id="242eb-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="242eb-136"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="242eb-136"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




