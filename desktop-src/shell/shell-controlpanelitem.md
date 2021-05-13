---
description: 執行指定的主控台 (\* cpl) 應用程式。
title: '傳送至 get-controlpanelitem 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ControlPanelItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 54979bbd-b36b-4b5b-a8a0-5f63e9526fa5
ms.openlocfilehash: 04d2493f5d0ec5b86d19689cb8e7c2a02a82e536
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841799"
---
# <a name="shellcontrolpanelitem-method"></a><span data-ttu-id="b6c0f-103">傳送至 get-controlpanelitem 方法</span><span class="sxs-lookup"><span data-stu-id="b6c0f-103">Shell.ControlPanelItem method</span></span>

<span data-ttu-id="b6c0f-104">執行指定的主控台 (\* cpl) 應用程式。</span><span class="sxs-lookup"><span data-stu-id="b6c0f-104">Runs the specified Control Panel (\*.cpl) application.</span></span> <span data-ttu-id="b6c0f-105">如果應用程式已經開啟，則會啟動執行中的實例。</span><span class="sxs-lookup"><span data-stu-id="b6c0f-105">If the application is already open, it will activate the running instance.</span></span>

> [!Note]  
> <span data-ttu-id="b6c0f-106">從 Windows Vista 開始，大部分的主控台應用程式都是 Shell 專案，無法使用此功能開啟。</span><span class="sxs-lookup"><span data-stu-id="b6c0f-106">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="b6c0f-107">若要開啟這些主控台的應用程式，請將正式名稱傳遞給 control.exe。</span><span class="sxs-lookup"><span data-stu-id="b6c0f-107">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="b6c0f-108">例如：</span><span class="sxs-lookup"><span data-stu-id="b6c0f-108">For example:</span></span>
>
> ``` syntax
> control.exe /name Microsoft.Personalization
> ```

 

## <a name="syntax"></a><span data-ttu-id="b6c0f-109">語法</span><span class="sxs-lookup"><span data-stu-id="b6c0f-109">Syntax</span></span>


```JScript
Shell.ControlPanelItem(
  bstrDir
)
```


```VB

Shell.ControlPanelItem( _
  ByVal bstrDir As BSTR _
)
```





## <a name="parameters"></a><span data-ttu-id="b6c0f-110">參數</span><span class="sxs-lookup"><span data-stu-id="b6c0f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6c0f-111">*bstrDir* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b6c0f-111">*bstrDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6c0f-112">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="b6c0f-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="b6c0f-113">主控台應用程式的檔案名。</span><span class="sxs-lookup"><span data-stu-id="b6c0f-113">The Control Panel application's file name.</span></span> <span data-ttu-id="b6c0f-114">所有主控台應用程式的副檔名為 cpl。</span><span class="sxs-lookup"><span data-stu-id="b6c0f-114">All Control Panel applications have the .cpl extension.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6c0f-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="b6c0f-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="b6c0f-116">JScript</span><span class="sxs-lookup"><span data-stu-id="b6c0f-116">JScript</span></span>

<span data-ttu-id="b6c0f-117">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b6c0f-117">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="b6c0f-118">VB</span><span class="sxs-lookup"><span data-stu-id="b6c0f-118">VB</span></span>

<span data-ttu-id="b6c0f-119">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b6c0f-119">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="b6c0f-120">範例</span><span class="sxs-lookup"><span data-stu-id="b6c0f-120">Examples</span></span>

<span data-ttu-id="b6c0f-121">下列範例會使用 **傳送至 get-controlpanelitem** 來執行主控台的 **顯示內容** 專案。</span><span class="sxs-lookup"><span data-stu-id="b6c0f-121">The following example uses **ControlPanelItem** to run the Control Panel's **Display Properties** item.</span></span> <span data-ttu-id="b6c0f-122">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="b6c0f-122">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="b6c0f-123">Jscript：</span><span class="sxs-lookup"><span data-stu-id="b6c0f-123">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellControlPanelItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ControlPanelItem("desk.cpl");
    }
</script>
```



<span data-ttu-id="b6c0f-124">VBScript</span><span class="sxs-lookup"><span data-stu-id="b6c0f-124">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellControlPanelItemVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.ControlPanelItem("desk.cpl")
       
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="b6c0f-125">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="b6c0f-125">Visual Basic:</span></span>


```VB
Private Sub fnShellControlPanelItemVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.ControlPanelItem ("desk.cpl")
    
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="b6c0f-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="b6c0f-126">Requirements</span></span>



| <span data-ttu-id="b6c0f-127">需求</span><span class="sxs-lookup"><span data-stu-id="b6c0f-127">Requirement</span></span> | <span data-ttu-id="b6c0f-128">值</span><span class="sxs-lookup"><span data-stu-id="b6c0f-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6c0f-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b6c0f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b6c0f-130">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b6c0f-130">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b6c0f-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b6c0f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b6c0f-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b6c0f-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b6c0f-133">標頭</span><span class="sxs-lookup"><span data-stu-id="b6c0f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6c0f-134"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="b6c0f-134"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b6c0f-135">Idl</span><span class="sxs-lookup"><span data-stu-id="b6c0f-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b6c0f-136"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="b6c0f-136"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b6c0f-137">DLL</span><span class="sxs-lookup"><span data-stu-id="b6c0f-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6c0f-138"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="b6c0f-138"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
