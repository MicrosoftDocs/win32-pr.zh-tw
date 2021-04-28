---
description: IShellDispatch2. GetSystemInformation 方法-捕獲系統資訊。
ms.assetid: 57c066e3-080f-4ecc-b56e-877f0569e901
title: 'IShellDispatch2. GetSystemInformation 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.GetSystemInformation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a81ac091dc1905c1cbcd2c41575c907ce957e60c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117106"
---
# <a name="ishelldispatch2getsysteminformation-method"></a><span data-ttu-id="dab48-103">IShellDispatch2. GetSystemInformation 方法</span><span class="sxs-lookup"><span data-stu-id="dab48-103">IShellDispatch2.GetSystemInformation method</span></span>

<span data-ttu-id="dab48-104">捕獲系統資訊。</span><span class="sxs-lookup"><span data-stu-id="dab48-104">Retrieves system information.</span></span>

## <a name="syntax"></a><span data-ttu-id="dab48-105">語法</span><span class="sxs-lookup"><span data-stu-id="dab48-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.GetSystemInformation(
  sName
)
```


```VB

IShellDispatch2.GetSystemInformation( _
  ByVal sName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="dab48-106">參數</span><span class="sxs-lookup"><span data-stu-id="dab48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dab48-107">*sName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dab48-107">*sName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dab48-108">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="dab48-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="dab48-109">**字串**，指定所要求的系統資訊。</span><span class="sxs-lookup"><span data-stu-id="dab48-109">A **String** that specifies the system information that is being requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dab48-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="dab48-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="dab48-111">JScript</span><span class="sxs-lookup"><span data-stu-id="dab48-111">JScript</span></span>

<span data-ttu-id="dab48-112">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="dab48-112">Type: **Variant**</span></span>

<span data-ttu-id="dab48-113">傳回所要求系統資訊的值。</span><span class="sxs-lookup"><span data-stu-id="dab48-113">Returns the value of the requested system information.</span></span> <span data-ttu-id="dab48-114">傳回型別取決於所要求的系統資訊。</span><span class="sxs-lookup"><span data-stu-id="dab48-114">The return type depends on which system information is requested.</span></span> <span data-ttu-id="dab48-115">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="dab48-115">See the Remarks section for details.</span></span>

### <a name="vb"></a><span data-ttu-id="dab48-116">VB</span><span class="sxs-lookup"><span data-stu-id="dab48-116">VB</span></span>

<span data-ttu-id="dab48-117">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="dab48-117">Type: **Variant**</span></span>

<span data-ttu-id="dab48-118">傳回所要求系統資訊的值。</span><span class="sxs-lookup"><span data-stu-id="dab48-118">Returns the value of the requested system information.</span></span> <span data-ttu-id="dab48-119">傳回型別取決於所要求的系統資訊。</span><span class="sxs-lookup"><span data-stu-id="dab48-119">The return type depends on which system information is requested.</span></span> <span data-ttu-id="dab48-120">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="dab48-120">See the Remarks section for details.</span></span>

## <a name="remarks"></a><span data-ttu-id="dab48-121">備註</span><span class="sxs-lookup"><span data-stu-id="dab48-121">Remarks</span></span>

<span data-ttu-id="dab48-122">這個方法是透過 [**GetSystemInformation**](./shell-getsysteminformation.md) 方法來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="dab48-122">This method is implemented and accessed through the [**Shell.GetSystemInformation**](./shell-getsysteminformation.md) method.</span></span>

<span data-ttu-id="dab48-123">這個方法可以用來要求許多系統資訊值。</span><span class="sxs-lookup"><span data-stu-id="dab48-123">This method can be used to request many system information values.</span></span> <span data-ttu-id="dab48-124">下表提供用來要求資訊的 *sName* 值，以及傳回值的相關聯類型。</span><span class="sxs-lookup"><span data-stu-id="dab48-124">The following table gives the *sName* value that is used to request the information and the associated type of the returned value.</span></span>



<span data-ttu-id="dab48-125">*sName*</span><span class="sxs-lookup"><span data-stu-id="dab48-125">*sName*</span></span>

<span data-ttu-id="dab48-126">傳回類型</span><span class="sxs-lookup"><span data-stu-id="dab48-126">Return type</span></span>

<span data-ttu-id="dab48-127">描述</span><span class="sxs-lookup"><span data-stu-id="dab48-127">Description</span></span>

<span data-ttu-id="dab48-128">DirectoryServiceAvailable</span><span class="sxs-lookup"><span data-stu-id="dab48-128">DirectoryServiceAvailable</span></span>

<span data-ttu-id="dab48-129">**布林值**</span><span class="sxs-lookup"><span data-stu-id="dab48-129">**Boolean**</span></span>

<span data-ttu-id="dab48-130">如果目錄服務可以使用，則設定為 **true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="dab48-130">Set to **true** if the directory service is available; otherwise, **false**.</span></span>

<span data-ttu-id="dab48-131">DoubleClickTime</span><span class="sxs-lookup"><span data-stu-id="dab48-131">DoubleClickTime</span></span>

<span data-ttu-id="dab48-132">**整數**</span><span class="sxs-lookup"><span data-stu-id="dab48-132">**Integer**</span></span>

<span data-ttu-id="dab48-133">按兩下時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="dab48-133">The double-click time, in milliseconds.</span></span>

<span data-ttu-id="dab48-134">ProcessorLevel</span><span class="sxs-lookup"><span data-stu-id="dab48-134">ProcessorLevel</span></span>

<span data-ttu-id="dab48-135">**整數**</span><span class="sxs-lookup"><span data-stu-id="dab48-135">**Integer**</span></span>

<span data-ttu-id="dab48-136">**Windows Vista**（含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="dab48-136">**Windows Vista and later**.</span></span> <span data-ttu-id="dab48-137">處理器層級。</span><span class="sxs-lookup"><span data-stu-id="dab48-137">The processor level.</span></span> <span data-ttu-id="dab48-138">分別針對 x386、x486 和 Pentium 層處理器傳回3、4或5。</span><span class="sxs-lookup"><span data-stu-id="dab48-138">Returns 3, 4, or 5, for x386, x486, and Pentium-level processors, respectively.</span></span>

<span data-ttu-id="dab48-139">>processorspeed</span><span class="sxs-lookup"><span data-stu-id="dab48-139">ProcessorSpeed</span></span>

<span data-ttu-id="dab48-140">**整數**</span><span class="sxs-lookup"><span data-stu-id="dab48-140">**Integer**</span></span>

<span data-ttu-id="dab48-141">處理器速度，以 MHz (MHz) 。</span><span class="sxs-lookup"><span data-stu-id="dab48-141">The processor speed, in megahertz (MHz).</span></span>

<span data-ttu-id="dab48-142">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="dab48-142">ProcessorArchitecture</span></span>

<span data-ttu-id="dab48-143">**整數**</span><span class="sxs-lookup"><span data-stu-id="dab48-143">**Integer**</span></span>

<span data-ttu-id="dab48-144">處理器架構。</span><span class="sxs-lookup"><span data-stu-id="dab48-144">The processor architecture.</span></span> <span data-ttu-id="dab48-145">如需詳細資訊，請參閱 [**系統 \_ 資訊**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info)結構的 **wProcessorArchitecture** 成員討論。</span><span class="sxs-lookup"><span data-stu-id="dab48-145">For details, see the discussion of the **wProcessorArchitecture** member of the [**SYSTEM\_INFO**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) structure.</span></span>

<span data-ttu-id="dab48-146">PhysicalMemoryInstalled</span><span class="sxs-lookup"><span data-stu-id="dab48-146">PhysicalMemoryInstalled</span></span>

<span data-ttu-id="dab48-147">**整數**</span><span class="sxs-lookup"><span data-stu-id="dab48-147">**Integer**</span></span>

<span data-ttu-id="dab48-148">已安裝的實體記憶體數量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="dab48-148">The amount of physical memory installed, in bytes.</span></span>

<span data-ttu-id="dab48-149">以下僅適用于 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="dab48-149">The following are valid only on Windows XP.</span></span>

<span data-ttu-id="dab48-150">Iso \_ Professional</span><span class="sxs-lookup"><span data-stu-id="dab48-150">IsOS\_Professional</span></span>

<span data-ttu-id="dab48-151">**布林值**</span><span class="sxs-lookup"><span data-stu-id="dab48-151">**Boolean**</span></span>

<span data-ttu-id="dab48-152">如果作業系統是 Windows XP Professional Edition，則設定為 **true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="dab48-152">Set to **true** if the operating system is Windows XP Professional Edition; otherwise, **false**.</span></span>

<span data-ttu-id="dab48-153">Iso \_ 個人</span><span class="sxs-lookup"><span data-stu-id="dab48-153">IsOS\_Personal</span></span>

<span data-ttu-id="dab48-154">**布林值**</span><span class="sxs-lookup"><span data-stu-id="dab48-154">**Boolean**</span></span>

<span data-ttu-id="dab48-155">如果作業系統是 Windows XP Home Edition，則設定為 **true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="dab48-155">Set to **true** if the operating system is Windows XP Home Edition; otherwise, **false**.</span></span>

<span data-ttu-id="dab48-156">以下僅適用于 Windows XP 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="dab48-156">The following is valid only on Windows XP and later.</span></span>

<span data-ttu-id="dab48-157">Iso \_ DomainMember</span><span class="sxs-lookup"><span data-stu-id="dab48-157">IsOS\_DomainMember</span></span>

<span data-ttu-id="dab48-158">**布林值**</span><span class="sxs-lookup"><span data-stu-id="dab48-158">**Boolean**</span></span>

<span data-ttu-id="dab48-159">如果電腦是網域的成員，則設定為 **true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="dab48-159">Set to **true** if the computer is a member of a domain; otherwise, **false**.</span></span>



 

<span data-ttu-id="dab48-160">Microsoft Visual Basic 目前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="dab48-160">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="dab48-161">範例</span><span class="sxs-lookup"><span data-stu-id="dab48-161">Examples</span></span>

<span data-ttu-id="dab48-162">下列範例顯示 JScript 和 VBScript 的 **GetSystemInformation** 用法。</span><span class="sxs-lookup"><span data-stu-id="dab48-162">The following examples show the use of **GetSystemInformation** for JScript and VBScript.</span></span>

<span data-ttu-id="dab48-163">Jscript：</span><span class="sxs-lookup"><span data-stu-id="dab48-163">JScript:</span></span>


```JScript
<script language="JavaScript">
    function fnGetSystemInformationJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;

        vReturn = objShell.GetSystemInformation("ProcessorLevel");
        document.write(vReturn);
    }
</script>
```



<span data-ttu-id="dab48-164">VBScript</span><span class="sxs-lookup"><span data-stu-id="dab48-164">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnGetSystemInformationVB()
        dim objShell
        dim vReturn

        set objShell = CreateObject("shell.application")

        vReturn = objShell.GetSystemInformation("ProcessorLevel")
        document.write(vReturn)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="dab48-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="dab48-165">Requirements</span></span>



| <span data-ttu-id="dab48-166">需求</span><span class="sxs-lookup"><span data-stu-id="dab48-166">Requirement</span></span> | <span data-ttu-id="dab48-167">值</span><span class="sxs-lookup"><span data-stu-id="dab48-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dab48-168">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dab48-168">Minimum supported client</span></span><br/> | <span data-ttu-id="dab48-169">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dab48-169">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dab48-170">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dab48-170">Minimum supported server</span></span><br/> | <span data-ttu-id="dab48-171">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dab48-171">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="dab48-172">標頭</span><span class="sxs-lookup"><span data-stu-id="dab48-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="dab48-173"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="dab48-173"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="dab48-174">Idl</span><span class="sxs-lookup"><span data-stu-id="dab48-174">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dab48-175"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="dab48-175"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="dab48-176">DLL</span><span class="sxs-lookup"><span data-stu-id="dab48-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dab48-177"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="dab48-177"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
