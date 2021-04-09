---
title: 如何指定比較值
description: 每個屬性類型都有一個語法，可決定您可以在該屬性的搜尋篩選中指定的比較數值型別。
ms.assetid: 72bd58e4-e1c3-40a5-9917-4910f40c52c5
ms.tgt_platform: multiple
keywords:
- 如何指定比較值 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95f9355bc4853fa6dc62645e1c241d8e26f731f9
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681655"
---
# <a name="how-to-specify-comparison-values"></a><span data-ttu-id="d0e72-104">如何指定比較值</span><span class="sxs-lookup"><span data-stu-id="d0e72-104">How to Specify Comparison Values</span></span>

<span data-ttu-id="d0e72-105">每個屬性類型都有一個語法，可決定您可以在該屬性的搜尋篩選中指定的比較數值型別。</span><span class="sxs-lookup"><span data-stu-id="d0e72-105">Each attribute type has a syntax that determines the type of comparison values that you can specify in a search filter for that attribute.</span></span>

<span data-ttu-id="d0e72-106">下列各節說明每個屬性語法的需求。</span><span class="sxs-lookup"><span data-stu-id="d0e72-106">The following sections describe requirements for each attribute syntax.</span></span> <span data-ttu-id="d0e72-107">如需屬性語法的詳細資訊，請參閱 [Active Directory Domain Services 中的屬性語法](syntaxes-for-attributes-in-active-directory-domain-services.md)。</span><span class="sxs-lookup"><span data-stu-id="d0e72-107">For more information about attribute syntaxes, see [Syntaxes for Attributes in Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).</span></span>

<dl> <dt>

<span data-ttu-id="d0e72-108"><span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>布林</span><span class="sxs-lookup"><span data-stu-id="d0e72-108"><span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>Boolean</span></span>
</dt> <dd>

<span data-ttu-id="d0e72-109">篩選準則中指定的值必須是 "TRUE" 或 "FALSE" 的字串值。</span><span class="sxs-lookup"><span data-stu-id="d0e72-109">The value specified in a filter must be a string value that is either "TRUE" or "FALSE".</span></span> <span data-ttu-id="d0e72-110">下列範例示範如何指定布林值比較字串。</span><span class="sxs-lookup"><span data-stu-id="d0e72-110">The following examples show how to specify a Boolean comparison string.</span></span>

<span data-ttu-id="d0e72-111">下列範例會搜尋將 **showInAdvancedViewOnly** 設為 **TRUE** 的物件：</span><span class="sxs-lookup"><span data-stu-id="d0e72-111">The following example will search for objects that have a **showInAdvancedViewOnly** set to **TRUE**:</span></span>


```C++
(showInAdvancedViewOnly=TRUE)
```



<span data-ttu-id="d0e72-112">下列範例會搜尋將 **showInAdvancedViewOnly** 設為 **FALSE** 的物件：</span><span class="sxs-lookup"><span data-stu-id="d0e72-112">The following example will search for objects that have a **showInAdvancedViewOnly** set to **FALSE**:</span></span>


```C++
(showInAdvancedViewOnly=FALSE)
```



</dd> <dt>

<span data-ttu-id="d0e72-113"><span id="Integer_and_Enumeration"></span><span id="integer_and_enumeration"></span><span id="INTEGER_AND_ENUMERATION"></span>整數和列舉</span><span class="sxs-lookup"><span data-stu-id="d0e72-113"><span id="Integer_and_Enumeration"></span><span id="integer_and_enumeration"></span><span id="INTEGER_AND_ENUMERATION"></span>Integer and Enumeration</span></span>
</dt> <dd>

<span data-ttu-id="d0e72-114">篩選準則中指定的值必須是十進位整數。</span><span class="sxs-lookup"><span data-stu-id="d0e72-114">The value specified in a filter must be a decimal Integer.</span></span> <span data-ttu-id="d0e72-115">十六進位值必須轉換成 decimal。</span><span class="sxs-lookup"><span data-stu-id="d0e72-115">Hexadecimal values must be converted to decimal.</span></span> <span data-ttu-id="d0e72-116">值比較字串採用下列格式：</span><span class="sxs-lookup"><span data-stu-id="d0e72-116">A value comparison string takes the following form:</span></span>


```C++
<attribute name>:<value>
```



<span data-ttu-id="d0e72-117">" <attribute name> " 是屬性的 **lDAPDisplayName** 和 "</span><span class="sxs-lookup"><span data-stu-id="d0e72-117">"<attribute name>" is the **lDAPDisplayName** of the attribute and "</span></span><value><span data-ttu-id="d0e72-118">"是要用於比較的值。</span><span class="sxs-lookup"><span data-stu-id="d0e72-118">" is the value to use for comparison.</span></span>

<span data-ttu-id="d0e72-119">下列程式碼範例示範的篩選準則會搜尋其 **groupType** 值等於 **ADS \_ 群組 \_ 類型 \_ 通用 \_ 群組** (8) 旗標和 **ads \_ 群組 \_ 類型 \_ 安全性 \_** (0x80000000) 旗標的物件。</span><span class="sxs-lookup"><span data-stu-id="d0e72-119">The following code example shows a filter that will search for objects that have a **groupType** value that is equal to the **ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP** (8) flag and the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** (0x80000000) flag.</span></span> <span data-ttu-id="d0e72-120">這兩個旗標會組合相等的0x80000008 （轉換為 decimal）為2147483656。</span><span class="sxs-lookup"><span data-stu-id="d0e72-120">The two flags combined equal 0x80000008, which converted to decimal is 2147483656.</span></span>


```C++
(groupType=2147483656)
```



<span data-ttu-id="d0e72-121">LDAP 比對規則運算子也可以用來執行位比較。</span><span class="sxs-lookup"><span data-stu-id="d0e72-121">The LDAP matching rule operators can also be used to perform bitwise comparisons.</span></span> <span data-ttu-id="d0e72-122">如需相符規則的詳細資訊，請參閱 [搜尋篩選語法](/windows/desktop/ADSI/search-filter-syntax)。</span><span class="sxs-lookup"><span data-stu-id="d0e72-122">For more information about matching rules, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span> <span data-ttu-id="d0e72-123">下列程式碼範例會示範篩選準則，以搜尋已 **\_ \_ \_ \_ 啟用 ADS 群組類型** (0X80000000 = 2147483648) 位設定 **groupType** 的物件。</span><span class="sxs-lookup"><span data-stu-id="d0e72-123">The following code example shows a filter that will search for objects that have a **groupType** with the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** (0x80000000 = 2147483648) bit set.</span></span>


```C++
(groupType:1.2.840.113556.1.4.803:=2147483648))
```



</dd> <dt>

<span data-ttu-id="d0e72-124"><span id="OctetString"></span><span id="octetstring"></span><span id="OCTETSTRING"></span>OctetString</span><span class="sxs-lookup"><span data-stu-id="d0e72-124"><span id="OctetString"></span><span id="octetstring"></span><span id="OCTETSTRING"></span>OctetString</span></span>
</dt> <dd>

<span data-ttu-id="d0e72-125">在篩選中指定的值是要尋找的資料。</span><span class="sxs-lookup"><span data-stu-id="d0e72-125">The value specified in a filter is the data to be found.</span></span> <span data-ttu-id="d0e72-126">資料必須以兩個字元編碼的位元組字串表示，其中每個位元組之前都是反斜線 (\) 。</span><span class="sxs-lookup"><span data-stu-id="d0e72-126">The data must be represented as a two character encoded byte string where each byte is preceded by a backslash (\).</span></span> <span data-ttu-id="d0e72-127">例如，值0x05 會以 "05" 的形式出現在字串中 \\ 。</span><span class="sxs-lookup"><span data-stu-id="d0e72-127">For example, the value 0x05 will appear in the string as "\\05".</span></span>

<span data-ttu-id="d0e72-128">[**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata)函數可以用來建立二進位資料的編碼字串表示。</span><span class="sxs-lookup"><span data-stu-id="d0e72-128">The [**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) function can be used to create an encoded string representation of binary data.</span></span> <span data-ttu-id="d0e72-129">**ADsEncodeBinaryData** 函數不會編碼代表英數位元的位元組值。</span><span class="sxs-lookup"><span data-stu-id="d0e72-129">The **ADsEncodeBinaryData** function does not encode byte values that represent alpha-numeric characters.</span></span> <span data-ttu-id="d0e72-130">相反地，它會將字元放在字串中，而不將其編碼。</span><span class="sxs-lookup"><span data-stu-id="d0e72-130">It will, instead, place the character into the string without encoding it.</span></span> <span data-ttu-id="d0e72-131">這會產生包含編碼和未編碼字元混合的字串。</span><span class="sxs-lookup"><span data-stu-id="d0e72-131">This results in the string containing a mixture of encoded and unencoded characters.</span></span> <span data-ttu-id="d0e72-132">例如，如果二進位資料是 0x05 \| 0x1A \| 0x1b \| 0x43 \| 0x32，編碼的字串將會包含 " \\ 05 \\ 1a \\ 1BC2"。</span><span class="sxs-lookup"><span data-stu-id="d0e72-132">For example, if the binary data is 0x05\|0x1A\|0x1B\|0x43\|0x32, the encoded string will contain "\\05\\1A\\1BC2".</span></span> <span data-ttu-id="d0e72-133">這對篩選不會有任何影響，且搜尋篩選器會正確地使用這些類型的字串。</span><span class="sxs-lookup"><span data-stu-id="d0e72-133">This has no effect on the filter and the search filters will work correctly with these types of strings.</span></span>

<span data-ttu-id="d0e72-134">可使用萬用字元。</span><span class="sxs-lookup"><span data-stu-id="d0e72-134">Wildcards are accepted.</span></span>

<span data-ttu-id="d0e72-135">下列程式碼範例顯示篩選準則，其中包含 GUID 值為 "{BF967ABA-0DE6-11D0-A285-00AA003049E2}" 之 **schemaIDGUID** 的編碼字串：</span><span class="sxs-lookup"><span data-stu-id="d0e72-135">The following code example shows a filter that contains encoded string for **schemaIDGUID** with GUID value of "{BF967ABA-0DE6-11D0-A285-00AA003049E2}":</span></span>


```C++
(schemaidguid=\BA\7A\96\BF\E6\0D\D0\11\A2\85\00\AA\00\30\49\E2)
```



</dd> <dt>

<span data-ttu-id="d0e72-136"><span id="Sid"></span><span id="sid"></span><span id="SID"></span>希</span><span class="sxs-lookup"><span data-stu-id="d0e72-136"><span id="Sid"></span><span id="sid"></span><span id="SID"></span>Sid</span></span>
</dt> <dd>

<span data-ttu-id="d0e72-137">在篩選中指定的值是 SID 的編碼位元組字串表示。</span><span class="sxs-lookup"><span data-stu-id="d0e72-137">The value specified in a filter is the encoded byte string representation of the SID.</span></span> <span data-ttu-id="d0e72-138">如需編碼位元組字串的詳細資訊，請參閱本主題中的上一節討論 OctetString 語法。</span><span class="sxs-lookup"><span data-stu-id="d0e72-138">For more information about encoded byte strings, see the previous section in this topic which discusses OctetString syntax.</span></span>

<span data-ttu-id="d0e72-139">下列程式碼範例顯示的篩選準則包含 **objectSid** 的編碼字串，其 SID 字串值為 "S-1-5-21-1935655697-308236825-1417001333"：</span><span class="sxs-lookup"><span data-stu-id="d0e72-139">The following code example shows a filter that contains an encoded string for **objectSid** with SID string value of "S-1-5-21-1935655697-308236825-1417001333":</span></span>


```C++
(ObjectSid=\01\04\00\00\00\00\00\05\15\00\00\00\11\C3\5Fs\19R\5F\12u\B9uT)
```



</dd> <dt>

<span data-ttu-id="d0e72-140"><span id="DN"></span><span id="dn"></span>Dn</span><span class="sxs-lookup"><span data-stu-id="d0e72-140"><span id="DN"></span><span id="dn"></span>DN</span></span>
</dt> <dd>

<span data-ttu-id="d0e72-141">必須提供要比對的整個分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="d0e72-141">The entire distinguished name, to be matched, must be supplied.</span></span>

<span data-ttu-id="d0e72-142">不接受萬用字元。</span><span class="sxs-lookup"><span data-stu-id="d0e72-142">Wildcards are not accepted.</span></span>

<span data-ttu-id="d0e72-143">請注意， **objectCategory** 屬性也可讓您指定在屬性上設定之類別的 **lDAPDisplayName** 。</span><span class="sxs-lookup"><span data-stu-id="d0e72-143">Be aware that the **objectCategory** attribute also enables you to specify the **lDAPDisplayName** of the class set on the attribute.</span></span>

<span data-ttu-id="d0e72-144">下列範例顯示的篩選準則會指定包含 "CN = TestUser，DC = Fabrikam，DC = COM" 的 **成員** ：</span><span class="sxs-lookup"><span data-stu-id="d0e72-144">The following example shows a filter that specifies a **member** that contains "CN=TestUser,DC=Fabrikam,DC=COM":</span></span>


```C++
(member=CN=TestUser,DC=Fabrikam,DC=COM)
```



</dd> <dt>

<span data-ttu-id="d0e72-145"><span id="INTEGER8"></span><span id="integer8"></span>INTEGER8</span><span class="sxs-lookup"><span data-stu-id="d0e72-145"><span id="INTEGER8"></span><span id="integer8"></span>INTEGER8</span></span>
</dt> <dd>

<span data-ttu-id="d0e72-146">篩選準則中指定的值必須是十進位整數。</span><span class="sxs-lookup"><span data-stu-id="d0e72-146">The value specified in a filter must be a decimal integer.</span></span> <span data-ttu-id="d0e72-147">將十六進位值轉換成十進位。</span><span class="sxs-lookup"><span data-stu-id="d0e72-147">Convert hexadecimal values to decimal.</span></span>

<span data-ttu-id="d0e72-148">下列程式碼範例顯示的篩選準則，會將 **creationTime** 設定為 "1999-12-31 23:59:59 (UTC/GMT) " 的 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) ：</span><span class="sxs-lookup"><span data-stu-id="d0e72-148">The following code example shows a filter that specifies a **creationTime** set to a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) of "1999-12-31 23:59:59 (UTC/GMT)":</span></span>


```C++
(creationTime=125911583990000000)
```



<span data-ttu-id="d0e72-149">下列函數會建立完全相符的 (=) 篩選大型整數屬性，並驗證架構中的屬性及其語法：</span><span class="sxs-lookup"><span data-stu-id="d0e72-149">The following functions create an exact match (=) filter for a large integer attribute and verify the attribute in the schema and its syntax:</span></span>


```C++
//***************************************************************************
//
//  CheckAttribute()
//
//***************************************************************************

HRESULT CheckAttribute(LPOLESTR szAttribute, LPOLESTR szSyntax)
{
    HRESULT hr = E_FAIL;
    BSTR bstr;
    IADsProperty *pObject = NULL;
    LPWSTR szPrefix = L"LDAP://schema/";
    LPWSTR szPath;
     
    if((!szAttribute) || (!szSyntax))
    {
        return E_POINTER;
    }

    // Allocate a buffer large enough to hold the ADsPath of the attribute.
    szPath = new WCHAR[lstrlenW(szPrefix) + lstrlenW(szAttribute) + 1];
    if(NULL == szPath)
    {
        return E_OUTOFMEMORY;
    }
     
    // Create the ADsPath of the attribute.
    wcscpy_s(szPath, szPrefix);
    wcscat_s(szPath, szAttribute);

    hr = ADsOpenObject( szPath,
                        NULL,
                        NULL,
                        ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                        IID_IADsProperty,
                        (void**)&pObject);
    if(SUCCEEDED(hr)) 
    {
        hr = pObject->get_Syntax(&bstr);
        if (SUCCEEDED(hr)) 
        {
            if (0==lstrcmpiW(bstr, szSyntax)) 
            {
                hr = S_OK;
            }
            else
            {
                hr = S_FALSE;
            }
        }

        SysFreeString(bstr);
    }
    
    if(pObject)
    {
        pObject->Release();
    }

    delete szPath;
    
    return hr;
}

//***************************************************************************
//
//  CreateExactMatchFilterLargeInteger()
//
//***************************************************************************

HRESULT CreateExactMatchFilterLargeInteger( LPOLESTR szAttribute, 
                                            INT64 liValue, 
                                            LPOLESTR *pszFilter)
{
    HRESULT hr = E_FAIL;
     
    if ((!szAttribute) || (!pszFilter))
    {
        return E_POINTER;
    }
     
    // Verify that the attribute exists and has 
    // Integer8 (Large Integer) syntax.
     
    hr = CheckAttribute(szAttribute, L"Integer8");
    if (S_OK == hr) 
    {
        LPWSTR szFormat = L"%s=%I64d";
        LPWSTR szTempFilter = new WCHAR[lstrlenW(szFormat) + lstrlenW(szAttribute) + 20 + 1];

        if(NULL == szTempFilter)
        {
            return E_OUTOFMEMORY;
        }
        
        swprintf_s(szTempFilter, L"%s=%I64d", szAttribute, liValue);
     
        // Allocate buffer for the filter string.
        // Caller must free the buffer using CoTaskMemFree.
        *pszFilter = (OLECHAR *)CoTaskMemAlloc(sizeof(OLECHAR) * (lstrlenW(szTempFilter) + 1));
        if (*pszFilter) 
        {
            wcscpy_s(*pszFilter, szTempFilter);
            hr = S_OK;
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }

        delete szTempFilter;
    }

    return hr;
}
```



</dd> <dt>

<span data-ttu-id="d0e72-150"><span id="PrintableString"></span><span id="printablestring"></span><span id="PRINTABLESTRING"></span>PrintableString</span><span class="sxs-lookup"><span data-stu-id="d0e72-150"><span id="PrintableString"></span><span id="printablestring"></span><span id="PRINTABLESTRING"></span>PrintableString</span></span>
</dt> <dd>

<span data-ttu-id="d0e72-151">具有這些語法的屬性應遵守特定字元集。</span><span class="sxs-lookup"><span data-stu-id="d0e72-151">Attributes with these syntaxes should adhere to specific character sets.</span></span> <span data-ttu-id="d0e72-152">如需詳細資訊，請參閱 [Active Directory Domain Services 中的屬性語法](syntaxes-for-attributes-in-active-directory-domain-services.md)。</span><span class="sxs-lookup"><span data-stu-id="d0e72-152">For more information, see [Syntaxes for Attributes in Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).</span></span>

<span data-ttu-id="d0e72-153">目前，Active Directory Domain Services 不會強制執行這些字元集。</span><span class="sxs-lookup"><span data-stu-id="d0e72-153">Currently, Active Directory Domain Services do not enforce those character sets.</span></span>

<span data-ttu-id="d0e72-154">在篩選中指定的值是字串。</span><span class="sxs-lookup"><span data-stu-id="d0e72-154">The value specified in a filter is a string.</span></span> <span data-ttu-id="d0e72-155">比較會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="d0e72-155">The comparison is case-sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="d0e72-156"><span id="GeneralizedTime"></span><span id="generalizedtime"></span><span id="GENERALIZEDTIME"></span>GeneralizedTime</span><span class="sxs-lookup"><span data-stu-id="d0e72-156"><span id="GeneralizedTime"></span><span id="generalizedtime"></span><span id="GENERALIZEDTIME"></span>GeneralizedTime</span></span>
</dt> <dd>

<span data-ttu-id="d0e72-157">在篩選中指定的值是表示日期的字串，其格式如下：</span><span class="sxs-lookup"><span data-stu-id="d0e72-157">The value specified in a filter is a string that represents the date in the following form:</span></span>


```C++
YYYYMMDDHHMMSS.0Z
```



<span data-ttu-id="d0e72-158">"0Z" 表示沒有時間差異。</span><span class="sxs-lookup"><span data-stu-id="d0e72-158">"0Z" indicates no time differential.</span></span> <span data-ttu-id="d0e72-159">請注意，Active Directory 伺服器會以格林威治標準時間 (GMT) 儲存日期/時間。</span><span class="sxs-lookup"><span data-stu-id="d0e72-159">Be aware that the Active Directory server stores date/time as Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="d0e72-160">如果未指定時間差異，預設值為 GMT。</span><span class="sxs-lookup"><span data-stu-id="d0e72-160">If a time differential is not specified, the default is GMT.</span></span>

<span data-ttu-id="d0e72-161">如果本地時區不是 GMT，請使用差異值來指定您的當地時區，並將差異套用至 GMT。</span><span class="sxs-lookup"><span data-stu-id="d0e72-161">If the local time zone is not GMT, use a differential value to specify your local time zone and apply the differential to GMT.</span></span> <span data-ttu-id="d0e72-162">差異以： GMT = Local + 差異為基礎。</span><span class="sxs-lookup"><span data-stu-id="d0e72-162">The differential is based on: GMT=Local+differential.</span></span>

<span data-ttu-id="d0e72-163">若要指定差異，請使用：</span><span class="sxs-lookup"><span data-stu-id="d0e72-163">To specify a differential, use:</span></span>


```C++
YYYYMMDDHHMMSS.0[+/-]HHMM
```



<span data-ttu-id="d0e72-164">下列範例顯示的篩選準則指定的 **whenCreated** 時間設定為 3/23/99 8:52:58 PM GMT：</span><span class="sxs-lookup"><span data-stu-id="d0e72-164">The following example shows a filter that specifies a **whenCreated** time set to 3/23/99 8:52:58 PM GMT:</span></span>


```C++
(whenCreated=19990323205258.0Z)
```



<span data-ttu-id="d0e72-165">下列範例顯示的篩選準則指定的 **whenCreated** 時間設定為 3/23/99 8:52:58 PM 的紐西蘭標準時間 (差異是 + 12 小時) ：</span><span class="sxs-lookup"><span data-stu-id="d0e72-165">The following example shows a filter that specifies a **whenCreated** time set to 3/23/99 8:52:58 PM New Zealand Standard Time (differential is +12 hours):</span></span>


```C++
(whenCreated=19990323205258.0+1200)
```



<span data-ttu-id="d0e72-166">下列程式碼範例顯示如何計算時區差異。</span><span class="sxs-lookup"><span data-stu-id="d0e72-166">The following code example shows how to calculate time zone differential.</span></span> <span data-ttu-id="d0e72-167">函數會傳回目前當地時區與 GMT 之間的差異。</span><span class="sxs-lookup"><span data-stu-id="d0e72-167">The function returns the differential between the current local time zone and GMT.</span></span> <span data-ttu-id="d0e72-168">傳回的值是採用下列格式的字串：</span><span class="sxs-lookup"><span data-stu-id="d0e72-168">The value returned is a string in the following format:</span></span>


```C++
[+/-]HHMM
```



<span data-ttu-id="d0e72-169">例如，太平洋標準時間為-0800。</span><span class="sxs-lookup"><span data-stu-id="d0e72-169">For example, Pacific Standard Time is -0800.</span></span>


```C++
//***************************************************************************
//
//  GetLocalTimeZoneDifferential()
//
//***************************************************************************

HRESULT GetLocalTimeZoneDifferential(LPOLESTR *pszDifferential)
{
    if(NULL == pszDifferential)
    {
        return E_INVALIDARG;
    }
    
    HRESULT hr = E_FAIL;
    DWORD dwReturn;
    TIME_ZONE_INFORMATION timezoneinfo;
    LONG lTimeDifferential;
    LONG lHours;
    LONG lMinutes;
    
    dwReturn  = GetTimeZoneInformation(&timezoneinfo);

    switch (dwReturn)
    {
    case TIME_ZONE_ID_STANDARD:
        lTimeDifferential = timezoneinfo.Bias + timezoneinfo.StandardBias;
        
        // Bias is in minutes. Calculate the hours for HHMM format.
        lHours = -(lTimeDifferential/60);
        
        // Bias is in minutes. Calculate the minutes for HHMM format.
        lMinutes = lTimeDifferential%60L;

        hr = S_OK;
        break;

    case TIME_ZONE_ID_DAYLIGHT:
        lTimeDifferential = timezoneinfo.Bias + timezoneinfo.DaylightBias;
        
        // Bias is in minutes. Calculate the hours for HHMM format.
        // Apply the additive inverse.
        // Bias is based on GMT=Local+Bias.
        // A differential, based on GMT=Local-Bias, is required.
        lHours = -(lTimeDifferential/60);
        
        // Bias is in minutes. Calculate the minutes for HHMM format.
        lMinutes = lTimeDifferential%60L;
        
        hr = S_OK;
        break;

    case TIME_ZONE_ID_INVALID:
    default:
        hr = E_FAIL;
        break;
    }
     
    if (SUCCEEDED(hr))
    {
        // The caller must free the memory using CoTaskMemFree.
        *pszDifferential = (OLECHAR *)CoTaskMemAlloc(sizeof(OLECHAR) * (3 + 2 + 1));
        if (*pszDifferential)
        {
            swprintf_s(*pszDifferential, L"%+03d%02d", lHours, lMinutes);
            
            hr = S_OK;
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }
    }
     
    return hr;
}
```



</dd> <dt>

<span data-ttu-id="d0e72-170"><span id="UTCTime"></span><span id="utctime"></span><span id="UTCTIME"></span>UTCTime</span><span class="sxs-lookup"><span data-stu-id="d0e72-170"><span id="UTCTime"></span><span id="utctime"></span><span id="UTCTIME"></span>UTCTime</span></span>
</dt> <dd>

<span data-ttu-id="d0e72-171">在篩選中指定的值是表示日期的字串，其格式如下：</span><span class="sxs-lookup"><span data-stu-id="d0e72-171">The value specified in a filter is a string that represents the date in the following form:</span></span>


```C++
YYMMDDHHMMSSZ
```



<span data-ttu-id="d0e72-172">Z 表示沒有時間差異。</span><span class="sxs-lookup"><span data-stu-id="d0e72-172">Z indicates no time differential.</span></span> <span data-ttu-id="d0e72-173">請注意，Active Directory 伺服器會將日期和時間儲存為 GMT 時間。</span><span class="sxs-lookup"><span data-stu-id="d0e72-173">Be aware that the Active Directory server stores date and time as GMT time.</span></span> <span data-ttu-id="d0e72-174">如果未指定時間差異，則預設值為 GMT。</span><span class="sxs-lookup"><span data-stu-id="d0e72-174">If a time differential is not specified, GMT is the default.</span></span>

<span data-ttu-id="d0e72-175">秒值 ( "SS" ) 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="d0e72-175">The seconds value ("SS") is optional.</span></span>

<span data-ttu-id="d0e72-176">如果 GMT 不是當地時區，請套用本機差異值以指定您的當地時區。</span><span class="sxs-lookup"><span data-stu-id="d0e72-176">If GMT is not the local time zone, apply a local differential value to specify your local time zone.</span></span> <span data-ttu-id="d0e72-177">差異是： GMT = Local + 差異。</span><span class="sxs-lookup"><span data-stu-id="d0e72-177">The differential is: GMT=Local+differential.</span></span>

<span data-ttu-id="d0e72-178">若要指定差異，請使用下列格式：</span><span class="sxs-lookup"><span data-stu-id="d0e72-178">To specify a differential, use the following form:</span></span>


```C++
YYMMDDHHMMSS[+/-]HHMM
```



<span data-ttu-id="d0e72-179">下列範例顯示的篩選準則指定的 **myTimeAttrib** 時間設定為 3/23/99 8:52:58 PM GMT：</span><span class="sxs-lookup"><span data-stu-id="d0e72-179">The following example shows a filter that specifies a **myTimeAttrib** time set to 3/23/99 8:52:58 PM GMT:</span></span>


```C++
(myTimeAttrib=990323205258Z)
```



<span data-ttu-id="d0e72-180">下列範例顯示的篩選準則指定的 **myTimeAttrib** 時間設定為 3/23/99 8:52:58 PM （未指定秒數）：</span><span class="sxs-lookup"><span data-stu-id="d0e72-180">The following example shows a filter that specifies a **myTimeAttrib** time set to 3/23/99 8:52:58 PM without seconds specified:</span></span>


```C++
(myTimeAttrib=9903232052Z)
```



<span data-ttu-id="d0e72-181">下列範例顯示的篩選準則指定的 **myTimeAttrib** 時間設定為 3/23/99 8:52:58 PM 的紐西蘭標準時間 (差異是12小時) 。</span><span class="sxs-lookup"><span data-stu-id="d0e72-181">The following example shows a filter that specifies a **myTimeAttrib** time set to 3/23/99 8:52:58 PM New Zealand Standard Time (differential is 12 hours).</span></span> <span data-ttu-id="d0e72-182">這相當於上午 3/23/99 8:52:58：（GMT）。</span><span class="sxs-lookup"><span data-stu-id="d0e72-182">This is equivalent to 3/23/99 8:52:58 AM GMT.</span></span>


```C++
(myTimeAttrib=990323205258+1200)
```



</dd> <dt>

<span data-ttu-id="d0e72-183"><span id="DirectoryString"></span><span id="directorystring"></span><span id="DIRECTORYSTRING"></span>DirectoryString</span><span class="sxs-lookup"><span data-stu-id="d0e72-183"><span id="DirectoryString"></span><span id="directorystring"></span><span id="DIRECTORYSTRING"></span>DirectoryString</span></span>
</dt> <dd>

<span data-ttu-id="d0e72-184">在篩選中指定的值是字串。</span><span class="sxs-lookup"><span data-stu-id="d0e72-184">The value specified in a filter is a string.</span></span> <span data-ttu-id="d0e72-185">DirectoryString 可包含 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="d0e72-185">DirectoryString can contain Unicode characters.</span></span> <span data-ttu-id="d0e72-186">此比較不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="d0e72-186">The comparison is case-insensitive.</span></span>

</dd> <dt>

<span data-ttu-id="d0e72-187"><span id="OID"></span><span id="oid"></span>老</span><span class="sxs-lookup"><span data-stu-id="d0e72-187"><span id="OID"></span><span id="oid"></span>OID</span></span>
</dt> <dd>

<span data-ttu-id="d0e72-188">必須提供要比對的整個 OID。</span><span class="sxs-lookup"><span data-stu-id="d0e72-188">The entire OID to be matched must be supplied.</span></span>

<span data-ttu-id="d0e72-189">不接受萬用字元。</span><span class="sxs-lookup"><span data-stu-id="d0e72-189">Wildcards are not accepted.</span></span>

<span data-ttu-id="d0e72-190">**ObjectCategory** 屬性可讓您指定屬性之類別集的 **lDAPDisplayName** 。</span><span class="sxs-lookup"><span data-stu-id="d0e72-190">The **objectCategory** attribute enables you to specify the **lDAPDisplayName** of the class set for the attribute.</span></span>

<span data-ttu-id="d0e72-191">下列範例顯示的篩選準則會指定 volume 類別的 **governsID** ：</span><span class="sxs-lookup"><span data-stu-id="d0e72-191">The following example shows a filter that specifies **governsID** for volume class:</span></span>


```C++
(governsID=1.2.840.113556.1.5.36)
```



<span data-ttu-id="d0e72-192">兩個對等篩選器，指定包含 **uNCName** 的 **systemMustContain** 屬性，該屬性具有1.2.840.113556.1.4.137 的 OID：</span><span class="sxs-lookup"><span data-stu-id="d0e72-192">Two equivalent filters that specifies **systemMustContain** attribute containing **uNCName**, which has an OID of 1.2.840.113556.1.4.137:</span></span>


```C++
(SystemMustContain=uNCName)
 
(SystemMustContain=1.2.840.113556.1.4.137)
```



</dd> <dt>

<span data-ttu-id="d0e72-193"><span id="Other_Syntaxes"></span><span id="other_syntaxes"></span><span id="OTHER_SYNTAXES"></span>其他語法</span><span class="sxs-lookup"><span data-stu-id="d0e72-193"><span id="Other_Syntaxes"></span><span id="other_syntaxes"></span><span id="OTHER_SYNTAXES"></span>Other Syntaxes</span></span>
</dt> <dd>

<span data-ttu-id="d0e72-194">下列語法會在類似于八位字串的篩選中進行評估：</span><span class="sxs-lookup"><span data-stu-id="d0e72-194">The following syntaxes are evaluated in a filter similar to an octet string:</span></span>

-   <span data-ttu-id="d0e72-195">ObjectSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="d0e72-195">ObjectSecurityDescriptor</span></span>
-   <span data-ttu-id="d0e72-196">AccessPointDN</span><span class="sxs-lookup"><span data-stu-id="d0e72-196">AccessPointDN</span></span>
-   <span data-ttu-id="d0e72-197">PresentationAddresses</span><span class="sxs-lookup"><span data-stu-id="d0e72-197">PresentationAddresses</span></span>
-   <span data-ttu-id="d0e72-198">ReplicaLink</span><span class="sxs-lookup"><span data-stu-id="d0e72-198">ReplicaLink</span></span>
-   <span data-ttu-id="d0e72-199">DNWithString</span><span class="sxs-lookup"><span data-stu-id="d0e72-199">DNWithString</span></span>
-   <span data-ttu-id="d0e72-200">DNWithOctetString</span><span class="sxs-lookup"><span data-stu-id="d0e72-200">DNWithOctetString</span></span>
-   <span data-ttu-id="d0e72-201">ORName</span><span class="sxs-lookup"><span data-stu-id="d0e72-201">ORName</span></span>

</dd> </dl>

 

 