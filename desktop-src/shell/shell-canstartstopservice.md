---
description: CanStartStopService 方法-判斷目前的使用者是否可以啟動和停止命名服務。
ms.assetid: 1428F529-61F6-4113-A553-2C0D617FD859
title: 'CanStartStopService 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.CanStartStopService
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 29561519b95329093ef1f7bfc64023fd1ac4533d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083686"
---
# <a name="shellcanstartstopservice-method"></a><span data-ttu-id="fcbf6-103">CanStartStopService 方法</span><span class="sxs-lookup"><span data-stu-id="fcbf6-103">Shell.CanStartStopService method</span></span>

<span data-ttu-id="fcbf6-104">判斷目前的使用者是否可以啟動和停止命名服務。</span><span class="sxs-lookup"><span data-stu-id="fcbf6-104">Determines if the current user can start and stop the named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcbf6-105">語法</span><span class="sxs-lookup"><span data-stu-id="fcbf6-105">Syntax</span></span>


```JScript
retVal = Shell.CanStartStopService(
  sServiceName
)
```


```VB

Shell.CanStartStopService( _
  ByVal sServiceName As String _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="fcbf6-106">參數</span><span class="sxs-lookup"><span data-stu-id="fcbf6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcbf6-107">*sServiceName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fcbf6-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcbf6-108">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fcbf6-108">Type: **String**</span></span>

<span data-ttu-id="fcbf6-109">包含服務名稱的 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="fcbf6-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcbf6-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="fcbf6-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="fcbf6-111">JScript</span><span class="sxs-lookup"><span data-stu-id="fcbf6-111">JScript</span></span>

<span data-ttu-id="fcbf6-112">類型： **Variant \***</span><span class="sxs-lookup"><span data-stu-id="fcbf6-112">Type: **Variant\***</span></span>

<span data-ttu-id="fcbf6-113">如果使用者可以啟動和停止服務，則傳回 **true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="fcbf6-113">Returns **true** if the user can start and stop the service; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="fcbf6-114">VB</span><span class="sxs-lookup"><span data-stu-id="fcbf6-114">VB</span></span>

<span data-ttu-id="fcbf6-115">類型： **Variant \***</span><span class="sxs-lookup"><span data-stu-id="fcbf6-115">Type: **Variant\***</span></span>

<span data-ttu-id="fcbf6-116">如果使用者可以啟動和停止服務，則傳回 **true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="fcbf6-116">Returns **true** if the user can start and stop the service; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcbf6-117">備註</span><span class="sxs-lookup"><span data-stu-id="fcbf6-117">Remarks</span></span>

<span data-ttu-id="fcbf6-118">Microsoft Visual Basic 目前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="fcbf6-118">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="fcbf6-119">範例</span><span class="sxs-lookup"><span data-stu-id="fcbf6-119">Examples</span></span>

<span data-ttu-id="fcbf6-120">下列範例顯示 JScript 和 VBScript 的 **CanStartStopService** 用法。</span><span class="sxs-lookup"><span data-stu-id="fcbf6-120">The following examples show the usage of **CanStartStopService** for JScript and VBScript.</span></span>

<span data-ttu-id="fcbf6-121">Jscript：</span><span class="sxs-lookup"><span data-stu-id="fcbf6-121">JScript:</span></span>


```JScript
<script language="JScript">
    function fnCanStartStopServiceJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;

        bReturn = objShell.CanStartStopService("service name");
    }
</script>
```



<span data-ttu-id="fcbf6-122">VBScript</span><span class="sxs-lookup"><span data-stu-id="fcbf6-122">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnCanStartStopServiceVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.CanStartStopService("service name")

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="fcbf6-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="fcbf6-123">Requirements</span></span>



| <span data-ttu-id="fcbf6-124">需求</span><span class="sxs-lookup"><span data-stu-id="fcbf6-124">Requirement</span></span> | <span data-ttu-id="fcbf6-125">值</span><span class="sxs-lookup"><span data-stu-id="fcbf6-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcbf6-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fcbf6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fcbf6-127">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fcbf6-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fcbf6-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fcbf6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fcbf6-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fcbf6-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fcbf6-130">標頭</span><span class="sxs-lookup"><span data-stu-id="fcbf6-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcbf6-131"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="fcbf6-131"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="fcbf6-132">Idl</span><span class="sxs-lookup"><span data-stu-id="fcbf6-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fcbf6-133"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="fcbf6-133"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="fcbf6-134">DLL</span><span class="sxs-lookup"><span data-stu-id="fcbf6-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fcbf6-135"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="fcbf6-135"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




