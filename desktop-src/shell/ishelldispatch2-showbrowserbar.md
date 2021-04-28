---
description: IShellDispatch2. ShowBrowserBar 方法-顯示瀏覽器列。
ms.assetid: 5776370c-3bbf-449b-a8fe-2dbc7d89dd25
title: 'IShellDispatch2. ShowBrowserBar 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ShowBrowserBar
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7143b55ae59c8fca845d256ddc1f79e69672364b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116936"
---
# <a name="ishelldispatch2showbrowserbar-method"></a><span data-ttu-id="cbbca-103">IShellDispatch2. ShowBrowserBar 方法</span><span class="sxs-lookup"><span data-stu-id="cbbca-103">IShellDispatch2.ShowBrowserBar method</span></span>

<span data-ttu-id="cbbca-104">顯示瀏覽器列。</span><span class="sxs-lookup"><span data-stu-id="cbbca-104">Displays a browser bar.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbbca-105">語法</span><span class="sxs-lookup"><span data-stu-id="cbbca-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.ShowBrowserBar(
  sCLSID,
  vShow
)
```


```VB

IShellDispatch2.ShowBrowserBar( _
  ByVal sCLSID As BSTR, _
  ByVal vShow As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="cbbca-106">參數</span><span class="sxs-lookup"><span data-stu-id="cbbca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbbca-107">*sCLSID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cbbca-107">*sCLSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbbca-108">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="cbbca-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="cbbca-109">**字串**，包含要顯示的瀏覽器列之 CLSID 的字串形式。</span><span class="sxs-lookup"><span data-stu-id="cbbca-109">A **String** that contains the string form of the CLSID of the browser bar to be displayed.</span></span> <span data-ttu-id="cbbca-110">物件必須註冊為具有 CATID \_ InfoBand 元件類別目錄的 Explorer Bar 物件。</span><span class="sxs-lookup"><span data-stu-id="cbbca-110">The object must be registered as an Explorer Bar object with a CATID\_InfoBand component category.</span></span> <span data-ttu-id="cbbca-111">如需詳細資訊，請參閱 [建立自訂的瀏覽器列、工具區和書桌等區](band-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="cbbca-111">For further information, see [Creating Custom Explorer Bars, Tool Bands, and Desk Bands](band-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="cbbca-112">*vShow* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cbbca-112">*vShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbbca-113">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="cbbca-113">Type: **Variant**</span></span>

<span data-ttu-id="cbbca-114">設定為 **true** 會顯示流覽列，或設定為 **false** 以隱藏它。</span><span class="sxs-lookup"><span data-stu-id="cbbca-114">Set to **true** to show the browser bar or **false** to hide it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbbca-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="cbbca-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="cbbca-116">JScript</span><span class="sxs-lookup"><span data-stu-id="cbbca-116">JScript</span></span>

<span data-ttu-id="cbbca-117">類型： **Variant \***</span><span class="sxs-lookup"><span data-stu-id="cbbca-117">Type: **Variant\***</span></span>

<span data-ttu-id="cbbca-118">如果成功，則傳回 **true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="cbbca-118">Returns **true** if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="cbbca-119">VB</span><span class="sxs-lookup"><span data-stu-id="cbbca-119">VB</span></span>

<span data-ttu-id="cbbca-120">類型： **Variant \***</span><span class="sxs-lookup"><span data-stu-id="cbbca-120">Type: **Variant\***</span></span>

<span data-ttu-id="cbbca-121">如果成功，則傳回 **true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="cbbca-121">Returns **true** if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbbca-122">備註</span><span class="sxs-lookup"><span data-stu-id="cbbca-122">Remarks</span></span>

<span data-ttu-id="cbbca-123">這個方法是透過 [**ShowBrowserBar**](./shell-showbrowserbar.md) 方法來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="cbbca-123">This method is implemented and accessed through the [**Shell.ShowBrowserBar**](./shell-showbrowserbar.md) method.</span></span>

<span data-ttu-id="cbbca-124">您可以將 *sCLSID* 參數設定為該 explorer 列的 CLSID，以顯示其中一個標準 Explorer 列。</span><span class="sxs-lookup"><span data-stu-id="cbbca-124">You can display one of the standard Explorer Bars by setting the *sCLSID* parameter to the CLSID of that Explorer Bar.</span></span> <span data-ttu-id="cbbca-125">標準 Explorer 列和其 CLSID 字串如下所示：</span><span class="sxs-lookup"><span data-stu-id="cbbca-125">The standard Explorer Bars and their CLSID strings are as follows:</span></span>



| <span data-ttu-id="cbbca-126">Explorer Bar</span><span class="sxs-lookup"><span data-stu-id="cbbca-126">Explorer Bar</span></span> | <span data-ttu-id="cbbca-127">CLSID 字串</span><span class="sxs-lookup"><span data-stu-id="cbbca-127">CLSID string</span></span>                           |
|--------------|----------------------------------------|
| <span data-ttu-id="cbbca-128">我的最愛</span><span class="sxs-lookup"><span data-stu-id="cbbca-128">Favorites</span></span>    | <span data-ttu-id="cbbca-129">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="cbbca-129">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="cbbca-130">資料夾</span><span class="sxs-lookup"><span data-stu-id="cbbca-130">Folders</span></span>      | <span data-ttu-id="cbbca-131">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="cbbca-131">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="cbbca-132">記錄</span><span class="sxs-lookup"><span data-stu-id="cbbca-132">History</span></span>      | <span data-ttu-id="cbbca-133">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="cbbca-133">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="cbbca-134">搜尋</span><span class="sxs-lookup"><span data-stu-id="cbbca-134">Search</span></span>       | <span data-ttu-id="cbbca-135">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span><span class="sxs-lookup"><span data-stu-id="cbbca-135">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span></span> |



 

<span data-ttu-id="cbbca-136">Microsoft Visual Basic 目前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="cbbca-136">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="cbbca-137">範例</span><span class="sxs-lookup"><span data-stu-id="cbbca-137">Examples</span></span>

<span data-ttu-id="cbbca-138">下列範例示範如何使用 **ShowBrowserBar** 來顯示 [我的最愛 **]** 瀏覽器列。</span><span class="sxs-lookup"><span data-stu-id="cbbca-138">The following examples show the use of **ShowBrowserBar** to display the **Favorites** browser bar.</span></span> <span data-ttu-id="cbbca-139">JScript 和 VBScript 會顯示使用方式。</span><span class="sxs-lookup"><span data-stu-id="cbbca-139">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="cbbca-140">Jscript：</span><span class="sxs-lookup"><span data-stu-id="cbbca-140">JScript:</span></span>


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



<span data-ttu-id="cbbca-141">VBScript</span><span class="sxs-lookup"><span data-stu-id="cbbca-141">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="cbbca-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="cbbca-142">Requirements</span></span>



| <span data-ttu-id="cbbca-143">需求</span><span class="sxs-lookup"><span data-stu-id="cbbca-143">Requirement</span></span> | <span data-ttu-id="cbbca-144">值</span><span class="sxs-lookup"><span data-stu-id="cbbca-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbbca-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cbbca-145">Minimum supported client</span></span><br/> | <span data-ttu-id="cbbca-146">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cbbca-146">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cbbca-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cbbca-147">Minimum supported server</span></span><br/> | <span data-ttu-id="cbbca-148">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cbbca-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="cbbca-149">標頭</span><span class="sxs-lookup"><span data-stu-id="cbbca-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbbca-150"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="cbbca-150"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="cbbca-151">Idl</span><span class="sxs-lookup"><span data-stu-id="cbbca-151">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cbbca-152"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="cbbca-152"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="cbbca-153">DLL</span><span class="sxs-lookup"><span data-stu-id="cbbca-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbbca-154"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="cbbca-154"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
