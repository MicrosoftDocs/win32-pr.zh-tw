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
ms.openlocfilehash: 2d7e8cfbd1e7a2a2392b78487c6a58b62de6df6a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116806"
---
# <a name="ishelldispatch4windowssecurity-method"></a><span data-ttu-id="fa093-103">IShellDispatch4. WindowsSecurity 方法</span><span class="sxs-lookup"><span data-stu-id="fa093-103">IShellDispatch4.WindowsSecurity method</span></span>

<span data-ttu-id="fa093-104">顯示 [ **Windows 安全性** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="fa093-104">Displays the **Windows Security** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa093-105">語法</span><span class="sxs-lookup"><span data-stu-id="fa093-105">Syntax</span></span>


```JScript
IShellDispatch4.WindowsSecurity()
```


```VB

IShellDispatch4.WindowsSecurity()
```





## <a name="parameters"></a><span data-ttu-id="fa093-106">參數</span><span class="sxs-lookup"><span data-stu-id="fa093-106">Parameters</span></span>

<span data-ttu-id="fa093-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="fa093-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fa093-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="fa093-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="fa093-109">JScript</span><span class="sxs-lookup"><span data-stu-id="fa093-109">JScript</span></span>

<span data-ttu-id="fa093-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="fa093-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="fa093-111">VB</span><span class="sxs-lookup"><span data-stu-id="fa093-111">VB</span></span>

<span data-ttu-id="fa093-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="fa093-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa093-113">備註</span><span class="sxs-lookup"><span data-stu-id="fa093-113">Remarks</span></span>

<span data-ttu-id="fa093-114">這個方法會顯示按下 CTRL + ALT + DELETE 或使用 [ **開始** ] 功能表上的 [安全性] 選項之後所顯示的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="fa093-114">This method displays the dialog box shown after pressing CTRL+ALT+DELETE or using the security option on the **Start** menu.</span></span>

> [!Note]  
> <span data-ttu-id="fa093-115">只有當終端機會話連線到 Microsoft 終端機伺服器時，才能使用此方法。</span><span class="sxs-lookup"><span data-stu-id="fa093-115">This method can be used only when connected by a terminal session to Microsoft Terminal Server.</span></span>

 

## <a name="examples"></a><span data-ttu-id="fa093-116">範例</span><span class="sxs-lookup"><span data-stu-id="fa093-116">Examples</span></span>

<span data-ttu-id="fa093-117">下列範例示範如何使用 JScript、VBScript 和 Visual Basic 的 **WindowsSecurity** 。</span><span class="sxs-lookup"><span data-stu-id="fa093-117">The following examples show the use of **WindowsSecurity** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="fa093-118">Jscript：</span><span class="sxs-lookup"><span data-stu-id="fa093-118">JScript:</span></span>


```JScript
<script language="JScript">
     function fnIShellDispatch4WindowsSecurityJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.WindowsSecurity();
    }
</script>
```



<span data-ttu-id="fa093-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="fa093-119">VBScript:</span></span>


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



<span data-ttu-id="fa093-120">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="fa093-120">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4WindowsSecurityVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        objshell.WindowsSecurity
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="fa093-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa093-121">Requirements</span></span>



| <span data-ttu-id="fa093-122">需求</span><span class="sxs-lookup"><span data-stu-id="fa093-122">Requirement</span></span> | <span data-ttu-id="fa093-123">值</span><span class="sxs-lookup"><span data-stu-id="fa093-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa093-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa093-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fa093-125">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa093-125">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="fa093-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa093-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fa093-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa093-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fa093-128">標頭</span><span class="sxs-lookup"><span data-stu-id="fa093-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa093-129"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="fa093-129"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="fa093-130">Idl</span><span class="sxs-lookup"><span data-stu-id="fa093-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fa093-131"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="fa093-131"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="fa093-132">DLL</span><span class="sxs-lookup"><span data-stu-id="fa093-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa093-133"><dt>Shell32.dll (6.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="fa093-133"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




