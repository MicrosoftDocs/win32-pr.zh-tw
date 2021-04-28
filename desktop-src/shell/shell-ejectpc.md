---
description: EjectPC 方法-將電腦從其銜接站中取出。 如果您的電腦支援此命令，則這與按一下 [開始] 功能表並選取 [退出電腦] 相同。
ms.assetid: eaba3dce-8fea-453f-90c2-4a9b5cb05ecc
title: 'EjectPC 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.EjectPC
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5ec08aaa82d2f752fa06537434adede86b9d5a3a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104346"
---
# <a name="shellejectpc-method"></a><span data-ttu-id="2c605-104">EjectPC 方法</span><span class="sxs-lookup"><span data-stu-id="2c605-104">Shell.EjectPC method</span></span>

<span data-ttu-id="2c605-105">從其銜接站彈出電腦。</span><span class="sxs-lookup"><span data-stu-id="2c605-105">Ejects the computer from its docking station.</span></span> <span data-ttu-id="2c605-106">這與按一下 [ **開始** ] 功能表並選取 [ **退出** 電腦] 的方式相同，如果您的電腦支援此命令。</span><span class="sxs-lookup"><span data-stu-id="2c605-106">This is the same as clicking the **Start** menu and selecting **Eject PC**, if your computer supports this command.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c605-107">語法</span><span class="sxs-lookup"><span data-stu-id="2c605-107">Syntax</span></span>


```JScript
Shell.EjectPC()
```


```VB

Shell.EjectPC()
```





## <a name="parameters"></a><span data-ttu-id="2c605-108">參數</span><span class="sxs-lookup"><span data-stu-id="2c605-108">Parameters</span></span>

<span data-ttu-id="2c605-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2c605-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2c605-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="2c605-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="2c605-111">JScript</span><span class="sxs-lookup"><span data-stu-id="2c605-111">JScript</span></span>

<span data-ttu-id="2c605-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2c605-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="2c605-113">VB</span><span class="sxs-lookup"><span data-stu-id="2c605-113">VB</span></span>

<span data-ttu-id="2c605-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2c605-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="2c605-115">範例</span><span class="sxs-lookup"><span data-stu-id="2c605-115">Examples</span></span>

<span data-ttu-id="2c605-116">下列範例顯示使用中的 **EjectPC** 。</span><span class="sxs-lookup"><span data-stu-id="2c605-116">The following example shows **EjectPC** in use.</span></span> <span data-ttu-id="2c605-117">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="2c605-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="2c605-118">Jscript：</span><span class="sxs-lookup"><span data-stu-id="2c605-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellEjectPCJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.EjectPC();
    }
</script>
```



<span data-ttu-id="2c605-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="2c605-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellEjectPCVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.EjectPC

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="2c605-120">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="2c605-120">Visual Basic:</span></span>


```VB
Private Sub fnShellEjectPCVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.EjectPC

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="2c605-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c605-121">Requirements</span></span>



| <span data-ttu-id="2c605-122">需求</span><span class="sxs-lookup"><span data-stu-id="2c605-122">Requirement</span></span> | <span data-ttu-id="2c605-123">值</span><span class="sxs-lookup"><span data-stu-id="2c605-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c605-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c605-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2c605-125">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c605-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2c605-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c605-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2c605-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c605-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2c605-128">標頭</span><span class="sxs-lookup"><span data-stu-id="2c605-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c605-129"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="2c605-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="2c605-130">Idl</span><span class="sxs-lookup"><span data-stu-id="2c605-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2c605-131"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="2c605-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="2c605-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2c605-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c605-133"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="2c605-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




