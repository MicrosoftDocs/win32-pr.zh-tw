---
description: IShellDispatch4. WindowsSecurity 方法-顯示 [Windows 安全性] 對話方塊。
title: 'IShellDispatch4. WindowsSecurity 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.WindowsSecurity
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 665c4644-7749-446e-8212-3ecc9901a035
ms.openlocfilehash: 6eadb580c73e5e56592c94e997bdc22c2cf894b4
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843019"
---
# <a name="ishelldispatch4windowssecurity-method"></a><span data-ttu-id="737aa-103">IShellDispatch4. WindowsSecurity 方法</span><span class="sxs-lookup"><span data-stu-id="737aa-103">IShellDispatch4.WindowsSecurity method</span></span>

<span data-ttu-id="737aa-104">顯示 [ **Windows 安全性** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="737aa-104">Displays the **Windows Security** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="737aa-105">語法</span><span class="sxs-lookup"><span data-stu-id="737aa-105">Syntax</span></span>


```JScript
IShellDispatch4.WindowsSecurity()
```


```VB

IShellDispatch4.WindowsSecurity()
```





## <a name="parameters"></a><span data-ttu-id="737aa-106">參數</span><span class="sxs-lookup"><span data-stu-id="737aa-106">Parameters</span></span>

<span data-ttu-id="737aa-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="737aa-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="737aa-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="737aa-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="737aa-109">JScript</span><span class="sxs-lookup"><span data-stu-id="737aa-109">JScript</span></span>

<span data-ttu-id="737aa-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="737aa-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="737aa-111">VB</span><span class="sxs-lookup"><span data-stu-id="737aa-111">VB</span></span>

<span data-ttu-id="737aa-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="737aa-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="737aa-113">備註</span><span class="sxs-lookup"><span data-stu-id="737aa-113">Remarks</span></span>

<span data-ttu-id="737aa-114">這個方法會顯示按下 CTRL + ALT + DELETE 或使用 [ **開始** ] 功能表上的 [安全性] 選項之後所顯示的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="737aa-114">This method displays the dialog box shown after pressing CTRL+ALT+DELETE or using the security option on the **Start** menu.</span></span>

> [!Note]  
> <span data-ttu-id="737aa-115">只有當終端機會話連線到 Microsoft 終端機伺服器時，才能使用此方法。</span><span class="sxs-lookup"><span data-stu-id="737aa-115">This method can be used only when connected by a terminal session to Microsoft Terminal Server.</span></span>

 

## <a name="examples"></a><span data-ttu-id="737aa-116">範例</span><span class="sxs-lookup"><span data-stu-id="737aa-116">Examples</span></span>

<span data-ttu-id="737aa-117">下列範例示範如何使用 JScript、VBScript 和 Visual Basic 的 **WindowsSecurity** 。</span><span class="sxs-lookup"><span data-stu-id="737aa-117">The following examples show the use of **WindowsSecurity** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="737aa-118">Jscript：</span><span class="sxs-lookup"><span data-stu-id="737aa-118">JScript:</span></span>


```JScript
<script language="JScript">
     function fnIShellDispatch4WindowsSecurityJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.WindowsSecurity();
    }
</script>
```



<span data-ttu-id="737aa-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="737aa-119">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnIShellDispatch4WindowsSecurityVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            objshell.WindowsSecurity
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="737aa-120">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="737aa-120">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4WindowsSecurityVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        objshell.WindowsSecurity
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="737aa-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="737aa-121">Requirements</span></span>



| <span data-ttu-id="737aa-122">需求</span><span class="sxs-lookup"><span data-stu-id="737aa-122">Requirement</span></span> | <span data-ttu-id="737aa-123">值</span><span class="sxs-lookup"><span data-stu-id="737aa-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="737aa-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="737aa-124">Minimum supported client</span></span><br/> | <span data-ttu-id="737aa-125">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="737aa-125">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="737aa-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="737aa-126">Minimum supported server</span></span><br/> | <span data-ttu-id="737aa-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="737aa-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="737aa-128">標頭</span><span class="sxs-lookup"><span data-stu-id="737aa-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="737aa-129"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="737aa-129"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="737aa-130">Idl</span><span class="sxs-lookup"><span data-stu-id="737aa-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="737aa-131"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="737aa-131"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="737aa-132">DLL</span><span class="sxs-lookup"><span data-stu-id="737aa-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="737aa-133"><dt>Shell32.dll (6.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="737aa-133"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




