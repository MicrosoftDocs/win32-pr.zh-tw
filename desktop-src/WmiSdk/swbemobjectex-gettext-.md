---
description: 傳回物件或實例的 XML 表示。 文字檔會以指定的 XML 格式格式化，如 WbemObjectTextFormatEnum 中所示。
ms.assetid: 98961d94-8360-4ed7-b1b1-20b4fca45d45
ms.tgt_platform: multiple
title: 'SWbemObjectEx.GetText_ 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.GetText_
- ISWbemObjectEx.GetText_
- ISWbemObjectEx.GetText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6f174397b1ace85acd90ffe3def6b8122bf8d7f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027435"
---
# <a name="swbemobjectexgettext_-method"></a><span data-ttu-id="943ee-104">SWbemObjectEx. GetText \_ 方法</span><span class="sxs-lookup"><span data-stu-id="943ee-104">SWbemObjectEx.GetText\_ method</span></span>

<span data-ttu-id="943ee-105">[**SWbemObjectEx**](swbemobjectex.md)物件的 **GetText \_** 方法會傳回物件或實例的 XML 標記法。</span><span class="sxs-lookup"><span data-stu-id="943ee-105">The **GetText\_** method of the [**SWbemObjectEx**](swbemobjectex.md) object returns an XML representation of an object or instance.</span></span> <span data-ttu-id="943ee-106">文字檔會以指定的 XML 格式格式化，如 [**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)中所示。</span><span class="sxs-lookup"><span data-stu-id="943ee-106">The text file is formatted in the XML format specified as shown in [**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum).</span></span>

<span data-ttu-id="943ee-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="943ee-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="943ee-108">語法</span><span class="sxs-lookup"><span data-stu-id="943ee-108">Syntax</span></span>


```VB
strObj = .GetText_( _
  ByVal iTextFormat, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="943ee-109">參數</span><span class="sxs-lookup"><span data-stu-id="943ee-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="943ee-110">*iTextFormat* \[在\]</span><span class="sxs-lookup"><span data-stu-id="943ee-110">*iTextFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="943ee-111">必要。</span><span class="sxs-lookup"><span data-stu-id="943ee-111">Required.</span></span> <span data-ttu-id="943ee-112">[**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)中的值，指定產生的 XML 格式。</span><span class="sxs-lookup"><span data-stu-id="943ee-112">A value from [**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum) that specifies the resulting XML format.</span></span>

</dd> <dt>

<span data-ttu-id="943ee-113">*iFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="943ee-113">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="943ee-114">保留的作業旗標。</span><span class="sxs-lookup"><span data-stu-id="943ee-114">Reserved operation flags.</span></span> <span data-ttu-id="943ee-115">預設值是 0 (零)。</span><span class="sxs-lookup"><span data-stu-id="943ee-115">The default value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="943ee-116">*objWbemNamedValueSet* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="943ee-116">*objWbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="943ee-117">[**SWbemNamedValueSet**](swbemnamedvalueset.md)物件，它會設定作業的內容。</span><span class="sxs-lookup"><span data-stu-id="943ee-117">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that sets context for the operation.</span></span> <span data-ttu-id="943ee-118">預設值是 null。</span><span class="sxs-lookup"><span data-stu-id="943ee-118">The default is null.</span></span> <span data-ttu-id="943ee-119">如需所允許之名稱/值組的詳細資訊，請參閱下面的備註。</span><span class="sxs-lookup"><span data-stu-id="943ee-119">For more information about the name/value pairs permitted, see Remarks below.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="943ee-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="943ee-120">Return value</span></span>

<span data-ttu-id="943ee-121">這個方法沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="943ee-121">This method has no return values.</span></span>

## <a name="error-codes"></a><span data-ttu-id="943ee-122">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="943ee-122">Error codes</span></span>

<span data-ttu-id="943ee-123">完成 **GetText \_** 方法之後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="943ee-123">After completion of the **GetText\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="943ee-124">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="943ee-124">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="943ee-125">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="943ee-125">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="943ee-126">**wbemErrNotFound** -2147749890 (0x80041002) </span><span class="sxs-lookup"><span data-stu-id="943ee-126">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="943ee-127">找不到要求的格式。</span><span class="sxs-lookup"><span data-stu-id="943ee-127">The requested format was not found.</span></span>

</dd> <dt>

<span data-ttu-id="943ee-128">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="943ee-128">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="943ee-129">呼叫的其中一個參數不正確。</span><span class="sxs-lookup"><span data-stu-id="943ee-129">One of the parameters to the call is not correct.</span></span>

</dd> <dt>

<span data-ttu-id="943ee-130">**wbemErrCriticalError** -2147749898 (0x8004100A) </span><span class="sxs-lookup"><span data-stu-id="943ee-130">**wbemErrCriticalError** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="943ee-131">發生內部嚴重意外錯誤。</span><span class="sxs-lookup"><span data-stu-id="943ee-131">An internal, critical, and unexpected error occurred.</span></span> <span data-ttu-id="943ee-132">請向 Microsoft 技術支援反映這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="943ee-132">Report this error to Microsoft Technical Support.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="943ee-133">備註</span><span class="sxs-lookup"><span data-stu-id="943ee-133">Remarks</span></span>

<span data-ttu-id="943ee-134">當您建立 [**SWbemNamedValueSet**](swbemnamedvalueset.md)時，只允許下列名稱/值配對。</span><span class="sxs-lookup"><span data-stu-id="943ee-134">When constructing your [**SWbemNamedValueSet**](swbemnamedvalueset.md), only the following name/value pairs are permitted.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="943ee-135">Name</span><span class="sxs-lookup"><span data-stu-id="943ee-135">Name</span></span></th>
<th><span data-ttu-id="943ee-136">值</span><span class="sxs-lookup"><span data-stu-id="943ee-136">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="943ee-137">LocalOnly</span><span class="sxs-lookup"><span data-stu-id="943ee-137">LocalOnly</span></span></td>
<td><span data-ttu-id="943ee-138"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="943ee-138"><strong>VT_BOOL</strong></span></span><br/> <span data-ttu-id="943ee-139">若 <strong>為 TRUE</strong>，則產生的 XML 中只會出現本機定義的屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="943ee-139">If <strong>TRUE</strong>, only locally defined properties and methods are present in the resulting XML.</span></span> <span data-ttu-id="943ee-140">預設值為 <strong>FALSE</strong>。</span><span class="sxs-lookup"><span data-stu-id="943ee-140">The default is <strong>FALSE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="943ee-141">IncludeQualifiers</span><span class="sxs-lookup"><span data-stu-id="943ee-141">IncludeQualifiers</span></span></td>
<td><span data-ttu-id="943ee-142"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="943ee-142"><strong>VT_BOOL</strong></span></span><br/> <span data-ttu-id="943ee-143">若 <strong>為 TRUE</strong>，則會在產生的 XML 中包含類別、實例、屬性和方法的限定詞。</span><span class="sxs-lookup"><span data-stu-id="943ee-143">If <strong>TRUE</strong>, qualifiers of classes, instances, properties, and methods are included in the resulting XML.</span></span> <span data-ttu-id="943ee-144">預設值為 <strong>FALSE</strong>。</span><span class="sxs-lookup"><span data-stu-id="943ee-144">The default is <strong>FALSE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="943ee-145">PathLevel</span><span class="sxs-lookup"><span data-stu-id="943ee-145">PathLevel</span></span></td>
<td><span data-ttu-id="943ee-146"><strong>VT-I4</strong></span><span class="sxs-lookup"><span data-stu-id="943ee-146"><strong>VT-I4</strong></span></span><br/> <span data-ttu-id="943ee-147">預設值為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="943ee-147">Default is 0 (zero).</span></span> <span data-ttu-id="943ee-148">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="943ee-148">Possible values are:</span></span><br/>
<ul>
<li><span data-ttu-id="943ee-149">0： <CLASS> <INSTANCE> 根據物件是否為類別或實例，建立或專案。</span><span class="sxs-lookup"><span data-stu-id="943ee-149">0: A <CLASS> or <INSTANCE> element is created depending on whether the object is a class or instance.</span></span></li>
<li><span data-ttu-id="943ee-150">1： <VALUE.NAMEDOBJECT> 產生元素。</span><span class="sxs-lookup"><span data-stu-id="943ee-150">1: A <VALUE.NAMEDOBJECT> element is generated.</span></span></li>
<li><span data-ttu-id="943ee-151">2： <VALUE.OBJECTWITHLOCALPATH> 產生元素。</span><span class="sxs-lookup"><span data-stu-id="943ee-151">2: A <VALUE.OBJECTWITHLOCALPATH> element is generated.</span></span></li>
<li><span data-ttu-id="943ee-152">3： <VALUE.OBJECTWITHPATH> 產生元素。</span><span class="sxs-lookup"><span data-stu-id="943ee-152">3: A <VALUE.OBJECTWITHPATH> element is generated.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="943ee-153">ExcludeSystemProperties</span><span class="sxs-lookup"><span data-stu-id="943ee-153">ExcludeSystemProperties</span></span></td>
<td><span data-ttu-id="943ee-154"><strong>VT-BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="943ee-154"><strong>VT-BOOL</strong></span></span><br/> <span data-ttu-id="943ee-155">若 <strong>為 TRUE</strong>，系統屬性（例如 __NAMESPACE）會從輸出中排除。</span><span class="sxs-lookup"><span data-stu-id="943ee-155">If <strong>TRUE</strong>, system properties, like __NAMESPACE, are excluded from the output.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="943ee-156">IncludeClassOrigin</span><span class="sxs-lookup"><span data-stu-id="943ee-156">IncludeClassOrigin</span></span></td>
<td><span data-ttu-id="943ee-157"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="943ee-157"><strong>VT_BOOL</strong></span></span><br/> <span data-ttu-id="943ee-158">若 <strong>為 TRUE</strong>，則會在和元素上設定類別來源屬性 <PROPERTY> <METHOD> 。</span><span class="sxs-lookup"><span data-stu-id="943ee-158">If <strong>TRUE</strong>, the class origin attribute is set on the <PROPERTY> and <METHOD> elements.</span></span> <span data-ttu-id="943ee-159">預設值為 <strong>FALSE</strong>。</span><span class="sxs-lookup"><span data-stu-id="943ee-159">The default is <strong>FALSE</strong>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="943ee-160">如需建立 [**SWbemNamedValueSet**](swbemnamedvalueset.md)的詳細資訊，請參閱 [**SWbemNamedValueSet。**](swbemnamedvalueset-add.md)</span><span class="sxs-lookup"><span data-stu-id="943ee-160">For more information about creating an [**SWbemNamedValueSet**](swbemnamedvalueset.md), see [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md).</span></span>

## <a name="examples"></a><span data-ttu-id="943ee-161">範例</span><span class="sxs-lookup"><span data-stu-id="943ee-161">Examples</span></span>

<span data-ttu-id="943ee-162">下列腳本顯示如何取得 [**Win32 \_ Bios**](/windows/desktop/CIMWin32Prov/win32-bios) 類別定義的 XML 標記法。</span><span class="sxs-lookup"><span data-stu-id="943ee-162">The following script shows how to obtain an XML representation of the [**Win32\_Bios**](/windows/desktop/CIMWin32Prov/win32-bios) class definition.</span></span> <span data-ttu-id="943ee-163">您可以藉由指定特定的 **Win32 \_ Bios** 實例，以 XML 取得該物件的資料。</span><span class="sxs-lookup"><span data-stu-id="943ee-163">By specifying a particular instance of **Win32\_Bios**, you can obtain that object's data in XML.</span></span>


```VB
' Connect to the default namespace (root\cimv2) with the default
' impersonation level ("impersonate") and obtain a Win32_Bios class
' object.
Set obj = GetObject("winmgmts:win32_bios")

' Use the value for the desired XML CIM DTD format. 
XMLDtd = 1
Text = obj.GetText_(XMLDtd)
wscript.echo Text
```



## <a name="requirements"></a><span data-ttu-id="943ee-164">規格需求</span><span class="sxs-lookup"><span data-stu-id="943ee-164">Requirements</span></span>



| <span data-ttu-id="943ee-165">需求</span><span class="sxs-lookup"><span data-stu-id="943ee-165">Requirement</span></span> | <span data-ttu-id="943ee-166">值</span><span class="sxs-lookup"><span data-stu-id="943ee-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="943ee-167">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="943ee-167">Minimum supported client</span></span><br/> | <span data-ttu-id="943ee-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="943ee-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="943ee-169">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="943ee-169">Minimum supported server</span></span><br/> | <span data-ttu-id="943ee-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="943ee-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="943ee-171">標頭</span><span class="sxs-lookup"><span data-stu-id="943ee-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="943ee-172"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="943ee-172"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="943ee-173">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="943ee-173">Type library</span></span><br/>             | <dl> <span data-ttu-id="943ee-174"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="943ee-174"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="943ee-175">DLL</span><span class="sxs-lookup"><span data-stu-id="943ee-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="943ee-176"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="943ee-176"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="943ee-177">CLSID</span><span class="sxs-lookup"><span data-stu-id="943ee-177">CLSID</span></span><br/>                    | <span data-ttu-id="943ee-178">CLSID \_ SWbemObjectEx</span><span class="sxs-lookup"><span data-stu-id="943ee-178">CLSID\_SWbemObjectEx</span></span><br/>                                                         |
| <span data-ttu-id="943ee-179">IID</span><span class="sxs-lookup"><span data-stu-id="943ee-179">IID</span></span><br/>                      | <span data-ttu-id="943ee-180">IID \_ ISWbemObjectEx</span><span class="sxs-lookup"><span data-stu-id="943ee-180">IID\_ISWbemObjectEx</span></span><br/>                                                          |



 

