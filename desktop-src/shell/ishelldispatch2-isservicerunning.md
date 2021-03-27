---
description: 傳回值，這個值表示特定服務是否正在執行。
ms.assetid: 91f3fba1-7aa5-423a-bc37-49db230c79db
title: 'IShellDispatch2. IsServiceRunning 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.IsServiceRunning
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f39cd7da3d9959830208ab971b636e146e549775
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972396"
---
# <a name="ishelldispatch2isservicerunning-method"></a><span data-ttu-id="5df48-103">IShellDispatch2. IsServiceRunning 方法</span><span class="sxs-lookup"><span data-stu-id="5df48-103">IShellDispatch2.IsServiceRunning method</span></span>

<span data-ttu-id="5df48-104">傳回值，這個值表示特定服務是否正在執行。</span><span class="sxs-lookup"><span data-stu-id="5df48-104">Returns a value that indicates whether a particular service is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="5df48-105">語法</span><span class="sxs-lookup"><span data-stu-id="5df48-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.IsServiceRunning(
  sServiceName
)
```


```VB

IShellDispatch2.IsServiceRunning( _
  ByVal sServiceName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="5df48-106">參數</span><span class="sxs-lookup"><span data-stu-id="5df48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5df48-107">*sServiceName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5df48-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5df48-108">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="5df48-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="5df48-109">包含服務名稱的 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="5df48-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5df48-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="5df48-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="5df48-111">JScript</span><span class="sxs-lookup"><span data-stu-id="5df48-111">JScript</span></span>

<span data-ttu-id="5df48-112">類型： \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="5df48-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="5df48-113">如果 *sServiceName* 所指定的服務正在執行，則傳回 _ \*true\*\*。否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="5df48-113">Returns _ *true*\* if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="5df48-114">VB</span><span class="sxs-lookup"><span data-stu-id="5df48-114">VB</span></span>

<span data-ttu-id="5df48-115">類型： \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="5df48-115">Type: \**Variant\** _</span></span>

<span data-ttu-id="5df48-116">如果 *sServiceName* 所指定的服務正在執行，則傳回 _ \*true\*\*。否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="5df48-116">Returns _ *true*\* if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5df48-117">備註</span><span class="sxs-lookup"><span data-stu-id="5df48-117">Remarks</span></span>

<span data-ttu-id="5df48-118">這個方法是透過 [**IsServiceRunning**](./shell-isservicerunning.md) 方法來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="5df48-118">This method is implemented and accessed through the [**Shell.IsServiceRunning**](./shell-isservicerunning.md) method.</span></span>

<span data-ttu-id="5df48-119">Microsoft Visual Basic 目前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="5df48-119">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="5df48-120">範例</span><span class="sxs-lookup"><span data-stu-id="5df48-120">Examples</span></span>

<span data-ttu-id="5df48-121">下列範例示範如何使用 **IsServiceRunning** 來判斷應用程式的主題服務是否正在執行。</span><span class="sxs-lookup"><span data-stu-id="5df48-121">The following examples show the use of **IsServiceRunning** to determine whether the Themes service is running for an application.</span></span> <span data-ttu-id="5df48-122">JScript 和 VBScript 會顯示使用方式。</span><span class="sxs-lookup"><span data-stu-id="5df48-122">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="5df48-123">Jscript：</span><span class="sxs-lookup"><span data-stu-id="5df48-123">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIsServiceRunningJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
    
        bReturn = objShell.IsServiceRunning("Themes");
    }
</script>
```



<span data-ttu-id="5df48-124">VBScript</span><span class="sxs-lookup"><span data-stu-id="5df48-124">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIsServiceRunningVB()
        dim objShell
        dim bReturn
    
        set objShell = CreateObject("shell.application")
    
        bReturn = objShell.IsServiceRunning("Themes")
    
        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="5df48-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="5df48-125">Requirements</span></span>



| <span data-ttu-id="5df48-126">需求</span><span class="sxs-lookup"><span data-stu-id="5df48-126">Requirement</span></span> | <span data-ttu-id="5df48-127">值</span><span class="sxs-lookup"><span data-stu-id="5df48-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5df48-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5df48-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5df48-129">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5df48-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5df48-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5df48-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5df48-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5df48-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="5df48-132">標頭</span><span class="sxs-lookup"><span data-stu-id="5df48-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="5df48-133"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="5df48-133"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="5df48-134">Idl</span><span class="sxs-lookup"><span data-stu-id="5df48-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5df48-135"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="5df48-135"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="5df48-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5df48-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5df48-137"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="5df48-137"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
