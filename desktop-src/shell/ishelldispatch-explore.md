---
description: IShellDispatch：流覽方法-在 Windows 檔案總管視窗中開啟指定的資料夾。
ms.assetid: DB434D02-56B2-4e8f-9E43-BBF47C7BE377
title: 'IShellDispatch： (Shldisp 的流覽方法) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Explore
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e693985cf7d8d83bd5a00595c42cd4427b0ebd5b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100556"
---
# <a name="ishelldispatchexplore-method"></a><span data-ttu-id="6c7a7-103">IShellDispatch。流覽方法</span><span class="sxs-lookup"><span data-stu-id="6c7a7-103">IShellDispatch.Explore method</span></span>

<span data-ttu-id="6c7a7-104">在 Windows 檔案總管視窗中開啟指定的資料夾。</span><span class="sxs-lookup"><span data-stu-id="6c7a7-104">Opens a specified folder in a Windows Explorer window.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c7a7-105">語法</span><span class="sxs-lookup"><span data-stu-id="6c7a7-105">Syntax</span></span>


```JScript
IShellDispatch.Explore(
  vDir
)
```


```VB

IShellDispatch.Explore( _
  ByVal vDir As Variant _
)
```





## <a name="parameters"></a><span data-ttu-id="6c7a7-106">參數</span><span class="sxs-lookup"><span data-stu-id="6c7a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c7a7-107">*vDir* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c7a7-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c7a7-108">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="6c7a7-108">Type: **Variant**</span></span>

<span data-ttu-id="6c7a7-109">要顯示的資料夾。</span><span class="sxs-lookup"><span data-stu-id="6c7a7-109">The folder to be displayed.</span></span> <span data-ttu-id="6c7a7-110">這可以是指定資料夾路徑或其中一個 [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) 值的字串。</span><span class="sxs-lookup"><span data-stu-id="6c7a7-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="6c7a7-111">請注意，在 **ShellSpecialFolderConstants** 中找到的常數名稱可以在 Visual Basic 中使用，但不能在 VBScript 或 JScript 中使用。</span><span class="sxs-lookup"><span data-stu-id="6c7a7-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="6c7a7-112">在這些情況下，必須在其位置使用數值。</span><span class="sxs-lookup"><span data-stu-id="6c7a7-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c7a7-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c7a7-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="6c7a7-114">JScript</span><span class="sxs-lookup"><span data-stu-id="6c7a7-114">JScript</span></span>

<span data-ttu-id="6c7a7-115">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6c7a7-115">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="6c7a7-116">VB</span><span class="sxs-lookup"><span data-stu-id="6c7a7-116">VB</span></span>

<span data-ttu-id="6c7a7-117">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6c7a7-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c7a7-118">備註</span><span class="sxs-lookup"><span data-stu-id="6c7a7-118">Remarks</span></span>

<span data-ttu-id="6c7a7-119">這個方法是透過 Shell 來執行和存取。請 [**流覽**](shell-explore.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="6c7a7-119">This method is implemented and accessed through the [**Shell.Explore**](shell-explore.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="6c7a7-120">範例</span><span class="sxs-lookup"><span data-stu-id="6c7a7-120">Examples</span></span>

<span data-ttu-id="6c7a7-121">下列範例示範如何在 JScript、VBScript 和 Visual Basic 中使用 **探索** 。</span><span class="sxs-lookup"><span data-stu-id="6c7a7-121">The following examples show the use of **Explore** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="6c7a7-122">Jscript：</span><span class="sxs-lookup"><span data-stu-id="6c7a7-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellExploreJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Explore("C:\\");
    }
</script>
```



<span data-ttu-id="6c7a7-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="6c7a7-123">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellExploreVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objshell.Explore(ssfWINDOWS)

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="6c7a7-124">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="6c7a7-124">Visual Basic:</span></span>


```VB
Private Sub fnShellExploreVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.Explore (ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="6c7a7-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c7a7-125">Requirements</span></span>



| <span data-ttu-id="6c7a7-126">需求</span><span class="sxs-lookup"><span data-stu-id="6c7a7-126">Requirement</span></span> | <span data-ttu-id="6c7a7-127">值</span><span class="sxs-lookup"><span data-stu-id="6c7a7-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c7a7-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c7a7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6c7a7-129">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c7a7-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6c7a7-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c7a7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6c7a7-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c7a7-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6c7a7-132">標頭</span><span class="sxs-lookup"><span data-stu-id="6c7a7-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c7a7-133"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="6c7a7-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="6c7a7-134">Idl</span><span class="sxs-lookup"><span data-stu-id="6c7a7-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6c7a7-135"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="6c7a7-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="6c7a7-136">DLL</span><span class="sxs-lookup"><span data-stu-id="6c7a7-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c7a7-137"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="6c7a7-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




