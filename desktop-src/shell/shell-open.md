---
description: 開啟指定的資料夾。
ms.assetid: 96ed9360-fb8f-4f7e-aefb-4a63ec95df07
title: 'Shell. Open method (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Open
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3572f48a7b129500c38c3c0227ba479ecb775067
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850028"
---
# <a name="shellopen-method"></a><span data-ttu-id="12d57-103">Shell. Open 方法</span><span class="sxs-lookup"><span data-stu-id="12d57-103">Shell.Open method</span></span>

<span data-ttu-id="12d57-104">開啟指定的資料夾。</span><span class="sxs-lookup"><span data-stu-id="12d57-104">Opens the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="12d57-105">語法</span><span class="sxs-lookup"><span data-stu-id="12d57-105">Syntax</span></span>


```JScript
iRetVal = Shell.Open(
  vDir
)
```


```VB

Shell.Open( _
  ByVal vDir As Variant _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="12d57-106">參數</span><span class="sxs-lookup"><span data-stu-id="12d57-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12d57-107">*vDir* \[在\]</span><span class="sxs-lookup"><span data-stu-id="12d57-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12d57-108">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="12d57-108">Type: **Variant**</span></span>

<span data-ttu-id="12d57-109">字串，指定資料夾的路徑或其中一個 [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) 值。</span><span class="sxs-lookup"><span data-stu-id="12d57-109">A string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="12d57-110">請注意，在 **ShellSpecialFolderConstants** 中找到的常數名稱可以在 Visual Basic 中使用，但不能在 VBScript 或 JScript 中使用。</span><span class="sxs-lookup"><span data-stu-id="12d57-110">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="12d57-111">在這些情況下，必須在其位置使用數值。</span><span class="sxs-lookup"><span data-stu-id="12d57-111">In those cases, the numeric values must be used in their place.</span></span>

<span data-ttu-id="12d57-112">如果 *vDir* 設定為其中一個 [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) 且特殊資料夾不存在，此函式將會建立資料夾。</span><span class="sxs-lookup"><span data-stu-id="12d57-112">If *vDir* is set to one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) and the special folder does not exist, this function will create the folder.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="12d57-113">範例</span><span class="sxs-lookup"><span data-stu-id="12d57-113">Examples</span></span>

<span data-ttu-id="12d57-114">下列範例顯示「 **開啟** 于使用中」。</span><span class="sxs-lookup"><span data-stu-id="12d57-114">The following example shows **Open** in use.</span></span> <span data-ttu-id="12d57-115">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="12d57-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="12d57-116">Jscript：</span><span class="sxs-lookup"><span data-stu-id="12d57-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellOpenJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36
        
        objShell.Shell.Open(ssfWINDOWS);
    }
</script>
```



<span data-ttu-id="12d57-117">VBScript</span><span class="sxs-lookup"><span data-stu-id="12d57-117">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellOpenVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.Shell.Open("C:\\")

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="12d57-118">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="12d57-118">Visual Basic:</span></span>


```VB
Private Sub fnShellOpenVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.Shell.Open(ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="12d57-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="12d57-119">Requirements</span></span>



| <span data-ttu-id="12d57-120">需求</span><span class="sxs-lookup"><span data-stu-id="12d57-120">Requirement</span></span> | <span data-ttu-id="12d57-121">值</span><span class="sxs-lookup"><span data-stu-id="12d57-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12d57-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="12d57-122">Minimum supported client</span></span><br/> | <span data-ttu-id="12d57-123">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12d57-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="12d57-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="12d57-124">Minimum supported server</span></span><br/> | <span data-ttu-id="12d57-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12d57-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="12d57-126">標頭</span><span class="sxs-lookup"><span data-stu-id="12d57-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="12d57-127"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="12d57-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="12d57-128">Idl</span><span class="sxs-lookup"><span data-stu-id="12d57-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="12d57-129"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="12d57-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="12d57-130">DLL</span><span class="sxs-lookup"><span data-stu-id="12d57-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12d57-131"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="12d57-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12d57-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12d57-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12d57-133">**殼層**</span><span class="sxs-lookup"><span data-stu-id="12d57-133">**Shell**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="12d57-134">**探索**</span><span class="sxs-lookup"><span data-stu-id="12d57-134">**Explore**</span></span>](shell-explore.md)
</dt> </dl>

 

 




