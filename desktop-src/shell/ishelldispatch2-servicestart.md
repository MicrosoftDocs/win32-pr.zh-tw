---
description: 啟動命名服務。
ms.assetid: 3af57cdc-f449-433d-a9e1-119038045e4c
title: 'IShellDispatch2. ServiceStart 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ServiceStart
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 508b4f1c05625acdaed2b5a235ee697cceb544c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972385"
---
# <a name="ishelldispatch2servicestart-method"></a><span data-ttu-id="2c674-103">IShellDispatch2. ServiceStart 方法</span><span class="sxs-lookup"><span data-stu-id="2c674-103">IShellDispatch2.ServiceStart method</span></span>

<span data-ttu-id="2c674-104">啟動命名服務。</span><span class="sxs-lookup"><span data-stu-id="2c674-104">Starts a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c674-105">語法</span><span class="sxs-lookup"><span data-stu-id="2c674-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.ServiceStart(
  sServiceName,
  vPersistent
)
```


```VB

IShellDispatch2.ServiceStart( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="2c674-106">參數</span><span class="sxs-lookup"><span data-stu-id="2c674-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c674-107">*sServiceName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2c674-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c674-108">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="2c674-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="2c674-109">包含服務名稱的 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="2c674-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="2c674-110">*vPersistent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2c674-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c674-111">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="2c674-111">Type: **Variant**</span></span>

<span data-ttu-id="2c674-112">設定為 **true** ，讓服務控制管理員在系統啟動期間自動啟動服務。</span><span class="sxs-lookup"><span data-stu-id="2c674-112">Set to **true** to have the service started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="2c674-113">設定為 **false** ，讓服務設定保持不變。</span><span class="sxs-lookup"><span data-stu-id="2c674-113">Set to **false** to leave the service configuration unchanged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c674-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="2c674-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="2c674-115">JScript</span><span class="sxs-lookup"><span data-stu-id="2c674-115">JScript</span></span>

<span data-ttu-id="2c674-116">類型： \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="2c674-116">Type: \**Variant\** _</span></span>

<span data-ttu-id="2c674-117">如果成功，則傳回 _ \*true\*\*;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="2c674-117">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="2c674-118">VB</span><span class="sxs-lookup"><span data-stu-id="2c674-118">VB</span></span>

<span data-ttu-id="2c674-119">類型： \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="2c674-119">Type: \**Variant\** _</span></span>

<span data-ttu-id="2c674-120">如果成功，則傳回 _ \*true\*\*;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="2c674-120">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c674-121">備註</span><span class="sxs-lookup"><span data-stu-id="2c674-121">Remarks</span></span>

<span data-ttu-id="2c674-122">這個方法是透過 [**ServiceStart**](./shell-servicestart.md) 方法來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="2c674-122">This method is implemented and accessed through the [**Shell.ServiceStart**](./shell-servicestart.md) method.</span></span>

<span data-ttu-id="2c674-123">如果服務已經啟動，方法會傳回 **false** 。</span><span class="sxs-lookup"><span data-stu-id="2c674-123">The method returns **false** if the service has already been started.</span></span> <span data-ttu-id="2c674-124">在呼叫這個方法之前，您可以呼叫 [**IsServiceRunning**](./shell-isservicerunning.md) 來確定服務的狀態。</span><span class="sxs-lookup"><span data-stu-id="2c674-124">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="2c674-125">Microsoft Visual Basic 目前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="2c674-125">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="2c674-126">範例</span><span class="sxs-lookup"><span data-stu-id="2c674-126">Examples</span></span>

<span data-ttu-id="2c674-127">下列範例示範如何使用 **ServiceStart** 來啟動 Messenger 服務。</span><span class="sxs-lookup"><span data-stu-id="2c674-127">The following examples show the use of **ServiceStart** to start the Messenger service.</span></span> <span data-ttu-id="2c674-128">JScript 和 VBScript 會顯示使用方式。</span><span class="sxs-lookup"><span data-stu-id="2c674-128">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="2c674-129">Jscript：</span><span class="sxs-lookup"><span data-stu-id="2c674-129">JScript:</span></span>


```JScript
<script language="JScript">
    function fnServiceStartJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStart("Messenger", true);
    }
</script>
```



<span data-ttu-id="2c674-130">VBScript</span><span class="sxs-lookup"><span data-stu-id="2c674-130">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnServiceStartVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ServiceStart("Messenger", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="2c674-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c674-131">Requirements</span></span>



| <span data-ttu-id="2c674-132">需求</span><span class="sxs-lookup"><span data-stu-id="2c674-132">Requirement</span></span> | <span data-ttu-id="2c674-133">值</span><span class="sxs-lookup"><span data-stu-id="2c674-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c674-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c674-134">Minimum supported client</span></span><br/> | <span data-ttu-id="2c674-135">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c674-135">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2c674-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c674-136">Minimum supported server</span></span><br/> | <span data-ttu-id="2c674-137">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c674-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2c674-138">標頭</span><span class="sxs-lookup"><span data-stu-id="2c674-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c674-139"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="2c674-139"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="2c674-140">Idl</span><span class="sxs-lookup"><span data-stu-id="2c674-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2c674-141"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="2c674-141"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="2c674-142">DLL</span><span class="sxs-lookup"><span data-stu-id="2c674-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c674-143"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="2c674-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
