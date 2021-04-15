---
title: 'IADsPropertyValue 屬性方法 (Iads .h) '
description: IADsPropertyValue 介面的屬性方法會提供下表所述屬性的存取權。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: 1039d4a9-bef8-457d-9a32-3743c14adef1
ms.tgt_platform: multiple
keywords:
- IADsPropertyValue 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsPropertyValue Property Methods
- IADsPropertyValue.ADsType
- IADsPropertyValue.get_ADsType
- IADsPropertyValue.put_ADsType
- IADsPropertyValue.DNString
- IADsPropertyValue.get_DNString
- IADsPropertyValue.put_DNString
- IADsPropertyValue.CaseExactString
- IADsPropertyValue.get_CaseExactString
- IADsPropertyValue.put_CaseExactString
- IADsPropertyValue.CaseIgnoreString
- IADsPropertyValue.get_CaseIgnoreString
- IADsPropertyValue.put_CaseIgnoreString
- IADsPropertyValue.PrintableString
- IADsPropertyValue.get_PrintableString
- IADsPropertyValue.put_PrintableString
- IADsPropertyValue.NumericString
- IADsPropertyValue.get_NumericString
- IADsPropertyValue.put_NumericString
- IADsPropertyValue.Boolean
- IADsPropertyValue.get_Boolean
- IADsPropertyValue.put_Boolean
- IADsPropertyValue.Integer
- IADsPropertyValue.get_Integer
- IADsPropertyValue.put_Integer
- IADsPropertyValue.OctetString
- IADsPropertyValue.get_OctetString
- IADsPropertyValue.put_OctetString
- IADsPropertyValue.SecurityDescriptor
- IADsPropertyValue.get_SecurityDescriptor
- IADsPropertyValue.put_SecurityDescriptor
- IADsPropertyValue.LargeInteger
- IADsPropertyValue.get_LargeInteger
- IADsPropertyValue.put_LargeInteger
- IADsPropertyValue.UTCTime
- IADsPropertyValue.get_UTCTime
- IADsPropertyValue.put_UTCTime
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 196e8097e5beaa5350738971be29de89b43c17a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465065"
---
# <a name="iadspropertyvalue-property-methods"></a><span data-ttu-id="ba049-105">IADsPropertyValue 屬性方法</span><span class="sxs-lookup"><span data-stu-id="ba049-105">IADsPropertyValue Property Methods</span></span>

<span data-ttu-id="ba049-106">[**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)介面的屬性方法會提供下表所述屬性的存取權。</span><span class="sxs-lookup"><span data-stu-id="ba049-106">The property methods of the [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) interface provide access to the properties described in the following table.</span></span> <span data-ttu-id="ba049-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="ba049-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="ba049-108">屬性</span><span class="sxs-lookup"><span data-stu-id="ba049-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="ba049-109">**ADsType**</span><span class="sxs-lookup"><span data-stu-id="ba049-109">**ADsType**</span></span>
<span data-ttu-id="ba049-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ba049-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="ba049-111">值屬性之屬性值的資料類型，取自 [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) 列舉。</span><span class="sxs-lookup"><span data-stu-id="ba049-111">The data type of the value of the property, taken from the [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) enumeration, of the value property.</span></span>

<dt>

<span data-ttu-id="ba049-112">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ba049-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ba049-113">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="ba049-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ADsType(
  [out] LONG* ADsType
);
HRESULT put_ADsType(
  [in] LONG ADsType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba049-114">**布林值**</span><span class="sxs-lookup"><span data-stu-id="ba049-114">**Boolean**</span></span>
<span data-ttu-id="ba049-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ba049-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="ba049-116">布林值。</span><span class="sxs-lookup"><span data-stu-id="ba049-116">Boolean value.</span></span>

<dt>

<span data-ttu-id="ba049-117">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ba049-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ba049-118">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="ba049-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Boolean(
  [out] LONG* lnBoolean
);
HRESULT put_Boolean(
  [in] LONG lnBoolean
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba049-119">**CaseExactString**</span><span class="sxs-lookup"><span data-stu-id="ba049-119">**CaseExactString**</span></span>
<span data-ttu-id="ba049-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ba049-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="ba049-121">要轉譯的字串。</span><span class="sxs-lookup"><span data-stu-id="ba049-121">String to be interpreted.</span></span> <span data-ttu-id="ba049-122">區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="ba049-122">Case-sensitive.</span></span>

<dt>

<span data-ttu-id="ba049-123">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ba049-123">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ba049-124">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ba049-124">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CaseExactString(
  [out] BSTR* bstrCaseExactString
);
HRESULT put_CaseExactString(
  [in] BSTR bstrCaseExactString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba049-125">**CaseIgnoreString**</span><span class="sxs-lookup"><span data-stu-id="ba049-125">**CaseIgnoreString**</span></span>
<span data-ttu-id="ba049-126"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ba049-126"></dt> <dd> <dl></span></span>

<span data-ttu-id="ba049-127">要轉譯的字串。</span><span class="sxs-lookup"><span data-stu-id="ba049-127">String to be interpreted.</span></span> <span data-ttu-id="ba049-128">不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="ba049-128">Case insensitive.</span></span>

<dt>

<span data-ttu-id="ba049-129">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ba049-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ba049-130">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ba049-130">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CaseIgnoreString(
  [out] BSTR* bstrCaseIgnoreString
);
HRESULT put_CaseIgnoreString(
  [in] BSTR bstrCaseIgnoreString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba049-131">**DNString**</span><span class="sxs-lookup"><span data-stu-id="ba049-131">**DNString**</span></span>
<span data-ttu-id="ba049-132"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ba049-132"></dt> <dd> <dl></span></span>

<span data-ttu-id="ba049-133">識別目錄服務值物件的辨別名稱 (路徑) 的字串。</span><span class="sxs-lookup"><span data-stu-id="ba049-133">String that identifies the distinguished name (path) of a directory service value object.</span></span>

<dt>

<span data-ttu-id="ba049-134">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ba049-134">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ba049-135">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ba049-135">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DNString(
  [out] BSTR* bstrDNString
);
HRESULT put_DNString(
  [in] BSTR bstrDNString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba049-136">**整數**</span><span class="sxs-lookup"><span data-stu-id="ba049-136">**Integer**</span></span>
<span data-ttu-id="ba049-137"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ba049-137"></dt> <dd> <dl></span></span>

<span data-ttu-id="ba049-138">整數值。</span><span class="sxs-lookup"><span data-stu-id="ba049-138">Integer value.</span></span>

<dt>

<span data-ttu-id="ba049-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ba049-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ba049-140">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="ba049-140">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Integer(
  [out] LONG* lnInteger
);
HRESULT put_Integer(
  [in] LONG lnInteger
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba049-141">**LargeInteger**</span><span class="sxs-lookup"><span data-stu-id="ba049-141">**LargeInteger**</span></span>
<span data-ttu-id="ba049-142"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ba049-142"></dt> <dd> <dl></span></span>

<span data-ttu-id="ba049-143">針對此值執行 [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)之物件的 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面指標。</span><span class="sxs-lookup"><span data-stu-id="ba049-143">Pointer to the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface of the object implementing [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) for this value.</span></span>

<dt>

<span data-ttu-id="ba049-144">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ba049-144">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ba049-145">腳本資料類型： **IDispatch**</span><span class="sxs-lookup"><span data-stu-id="ba049-145">Scripting data type: **IDispatch**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LargeInteger(
  [out] IDispatch** ppLargeInteger
);
HRESULT put_LargeInteger(
  [in] IDispatch* pLargeInteger
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba049-146">**NumericString**</span><span class="sxs-lookup"><span data-stu-id="ba049-146">**NumericString**</span></span>
<span data-ttu-id="ba049-147"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ba049-147"></dt> <dd> <dl></span></span>

<span data-ttu-id="ba049-148">要轉譯的文字。</span><span class="sxs-lookup"><span data-stu-id="ba049-148">Text to be interpreted.</span></span> <span data-ttu-id="ba049-149">數數值型別。</span><span class="sxs-lookup"><span data-stu-id="ba049-149">Numeric type.</span></span>

<dt>

<span data-ttu-id="ba049-150">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ba049-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ba049-151">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ba049-151">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NumericString(
  [out] BSTR* bstrNumericString
);
HRESULT put_NumericString(
  [in] BSTR bstrNumericString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba049-152">**OctetString**</span><span class="sxs-lookup"><span data-stu-id="ba049-152">**OctetString**</span></span>
<span data-ttu-id="ba049-153"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ba049-153"></dt> <dd> <dl></span></span>

<span data-ttu-id="ba049-154">單一位元組字元的 Variant 陣列。</span><span class="sxs-lookup"><span data-stu-id="ba049-154">Variant array of one-byte characters.</span></span>

<dt>

<span data-ttu-id="ba049-155">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ba049-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ba049-156">腳本資料類型： **VARIANT**</span><span class="sxs-lookup"><span data-stu-id="ba049-156">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OctetString(
  [in] VARIANT* vOctetString
);
HRESULT put_OctetString(
  [in] VARIANT* vOctetString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba049-157">**PrintableString**</span><span class="sxs-lookup"><span data-stu-id="ba049-157">**PrintableString**</span></span>
<span data-ttu-id="ba049-158"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ba049-158"></dt> <dd> <dl></span></span>

<span data-ttu-id="ba049-159">顯示或列印字串。</span><span class="sxs-lookup"><span data-stu-id="ba049-159">Display or print string.</span></span>

<dt>

<span data-ttu-id="ba049-160">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ba049-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ba049-161">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ba049-161">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrintableString(
  [out] BSTR* bstrPrintableString
);
HRESULT put_PrintableString(
  [in] BSTR bstrPrintableString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba049-162">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="ba049-162">**SecurityDescriptor**</span></span>
<span data-ttu-id="ba049-163"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ba049-163"></dt> <dd> <dl></span></span>

<span data-ttu-id="ba049-164">針對此值執行 [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)之物件的 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面指標。</span><span class="sxs-lookup"><span data-stu-id="ba049-164">Pointer to the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface of the object implementing [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) for this value.</span></span>

<dt>

<span data-ttu-id="ba049-165">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ba049-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ba049-166">腳本資料類型： **IDispatch**</span><span class="sxs-lookup"><span data-stu-id="ba049-166">Scripting data type: **IDispatch**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SecurityDescriptor(
  [out] IDispatch** ppSecurityDescriptor
);
HRESULT put_SecurityDescriptor(
  [in] IDispatch* pSecurityDescriptor
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba049-167">**UTCTime**</span><span class="sxs-lookup"><span data-stu-id="ba049-167">**UTCTime**</span></span>
<span data-ttu-id="ba049-168"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ba049-168"></dt> <dd> <dl></span></span>

<span data-ttu-id="ba049-169">以國際標準時間 (UTC) 格式表示的 **VT \_ 日期** 類型日期。</span><span class="sxs-lookup"><span data-stu-id="ba049-169">A date of the **VT\_DATE** type expressed in Coordinated Universal Time (UTC) format.</span></span>

<dt>

<span data-ttu-id="ba049-170">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ba049-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ba049-171">腳本資料類型： **日期**</span><span class="sxs-lookup"><span data-stu-id="ba049-171">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UTCTime(
  [out] DATE* daUTCTime
);
HRESULT put_UTCTime(
  [in] DATE daUTCTime
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="ba049-172">備註</span><span class="sxs-lookup"><span data-stu-id="ba049-172">Remarks</span></span>

<span data-ttu-id="ba049-173">[**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)屬性只會設定或抓取指定類型的屬性值。</span><span class="sxs-lookup"><span data-stu-id="ba049-173">The [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) properties will only set or retrieve a property value of the specified type.</span></span> <span data-ttu-id="ba049-174">例如， **ADSTYPE \_ DN \_ 字串** 類型屬性（attribute）的 **CaseIgnoreString** 屬性 **（attribute）** 將會產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="ba049-174">For example, the **CaseIgnoreString** property on an attribute of type **ADSTYPE\_DN\_STRING**, like the **distinguishedName** attribute, will result in an error.</span></span> <span data-ttu-id="ba049-175">**CaseIgnoreString** 屬性只適用于型別 **ADS \_ 案例 \_ 忽略 \_ 字串** 的屬性。</span><span class="sxs-lookup"><span data-stu-id="ba049-175">The **CaseIgnoreString** property will only work on attributes of type **ADS\_CASE\_IGNORE\_STRING**.</span></span> <span data-ttu-id="ba049-176">下表將 [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) 值對應至可用於存取該屬性類型的對應 **IADsPropertyValue** 屬性。</span><span class="sxs-lookup"><span data-stu-id="ba049-176">The following table maps the [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) value to the corresponding **IADsPropertyValue** property that can be used to access that attribute type.</span></span> <span data-ttu-id="ba049-177">如果 **ADSTYPEENUM** 值未列在此資料表中，則無法從 **IADsPropertyValue** 介面使用。</span><span class="sxs-lookup"><span data-stu-id="ba049-177">If an **ADSTYPEENUM** value is not listed in this table, it is not available from the **IADsPropertyValue** interface.</span></span> <span data-ttu-id="ba049-178">[**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)介面應該用來取得其他格式的資料。</span><span class="sxs-lookup"><span data-stu-id="ba049-178">The [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2) interface should be used to obtain data in the other formats.</span></span>



| <span data-ttu-id="ba049-179">[**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) 值</span><span class="sxs-lookup"><span data-stu-id="ba049-179">[**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) value</span></span> | <span data-ttu-id="ba049-180">[**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) 屬性</span><span class="sxs-lookup"><span data-stu-id="ba049-180">[**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) property</span></span> |
|------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="ba049-181">**ADSTYPE \_ DN \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="ba049-181">**ADSTYPE\_DN\_STRING**</span></span>                  | <span data-ttu-id="ba049-182">**DNString**</span><span class="sxs-lookup"><span data-stu-id="ba049-182">**DNString**</span></span>                                            |
| <span data-ttu-id="ba049-183">**ADSTYPE \_ CASE \_ 精確 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="ba049-183">**ADSTYPE\_CASE\_EXACT\_STRING**</span></span>         | <span data-ttu-id="ba049-184">**CaseExactString**</span><span class="sxs-lookup"><span data-stu-id="ba049-184">**CaseExactString**</span></span>                                     |
| <span data-ttu-id="ba049-185">**ADSTYPE \_ CASE \_ 忽略 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="ba049-185">**ADSTYPE\_CASE\_IGNORE\_STRING**</span></span>        | <span data-ttu-id="ba049-186">**CaseIgnoreString**</span><span class="sxs-lookup"><span data-stu-id="ba049-186">**CaseIgnoreString**</span></span>                                    |
| <span data-ttu-id="ba049-187">**ADSTYPE \_ 可列印的 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="ba049-187">**ADSTYPE\_PRINTABLE\_STRING**</span></span>           | <span data-ttu-id="ba049-188">**PrintableString**</span><span class="sxs-lookup"><span data-stu-id="ba049-188">**PrintableString**</span></span>                                     |
| <span data-ttu-id="ba049-189">**ADSTYPE \_ 數值 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="ba049-189">**ADSTYPE\_NUMERIC\_STRING**</span></span>             | <span data-ttu-id="ba049-190">**NumericString**</span><span class="sxs-lookup"><span data-stu-id="ba049-190">**NumericString**</span></span>                                       |
| <span data-ttu-id="ba049-191">**ADSTYPE \_ 布林值**</span><span class="sxs-lookup"><span data-stu-id="ba049-191">**ADSTYPE\_BOOLEAN**</span></span>                     | <span data-ttu-id="ba049-192">**布林值**</span><span class="sxs-lookup"><span data-stu-id="ba049-192">**Boolean**</span></span>                                             |
| <span data-ttu-id="ba049-193">**ADSTYPE \_ 整數**</span><span class="sxs-lookup"><span data-stu-id="ba049-193">**ADSTYPE\_INTEGER**</span></span>                     | <span data-ttu-id="ba049-194">**整數**</span><span class="sxs-lookup"><span data-stu-id="ba049-194">**Integer**</span></span>                                             |
| <span data-ttu-id="ba049-195">**ADSTYPE \_ 八位 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="ba049-195">**ADSTYPE\_OCTET\_STRING**</span></span>               | <span data-ttu-id="ba049-196">**OctetString**</span><span class="sxs-lookup"><span data-stu-id="ba049-196">**OctetString**</span></span>                                         |
| <span data-ttu-id="ba049-197">**ADSTYPE \_ UTC \_ 時間**</span><span class="sxs-lookup"><span data-stu-id="ba049-197">**ADSTYPE\_UTC\_TIME**</span></span>                   | <span data-ttu-id="ba049-198">**UTCTime**</span><span class="sxs-lookup"><span data-stu-id="ba049-198">**UTCTime**</span></span>                                             |
| <span data-ttu-id="ba049-199">**ADSTYPE \_ 大型 \_ 整數**</span><span class="sxs-lookup"><span data-stu-id="ba049-199">**ADSTYPE\_LARGE\_INTEGER**</span></span>              | <span data-ttu-id="ba049-200">**LargeInteger**</span><span class="sxs-lookup"><span data-stu-id="ba049-200">**LargeInteger**</span></span>                                        |
| <span data-ttu-id="ba049-201">**ADSTYPE \_ NT \_ 安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="ba049-201">**ADSTYPE\_NT\_SECURITY\_DESCRIPTOR**</span></span>    | <span data-ttu-id="ba049-202">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="ba049-202">**SecurityDescriptor**</span></span>                                  |



 

## <a name="examples"></a><span data-ttu-id="ba049-203">範例</span><span class="sxs-lookup"><span data-stu-id="ba049-203">Examples</span></span>

<span data-ttu-id="ba049-204">下列程式碼範例會示範如何從屬性清單中取得屬性。</span><span class="sxs-lookup"><span data-stu-id="ba049-204">The following code example shows how to retrieve a property from the property list.</span></span>


```VB
Dim propList As IADsPropertyList
Dim propEntry As IADsPropertyEntry
Dim propVal As IADsPropertyValue

On Error GoTo Cleanup
 
' Retrieve the property list.
Set propList = GetObject("LDAP://dc01/DC=Fabrikam,DC=com")
propList.GetInfo
 
' Retrieve a property entry. If you are certain of the property type,
' replace ADSTYPE_UNKNOWN with the actual property type.
Set propEntry = propList.GetPropertyItem("description", ADSTYPE_UNKNOWN)
 
' Print the property entry values.
For Each v In propEntry.Values
    Set propVal = v
    Select Case propVal.ADsType
        Case ADSTYPE_CASE_EXACT_STRING
            Debug.Print propVal.CaseExactString
        Case ADSTYPE_CASE_IGNORE_STRING
            Debug.Print propVal.CaseIgnoreString
        Case Else
            Debug.Print "Unable to handle a property of type: " & propVal.ADsType
    End Select
    
Next

Cleanup:
    If (Err.Number<>0) Then
       Debug.Print "An error has occurred. " & Err.Number
    End If
    Set propList = Nothing
    Set propEntry = Nothing
    Set propVal = Nothing
```



<span data-ttu-id="ba049-205">下列程式碼示範如何使用 **IADsPropertyValue：： get \_ CaseIgnoreString** ，從屬性清單中取出 description 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="ba049-205">The following code shows how to use **IADsPropertyValue::get\_CaseIgnoreString** to retrieve the value of the description property from a property list.</span></span>


```C++
#include <activeds.h>
#include <stdio.h>
 
IADsPropertyList *pList = NULL;
IADsPropertyEntry *pEntry = NULL;
IADsPropertyValue *pVal = NULL;
IADs *pObj = NULL;
VARIANT var, varItem;
BSTR valStr;
IEnumVARIANT *pEnum = NULL;
LONG lstart = 0;
LONG lend = 0;
LONG lADsType = ADSTYPE_UNKNOWN;
 
VariantInit(&var);
VariantInit(&varItem);
 
// Bind to the directory object.
HRESULT hr = ADsGetObject(L"LDAP://dc01/DC=Fabrikam,DC=com",
                          IID_IADsPropertyList,
                          (void**)&pList);

if(FAILED(hr)){goto Cleanup;}

// Initialize the property cache.
hr = pList->QueryInterface(IID_IADs,(void**)&pObj);
if(FAILED(hr)){goto Cleanup;}

pObj->GetInfo();
pObj->Release();
 
// Retrieve the property entry.
hr = pList->GetPropertyItem(CComBSTR("description"), ADSTYPE_CASE_IGNORE_STRING, &var);
pList->Release();
if(FAILED(hr)){goto Cleanup;}

hr = V_DISPATCH(&var)->QueryInterface(IID_IADsPropertyEntry,
                                      (void**)&pEntry);
VariantClear(&var);
if(FAILED(hr)){goto Cleanup;}
 
// Retrieve the value array of the property entry.
hr = pEntry->get_Values(&var);
if(FAILED(hr)){goto Cleanup;}

SAFEARRAY *sa = V_ARRAY( &var );
 
// Retrieve the lower and upper bound. Iterate and print the values.
hr = SafeArrayGetLBound( sa, 1, &lstart );
hr = SafeArrayGetUBound( sa, 1, &lend );
printf(" Property value(s) = ");
for ( long idx=lstart; idx < lend+1; idx++ )    {
    hr = SafeArrayGetElement( sa, &idx, &varItem );
    hr = V_DISPATCH(&varItem)->QueryInterface(IID_IADsPropertyValue,
                                              (void**)&pVal);
    if(FAILED(hr)){goto Cleanup;}

    pVal->get_ADsType(&lADsType);

    switch(lADsType)
    {
        case ADSTYPE_CASE_IGNORE_STRING:
        {
            hr = pVal->get_CaseIgnoreString(&valStr);
            break;
        }
        case ADSTYPE_CASE_EXACT_STRING:
        {
            hr = pVal->get_CaseExactString(&valStr);
            break;
        }
        default:
        {
            valStr = SysAllocString(L"Unable to handle a property of this type");
            break;
        }
    }

    if(FAILED(hr)){goto Cleanup;}
    printf(" %S ", valStr);
    SysFreeString(valStr);
    VariantClear(&varItem);
}
printf("\n");

Cleanup:
    if(pList)
        pList = NULL;

    if(pEntry)
        pEntry = NULL;

    if(pVal)
        pVal = NULL;

    if(pObj)
        pObj = NULL;

    if(pEnum)
        pEnum = NULL;

    SysFreeString(valStr);
    VariantClear(&varItem);
    VariantClear(&var);
```



## <a name="requirements"></a><span data-ttu-id="ba049-206">規格需求</span><span class="sxs-lookup"><span data-stu-id="ba049-206">Requirements</span></span>



| <span data-ttu-id="ba049-207">需求</span><span class="sxs-lookup"><span data-stu-id="ba049-207">Requirement</span></span> | <span data-ttu-id="ba049-208">值</span><span class="sxs-lookup"><span data-stu-id="ba049-208">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba049-209">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ba049-209">Minimum supported client</span></span><br/> | <span data-ttu-id="ba049-210">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ba049-210">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ba049-211">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ba049-211">Minimum supported server</span></span><br/> | <span data-ttu-id="ba049-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba049-212">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ba049-213">標頭</span><span class="sxs-lookup"><span data-stu-id="ba049-213">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba049-214"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="ba049-214"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="ba049-215">DLL</span><span class="sxs-lookup"><span data-stu-id="ba049-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba049-216"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba049-216"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="ba049-217">IID</span><span class="sxs-lookup"><span data-stu-id="ba049-217">IID</span></span><br/>                      | <span data-ttu-id="ba049-218">IID \_ IADsPropertyValue 定義為79FA9AD0-A97C-11D0-8534-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="ba049-218">IID\_IADsPropertyValue is defined as 79FA9AD0-A97C-11D0-8534-00C04FD8D503</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="ba049-219">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ba049-219">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba049-220">**IADsPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="ba049-220">**IADsPropertyValue**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)
</dt> <dt>

[<span data-ttu-id="ba049-221">**ADSTYPEENUM**</span><span class="sxs-lookup"><span data-stu-id="ba049-221">**ADSTYPEENUM**</span></span>](/windows/win32/api/iads/ne-iads-adstypeenum)
</dt> <dt>

[<span data-ttu-id="ba049-222">**IADsPropertyEntry**</span><span class="sxs-lookup"><span data-stu-id="ba049-222">**IADsPropertyEntry**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)
</dt> <dt>

[<span data-ttu-id="ba049-223">**IADsPropertyList**</span><span class="sxs-lookup"><span data-stu-id="ba049-223">**IADsPropertyList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertylist)
</dt> <dt>

[<span data-ttu-id="ba049-224">**IADsPropertyValue2**</span><span class="sxs-lookup"><span data-stu-id="ba049-224">**IADsPropertyValue2**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)
</dt> <dt>

[<span data-ttu-id="ba049-225">**IADsSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="ba049-225">**IADsSecurityDescriptor**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> <dt>

[<span data-ttu-id="ba049-226">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="ba049-226">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> </dl>

 

