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
# <a name="how-to-specify-comparison-values"></a>如何指定比較值

每個屬性類型都有一個語法，可決定您可以在該屬性的搜尋篩選中指定的比較數值型別。

下列各節說明每個屬性語法的需求。 如需屬性語法的詳細資訊，請參閱 [Active Directory Domain Services 中的屬性語法](syntaxes-for-attributes-in-active-directory-domain-services.md)。

<dl> <dt>

<span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>布林
</dt> <dd>

篩選準則中指定的值必須是 "TRUE" 或 "FALSE" 的字串值。 下列範例示範如何指定布林值比較字串。

下列範例會搜尋將 **showInAdvancedViewOnly** 設為 **TRUE** 的物件：


```C++
(showInAdvancedViewOnly=TRUE)
```



下列範例會搜尋將 **showInAdvancedViewOnly** 設為 **FALSE** 的物件：


```C++
(showInAdvancedViewOnly=FALSE)
```



</dd> <dt>

<span id="Integer_and_Enumeration"></span><span id="integer_and_enumeration"></span><span id="INTEGER_AND_ENUMERATION"></span>整數和列舉
</dt> <dd>

篩選準則中指定的值必須是十進位整數。 十六進位值必須轉換成 decimal。 值比較字串採用下列格式：


```C++
<attribute name>:<value>
```



" <attribute name> " 是屬性的 **lDAPDisplayName** 和 "<value>"是要用於比較的值。

下列程式碼範例示範的篩選準則會搜尋其 **groupType** 值等於 **ADS \_ 群組 \_ 類型 \_ 通用 \_ 群組** (8) 旗標和 **ads \_ 群組 \_ 類型 \_ 安全性 \_** (0x80000000) 旗標的物件。 這兩個旗標會組合相等的0x80000008 （轉換為 decimal）為2147483656。


```C++
(groupType=2147483656)
```



LDAP 比對規則運算子也可以用來執行位比較。 如需相符規則的詳細資訊，請參閱 [搜尋篩選語法](/windows/desktop/ADSI/search-filter-syntax)。 下列程式碼範例會示範篩選準則，以搜尋已 **\_ \_ \_ \_ 啟用 ADS 群組類型** (0X80000000 = 2147483648) 位設定 **groupType** 的物件。


```C++
(groupType:1.2.840.113556.1.4.803:=2147483648))
```



</dd> <dt>

<span id="OctetString"></span><span id="octetstring"></span><span id="OCTETSTRING"></span>OctetString
</dt> <dd>

在篩選中指定的值是要尋找的資料。 資料必須以兩個字元編碼的位元組字串表示，其中每個位元組之前都是反斜線 (\) 。 例如，值0x05 會以 "05" 的形式出現在字串中 \\ 。

[**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata)函數可以用來建立二進位資料的編碼字串表示。 **ADsEncodeBinaryData** 函數不會編碼代表英數位元的位元組值。 相反地，它會將字元放在字串中，而不將其編碼。 這會產生包含編碼和未編碼字元混合的字串。 例如，如果二進位資料是 0x05 \| 0x1A \| 0x1b \| 0x43 \| 0x32，編碼的字串將會包含 " \\ 05 \\ 1a \\ 1BC2"。 這對篩選不會有任何影響，且搜尋篩選器會正確地使用這些類型的字串。

可使用萬用字元。

下列程式碼範例顯示篩選準則，其中包含 GUID 值為 "{BF967ABA-0DE6-11D0-A285-00AA003049E2}" 之 **schemaIDGUID** 的編碼字串：


```C++
(schemaidguid=\BA\7A\96\BF\E6\0D\D0\11\A2\85\00\AA\00\30\49\E2)
```



</dd> <dt>

<span id="Sid"></span><span id="sid"></span><span id="SID"></span>希
</dt> <dd>

在篩選中指定的值是 SID 的編碼位元組字串表示。 如需編碼位元組字串的詳細資訊，請參閱本主題中的上一節討論 OctetString 語法。

下列程式碼範例顯示的篩選準則包含 **objectSid** 的編碼字串，其 SID 字串值為 "S-1-5-21-1935655697-308236825-1417001333"：


```C++
(ObjectSid=\01\04\00\00\00\00\00\05\15\00\00\00\11\C3\5Fs\19R\5F\12u\B9uT)
```



</dd> <dt>

<span id="DN"></span><span id="dn"></span>Dn
</dt> <dd>

必須提供要比對的整個分辨名稱。

不接受萬用字元。

請注意， **objectCategory** 屬性也可讓您指定在屬性上設定之類別的 **lDAPDisplayName** 。

下列範例顯示的篩選準則會指定包含 "CN = TestUser，DC = Fabrikam，DC = COM" 的 **成員** ：


```C++
(member=CN=TestUser,DC=Fabrikam,DC=COM)
```



</dd> <dt>

<span id="INTEGER8"></span><span id="integer8"></span>INTEGER8
</dt> <dd>

篩選準則中指定的值必須是十進位整數。 將十六進位值轉換成十進位。

下列程式碼範例顯示的篩選準則，會將 **creationTime** 設定為 "1999-12-31 23:59:59 (UTC/GMT) " 的 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) ：


```C++
(creationTime=125911583990000000)
```



下列函數會建立完全相符的 (=) 篩選大型整數屬性，並驗證架構中的屬性及其語法：


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

<span id="PrintableString"></span><span id="printablestring"></span><span id="PRINTABLESTRING"></span>PrintableString
</dt> <dd>

具有這些語法的屬性應遵守特定字元集。 如需詳細資訊，請參閱 [Active Directory Domain Services 中的屬性語法](syntaxes-for-attributes-in-active-directory-domain-services.md)。

目前，Active Directory Domain Services 不會強制執行這些字元集。

在篩選中指定的值是字串。 比較會區分大小寫。

</dd> <dt>

<span id="GeneralizedTime"></span><span id="generalizedtime"></span><span id="GENERALIZEDTIME"></span>GeneralizedTime
</dt> <dd>

在篩選中指定的值是表示日期的字串，其格式如下：


```C++
YYYYMMDDHHMMSS.0Z
```



"0Z" 表示沒有時間差異。 請注意，Active Directory 伺服器會以格林威治標準時間 (GMT) 儲存日期/時間。 如果未指定時間差異，預設值為 GMT。

如果本地時區不是 GMT，請使用差異值來指定您的當地時區，並將差異套用至 GMT。 差異以： GMT = Local + 差異為基礎。

若要指定差異，請使用：


```C++
YYYYMMDDHHMMSS.0[+/-]HHMM
```



下列範例顯示的篩選準則指定的 **whenCreated** 時間設定為 3/23/99 8:52:58 PM GMT：


```C++
(whenCreated=19990323205258.0Z)
```



下列範例顯示的篩選準則指定的 **whenCreated** 時間設定為 3/23/99 8:52:58 PM 的紐西蘭標準時間 (差異是 + 12 小時) ：


```C++
(whenCreated=19990323205258.0+1200)
```



下列程式碼範例顯示如何計算時區差異。 函數會傳回目前當地時區與 GMT 之間的差異。 傳回的值是採用下列格式的字串：


```C++
[+/-]HHMM
```



例如，太平洋標準時間為-0800。


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

<span id="UTCTime"></span><span id="utctime"></span><span id="UTCTIME"></span>UTCTime
</dt> <dd>

在篩選中指定的值是表示日期的字串，其格式如下：


```C++
YYMMDDHHMMSSZ
```



Z 表示沒有時間差異。 請注意，Active Directory 伺服器會將日期和時間儲存為 GMT 時間。 如果未指定時間差異，則預設值為 GMT。

秒值 ( "SS" ) 是選擇性的。

如果 GMT 不是當地時區，請套用本機差異值以指定您的當地時區。 差異是： GMT = Local + 差異。

若要指定差異，請使用下列格式：


```C++
YYMMDDHHMMSS[+/-]HHMM
```



下列範例顯示的篩選準則指定的 **myTimeAttrib** 時間設定為 3/23/99 8:52:58 PM GMT：


```C++
(myTimeAttrib=990323205258Z)
```



下列範例顯示的篩選準則指定的 **myTimeAttrib** 時間設定為 3/23/99 8:52:58 PM （未指定秒數）：


```C++
(myTimeAttrib=9903232052Z)
```



下列範例顯示的篩選準則指定的 **myTimeAttrib** 時間設定為 3/23/99 8:52:58 PM 的紐西蘭標準時間 (差異是12小時) 。 這相當於上午 3/23/99 8:52:58：（GMT）。


```C++
(myTimeAttrib=990323205258+1200)
```



</dd> <dt>

<span id="DirectoryString"></span><span id="directorystring"></span><span id="DIRECTORYSTRING"></span>DirectoryString
</dt> <dd>

在篩選中指定的值是字串。 DirectoryString 可包含 Unicode 字元。 此比較不區分大小寫。

</dd> <dt>

<span id="OID"></span><span id="oid"></span>老
</dt> <dd>

必須提供要比對的整個 OID。

不接受萬用字元。

**ObjectCategory** 屬性可讓您指定屬性之類別集的 **lDAPDisplayName** 。

下列範例顯示的篩選準則會指定 volume 類別的 **governsID** ：


```C++
(governsID=1.2.840.113556.1.5.36)
```



兩個對等篩選器，指定包含 **uNCName** 的 **systemMustContain** 屬性，該屬性具有1.2.840.113556.1.4.137 的 OID：


```C++
(SystemMustContain=uNCName)
 
(SystemMustContain=1.2.840.113556.1.4.137)
```



</dd> <dt>

<span id="Other_Syntaxes"></span><span id="other_syntaxes"></span><span id="OTHER_SYNTAXES"></span>其他語法
</dt> <dd>

下列語法會在類似于八位字串的篩選中進行評估：

-   ObjectSecurityDescriptor
-   AccessPointDN
-   PresentationAddresses
-   ReplicaLink
-   DNWithString
-   DNWithOctetString
-   ORName

</dd> </dl>

 

 