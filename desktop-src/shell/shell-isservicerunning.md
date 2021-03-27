---
description: 傳回值，這個值表示特定服務是否正在執行。
ms.assetid: FDC41C2D-7462-458f-BBE6-D97260C26B6C
title: 'IsServiceRunning 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.IsServiceRunning
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c3a65be4955c6f49e8e6baa49cd9dedb82fc5cc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849363"
---
# <a name="shellisservicerunning-method"></a><span data-ttu-id="48ed8-103">IsServiceRunning 方法</span><span class="sxs-lookup"><span data-stu-id="48ed8-103">Shell.IsServiceRunning method</span></span>

<span data-ttu-id="48ed8-104">傳回值，這個值表示特定服務是否正在執行。</span><span class="sxs-lookup"><span data-stu-id="48ed8-104">Returns a value that indicates whether a particular service is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="48ed8-105">語法</span><span class="sxs-lookup"><span data-stu-id="48ed8-105">Syntax</span></span>


```JScript
retVal = Shell.IsServiceRunning(
  sServiceName
)
```


```VB

Shell.IsServiceRunning( _
  ByVal sServiceName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="48ed8-106">參數</span><span class="sxs-lookup"><span data-stu-id="48ed8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48ed8-107">*sServiceName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="48ed8-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48ed8-108">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="48ed8-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="48ed8-109">包含服務名稱的 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="48ed8-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48ed8-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="48ed8-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="48ed8-111">JScript</span><span class="sxs-lookup"><span data-stu-id="48ed8-111">JScript</span></span>

<span data-ttu-id="48ed8-112">類型： \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="48ed8-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="48ed8-113">如果 *sServiceName* 所指定的服務正在執行，則傳回 _ \*true\*\*。否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="48ed8-113">Returns _ *true*\* if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="48ed8-114">VB</span><span class="sxs-lookup"><span data-stu-id="48ed8-114">VB</span></span>

<span data-ttu-id="48ed8-115">類型： \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="48ed8-115">Type: \**Variant\** _</span></span>

<span data-ttu-id="48ed8-116">如果 *sServiceName* 所指定的服務正在執行，則傳回 _ \*true\*\*。否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="48ed8-116">Returns _ *true*\* if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="48ed8-117">備註</span><span class="sxs-lookup"><span data-stu-id="48ed8-117">Remarks</span></span>

<span data-ttu-id="48ed8-118">Microsoft Visual Basic 目前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="48ed8-118">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="48ed8-119">範例</span><span class="sxs-lookup"><span data-stu-id="48ed8-119">Examples</span></span>

<span data-ttu-id="48ed8-120">下列範例示範如何使用 **IsServiceRunning** 來判斷應用程式的主題服務是否正在執行。</span><span class="sxs-lookup"><span data-stu-id="48ed8-120">The following examples show the use of **IsServiceRunning** to determine whether the Themes service is running for an application.</span></span> <span data-ttu-id="48ed8-121">JScript 和 VBScript 會顯示使用方式。</span><span class="sxs-lookup"><span data-stu-id="48ed8-121">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="48ed8-122">Jscript：</span><span class="sxs-lookup"><span data-stu-id="48ed8-122">JScript:</span></span>


```JScript
function fnIsServiceRunningJ()
{
    var objShell = new ActiveXObject("shell.application");
    var bReturn;

    bReturn = objShell.IsServiceRunning("Themes");
}
```



<span data-ttu-id="48ed8-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="48ed8-123">VBScript:</span></span>


```VB
function fnIsServiceRunningVB()
    dim objShell
    dim bReturn

    set objShell = CreateObject("shell.application")

    bReturn = objShell.IsServiceRunning("Themes")

    set objShell = nothing
end function
```



## <a name="requirements"></a><span data-ttu-id="48ed8-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="48ed8-124">Requirements</span></span>



| <span data-ttu-id="48ed8-125">需求</span><span class="sxs-lookup"><span data-stu-id="48ed8-125">Requirement</span></span> | <span data-ttu-id="48ed8-126">值</span><span class="sxs-lookup"><span data-stu-id="48ed8-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48ed8-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="48ed8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="48ed8-128">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48ed8-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="48ed8-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="48ed8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="48ed8-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48ed8-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="48ed8-131">標頭</span><span class="sxs-lookup"><span data-stu-id="48ed8-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="48ed8-132"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="48ed8-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="48ed8-133">Idl</span><span class="sxs-lookup"><span data-stu-id="48ed8-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="48ed8-134"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="48ed8-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="48ed8-135">DLL</span><span class="sxs-lookup"><span data-stu-id="48ed8-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48ed8-136"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="48ed8-136"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
