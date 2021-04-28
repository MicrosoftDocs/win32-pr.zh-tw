---
description: ServiceStart 方法-啟動命名服務。
ms.assetid: 72214E80-38A2-4a57-B555-942902BAFC3D
title: 'ServiceStart 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ServiceStart
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9c88b1980d215ad088a4a24362f17147b5d6e432
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083746"
---
# <a name="shellservicestart-method"></a><span data-ttu-id="17106-103">ServiceStart 方法</span><span class="sxs-lookup"><span data-stu-id="17106-103">Shell.ServiceStart method</span></span>

<span data-ttu-id="17106-104">啟動命名服務。</span><span class="sxs-lookup"><span data-stu-id="17106-104">Starts a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="17106-105">語法</span><span class="sxs-lookup"><span data-stu-id="17106-105">Syntax</span></span>


```JScript
retVal = Shell.ServiceStart(
  sServiceName,
  vPersistent
)
```


```VB

Shell.ServiceStart( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="17106-106">參數</span><span class="sxs-lookup"><span data-stu-id="17106-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17106-107">*sServiceName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="17106-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17106-108">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="17106-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="17106-109">包含服務名稱的 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="17106-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="17106-110">*vPersistent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="17106-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17106-111">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="17106-111">Type: **Variant**</span></span>

<span data-ttu-id="17106-112">設定為 **true** ，讓服務控制管理員在系統啟動期間自動啟動服務。</span><span class="sxs-lookup"><span data-stu-id="17106-112">Set to **true** to have the service started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="17106-113">設定為 **false** ，讓服務設定保持不變。</span><span class="sxs-lookup"><span data-stu-id="17106-113">Set to **false** to leave the service configuration unchanged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17106-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="17106-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="17106-115">JScript</span><span class="sxs-lookup"><span data-stu-id="17106-115">JScript</span></span>

<span data-ttu-id="17106-116">類型： **Variant \***</span><span class="sxs-lookup"><span data-stu-id="17106-116">Type: **Variant\***</span></span>

<span data-ttu-id="17106-117">如果成功，則傳回 **true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="17106-117">Returns **true** if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="17106-118">VB</span><span class="sxs-lookup"><span data-stu-id="17106-118">VB</span></span>

<span data-ttu-id="17106-119">類型： **Variant \***</span><span class="sxs-lookup"><span data-stu-id="17106-119">Type: **Variant\***</span></span>

<span data-ttu-id="17106-120">如果成功，則傳回 **true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="17106-120">Returns **true** if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="17106-121">備註</span><span class="sxs-lookup"><span data-stu-id="17106-121">Remarks</span></span>

<span data-ttu-id="17106-122">如果服務已經啟動，方法會傳回 **false** 。</span><span class="sxs-lookup"><span data-stu-id="17106-122">The method returns **false** if the service has already been started.</span></span> <span data-ttu-id="17106-123">在呼叫這個方法之前，您可以呼叫 [**IsServiceRunning**](./shell-isservicerunning.md) 來確定服務的狀態。</span><span class="sxs-lookup"><span data-stu-id="17106-123">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="17106-124">Microsoft Visual Basic 目前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="17106-124">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="17106-125">範例</span><span class="sxs-lookup"><span data-stu-id="17106-125">Examples</span></span>

<span data-ttu-id="17106-126">下列範例示範如何使用 **ServiceStart** 來啟動 Messenger 服務。</span><span class="sxs-lookup"><span data-stu-id="17106-126">The following examples show the use of **ServiceStart** to start the Messenger service.</span></span> <span data-ttu-id="17106-127">JScript 和 VBScript 會顯示使用方式。</span><span class="sxs-lookup"><span data-stu-id="17106-127">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="17106-128">Jscript：</span><span class="sxs-lookup"><span data-stu-id="17106-128">JScript:</span></span>


```JScript
<script language="JScript">
    function fnServiceStartJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStart("Messenger", true);
    }
```



<span data-ttu-id="17106-129">VBScript</span><span class="sxs-lookup"><span data-stu-id="17106-129">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="17106-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="17106-130">Requirements</span></span>



| <span data-ttu-id="17106-131">需求</span><span class="sxs-lookup"><span data-stu-id="17106-131">Requirement</span></span> | <span data-ttu-id="17106-132">值</span><span class="sxs-lookup"><span data-stu-id="17106-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17106-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="17106-133">Minimum supported client</span></span><br/> | <span data-ttu-id="17106-134">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="17106-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="17106-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="17106-135">Minimum supported server</span></span><br/> | <span data-ttu-id="17106-136">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="17106-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="17106-137">標頭</span><span class="sxs-lookup"><span data-stu-id="17106-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="17106-138"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="17106-138"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="17106-139">Idl</span><span class="sxs-lookup"><span data-stu-id="17106-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="17106-140"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="17106-140"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="17106-141">DLL</span><span class="sxs-lookup"><span data-stu-id="17106-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17106-142"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="17106-142"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
