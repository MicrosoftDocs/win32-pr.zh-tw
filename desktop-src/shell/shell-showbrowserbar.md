---
description: ShowBrowserBar 方法-顯示瀏覽器列。
ms.assetid: 203636D2-54D3-4163-B9AC-39213D6F4203
title: 'ShowBrowserBar 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShowBrowserBar
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d19cd5b98ce39470860cc481ab05e4bb41adc9a4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083722"
---
# <a name="shellshowbrowserbar-method"></a><span data-ttu-id="eaafc-103">ShowBrowserBar 方法</span><span class="sxs-lookup"><span data-stu-id="eaafc-103">Shell.ShowBrowserBar method</span></span>

<span data-ttu-id="eaafc-104">顯示瀏覽器列。</span><span class="sxs-lookup"><span data-stu-id="eaafc-104">Displays a browser bar.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaafc-105">語法</span><span class="sxs-lookup"><span data-stu-id="eaafc-105">Syntax</span></span>


```JScript
retVal = Shell.ShowBrowserBar(
  sCLSID,
  vShow
)
```


```VB

Shell.ShowBrowserBar( _
  ByVal sCLSID As BSTR, _
  ByVal vShow As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="eaafc-106">參數</span><span class="sxs-lookup"><span data-stu-id="eaafc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaafc-107">*sCLSID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eaafc-107">*sCLSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eaafc-108">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="eaafc-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="eaafc-109">**字串**，包含要顯示的瀏覽器列之 CLSID 的字串形式。</span><span class="sxs-lookup"><span data-stu-id="eaafc-109">A **String** that contains the string form of the CLSID of the browser bar to be displayed.</span></span> <span data-ttu-id="eaafc-110">物件必須註冊為具有 CATID \_ InfoBand 元件類別目錄的 Explorer Bar 物件。</span><span class="sxs-lookup"><span data-stu-id="eaafc-110">The object must be registered as an Explorer Bar object with a CATID\_InfoBand component category.</span></span> <span data-ttu-id="eaafc-111">如需詳細資訊，請參閱 [建立自訂的瀏覽器列、工具區和書桌等區](band-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="eaafc-111">For further information, see [Creating Custom Explorer Bars, Tool Bands, and Desk Bands](band-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="eaafc-112">*vShow* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eaafc-112">*vShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eaafc-113">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="eaafc-113">Type: **Variant**</span></span>

<span data-ttu-id="eaafc-114">設定為 **true** 會顯示流覽列，或設定為 **false** 以隱藏它。</span><span class="sxs-lookup"><span data-stu-id="eaafc-114">Set to **true** to show the browser bar or **false** to hide it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eaafc-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="eaafc-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="eaafc-116">JScript</span><span class="sxs-lookup"><span data-stu-id="eaafc-116">JScript</span></span>

<span data-ttu-id="eaafc-117">類型： **Variant \***</span><span class="sxs-lookup"><span data-stu-id="eaafc-117">Type: **Variant\***</span></span>

<span data-ttu-id="eaafc-118">如果成功，則傳回 **true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="eaafc-118">Returns **true** if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="eaafc-119">VB</span><span class="sxs-lookup"><span data-stu-id="eaafc-119">VB</span></span>

<span data-ttu-id="eaafc-120">類型： **Variant \***</span><span class="sxs-lookup"><span data-stu-id="eaafc-120">Type: **Variant\***</span></span>

<span data-ttu-id="eaafc-121">如果成功，則傳回 **true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="eaafc-121">Returns **true** if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="eaafc-122">備註</span><span class="sxs-lookup"><span data-stu-id="eaafc-122">Remarks</span></span>

<span data-ttu-id="eaafc-123">您可以將 *sCLSID* 參數設定為該 explorer 列的 CLSID，以顯示其中一個標準 Explorer 列。</span><span class="sxs-lookup"><span data-stu-id="eaafc-123">You can display one of the standard Explorer Bars by setting the *sCLSID* parameter to the CLSID of that Explorer Bar.</span></span> <span data-ttu-id="eaafc-124">標準 Explorer 列和其 CLSID 字串如下所示：</span><span class="sxs-lookup"><span data-stu-id="eaafc-124">The standard Explorer Bars and their CLSID strings are as follows:</span></span>



| <span data-ttu-id="eaafc-125">Explorer Bar</span><span class="sxs-lookup"><span data-stu-id="eaafc-125">Explorer Bar</span></span> | <span data-ttu-id="eaafc-126">CLSID 字串</span><span class="sxs-lookup"><span data-stu-id="eaafc-126">CLSID string</span></span>                           |
|--------------|----------------------------------------|
| <span data-ttu-id="eaafc-127">我的最愛</span><span class="sxs-lookup"><span data-stu-id="eaafc-127">Favorites</span></span>    | <span data-ttu-id="eaafc-128">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="eaafc-128">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="eaafc-129">資料夾</span><span class="sxs-lookup"><span data-stu-id="eaafc-129">Folders</span></span>      | <span data-ttu-id="eaafc-130">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="eaafc-130">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="eaafc-131">記錄</span><span class="sxs-lookup"><span data-stu-id="eaafc-131">History</span></span>      | <span data-ttu-id="eaafc-132">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="eaafc-132">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="eaafc-133">搜尋</span><span class="sxs-lookup"><span data-stu-id="eaafc-133">Search</span></span>       | <span data-ttu-id="eaafc-134">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span><span class="sxs-lookup"><span data-stu-id="eaafc-134">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span></span> |



 

<span data-ttu-id="eaafc-135">Microsoft Visual Basic 目前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="eaafc-135">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="eaafc-136">範例</span><span class="sxs-lookup"><span data-stu-id="eaafc-136">Examples</span></span>

<span data-ttu-id="eaafc-137">下列範例示範如何使用 **ShowBrowserBar** 來顯示 [我的最愛 **]** 瀏覽器列。</span><span class="sxs-lookup"><span data-stu-id="eaafc-137">The following examples show the use of **Shell.ShowBrowserBar** to display the **Favorites** browser bar.</span></span> <span data-ttu-id="eaafc-138">JScript 和 VBScript 會顯示使用方式。</span><span class="sxs-lookup"><span data-stu-id="eaafc-138">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="eaafc-139">Jscript：</span><span class="sxs-lookup"><span data-stu-id="eaafc-139">JScript:</span></span>


```JScript
<script language="JavaScript">
    function fnShowBrowserBarJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true);
    }
</script>
```



<span data-ttu-id="eaafc-140">VBScript</span><span class="sxs-lookup"><span data-stu-id="eaafc-140">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShowBrowserBarVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="eaafc-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="eaafc-141">Requirements</span></span>



| <span data-ttu-id="eaafc-142">需求</span><span class="sxs-lookup"><span data-stu-id="eaafc-142">Requirement</span></span> | <span data-ttu-id="eaafc-143">值</span><span class="sxs-lookup"><span data-stu-id="eaafc-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaafc-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eaafc-144">Minimum supported client</span></span><br/> | <span data-ttu-id="eaafc-145">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eaafc-145">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eaafc-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eaafc-146">Minimum supported server</span></span><br/> | <span data-ttu-id="eaafc-147">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eaafc-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="eaafc-148">標頭</span><span class="sxs-lookup"><span data-stu-id="eaafc-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="eaafc-149"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="eaafc-149"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="eaafc-150">Idl</span><span class="sxs-lookup"><span data-stu-id="eaafc-150">IDL</span></span><br/>                      | <dl> <span data-ttu-id="eaafc-151"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="eaafc-151"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="eaafc-152">DLL</span><span class="sxs-lookup"><span data-stu-id="eaafc-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eaafc-153"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="eaafc-153"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
