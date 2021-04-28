---
description: IShellDispatch： Open method-開啟指定的資料夾。
ms.assetid: 30FE669A-4AFD-4dfa-9F62-E62E744469C7
title: 'IShellDispatch： Open 方法 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Open
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4b5301e030926b9bcfdc18949b6a04706c22bb71
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086626"
---
# <a name="ishelldispatchopen-method"></a><span data-ttu-id="41a13-103">IShellDispatch，Open 方法</span><span class="sxs-lookup"><span data-stu-id="41a13-103">IShellDispatch.Open method</span></span>

<span data-ttu-id="41a13-104">開啟指定的資料夾。</span><span class="sxs-lookup"><span data-stu-id="41a13-104">Opens the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="41a13-105">語法</span><span class="sxs-lookup"><span data-stu-id="41a13-105">Syntax</span></span>


```JScript
IShellDispatch.Open(
  vDir
)
```


```VB

IShellDispatch.Open( _
  ByVal vDir As Variant _
)
```





## <a name="parameters"></a><span data-ttu-id="41a13-106">參數</span><span class="sxs-lookup"><span data-stu-id="41a13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41a13-107">*vDir* \[在\]</span><span class="sxs-lookup"><span data-stu-id="41a13-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41a13-108">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="41a13-108">Type: **Variant**</span></span>

<span data-ttu-id="41a13-109">字串，指定資料夾的路徑或其中一個 [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) 值。</span><span class="sxs-lookup"><span data-stu-id="41a13-109">A string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="41a13-110">請注意，在 **ShellSpecialFolderConstants** 中找到的常數名稱可以在 Visual Basic 中使用，但不能在 VBScript 或 JScript 中使用。</span><span class="sxs-lookup"><span data-stu-id="41a13-110">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="41a13-111">在這些情況下，必須在其位置使用數值。</span><span class="sxs-lookup"><span data-stu-id="41a13-111">In those cases, the numeric values must be used in their place.</span></span>

<span data-ttu-id="41a13-112">如果 *vDir* 設定為其中一個 [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) 且特殊資料夾不存在，此函式將會建立資料夾。</span><span class="sxs-lookup"><span data-stu-id="41a13-112">If *vDir* is set to one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) and the special folder does not exist, this function will create the folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41a13-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="41a13-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="41a13-114">JScript</span><span class="sxs-lookup"><span data-stu-id="41a13-114">JScript</span></span>

<span data-ttu-id="41a13-115">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="41a13-115">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="41a13-116">VB</span><span class="sxs-lookup"><span data-stu-id="41a13-116">VB</span></span>

<span data-ttu-id="41a13-117">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="41a13-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="41a13-118">備註</span><span class="sxs-lookup"><span data-stu-id="41a13-118">Remarks</span></span>

<span data-ttu-id="41a13-119">這個方法是透過 [**Shell. Open**](shell-open.md) 方法來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="41a13-119">This method is implemented and accessed through the [**Shell.Open**](shell-open.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="41a13-120">範例</span><span class="sxs-lookup"><span data-stu-id="41a13-120">Examples</span></span>

<span data-ttu-id="41a13-121">下列範例示範如何在 JScript、VBScript 和 Visual Basic 中使用 **Open** 。</span><span class="sxs-lookup"><span data-stu-id="41a13-121">The following examples show the use of **Open** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="41a13-122">Jscript：</span><span class="sxs-lookup"><span data-stu-id="41a13-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellOpenJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36
        
        objshell.Open(ssfWINDOWS);
    }
</script>
```



<span data-ttu-id="41a13-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="41a13-123">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellOpenVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.Open("C:\")

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="41a13-124">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="41a13-124">Visual Basic:</span></span>


```VB
Private Sub fnShellOpenVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.Open (ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="41a13-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="41a13-125">Requirements</span></span>



| <span data-ttu-id="41a13-126">需求</span><span class="sxs-lookup"><span data-stu-id="41a13-126">Requirement</span></span> | <span data-ttu-id="41a13-127">值</span><span class="sxs-lookup"><span data-stu-id="41a13-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41a13-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="41a13-128">Minimum supported client</span></span><br/> | <span data-ttu-id="41a13-129">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41a13-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="41a13-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="41a13-130">Minimum supported server</span></span><br/> | <span data-ttu-id="41a13-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41a13-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="41a13-132">標頭</span><span class="sxs-lookup"><span data-stu-id="41a13-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="41a13-133"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="41a13-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="41a13-134">Idl</span><span class="sxs-lookup"><span data-stu-id="41a13-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="41a13-135"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="41a13-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="41a13-136">DLL</span><span class="sxs-lookup"><span data-stu-id="41a13-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41a13-137"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="41a13-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41a13-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41a13-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41a13-139">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="41a13-139">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="41a13-140">**探索**</span><span class="sxs-lookup"><span data-stu-id="41a13-140">**Explore**</span></span>](shell-explore.md)
</dt> </dl>

 

 




