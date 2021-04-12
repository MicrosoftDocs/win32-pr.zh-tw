---
description: 停止已命名的服務。
ms.assetid: AC22C91E-BBC6-4a2e-8D39-F9D7C0AC0947
title: 'ServiceStop 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ServiceStop
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 31388078fe1c0e15c2e54efc86f0ff76bcfb7ed2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193344"
---
# <a name="shellservicestop-method"></a><span data-ttu-id="02dc4-103">ServiceStop 方法</span><span class="sxs-lookup"><span data-stu-id="02dc4-103">Shell.ServiceStop method</span></span>

<span data-ttu-id="02dc4-104">停止已命名的服務。</span><span class="sxs-lookup"><span data-stu-id="02dc4-104">Stops a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="02dc4-105">語法</span><span class="sxs-lookup"><span data-stu-id="02dc4-105">Syntax</span></span>


```JScript
retVal = Shell.ServiceStop(
  sServiceName,
  vPersistent
)
```


```VB

Shell.ServiceStop( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="02dc4-106">參數</span><span class="sxs-lookup"><span data-stu-id="02dc4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02dc4-107">*sServiceName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="02dc4-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02dc4-108">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="02dc4-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="02dc4-109">包含服務名稱的 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="02dc4-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="02dc4-110">*vPersistent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="02dc4-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02dc4-111">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="02dc4-111">Type: **Variant**</span></span>

<span data-ttu-id="02dc4-112">設定為 **true** ，以在呼叫 [**ServiceStart**](./shell-servicestart.md) 時由服務控制管理員啟動服務。</span><span class="sxs-lookup"><span data-stu-id="02dc4-112">Set to **true** to have the service started by the service control manager when [**ServiceStart**](./shell-servicestart.md) is called.</span></span> <span data-ttu-id="02dc4-113">若要讓服務設定保持不變，請將 *vPersistent* 設定為 **false**。</span><span class="sxs-lookup"><span data-stu-id="02dc4-113">To leave the service configuration unchanged, set *vPersistent* to **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02dc4-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="02dc4-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="02dc4-115">JScript</span><span class="sxs-lookup"><span data-stu-id="02dc4-115">JScript</span></span>

<span data-ttu-id="02dc4-116">類型： \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="02dc4-116">Type: \**Variant\** _</span></span>

<span data-ttu-id="02dc4-117">如果成功，則傳回 _ \*true\*\*;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="02dc4-117">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="02dc4-118">VB</span><span class="sxs-lookup"><span data-stu-id="02dc4-118">VB</span></span>

<span data-ttu-id="02dc4-119">類型： \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="02dc4-119">Type: \**Variant\** _</span></span>

<span data-ttu-id="02dc4-120">如果成功，則傳回 _ \*true\*\*;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="02dc4-120">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="02dc4-121">備註</span><span class="sxs-lookup"><span data-stu-id="02dc4-121">Remarks</span></span>

<span data-ttu-id="02dc4-122">如果服務已停止，則此方法會傳回 **false** 。</span><span class="sxs-lookup"><span data-stu-id="02dc4-122">The method returns **false** if the service has already been stopped.</span></span> <span data-ttu-id="02dc4-123">在呼叫這個方法之前，您可以呼叫 [**IsServiceRunning**](./shell-isservicerunning.md) 來確定服務的狀態。</span><span class="sxs-lookup"><span data-stu-id="02dc4-123">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="02dc4-124">Microsoft Visual Basic 目前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="02dc4-124">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="02dc4-125">範例</span><span class="sxs-lookup"><span data-stu-id="02dc4-125">Examples</span></span>

<span data-ttu-id="02dc4-126">下列範例示範如何使用 **ServiceStop** 來停止 Messenger 服務。</span><span class="sxs-lookup"><span data-stu-id="02dc4-126">The following examples show the use of **ServiceStop** to stop the Messenger service.</span></span> <span data-ttu-id="02dc4-127">JScript 和 VBScript 會顯示使用方式。</span><span class="sxs-lookup"><span data-stu-id="02dc4-127">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="02dc4-128">Jscript：</span><span class="sxs-lookup"><span data-stu-id="02dc4-128">JScript:</span></span>


```JScript
<script language="JScript">
    function fnServiceStopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStop("Messenger", true);
    }
</script>
```



<span data-ttu-id="02dc4-129">VBScript</span><span class="sxs-lookup"><span data-stu-id="02dc4-129">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnServiceStopVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ServiceStop("Messenger", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="02dc4-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="02dc4-130">Requirements</span></span>



| <span data-ttu-id="02dc4-131">需求</span><span class="sxs-lookup"><span data-stu-id="02dc4-131">Requirement</span></span> | <span data-ttu-id="02dc4-132">值</span><span class="sxs-lookup"><span data-stu-id="02dc4-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02dc4-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="02dc4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="02dc4-134">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02dc4-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="02dc4-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="02dc4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="02dc4-136">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02dc4-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="02dc4-137">標頭</span><span class="sxs-lookup"><span data-stu-id="02dc4-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="02dc4-138"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="02dc4-138"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="02dc4-139">Idl</span><span class="sxs-lookup"><span data-stu-id="02dc4-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="02dc4-140"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="02dc4-140"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="02dc4-141">DLL</span><span class="sxs-lookup"><span data-stu-id="02dc4-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02dc4-142"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="02dc4-142"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
