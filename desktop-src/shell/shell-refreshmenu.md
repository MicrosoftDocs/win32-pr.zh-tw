---
description: 深入瞭解 RefreshMenu 方法，此方法會重新整理 [開始] 功能表的內容。 只能與 Windows XP 之前的系統搭配使用。
ms.assetid: 1269c66d-61df-432d-9220-5ac975e3ad58
title: 'RefreshMenu 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.RefreshMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 90020cd128f5cbc585bd7bc9ab33a8a81c745f8e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404531"
---
# <a name="shellrefreshmenu-method"></a><span data-ttu-id="255e1-104">RefreshMenu 方法</span><span class="sxs-lookup"><span data-stu-id="255e1-104">Shell.RefreshMenu method</span></span>

<span data-ttu-id="255e1-105">重新整理 [ **開始** ] 功能表的內容。</span><span class="sxs-lookup"><span data-stu-id="255e1-105">Refreshes the contents of the **Start** menu.</span></span> <span data-ttu-id="255e1-106">只能與 Windows XP 之前的系統搭配使用。</span><span class="sxs-lookup"><span data-stu-id="255e1-106">Used only with systems preceding Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="255e1-107">語法</span><span class="sxs-lookup"><span data-stu-id="255e1-107">Syntax</span></span>


```JScript
iRetVal = Shell.RefreshMenu()
```


```VB

Shell.RefreshMenu() As Integer
```





## <a name="parameters"></a><span data-ttu-id="255e1-108">參數</span><span class="sxs-lookup"><span data-stu-id="255e1-108">Parameters</span></span>

<span data-ttu-id="255e1-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="255e1-109">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="255e1-110">備註</span><span class="sxs-lookup"><span data-stu-id="255e1-110">Remarks</span></span>

<span data-ttu-id="255e1-111">**RefreshMenu** 提供的功能會在 Windows XP 或更新版本下自動處理。</span><span class="sxs-lookup"><span data-stu-id="255e1-111">The functionality that **RefreshMenu** provides is handled automatically under Windows XP or later.</span></span> <span data-ttu-id="255e1-112">請勿在該作業系統下呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="255e1-112">Do not call this method under that operating system.</span></span>

## <a name="examples"></a><span data-ttu-id="255e1-113">範例</span><span class="sxs-lookup"><span data-stu-id="255e1-113">Examples</span></span>

<span data-ttu-id="255e1-114">下列範例顯示使用中的 **RefreshMenu** 。</span><span class="sxs-lookup"><span data-stu-id="255e1-114">The following example shows **RefreshMenu** in use.</span></span> <span data-ttu-id="255e1-115">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="255e1-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="255e1-116">Jscript：</span><span class="sxs-lookup"><span data-stu-id="255e1-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.RefreshMenu();
    }
</script>
```



<span data-ttu-id="255e1-117">VBScript</span><span class="sxs-lookup"><span data-stu-id="255e1-117">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellRefreshMenuVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.RefreshMenu

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="255e1-118">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="255e1-118">Visual Basic:</span></span>


```VB
Private Sub fnShellRefreshMenuVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.RefreshMenu

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="255e1-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="255e1-119">Requirements</span></span>



| <span data-ttu-id="255e1-120">需求</span><span class="sxs-lookup"><span data-stu-id="255e1-120">Requirement</span></span> | <span data-ttu-id="255e1-121">值</span><span class="sxs-lookup"><span data-stu-id="255e1-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="255e1-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="255e1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="255e1-123">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="255e1-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="255e1-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="255e1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="255e1-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="255e1-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="255e1-126">標頭</span><span class="sxs-lookup"><span data-stu-id="255e1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="255e1-127"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="255e1-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="255e1-128">Idl</span><span class="sxs-lookup"><span data-stu-id="255e1-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="255e1-129"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="255e1-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="255e1-130">DLL</span><span class="sxs-lookup"><span data-stu-id="255e1-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="255e1-131"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="255e1-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




