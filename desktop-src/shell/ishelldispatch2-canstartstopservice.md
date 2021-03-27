---
description: 判斷目前的使用者是否可以啟動和停止命名服務。
ms.assetid: cbb54ae9-02e6-4243-a782-e9f125c21c0d
title: 'IShellDispatch2. CanStartStopService 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.CanStartStopService
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 92655c2c561284f00204826e1848a75f00f4a04d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512213"
---
# <a name="ishelldispatch2canstartstopservice-method"></a><span data-ttu-id="f0947-103">IShellDispatch2. CanStartStopService 方法</span><span class="sxs-lookup"><span data-stu-id="f0947-103">IShellDispatch2.CanStartStopService method</span></span>

<span data-ttu-id="f0947-104">判斷目前的使用者是否可以啟動和停止命名服務。</span><span class="sxs-lookup"><span data-stu-id="f0947-104">Determines if the current user can start and stop the named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0947-105">語法</span><span class="sxs-lookup"><span data-stu-id="f0947-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.CanStartStopService(
  sServiceName
)
```


```VB

IShellDispatch2.CanStartStopService( _
  ByVal sServiceName As String _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="f0947-106">參數</span><span class="sxs-lookup"><span data-stu-id="f0947-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0947-107">*sServiceName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f0947-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0947-108">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f0947-108">Type: **String**</span></span>

<span data-ttu-id="f0947-109">包含服務名稱的 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="f0947-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0947-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="f0947-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="f0947-111">JScript</span><span class="sxs-lookup"><span data-stu-id="f0947-111">JScript</span></span>

<span data-ttu-id="f0947-112">類型： \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="f0947-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="f0947-113">如果使用者可以啟動和停止服務，則傳回 _ \*true\*\*。否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="f0947-113">Returns _ *true*\* if the user can start and stop the service; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="f0947-114">VB</span><span class="sxs-lookup"><span data-stu-id="f0947-114">VB</span></span>

<span data-ttu-id="f0947-115">類型： \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="f0947-115">Type: \**Variant\** _</span></span>

<span data-ttu-id="f0947-116">如果使用者可以啟動和停止服務，則傳回 _ \*true\*\*。否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="f0947-116">Returns _ *true*\* if the user can start and stop the service; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0947-117">備註</span><span class="sxs-lookup"><span data-stu-id="f0947-117">Remarks</span></span>

<span data-ttu-id="f0947-118">這個方法是透過 [**CanStartStopService**](./shell-canstartstopservice.md) 方法來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="f0947-118">This method is implemented and accessed through the [**Shell.CanStartStopService**](./shell-canstartstopservice.md) method.</span></span>

<span data-ttu-id="f0947-119">Microsoft Visual Basic 目前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="f0947-119">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="f0947-120">範例</span><span class="sxs-lookup"><span data-stu-id="f0947-120">Examples</span></span>

<span data-ttu-id="f0947-121">下列範例顯示 JScript 和 VBScript 的 **CanStartStopService** 用法。</span><span class="sxs-lookup"><span data-stu-id="f0947-121">The following examples show the usage of **CanStartStopService** for JScript and VBScript.</span></span>

<span data-ttu-id="f0947-122">Jscript：</span><span class="sxs-lookup"><span data-stu-id="f0947-122">JScript:</span></span>


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



<span data-ttu-id="f0947-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="f0947-123">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="f0947-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0947-124">Requirements</span></span>



| <span data-ttu-id="f0947-125">需求</span><span class="sxs-lookup"><span data-stu-id="f0947-125">Requirement</span></span> | <span data-ttu-id="f0947-126">值</span><span class="sxs-lookup"><span data-stu-id="f0947-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0947-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f0947-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f0947-128">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0947-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f0947-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f0947-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f0947-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0947-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f0947-131">標頭</span><span class="sxs-lookup"><span data-stu-id="f0947-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0947-132"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="f0947-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="f0947-133">Idl</span><span class="sxs-lookup"><span data-stu-id="f0947-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f0947-134"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f0947-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="f0947-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f0947-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0947-136"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="f0947-136"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
