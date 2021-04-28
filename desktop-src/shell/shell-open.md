---
description: Shell. Open method-開啟指定的資料夾。
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
ms.openlocfilehash: 36f8914be3fce6b461e5267562e6f3ef40aa5fef
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104226"
---
# <a name="shellopen-method"></a><span data-ttu-id="499be-103">Shell. Open 方法</span><span class="sxs-lookup"><span data-stu-id="499be-103">Shell.Open method</span></span>

<span data-ttu-id="499be-104">開啟指定的資料夾。</span><span class="sxs-lookup"><span data-stu-id="499be-104">Opens the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="499be-105">語法</span><span class="sxs-lookup"><span data-stu-id="499be-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="499be-106">參數</span><span class="sxs-lookup"><span data-stu-id="499be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="499be-107">*vDir* \[在\]</span><span class="sxs-lookup"><span data-stu-id="499be-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="499be-108">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="499be-108">Type: **Variant**</span></span>

<span data-ttu-id="499be-109">字串，指定資料夾的路徑或其中一個 [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) 值。</span><span class="sxs-lookup"><span data-stu-id="499be-109">A string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="499be-110">請注意，在 **ShellSpecialFolderConstants** 中找到的常數名稱可以在 Visual Basic 中使用，但不能在 VBScript 或 JScript 中使用。</span><span class="sxs-lookup"><span data-stu-id="499be-110">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="499be-111">在這些情況下，必須在其位置使用數值。</span><span class="sxs-lookup"><span data-stu-id="499be-111">In those cases, the numeric values must be used in their place.</span></span>

<span data-ttu-id="499be-112">如果 *vDir* 設定為其中一個 [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) 且特殊資料夾不存在，此函式將會建立資料夾。</span><span class="sxs-lookup"><span data-stu-id="499be-112">If *vDir* is set to one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) and the special folder does not exist, this function will create the folder.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="499be-113">範例</span><span class="sxs-lookup"><span data-stu-id="499be-113">Examples</span></span>

<span data-ttu-id="499be-114">下列範例顯示「 **開啟** 于使用中」。</span><span class="sxs-lookup"><span data-stu-id="499be-114">The following example shows **Open** in use.</span></span> <span data-ttu-id="499be-115">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="499be-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="499be-116">Jscript：</span><span class="sxs-lookup"><span data-stu-id="499be-116">JScript:</span></span>


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



<span data-ttu-id="499be-117">VBScript</span><span class="sxs-lookup"><span data-stu-id="499be-117">VBScript:</span></span>


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



<span data-ttu-id="499be-118">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="499be-118">Visual Basic:</span></span>


```VB
Private Sub fnShellOpenVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.Shell.Open(ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="499be-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="499be-119">Requirements</span></span>



| <span data-ttu-id="499be-120">需求</span><span class="sxs-lookup"><span data-stu-id="499be-120">Requirement</span></span> | <span data-ttu-id="499be-121">值</span><span class="sxs-lookup"><span data-stu-id="499be-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="499be-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="499be-122">Minimum supported client</span></span><br/> | <span data-ttu-id="499be-123">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="499be-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="499be-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="499be-124">Minimum supported server</span></span><br/> | <span data-ttu-id="499be-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="499be-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="499be-126">標頭</span><span class="sxs-lookup"><span data-stu-id="499be-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="499be-127"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="499be-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="499be-128">Idl</span><span class="sxs-lookup"><span data-stu-id="499be-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="499be-129"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="499be-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="499be-130">DLL</span><span class="sxs-lookup"><span data-stu-id="499be-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="499be-131"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="499be-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="499be-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="499be-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="499be-133">**殼層**</span><span class="sxs-lookup"><span data-stu-id="499be-133">**Shell**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="499be-134">**探索**</span><span class="sxs-lookup"><span data-stu-id="499be-134">**Explore**</span></span>](shell-explore.md)
</dt> </dl>

 

 




