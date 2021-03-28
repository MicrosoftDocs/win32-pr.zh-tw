---
description: 判斷目前的使用者是否可以啟動和停止命名服務。
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
ms.openlocfilehash: 1d92fa076141bdebc8a2f24059a65e842e5a3d6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944490"
---
# <a name="shellcanstartstopservice-method"></a><span data-ttu-id="ba159-103">CanStartStopService 方法</span><span class="sxs-lookup"><span data-stu-id="ba159-103">Shell.CanStartStopService method</span></span>

<span data-ttu-id="ba159-104">判斷目前的使用者是否可以啟動和停止命名服務。</span><span class="sxs-lookup"><span data-stu-id="ba159-104">Determines if the current user can start and stop the named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba159-105">語法</span><span class="sxs-lookup"><span data-stu-id="ba159-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="ba159-106">參數</span><span class="sxs-lookup"><span data-stu-id="ba159-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba159-107">*sServiceName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ba159-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba159-108">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ba159-108">Type: **String**</span></span>

<span data-ttu-id="ba159-109">包含服務名稱的 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="ba159-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba159-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="ba159-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="ba159-111">JScript</span><span class="sxs-lookup"><span data-stu-id="ba159-111">JScript</span></span>

<span data-ttu-id="ba159-112">類型： \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="ba159-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="ba159-113">如果使用者可以啟動和停止服務，則傳回 _ \*true\*\*。否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="ba159-113">Returns _ *true*\* if the user can start and stop the service; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="ba159-114">VB</span><span class="sxs-lookup"><span data-stu-id="ba159-114">VB</span></span>

<span data-ttu-id="ba159-115">類型： \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="ba159-115">Type: \**Variant\** _</span></span>

<span data-ttu-id="ba159-116">如果使用者可以啟動和停止服務，則傳回 _ \*true\*\*。否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="ba159-116">Returns _ *true*\* if the user can start and stop the service; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba159-117">備註</span><span class="sxs-lookup"><span data-stu-id="ba159-117">Remarks</span></span>

<span data-ttu-id="ba159-118">Microsoft Visual Basic 目前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="ba159-118">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="ba159-119">範例</span><span class="sxs-lookup"><span data-stu-id="ba159-119">Examples</span></span>

<span data-ttu-id="ba159-120">下列範例顯示 JScript 和 VBScript 的 **CanStartStopService** 用法。</span><span class="sxs-lookup"><span data-stu-id="ba159-120">The following examples show the usage of **CanStartStopService** for JScript and VBScript.</span></span>

<span data-ttu-id="ba159-121">Jscript：</span><span class="sxs-lookup"><span data-stu-id="ba159-121">JScript:</span></span>


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



<span data-ttu-id="ba159-122">VBScript</span><span class="sxs-lookup"><span data-stu-id="ba159-122">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="ba159-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="ba159-123">Requirements</span></span>



| <span data-ttu-id="ba159-124">需求</span><span class="sxs-lookup"><span data-stu-id="ba159-124">Requirement</span></span> | <span data-ttu-id="ba159-125">值</span><span class="sxs-lookup"><span data-stu-id="ba159-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba159-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ba159-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ba159-127">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ba159-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ba159-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ba159-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ba159-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ba159-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ba159-130">標頭</span><span class="sxs-lookup"><span data-stu-id="ba159-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba159-131"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="ba159-131"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="ba159-132">Idl</span><span class="sxs-lookup"><span data-stu-id="ba159-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ba159-133"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="ba159-133"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="ba159-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ba159-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba159-135"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="ba159-135"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




