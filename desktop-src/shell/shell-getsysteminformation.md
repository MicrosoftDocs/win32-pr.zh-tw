---
description: 捕獲系統資訊。
ms.assetid: 94C10DD6-FE49-4dd4-AEED-69B73A75EDEF
title: 'GetSystemInformation 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.GetSystemInformation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 2ad7a865ba6ac5b62bc8a9b5ac105c0ef166d574
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973685"
---
# <a name="shellgetsysteminformation-method"></a><span data-ttu-id="629bb-103">GetSystemInformation 方法</span><span class="sxs-lookup"><span data-stu-id="629bb-103">Shell.GetSystemInformation method</span></span>

<span data-ttu-id="629bb-104">捕獲系統資訊。</span><span class="sxs-lookup"><span data-stu-id="629bb-104">Retrieves system information.</span></span>

## <a name="syntax"></a><span data-ttu-id="629bb-105">語法</span><span class="sxs-lookup"><span data-stu-id="629bb-105">Syntax</span></span>


```JScript
retVal = Shell.GetSystemInformation(
  sName
)
```


```VB

Shell.GetSystemInformation( _
  ByVal sName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="629bb-106">參數</span><span class="sxs-lookup"><span data-stu-id="629bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="629bb-107">*sName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="629bb-107">*sName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="629bb-108">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="629bb-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="629bb-109">**字串**，指定所要求的系統資訊。</span><span class="sxs-lookup"><span data-stu-id="629bb-109">A **String** that specifies the system information that is being requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="629bb-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="629bb-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="629bb-111">JScript</span><span class="sxs-lookup"><span data-stu-id="629bb-111">JScript</span></span>

<span data-ttu-id="629bb-112">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="629bb-112">Type: **Variant**</span></span>

<span data-ttu-id="629bb-113">傳回所要求系統資訊的值。</span><span class="sxs-lookup"><span data-stu-id="629bb-113">Returns the value of the requested system information.</span></span> <span data-ttu-id="629bb-114">傳回型別取決於所要求的系統資訊。</span><span class="sxs-lookup"><span data-stu-id="629bb-114">The return type depends on which system information is requested.</span></span> <span data-ttu-id="629bb-115">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="629bb-115">See the Remarks section for details.</span></span>

### <a name="vb"></a><span data-ttu-id="629bb-116">VB</span><span class="sxs-lookup"><span data-stu-id="629bb-116">VB</span></span>

<span data-ttu-id="629bb-117">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="629bb-117">Type: **Variant**</span></span>

<span data-ttu-id="629bb-118">傳回所要求系統資訊的值。</span><span class="sxs-lookup"><span data-stu-id="629bb-118">Returns the value of the requested system information.</span></span> <span data-ttu-id="629bb-119">傳回型別取決於所要求的系統資訊。</span><span class="sxs-lookup"><span data-stu-id="629bb-119">The return type depends on which system information is requested.</span></span> <span data-ttu-id="629bb-120">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="629bb-120">See the Remarks section for details.</span></span>

## <a name="remarks"></a><span data-ttu-id="629bb-121">備註</span><span class="sxs-lookup"><span data-stu-id="629bb-121">Remarks</span></span>

<span data-ttu-id="629bb-122">這個方法可以用來要求許多系統資訊值。</span><span class="sxs-lookup"><span data-stu-id="629bb-122">This method can be used to request many system information values.</span></span> <span data-ttu-id="629bb-123">下表提供用來要求資訊的 *sName* 值，以及傳回值的相關聯類型。</span><span class="sxs-lookup"><span data-stu-id="629bb-123">The following table gives the *sName* value that is used to request the information and the associated type of the returned value.</span></span>



<span data-ttu-id="629bb-124">*sName*</span><span class="sxs-lookup"><span data-stu-id="629bb-124">*sName*</span></span>

<span data-ttu-id="629bb-125">傳回類型</span><span class="sxs-lookup"><span data-stu-id="629bb-125">Return type</span></span>

<span data-ttu-id="629bb-126">描述</span><span class="sxs-lookup"><span data-stu-id="629bb-126">Description</span></span>

<span data-ttu-id="629bb-127">DirectoryServiceAvailable</span><span class="sxs-lookup"><span data-stu-id="629bb-127">DirectoryServiceAvailable</span></span>

<span data-ttu-id="629bb-128">**布林值**</span><span class="sxs-lookup"><span data-stu-id="629bb-128">**Boolean**</span></span>

<span data-ttu-id="629bb-129">如果目錄服務可以使用，則設定為 **true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="629bb-129">Set to **true** if the directory service is available; otherwise, **false**.</span></span>

<span data-ttu-id="629bb-130">DoubleClickTime</span><span class="sxs-lookup"><span data-stu-id="629bb-130">DoubleClickTime</span></span>

<span data-ttu-id="629bb-131">**整數**</span><span class="sxs-lookup"><span data-stu-id="629bb-131">**Integer**</span></span>

<span data-ttu-id="629bb-132">按兩下時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="629bb-132">The double-click time, in milliseconds.</span></span>

<span data-ttu-id="629bb-133">ProcessorLevel</span><span class="sxs-lookup"><span data-stu-id="629bb-133">ProcessorLevel</span></span>

<span data-ttu-id="629bb-134">**整數**</span><span class="sxs-lookup"><span data-stu-id="629bb-134">**Integer**</span></span>

<span data-ttu-id="629bb-135">**Windows Vista**（含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="629bb-135">**Windows Vista and later**.</span></span> <span data-ttu-id="629bb-136">處理器層級。</span><span class="sxs-lookup"><span data-stu-id="629bb-136">The processor level.</span></span> <span data-ttu-id="629bb-137">分別針對 x386、x486 和 Pentium 層處理器傳回3、4或5。</span><span class="sxs-lookup"><span data-stu-id="629bb-137">Returns 3, 4, or 5, for x386, x486, and Pentium-level processors, respectively.</span></span>

<span data-ttu-id="629bb-138">>processorspeed</span><span class="sxs-lookup"><span data-stu-id="629bb-138">ProcessorSpeed</span></span>

<span data-ttu-id="629bb-139">**整數**</span><span class="sxs-lookup"><span data-stu-id="629bb-139">**Integer**</span></span>

<span data-ttu-id="629bb-140">處理器速度，以 MHz (MHz) 。</span><span class="sxs-lookup"><span data-stu-id="629bb-140">The processor speed, in megahertz (MHz).</span></span>

<span data-ttu-id="629bb-141">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="629bb-141">ProcessorArchitecture</span></span>

<span data-ttu-id="629bb-142">**整數**</span><span class="sxs-lookup"><span data-stu-id="629bb-142">**Integer**</span></span>

<span data-ttu-id="629bb-143">處理器架構。</span><span class="sxs-lookup"><span data-stu-id="629bb-143">The processor architecture.</span></span> <span data-ttu-id="629bb-144">如需詳細資訊，請參閱 [**系統 \_ 資訊**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info)結構的 **wProcessorArchitecture** 成員討論。</span><span class="sxs-lookup"><span data-stu-id="629bb-144">For details, see the discussion of the **wProcessorArchitecture** member of the [**SYSTEM\_INFO**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) structure.</span></span>

<span data-ttu-id="629bb-145">PhysicalMemoryInstalled</span><span class="sxs-lookup"><span data-stu-id="629bb-145">PhysicalMemoryInstalled</span></span>

<span data-ttu-id="629bb-146">**整數**</span><span class="sxs-lookup"><span data-stu-id="629bb-146">**Integer**</span></span>

<span data-ttu-id="629bb-147">已安裝的實體記憶體數量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="629bb-147">The amount of physical memory installed, in bytes.</span></span>

<span data-ttu-id="629bb-148">以下僅適用于 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="629bb-148">The following are valid only on Windows XP.</span></span>

<span data-ttu-id="629bb-149">Iso \_ Professional</span><span class="sxs-lookup"><span data-stu-id="629bb-149">IsOS\_Professional</span></span>

<span data-ttu-id="629bb-150">**布林值**</span><span class="sxs-lookup"><span data-stu-id="629bb-150">**Boolean**</span></span>

<span data-ttu-id="629bb-151">如果作業系統是 Windows XP Professional Edition，則設定為 **true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="629bb-151">Set to **true** if the operating system is Windows XP Professional Edition; otherwise, **false**.</span></span>

<span data-ttu-id="629bb-152">Iso \_ 個人</span><span class="sxs-lookup"><span data-stu-id="629bb-152">IsOS\_Personal</span></span>

<span data-ttu-id="629bb-153">**布林值**</span><span class="sxs-lookup"><span data-stu-id="629bb-153">**Boolean**</span></span>

<span data-ttu-id="629bb-154">如果作業系統是 Windows XP Home Edition，則設定為 **true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="629bb-154">Set to **true** if the operating system is Windows XP Home Edition; otherwise, **false**.</span></span>

<span data-ttu-id="629bb-155">以下僅適用于 Windows XP 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="629bb-155">The following is valid only on Windows XP and later.</span></span>

<span data-ttu-id="629bb-156">Iso \_ DomainMember</span><span class="sxs-lookup"><span data-stu-id="629bb-156">IsOS\_DomainMember</span></span>

<span data-ttu-id="629bb-157">**布林值**</span><span class="sxs-lookup"><span data-stu-id="629bb-157">**Boolean**</span></span>

<span data-ttu-id="629bb-158">如果電腦是網域的成員，則設定為 **true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="629bb-158">Set to **true** if the computer is a member of a domain; otherwise, **false**.</span></span>



 

<span data-ttu-id="629bb-159">Microsoft Visual Basic 目前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="629bb-159">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="629bb-160">範例</span><span class="sxs-lookup"><span data-stu-id="629bb-160">Examples</span></span>

<span data-ttu-id="629bb-161">下列範例顯示 JScript 和 VBScript 的 **GetSystemInformation** 用法。</span><span class="sxs-lookup"><span data-stu-id="629bb-161">The following examples show the use of **GetSystemInformation** for JScript and VBScript.</span></span>

<span data-ttu-id="629bb-162">Jscript：</span><span class="sxs-lookup"><span data-stu-id="629bb-162">JScript:</span></span>


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



<span data-ttu-id="629bb-163">VBScript</span><span class="sxs-lookup"><span data-stu-id="629bb-163">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="629bb-164">規格需求</span><span class="sxs-lookup"><span data-stu-id="629bb-164">Requirements</span></span>



| <span data-ttu-id="629bb-165">需求</span><span class="sxs-lookup"><span data-stu-id="629bb-165">Requirement</span></span> | <span data-ttu-id="629bb-166">值</span><span class="sxs-lookup"><span data-stu-id="629bb-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="629bb-167">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="629bb-167">Minimum supported client</span></span><br/> | <span data-ttu-id="629bb-168">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="629bb-168">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="629bb-169">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="629bb-169">Minimum supported server</span></span><br/> | <span data-ttu-id="629bb-170">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="629bb-170">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="629bb-171">標頭</span><span class="sxs-lookup"><span data-stu-id="629bb-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="629bb-172"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="629bb-172"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="629bb-173">Idl</span><span class="sxs-lookup"><span data-stu-id="629bb-173">IDL</span></span><br/>                      | <dl> <span data-ttu-id="629bb-174"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="629bb-174"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="629bb-175">DLL</span><span class="sxs-lookup"><span data-stu-id="629bb-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="629bb-176"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="629bb-176"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
