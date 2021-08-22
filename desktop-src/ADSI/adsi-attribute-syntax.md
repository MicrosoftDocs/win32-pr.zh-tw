---
title: ADSI 屬性語法
description: 目錄中的每個屬性都有相關聯的語法。 例如，整數、字串、數值等等。 ADSI 會定義它自己的語法，以對應至原生目錄語法。 本節說明 ADSI 中的屬性語法類型。
ms.assetid: 83d3d42f-e35e-4bd1-b26e-d141e9ec9c31
ms.tgt_platform: multiple
keywords:
- 屬性 ADSI、語法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 310a678c48051909e4a3e7555b9d8ff0a508c339cfcd41ed6c66286529cadde1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023926"
---
# <a name="adsi-attribute-syntax"></a>ADSI 屬性語法

目錄中的每個屬性都有相關聯的語法。 例如，整數、字串、數值等等。 ADSI 會定義它自己的語法，以對應至原生目錄語法。 本節說明 ADSI 中的屬性語法類型。

## <a name="distinguished-name-string"></a>辨別名稱字串


```VB
Syntax Type: ADSTYPE_DN_STRING
```



辨別名稱適用于將兩個物件連結在一起。 例如，它可以建立一個連結，讓 Alice 物件成為 Bob 物件的管理員。 如果 Alice 物件移至不同的位置，則 Alice 和 Bob 之間的管理員連結會自動更新。

辨別名稱必須包含有效的辨別名稱物件。 如果辨別名稱未對應到有效的現有物件，大部分的伺服器會拒絕要求並傳回條件約束違規錯誤。

範例：


```VB
Set x = GetObject("LDAP://CN=Bob, OU=Sales,DC=Fabrikam, DC=com)
x.Put "manager", "CN=Alice, OU=Sales, DC=Fabrikam, DC=COM"
x.SetInfo
 
PADS_ATTR_INFO pInfo;
// .. IDirectoryObject::GetObjectAttribute
printf("%S\n", pInfo->pADsValues->DNString );
```



## <a name="case-exact-string-and-case-ignore-string"></a>Case 精確字串和 Case 忽略字串


```VB
Syntax Types: ADSTYPE_CASE_IGNORE_STRING, ADSTYPE_CASE_EXACT_STRING.
```



Case 精確字串為區分大小寫的字串，而 Case Ignore 字串則是不區分大小寫的字串。 目錄中的屬性百分比很大，使用此語法。

> [!Note]  
> 目錄不一定會將其儲存為 Unicode 字串。 但是，ADSI 會接受並傳回 Unicode 字串。

 

範例：


```VB
Dim propList As IADsPropertyList
Set propList = GetObject("LDAP://DC=Fabrikam,DC=com")
Set propVal = New PropertyValue
 
' --- Property Value ---
propVal.CaseIgnoreString = "Fabrikam, Inc - Seattle, WA"
propVal.ADsType = ADSTYPE_CASE_IGNORE_STRING
```



## <a name="printable-string"></a>可列印字串


```VB
Syntax Type: ADSTYPE_PRINTABLE_STRING
```



此語法適用于具有字串值的屬性，其中大寫和小寫會視為不相等的比較，例如 "FABRIKAM" 和 "Fabrikam" 不相符。 ADSI 接受可列印字串的任何內容;它不會嘗試確認它們確實可以列印。

## <a name="numeric-string"></a>數值字串


```VB
Syntax Type: ADSTYPE_NUMERIC_STRING
```



在這個語法中，字串會與可列印的字串比對，但在比較中會忽略所有空白字元。 ADSI 不會執行值檢查，以確保只會在此語法的值中顯示數位和空格。 Active Directory 接受數值字串的任何內容;它不會驗證字元是否為數值。

## <a name="utc-time"></a>UTC 時間


```VB
Syntax Type: ADSTYPE_UTC_TIME
```



此語法會將日期和時間儲存在單一字串中。 字串格式由三個串連的部分組成： (1) YYMMDD; (2) HHMM 或 HHMMSS (都可接受) ;和 (3) "Z" 表示指定的時間是格林威治標準時間 (GMT) ，或 "+/-HHMM" 表示指定的時間是當地時間，與 GMT 的指定差異。 差異是以公式： GMT = Local + 差異為基礎。

> [!Note]  
> 年份的前兩個數字不會儲存在此字串中。

 

合法值的一些範例包括 "9101311455Z"、"910131145503Z"、"9101314455-0500"、"910131145503 + 0130"。 這個字串會儲存為單一位元組 ASCII 字元，且不會儲存任何字碼頁編號。

雖然支援排序，但是只會以 ASCII 不區分大小寫的字串排序來完成，而不是正確地解讀字串的意義。

接受任何有效的字串值。 不嘗試確定字串包含有效的時間字串。

## <a name="generalized-time"></a>一般化時間


```VB
Syntax Type: ADSTYPE_UTC_TIME
```



如果要定義用來儲存時間值的新屬性，則應該使用 GeneralizedTime 語法。 GeneralizedTime 語法使用四個字元來代表年份，而不是使用 UTCTime 的兩個字元。

GeneralizedTime 語法的格式為 "YYYYMMDDHHMMSS.FFFFFF. 0Z"。 可接受值的範例是「20010928060000.0 Z」。 "Z" 表示沒有時間差異。 Active Directory 將日期/時間儲存為格林威治標準時間 (GMT) 。 如果未指定時間差異，則預設值為 GMT。

如果時間是在 GMT 以外的時區中指定，則時區與 gmt 之間的差異會附加至字串，而不是 "yyyymmddhhmmss.ffffff. 0 HHMM" 格式的 "Z" \[ +/- \] 。 可接受值的範例是 "20010928060000.0 + 0200"。

差異是以公式： GMT = Local + 差異為基礎。

## <a name="boolean"></a>Boolean


```VB
Syntax Type: ADSTYPE_BOOLEAN
```



Active Directory 只接受此語法的帶正負號32位值。 它會將零視為 **FALSE** ，並將所有非零值處理為 **TRUE**。

## <a name="integer"></a>整數


```VB
Syntax Type: ADSTYPE_INTEGER
```



32位帶正負號的數位值。

## <a name="large-integer"></a>大型整數


```VB
Syntax Type: ADSTYPE_LARGE_INTEGER
```



64位帶正負號的數位值。 大型整數實際上實作為 [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) 介面上的 COM 物件。 **HighPart** 和 **LowPart** 方法是用來存取大整數值的 2 32 位部分。

範例：


```VB
Dim x as IADsLargeInteger
Set o = GetObject("LDAP://DC=Fabrikam,DC=com")
Set x = o.Get("UsnCreated")
Debug.Print x.HighPart
Debug.Print x.LowPart
```



## <a name="octet-string"></a>八位字串


```VB
Syntax Type: ADSTYPE_OCTET_STRING
```



八進位字串會以位元組的變異陣列傳回。 這包括大小 (八位數) ，後面接著一系列八位。 八位為8位位元組，因此一連串的八位是二進位資料的字串。

## <a name="object-class"></a>物件類別


```VB
Syntax Type: ADSTYPE_CASE_IGNORE_STRING
```



Object 類別是指定之架構類別的唯一物件識別碼。 每個物件實例的類別都是由 **objectClass** 屬性來識別。 建立時，您永遠不能變更物件類別。 **objectClass** 是多重值屬性。 它會列出物件的特定類別，以及衍生特定類別之所有結構化或抽象類別類別的類別。 這包括 Top，也就是所有其他類別最終衍生的類別。 Active Directory 不會列出 **objectClass** 屬性中的輔助類別。

## <a name="security-descriptor"></a>安全性描述元


```VB
Syntax Type: ADSTYPE_NT_SECURITY_DESCRIPTOR
```



存取權限會定義安全性主體嘗試對 Active Directory 物件執行作業時的功能。 安全描述項描述與物件相關聯的存取控制資訊。

在 **nTSecurityDescriptor** 屬性中，安全描述項會儲存為目錄物件的屬性。 當已驗證的使用者嘗試存取目錄物件時，目錄伺服器會根據物件安全描述項，判斷授與或拒絕使用者的存取權。

[**ADS \_ SD \_ CONTROL \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_sd_control_enum)列舉會指定安全描述項的控制旗標。

下列程式碼範例顯示如何取得安全描述項。


```VB
' Obtain a security descriptor.
Dim x as IADs
Dim sd as IADsSecurityDescriptor
Dim acl as IADsAccessControlList
 
Set x = GetObject("LDAP://DC=Fabrikam, DC=com")
Set sd = x.Get("nTSecurityDescriptor")
 
Debug.Print sd.Control
Debug.Print sd.Group
Debug.Print sd.Owner
Debug.Print sd.Revision
 
Set acl = sd.DiscretionaryAcl
Set sacl = sd.SystemAcl
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[Active Directory 屬性的語法](/windows/desktop/AD/syntaxes-for-attributes-in-active-directory-domain-services)
</dt> <dt>

[選擇語法](/windows/desktop/AD/choosing-a-syntax)
</dt> <dt>

[如何指定比較值](/windows/desktop/AD/how-to-specify-comparison-values)
</dt> </dl>

 

 