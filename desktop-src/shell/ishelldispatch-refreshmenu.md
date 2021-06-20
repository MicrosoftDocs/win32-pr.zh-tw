---
description: 瞭解 IShellDispatch RefreshMenu 方法，這會重新整理 [開始] 功能表的內容。 只能與 Windows XP 之前的系統搭配使用。
ms.assetid: D36FA5A0-AF03-4627-86E0-869BF1440958
title: 'IShellDispatch. RefreshMenu 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.RefreshMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d9e1a3c326cfa79c7b754cc8a364e649cf2c9931
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404671"
---
# <a name="ishelldispatchrefreshmenu-method"></a><span data-ttu-id="f66f6-104">IShellDispatch. RefreshMenu 方法</span><span class="sxs-lookup"><span data-stu-id="f66f6-104">IShellDispatch.RefreshMenu method</span></span>

<span data-ttu-id="f66f6-105">重新整理 [ **開始** ] 功能表的內容。</span><span class="sxs-lookup"><span data-stu-id="f66f6-105">Refreshes the contents of the **Start** menu.</span></span> <span data-ttu-id="f66f6-106">只能與 Windows XP 之前的系統搭配使用。</span><span class="sxs-lookup"><span data-stu-id="f66f6-106">Used only with systems preceding Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="f66f6-107">語法</span><span class="sxs-lookup"><span data-stu-id="f66f6-107">Syntax</span></span>


```JScript
IShellDispatch.RefreshMenu()
```


```VB

IShellDispatch.RefreshMenu()
```





## <a name="parameters"></a><span data-ttu-id="f66f6-108">參數</span><span class="sxs-lookup"><span data-stu-id="f66f6-108">Parameters</span></span>

<span data-ttu-id="f66f6-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="f66f6-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f66f6-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="f66f6-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="f66f6-111">JScript</span><span class="sxs-lookup"><span data-stu-id="f66f6-111">JScript</span></span>

<span data-ttu-id="f66f6-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f66f6-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="f66f6-113">VB</span><span class="sxs-lookup"><span data-stu-id="f66f6-113">VB</span></span>

<span data-ttu-id="f66f6-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f66f6-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f66f6-115">備註</span><span class="sxs-lookup"><span data-stu-id="f66f6-115">Remarks</span></span>

<span data-ttu-id="f66f6-116">這個方法是透過 [**TrayProperties**](shell-trayproperties.md) 方法來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="f66f6-116">This method is implemented and accessed through the [**Shell.TrayProperties**](shell-trayproperties.md) method.</span></span>

<span data-ttu-id="f66f6-117">**RefreshMenu** 提供的功能會在 Windows XP 或更新版本下自動處理。</span><span class="sxs-lookup"><span data-stu-id="f66f6-117">The functionality that **RefreshMenu** provides is handled automatically under Windows XP or later.</span></span> <span data-ttu-id="f66f6-118">請勿在 Windows XP 或更新版本上呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="f66f6-118">Do not call this method on Windows XP or later.</span></span>

## <a name="examples"></a><span data-ttu-id="f66f6-119">範例</span><span class="sxs-lookup"><span data-stu-id="f66f6-119">Examples</span></span>

<span data-ttu-id="f66f6-120">下列範例示範如何在 JScript、VBScript 和 Visual Basic 中使用 **RefreshMenu** 。</span><span class="sxs-lookup"><span data-stu-id="f66f6-120">The following examples show the use of **RefreshMenu** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="f66f6-121">Jscript：</span><span class="sxs-lookup"><span data-stu-id="f66f6-121">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.RefreshMenu();
    }
</script>
```



<span data-ttu-id="f66f6-122">VBScript</span><span class="sxs-lookup"><span data-stu-id="f66f6-122">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellRefreshMenuVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.RefreshMenu

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="f66f6-123">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="f66f6-123">Visual Basic:</span></span>


```VB
Private Sub fnShellRefreshMenuVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.RefreshMenu

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="f66f6-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="f66f6-124">Requirements</span></span>



| <span data-ttu-id="f66f6-125">需求</span><span class="sxs-lookup"><span data-stu-id="f66f6-125">Requirement</span></span> | <span data-ttu-id="f66f6-126">值</span><span class="sxs-lookup"><span data-stu-id="f66f6-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f66f6-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f66f6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f66f6-128">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f66f6-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f66f6-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f66f6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f66f6-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f66f6-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f66f6-131">標頭</span><span class="sxs-lookup"><span data-stu-id="f66f6-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f66f6-132"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="f66f6-132"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f66f6-133">Idl</span><span class="sxs-lookup"><span data-stu-id="f66f6-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f66f6-134"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f66f6-134"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f66f6-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f66f6-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f66f6-136"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="f66f6-136"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




