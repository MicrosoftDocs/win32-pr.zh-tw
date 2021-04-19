---
description: '\_SWbemLastError 物件的 CompareTo 方法會比較兩個 SWbemObject 物件。 根據 iFlags 參數中指定的值，這項比較會受限於某些條件約束。'
ms.assetid: 541510e4-ef8d-4436-966f-19c5df422281
ms.tgt_platform: multiple
title: 'SWbemLastError.CompareTo_ 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.CompareTo_
- ISWbemLastError.CompareTo_
- ISWbemLastError.CompareTo_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4c24eb6e57e81c6c44922b2d6643be65198951ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978877"
---
# <a name="swbemlasterrorcompareto_-method"></a><span data-ttu-id="bba69-104">SWbemLastError. CompareTo \_ 方法</span><span class="sxs-lookup"><span data-stu-id="bba69-104">SWbemLastError.CompareTo\_ method</span></span>

<span data-ttu-id="bba69-105">[**SWbemLastError**](swbemlasterror.md)物件的 **CompareTo \_** 方法會比較兩個 [**SWbemObject**](swbemobject.md)物件。</span><span class="sxs-lookup"><span data-stu-id="bba69-105">The **CompareTo\_** method of the [**SWbemLastError**](swbemlasterror.md) object compares two [**SWbemObject**](swbemobject.md) objects.</span></span> <span data-ttu-id="bba69-106">根據 *iFlags* 參數中指定的值，這項比較會受限於某些條件約束。</span><span class="sxs-lookup"><span data-stu-id="bba69-106">This comparison is subject to certain constraints based on the values specified in the *iFlags* parameter.</span></span>

<span data-ttu-id="bba69-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="bba69-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bba69-108">語法</span><span class="sxs-lookup"><span data-stu-id="bba69-108">Syntax</span></span>


```VB
bAreEqual = .CompareTo_( _
  ByVal objwbemObject, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="bba69-109">參數</span><span class="sxs-lookup"><span data-stu-id="bba69-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bba69-110">*objwbemObject* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bba69-110">*objwbemObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bba69-111">必要。</span><span class="sxs-lookup"><span data-stu-id="bba69-111">Required.</span></span> <span data-ttu-id="bba69-112">[**SWbemObject**](swbemobject.md)類別物件。</span><span class="sxs-lookup"><span data-stu-id="bba69-112">An [**SWbemObject**](swbemobject.md) class object.</span></span> <span data-ttu-id="bba69-113">這個參數是用來比較第一個物件的物件。</span><span class="sxs-lookup"><span data-stu-id="bba69-113">This parameter is the object with which the first object is compared.</span></span> <span data-ttu-id="bba69-114">物件必須是有效的 **SWbemObject** 實例。</span><span class="sxs-lookup"><span data-stu-id="bba69-114">The object must be a valid **SWbemObject** instance.</span></span>

</dd> <dt>

<span data-ttu-id="bba69-115">*iFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="bba69-115">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bba69-116">指定運算其他旗標的整數。</span><span class="sxs-lookup"><span data-stu-id="bba69-116">An integer that specifies additional flags to the operation.</span></span> <span data-ttu-id="bba69-117">此參數會指定進行物件比較時要考慮的物件特性。</span><span class="sxs-lookup"><span data-stu-id="bba69-117">This parameter specifies the object characteristics to consider when object comparisons are made.</span></span> <span data-ttu-id="bba69-118">您可以使用 **wbemComparisonFlagIncludeAll** 將所有功能視為 (預設) 或下列值的任何組合。</span><span class="sxs-lookup"><span data-stu-id="bba69-118">You can use **wbemComparisonFlagIncludeAll** to consider all features (default) or any combination of the following values.</span></span>

<dt>

<span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>

<span data-ttu-id="bba69-119"><span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>wbemComparisonFlagIncludeAll \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="bba69-119"><span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>\*\*\*\*wbemComparisonFlagIncludeAll\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="bba69-120">造成所有屬性、限定詞和類別的比較。</span><span class="sxs-lookup"><span data-stu-id="bba69-120">Causes all properties, qualifiers, and flavors to be compared.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>

<span data-ttu-id="bba69-121"><span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>wbemComparisonFlagIgnoreQualifiers \* \* \* (1 (0x1) ) </span><span class="sxs-lookup"><span data-stu-id="bba69-121"><span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>\*\*\*\*wbemComparisonFlagIgnoreQualifiers\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="bba69-122">使所有限定詞 (包括索引 **鍵** 和 **動態**) ，以進行比較。</span><span class="sxs-lookup"><span data-stu-id="bba69-122">Causes all qualifiers (including **Key** and **Dynamic**) to be ignored in comparison.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>

<span data-ttu-id="bba69-123"><span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>wbemComparisonFlagIgnoreObjectSource \* \* \* (2 (0x2) ) </span><span class="sxs-lookup"><span data-stu-id="bba69-123"><span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>\*\*\*\*wbemComparisonFlagIgnoreObjectSource\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="bba69-124">使物件的來源（也就是伺服器及其來源的命名空間）與其他物件相比較，將會被忽略。</span><span class="sxs-lookup"><span data-stu-id="bba69-124">Causes the source of the objects, namely the server and the namespace they came from, to be ignored in comparison to other objects.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>

<span data-ttu-id="bba69-125"><span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>wbemComparisonFlagIgnoreDefaultValues \* \* \* (4 (0x4) ) </span><span class="sxs-lookup"><span data-stu-id="bba69-125"><span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>\*\*\*\*wbemComparisonFlagIgnoreDefaultValues\*\*\*\* (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="bba69-126">導致忽略屬性的預設值。</span><span class="sxs-lookup"><span data-stu-id="bba69-126">Causes the default values of properties to be ignored.</span></span> <span data-ttu-id="bba69-127">只有在比較類別時，此旗標才有意義。</span><span class="sxs-lookup"><span data-stu-id="bba69-127">This flag is only meaningful when comparing classes.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>

<span data-ttu-id="bba69-128"><span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>wbemComparisonFlagIgnoreClass \* \* \* (8 (0x8) ) </span><span class="sxs-lookup"><span data-stu-id="bba69-128"><span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>\*\*\*\*wbemComparisonFlagIgnoreClass\*\*\*\* (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="bba69-129">指示系統假設要比較的物件是相同類別的實例。</span><span class="sxs-lookup"><span data-stu-id="bba69-129">Instructs the system to assume that the objects being compared are instances of the same class.</span></span> <span data-ttu-id="bba69-130">因此，此旗標只會比較實例相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bba69-130">Consequently, this flag compares instance-related information only.</span></span> <span data-ttu-id="bba69-131">使用這個旗標，將效能最佳化。</span><span class="sxs-lookup"><span data-stu-id="bba69-131">Use this flag to optimize performance.</span></span> <span data-ttu-id="bba69-132">如果物件不屬於相同類別，則結果不會定義。</span><span class="sxs-lookup"><span data-stu-id="bba69-132">If the objects are not of the same class, the results are undefined.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>

<span data-ttu-id="bba69-133"><span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>wbemComparisonFlagIgnoreCase \* \* \* (16 (0x10) ) </span><span class="sxs-lookup"><span data-stu-id="bba69-133"><span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>\*\*\*\*wbemComparisonFlagIgnoreCase\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="bba69-134">使字串值以不區分大小寫的方式進行比較。</span><span class="sxs-lookup"><span data-stu-id="bba69-134">Causes string values to be compared in a case-insensitive manner.</span></span> <span data-ttu-id="bba69-135">這同時適用于字串和限定詞值。</span><span class="sxs-lookup"><span data-stu-id="bba69-135">This applies both to strings and to qualifier values.</span></span> <span data-ttu-id="bba69-136">不論這個旗標是否指定，屬性和限定詞名稱都是以區分大小寫的方式比較。</span><span class="sxs-lookup"><span data-stu-id="bba69-136">Property and qualifier names are always compared in a case-insensitive manner whether this flag is specified or not.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>

<span data-ttu-id="bba69-137"><span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>wbemComparisonFlagIgnoreFlavor \* \* \* (32 (0x20) ) </span><span class="sxs-lookup"><span data-stu-id="bba69-137"><span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>\*\*\*\*wbemComparisonFlagIgnoreFlavor\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="bba69-138">會忽略辨識符號的類別。</span><span class="sxs-lookup"><span data-stu-id="bba69-138">Causes qualifier flavors to be ignored.</span></span> <span data-ttu-id="bba69-139">這個旗標仍然會考慮限定詞值，但是會忽略類型差異，例如傳用原則和覆寫限制。</span><span class="sxs-lookup"><span data-stu-id="bba69-139">This flag still takes qualifier values into account, but ignores flavor distinctions such as propagation rules and override restrictions.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bba69-140">傳回值</span><span class="sxs-lookup"><span data-stu-id="bba69-140">Return value</span></span>

<span data-ttu-id="bba69-141">如果物件相符， **\_ CompareTo** 方法會傳回布林值 **TRUE** ; 否則會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="bba69-141">The **CompareTo\_** method returns the Boolean value **TRUE** if the objects match; otherwise, it returns **FALSE**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bba69-142">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="bba69-142">Error codes</span></span>

<span data-ttu-id="bba69-143">**CompareTo \_** 方法完成後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="bba69-143">Upon the completion of the **CompareTo\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="bba69-144">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="bba69-144">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="bba69-145">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="bba69-145">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="bba69-146">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="bba69-146">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="bba69-147">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="bba69-147">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="bba69-148">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="bba69-148">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="bba69-149">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="bba69-149">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bba69-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="bba69-150">Requirements</span></span>



| <span data-ttu-id="bba69-151">需求</span><span class="sxs-lookup"><span data-stu-id="bba69-151">Requirement</span></span> | <span data-ttu-id="bba69-152">值</span><span class="sxs-lookup"><span data-stu-id="bba69-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bba69-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bba69-153">Minimum supported client</span></span><br/> | <span data-ttu-id="bba69-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bba69-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bba69-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bba69-155">Minimum supported server</span></span><br/> | <span data-ttu-id="bba69-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bba69-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bba69-157">標頭</span><span class="sxs-lookup"><span data-stu-id="bba69-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="bba69-158"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="bba69-158"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bba69-159">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="bba69-159">Type library</span></span><br/>             | <dl> <span data-ttu-id="bba69-160"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bba69-160"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bba69-161">DLL</span><span class="sxs-lookup"><span data-stu-id="bba69-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bba69-162"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bba69-162"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bba69-163">CLSID</span><span class="sxs-lookup"><span data-stu-id="bba69-163">CLSID</span></span><br/>                    | <span data-ttu-id="bba69-164">CLSID \_ SWbemLastError</span><span class="sxs-lookup"><span data-stu-id="bba69-164">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="bba69-165">IID</span><span class="sxs-lookup"><span data-stu-id="bba69-165">IID</span></span><br/>                      | <span data-ttu-id="bba69-166">IID \_ ISWbemLastError</span><span class="sxs-lookup"><span data-stu-id="bba69-166">IID\_ISWbemLastError</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="bba69-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bba69-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bba69-168">**SWbemLastError**</span><span class="sxs-lookup"><span data-stu-id="bba69-168">**SWbemLastError**</span></span>](swbemlasterror.md)
</dt> <dt>

[<span data-ttu-id="bba69-169">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="bba69-169">**SWbemObject**</span></span>](swbemobject.md)
</dt> </dl>

 

 




