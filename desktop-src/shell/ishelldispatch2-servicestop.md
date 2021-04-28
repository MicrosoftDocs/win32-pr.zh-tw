---
description: IShellDispatch2. ServiceStop 方法-停止命名服務。
ms.assetid: f4cd0e2c-4ecc-4e9f-a0b5-d2a8a739f0e2
title: 'IShellDispatch2. ServiceStop 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ServiceStop
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 651138eb687cfd83406bc6e1a7fcf520ff001171
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117026"
---
# <a name="ishelldispatch2servicestop-method"></a><span data-ttu-id="fb72d-103">IShellDispatch2. ServiceStop 方法</span><span class="sxs-lookup"><span data-stu-id="fb72d-103">IShellDispatch2.ServiceStop method</span></span>

<span data-ttu-id="fb72d-104">停止已命名的服務。</span><span class="sxs-lookup"><span data-stu-id="fb72d-104">Stops a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb72d-105">語法</span><span class="sxs-lookup"><span data-stu-id="fb72d-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.ServiceStop(
  sServiceName,
  vPersistent
)
```


```VB

IShellDispatch2.ServiceStop( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="fb72d-106">參數</span><span class="sxs-lookup"><span data-stu-id="fb72d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb72d-107">*sServiceName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fb72d-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb72d-108">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="fb72d-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="fb72d-109">包含服務名稱的 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="fb72d-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="fb72d-110">*vPersistent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fb72d-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb72d-111">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="fb72d-111">Type: **Variant**</span></span>

<span data-ttu-id="fb72d-112">設定為 **true** ，以在呼叫 [**ServiceStart**](ishelldispatch2-servicestart.md) 時由服務控制管理員啟動服務。</span><span class="sxs-lookup"><span data-stu-id="fb72d-112">Set to **true** to have the service started by the service control manager when [**ServiceStart**](ishelldispatch2-servicestart.md) is called.</span></span> <span data-ttu-id="fb72d-113">若要讓服務設定保持不變，請將 *vPersistent* 設定為 **false**。</span><span class="sxs-lookup"><span data-stu-id="fb72d-113">To leave the service configuration unchanged, set *vPersistent* to **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb72d-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="fb72d-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="fb72d-115">JScript</span><span class="sxs-lookup"><span data-stu-id="fb72d-115">JScript</span></span>

<span data-ttu-id="fb72d-116">類型： **Variant \***</span><span class="sxs-lookup"><span data-stu-id="fb72d-116">Type: **Variant\***</span></span>

<span data-ttu-id="fb72d-117">如果成功，則傳回 **true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="fb72d-117">Returns **true** if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="fb72d-118">VB</span><span class="sxs-lookup"><span data-stu-id="fb72d-118">VB</span></span>

<span data-ttu-id="fb72d-119">類型： **Variant \***</span><span class="sxs-lookup"><span data-stu-id="fb72d-119">Type: **Variant\***</span></span>

<span data-ttu-id="fb72d-120">如果成功，則傳回 **true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="fb72d-120">Returns **true** if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb72d-121">備註</span><span class="sxs-lookup"><span data-stu-id="fb72d-121">Remarks</span></span>

<span data-ttu-id="fb72d-122">這個方法是透過 [**ServiceStop**](./shell-servicestop.md) 方法來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="fb72d-122">This method is implemented and accessed through the [**Shell.ServiceStop**](./shell-servicestop.md) method.</span></span>

<span data-ttu-id="fb72d-123">如果服務已停止，則此方法會傳回 **false** 。</span><span class="sxs-lookup"><span data-stu-id="fb72d-123">The method returns **false** if the service has already been stopped.</span></span> <span data-ttu-id="fb72d-124">在呼叫這個方法之前，您可以呼叫 [**IsServiceRunning**](./shell-isservicerunning.md) 來確定服務的狀態。</span><span class="sxs-lookup"><span data-stu-id="fb72d-124">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="fb72d-125">Microsoft Visual Basic 目前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="fb72d-125">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="fb72d-126">範例</span><span class="sxs-lookup"><span data-stu-id="fb72d-126">Examples</span></span>

<span data-ttu-id="fb72d-127">下列範例示範如何使用 **ServiceStop** 來停止 Messenger 服務。</span><span class="sxs-lookup"><span data-stu-id="fb72d-127">The following examples show the use of **ServiceStop** to stop the Messenger service.</span></span> <span data-ttu-id="fb72d-128">JScript 和 VBScript 會顯示使用方式。</span><span class="sxs-lookup"><span data-stu-id="fb72d-128">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="fb72d-129">Jscript：</span><span class="sxs-lookup"><span data-stu-id="fb72d-129">JScript:</span></span>


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



<span data-ttu-id="fb72d-130">VBScript</span><span class="sxs-lookup"><span data-stu-id="fb72d-130">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="fb72d-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb72d-131">Requirements</span></span>



| <span data-ttu-id="fb72d-132">需求</span><span class="sxs-lookup"><span data-stu-id="fb72d-132">Requirement</span></span> | <span data-ttu-id="fb72d-133">值</span><span class="sxs-lookup"><span data-stu-id="fb72d-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb72d-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fb72d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="fb72d-135">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb72d-135">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fb72d-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fb72d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="fb72d-137">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb72d-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fb72d-138">標頭</span><span class="sxs-lookup"><span data-stu-id="fb72d-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb72d-139"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="fb72d-139"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="fb72d-140">Idl</span><span class="sxs-lookup"><span data-stu-id="fb72d-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fb72d-141"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="fb72d-141"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="fb72d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="fb72d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb72d-143"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="fb72d-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
