---
description: 執行指定的主控台應用程式。
title: 'IShellDispatch. 傳送至 get-controlpanelitem 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.ControlPanelItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9A9B6B3F-FBBC-4e76-8018-8858B6392276
ms.openlocfilehash: 1a1c024b316472be00f119485326b704a4fe8dd0
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842839"
---
# <a name="ishelldispatchcontrolpanelitem-method"></a><span data-ttu-id="ec602-103">IShellDispatch. 傳送至 get-controlpanelitem 方法</span><span class="sxs-lookup"><span data-stu-id="ec602-103">IShellDispatch.ControlPanelItem method</span></span>

<span data-ttu-id="ec602-104">執行指定的主控台應用程式。</span><span class="sxs-lookup"><span data-stu-id="ec602-104">Runs the specified Control Panel application.</span></span> <span data-ttu-id="ec602-105">如果應用程式已經開啟，則會啟動執行中的實例。</span><span class="sxs-lookup"><span data-stu-id="ec602-105">If the application is already open, it will activate the running instance.</span></span>

> [!Note]  
> <span data-ttu-id="ec602-106">從 Windows Vista 開始，大部分的主控台應用程式都是 Shell 專案，無法使用此功能開啟。</span><span class="sxs-lookup"><span data-stu-id="ec602-106">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="ec602-107">若要開啟這些主控台的應用程式，請將正式名稱傳遞給 control.exe。</span><span class="sxs-lookup"><span data-stu-id="ec602-107">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="ec602-108">例如：</span><span class="sxs-lookup"><span data-stu-id="ec602-108">For example:</span></span>
>
> ``` syntax
> control.exe /name Microsoft.Personalization
> ```

 

## <a name="syntax"></a><span data-ttu-id="ec602-109">語法</span><span class="sxs-lookup"><span data-stu-id="ec602-109">Syntax</span></span>


```JScript
IShellDispatch.ControlPanelItem(
  bstrDir
)
```


```VB

IShellDispatch.ControlPanelItem( _
  ByVal bstrDir As BSTR _
)
```





## <a name="parameters"></a><span data-ttu-id="ec602-110">參數</span><span class="sxs-lookup"><span data-stu-id="ec602-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec602-111">*bstrDir* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ec602-111">*bstrDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec602-112">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="ec602-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="ec602-113">主控台應用程式的檔案名。</span><span class="sxs-lookup"><span data-stu-id="ec602-113">The Control Panel application's file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec602-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="ec602-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="ec602-115">JScript</span><span class="sxs-lookup"><span data-stu-id="ec602-115">JScript</span></span>

<span data-ttu-id="ec602-116">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ec602-116">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="ec602-117">VB</span><span class="sxs-lookup"><span data-stu-id="ec602-117">VB</span></span>

<span data-ttu-id="ec602-118">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ec602-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec602-119">備註</span><span class="sxs-lookup"><span data-stu-id="ec602-119">Remarks</span></span>

<span data-ttu-id="ec602-120">這個方法是透過 [**傳送至 get-controlpanelitem**](shell-controlpanelitem.md) 方法來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="ec602-120">This method is implemented and accessed through the [**Shell.ControlPanelItem**](shell-controlpanelitem.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="ec602-121">範例</span><span class="sxs-lookup"><span data-stu-id="ec602-121">Examples</span></span>

<span data-ttu-id="ec602-122">下列範例會使用 [**傳送至 get-controlpanelitem**](shell-controlpanelitem.md) 來執行主控台的 **顯示內容** 專案。</span><span class="sxs-lookup"><span data-stu-id="ec602-122">The following examples use [**ControlPanelItem**](shell-controlpanelitem.md) to run the Control Panel's **Display Properties** item.</span></span> <span data-ttu-id="ec602-123">JScript、VBScript 和 Visual Basic 會顯示使用方式。</span><span class="sxs-lookup"><span data-stu-id="ec602-123">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="ec602-124">Jscript：</span><span class="sxs-lookup"><span data-stu-id="ec602-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellControlPanelItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Shell_ControlPanelItem("desk.cpl");
    }
</script>
```



<span data-ttu-id="ec602-125">VBScript</span><span class="sxs-lookup"><span data-stu-id="ec602-125">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellControlPanelItemVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.Shell_ControlPanelItem("desk.cpl")
       
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="ec602-126">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="ec602-126">Visual Basic:</span></span>


```VB
Private Sub fnShellControlPanelItemVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.Shell_ControlPanelItem ("desk.cpl")
    
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="ec602-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec602-127">Requirements</span></span>



| <span data-ttu-id="ec602-128">需求</span><span class="sxs-lookup"><span data-stu-id="ec602-128">Requirement</span></span> | <span data-ttu-id="ec602-129">值</span><span class="sxs-lookup"><span data-stu-id="ec602-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec602-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ec602-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ec602-131">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec602-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ec602-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ec602-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ec602-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec602-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ec602-134">標頭</span><span class="sxs-lookup"><span data-stu-id="ec602-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec602-135"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="ec602-135"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="ec602-136">Idl</span><span class="sxs-lookup"><span data-stu-id="ec602-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ec602-137"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="ec602-137"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="ec602-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ec602-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec602-139"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="ec602-139"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
