---
title: ADSI 屬性語法
description: 目錄中的每個屬性都有相關聯的語法。 例如，整數、字串、數值等等。 ADSI 會定義它自己的語法，以對應至原生目錄語法。 本節說明 ADSI 中的屬性語法類型。
ms.assetid: 83d3d42f-e35e-4bd1-b26e-d141e9ec9c31
ms.tgt_platform: multiple
keywords:
- 屬性 ADSI、語法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b23d58b48b27fa88077f388b47535afd1dbd0a4f
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683086"
---
# <a name="adsi-attribute-syntax"></a><span data-ttu-id="08703-107">ADSI 屬性語法</span><span class="sxs-lookup"><span data-stu-id="08703-107">ADSI Attribute Syntax</span></span>

<span data-ttu-id="08703-108">目錄中的每個屬性都有相關聯的語法。</span><span class="sxs-lookup"><span data-stu-id="08703-108">Each attribute in the directory has an associated syntax.</span></span> <span data-ttu-id="08703-109">例如，整數、字串、數值等等。</span><span class="sxs-lookup"><span data-stu-id="08703-109">For example, integer, string, numeric, and so on.</span></span> <span data-ttu-id="08703-110">ADSI 會定義它自己的語法，以對應至原生目錄語法。</span><span class="sxs-lookup"><span data-stu-id="08703-110">ADSI defines its own syntax that maps to the native directory syntax.</span></span> <span data-ttu-id="08703-111">本節說明 ADSI 中的屬性語法類型。</span><span class="sxs-lookup"><span data-stu-id="08703-111">This section describes the types of attribute syntaxes in ADSI.</span></span>

## <a name="distinguished-name-string"></a><span data-ttu-id="08703-112">辨別名稱字串</span><span class="sxs-lookup"><span data-stu-id="08703-112">Distinguished Name String</span></span>


```VB
Syntax Type: ADSTYPE_DN_STRING
```



<span data-ttu-id="08703-113">辨別名稱適用于將兩個物件連結在一起。</span><span class="sxs-lookup"><span data-stu-id="08703-113">The distinguished name is useful for linking two objects together.</span></span> <span data-ttu-id="08703-114">例如，它可以建立一個連結，讓 Alice 物件成為 Bob 物件的管理員。</span><span class="sxs-lookup"><span data-stu-id="08703-114">For example, it can create a link that makes the Alice object a manager of the Bob object.</span></span> <span data-ttu-id="08703-115">如果 Alice 物件移至不同的位置，則 Alice 和 Bob 之間的管理員連結會自動更新。</span><span class="sxs-lookup"><span data-stu-id="08703-115">If the Alice object moves to different place, the manager link between Alice and Bob is updated automatically.</span></span>

<span data-ttu-id="08703-116">辨別名稱必須包含有效的辨別名稱物件。</span><span class="sxs-lookup"><span data-stu-id="08703-116">The distinguished name must contain a valid distinguished name object.</span></span> <span data-ttu-id="08703-117">如果辨別名稱未對應到有效的現有物件，大部分的伺服器會拒絕要求並傳回條件約束違規錯誤。</span><span class="sxs-lookup"><span data-stu-id="08703-117">If the distinguished name does not correspond to a valid existing object, most servers reject the request and return a constraint violation error.</span></span>

<span data-ttu-id="08703-118">範例：</span><span class="sxs-lookup"><span data-stu-id="08703-118">Examples:</span></span>


```VB
Set x = GetObject("LDAP://CN=Bob, OU=Sales,DC=Fabrikam, DC=com)
x.Put "manager", "CN=Alice, OU=Sales, DC=Fabrikam, DC=COM"
x.SetInfo
 
PADS_ATTR_INFO pInfo;
// .. IDirectoryObject::GetObjectAttribute
printf("%S\n", pInfo->pADsValues->DNString );
```



## <a name="case-exact-string-and-case-ignore-string"></a><span data-ttu-id="08703-119">Case 精確字串和 Case 忽略字串</span><span class="sxs-lookup"><span data-stu-id="08703-119">Case Exact String and Case Ignore String</span></span>


```VB
Syntax Types: ADSTYPE_CASE_IGNORE_STRING, ADSTYPE_CASE_EXACT_STRING.
```



<span data-ttu-id="08703-120">Case 精確字串為區分大小寫的字串，而 Case Ignore 字串則是不區分大小寫的字串。</span><span class="sxs-lookup"><span data-stu-id="08703-120">Case Exact String is a case-sensitive string while Case Ignore String is a case-insensitive string.</span></span> <span data-ttu-id="08703-121">目錄中的屬性百分比很大，使用此語法。</span><span class="sxs-lookup"><span data-stu-id="08703-121">A large percentage of attributes in the directory use this syntax.</span></span>

> [!Note]  
> <span data-ttu-id="08703-122">目錄不一定會將其儲存為 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="08703-122">The directory may or may not store this as a Unicode string.</span></span> <span data-ttu-id="08703-123">但是，ADSI 會接受並傳回 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="08703-123">However, ADSI accepts and returns Unicode strings.</span></span>

 

<span data-ttu-id="08703-124">範例：</span><span class="sxs-lookup"><span data-stu-id="08703-124">Example:</span></span>


```VB
Dim propList As IADsPropertyList
Set propList = GetObject("LDAP://DC=Fabrikam,DC=com")
Set propVal = New PropertyValue
 
' --- Property Value ---
propVal.CaseIgnoreString = "Fabrikam, Inc - Seattle, WA"
propVal.ADsType = ADSTYPE_CASE_IGNORE_STRING
```



## <a name="printable-string"></a><span data-ttu-id="08703-125">可列印字串</span><span class="sxs-lookup"><span data-stu-id="08703-125">Printable String</span></span>


```VB
Syntax Type: ADSTYPE_PRINTABLE_STRING
```



<span data-ttu-id="08703-126">此語法適用于具有字串值的屬性，其中大寫和小寫會視為不相等的比較，例如 "FABRIKAM" 和 "Fabrikam" 不相符。</span><span class="sxs-lookup"><span data-stu-id="08703-126">This syntax is used for attributes with string values where uppercase and lowercase are considered unequal for comparisons, for example, "FABRIKAM" and "Fabrikam" do not match.</span></span> <span data-ttu-id="08703-127">ADSI 接受可列印字串的任何內容;它不會嘗試確認它們確實可以列印。</span><span class="sxs-lookup"><span data-stu-id="08703-127">ADSI accepts any contents for a Printable-String; it does not attempt to verify that they are indeed printable.</span></span>

## <a name="numeric-string"></a><span data-ttu-id="08703-128">數值字串</span><span class="sxs-lookup"><span data-stu-id="08703-128">Numeric String</span></span>


```VB
Syntax Type: ADSTYPE_NUMERIC_STRING
```



<span data-ttu-id="08703-129">在這個語法中，字串會與可列印的字串比對，但在比較中會忽略所有空白字元。</span><span class="sxs-lookup"><span data-stu-id="08703-129">In this syntax, strings match as in Printable String, except that all space characters are ignored in comparisons.</span></span> <span data-ttu-id="08703-130">ADSI 不會執行值檢查，以確保只會在此語法的值中顯示數位和空格。</span><span class="sxs-lookup"><span data-stu-id="08703-130">ADSI does not perform value checking to ensure that only numerals and spaces appear in values of this syntax.</span></span> <span data-ttu-id="08703-131">Active Directory 接受數值字串的任何內容;它不會驗證字元是否為數值。</span><span class="sxs-lookup"><span data-stu-id="08703-131">Active Directory accepts any content for a numeric string; it does not verify that the characters are numeric.</span></span>

## <a name="utc-time"></a><span data-ttu-id="08703-132">UTC 時間</span><span class="sxs-lookup"><span data-stu-id="08703-132">UTC Time</span></span>


```VB
Syntax Type: ADSTYPE_UTC_TIME
```



<span data-ttu-id="08703-133">此語法會將日期和時間儲存在單一字串中。</span><span class="sxs-lookup"><span data-stu-id="08703-133">This syntax stores the date and time in a single string.</span></span> <span data-ttu-id="08703-134">字串格式由三個串連的部分組成： (1) YYMMDD; (2) HHMM 或 HHMMSS (都可接受) ;和 (3) "Z" 表示指定的時間是格林威治標準時間 (GMT) ，或 "+/-HHMM" 表示指定的時間是當地時間，與 GMT 的指定差異。</span><span class="sxs-lookup"><span data-stu-id="08703-134">The string format consists of three concatenated parts: (1) YYMMDD; (2) HHMM or HHMMSS (both are acceptable); and (3) "Z" to indicate that the time given is Greenwich Mean Time (GMT), or "+/-HHMM" to indicate that the time given is local time with the given differential from GMT.</span></span> <span data-ttu-id="08703-135">差異是以公式： GMT = Local + 差異為基礎。</span><span class="sxs-lookup"><span data-stu-id="08703-135">The differential is based on the formula: GMT=Local+differential.</span></span>

> [!Note]  
> <span data-ttu-id="08703-136">年份的前兩個數字不會儲存在此字串中。</span><span class="sxs-lookup"><span data-stu-id="08703-136">The first two digits of the year are not stored in this string.</span></span>

 

<span data-ttu-id="08703-137">合法值的一些範例包括 "9101311455Z"、"910131145503Z"、"9101314455-0500"、"910131145503 + 0130"。</span><span class="sxs-lookup"><span data-stu-id="08703-137">Some examples of legal values are "9101311455Z", "910131145503Z", "9101314455-0500", "910131145503+0130".</span></span> <span data-ttu-id="08703-138">這個字串會儲存為單一位元組 ASCII 字元，且不會儲存任何字碼頁編號。</span><span class="sxs-lookup"><span data-stu-id="08703-138">This string is stored as single-byte ASCII characters, and no code page number is stored with it.</span></span>

<span data-ttu-id="08703-139">雖然支援排序，但是只會以 ASCII 不區分大小寫的字串排序來完成，而不是正確地解讀字串的意義。</span><span class="sxs-lookup"><span data-stu-id="08703-139">Although ordering is supported, it is done only as an ASCII case-insensitive string sort, not by properly interpreting the meaning of the strings.</span></span>

<span data-ttu-id="08703-140">接受任何有效的字串值。</span><span class="sxs-lookup"><span data-stu-id="08703-140">Any valid string value is accepted.</span></span> <span data-ttu-id="08703-141">不嘗試確定字串包含有效的時間字串。</span><span class="sxs-lookup"><span data-stu-id="08703-141">No attempt is made to ensure that the string contains a valid time string.</span></span>

## <a name="generalized-time"></a><span data-ttu-id="08703-142">一般化時間</span><span class="sxs-lookup"><span data-stu-id="08703-142">Generalized Time</span></span>


```VB
Syntax Type: ADSTYPE_UTC_TIME
```



<span data-ttu-id="08703-143">如果要定義用來儲存時間值的新屬性，則應該使用 GeneralizedTime 語法。</span><span class="sxs-lookup"><span data-stu-id="08703-143">If a new attribute to store time values is being defined, the GeneralizedTime syntax should be used.</span></span> <span data-ttu-id="08703-144">GeneralizedTime 語法使用四個字元來代表年份，而不是使用 UTCTime 的兩個字元。</span><span class="sxs-lookup"><span data-stu-id="08703-144">GeneralizedTime syntax uses four characters to represent the year instead of two as with UTCTime.</span></span>

<span data-ttu-id="08703-145">GeneralizedTime 語法的格式為 "YYYYMMDDHHMMSS.FFFFFF. 0Z"。</span><span class="sxs-lookup"><span data-stu-id="08703-145">The format for the GeneralizedTime syntax is "YYYYMMDDHHMMSS.0Z".</span></span> <span data-ttu-id="08703-146">可接受值的範例是「20010928060000.0 Z」。</span><span class="sxs-lookup"><span data-stu-id="08703-146">An example of an acceptable value is "20010928060000.0Z".</span></span> <span data-ttu-id="08703-147">"Z" 表示沒有時間差異。</span><span class="sxs-lookup"><span data-stu-id="08703-147">The "Z" indicates no time differential.</span></span> <span data-ttu-id="08703-148">Active Directory 將日期/時間儲存為格林威治標準時間 (GMT) 。</span><span class="sxs-lookup"><span data-stu-id="08703-148">Active Directory stores date/time as Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="08703-149">如果未指定時間差異，則預設值為 GMT。</span><span class="sxs-lookup"><span data-stu-id="08703-149">If no time differential is specified, GMT is the default.</span></span>

<span data-ttu-id="08703-150">如果時間是在 GMT 以外的時區中指定，則時區與 gmt 之間的差異會附加至字串，而不是 "yyyymmddhhmmss.ffffff. 0 HHMM" 格式的 "Z" \[ +/- \] 。</span><span class="sxs-lookup"><span data-stu-id="08703-150">If the time is specified in a time zone other than GMT, the differential between the time zone and GMT is appended to the string instead of "Z" in the form "YYYYMMDDHHMMSS.0\[+/-\]HHMM".</span></span> <span data-ttu-id="08703-151">可接受值的範例是 "20010928060000.0 + 0200"。</span><span class="sxs-lookup"><span data-stu-id="08703-151">An example of an acceptable value is "20010928060000.0+0200".</span></span>

<span data-ttu-id="08703-152">差異是以公式： GMT = Local + 差異為基礎。</span><span class="sxs-lookup"><span data-stu-id="08703-152">The differential is based on the formula: GMT=Local+differential.</span></span>

## <a name="boolean"></a><span data-ttu-id="08703-153">Boolean</span><span class="sxs-lookup"><span data-stu-id="08703-153">Boolean</span></span>


```VB
Syntax Type: ADSTYPE_BOOLEAN
```



<span data-ttu-id="08703-154">Active Directory 只接受此語法的帶正負號32位值。</span><span class="sxs-lookup"><span data-stu-id="08703-154">Active Directory accepts only a signed 32-bit value for this syntax.</span></span> <span data-ttu-id="08703-155">它會將零視為 **FALSE** ，並將所有非零值處理為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="08703-155">It handles zero as **FALSE** and all nonzero values as **TRUE**.</span></span>

## <a name="integer"></a><span data-ttu-id="08703-156">整數</span><span class="sxs-lookup"><span data-stu-id="08703-156">Integer</span></span>


```VB
Syntax Type: ADSTYPE_INTEGER
```



<span data-ttu-id="08703-157">32位帶正負號的數位值。</span><span class="sxs-lookup"><span data-stu-id="08703-157">A 32-bit signed numeric value.</span></span>

## <a name="large-integer"></a><span data-ttu-id="08703-158">大型整數</span><span class="sxs-lookup"><span data-stu-id="08703-158">Large Integer</span></span>


```VB
Syntax Type: ADSTYPE_LARGE_INTEGER
```



<span data-ttu-id="08703-159">64位帶正負號的數位值。</span><span class="sxs-lookup"><span data-stu-id="08703-159">A 64-bit signed numeric value.</span></span> <span data-ttu-id="08703-160">大型整數實際上實作為 [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) 介面上的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="08703-160">Large integers are actually implemented as COM objects on the [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) interface.</span></span> <span data-ttu-id="08703-161">**HighPart** 和 **LowPart** 方法是用來存取大整數值的 2 32 位部分。</span><span class="sxs-lookup"><span data-stu-id="08703-161">The **HighPart** and **LowPart** methods are used to access the two 32-bit halves of the large integer value.</span></span>

<span data-ttu-id="08703-162">範例：</span><span class="sxs-lookup"><span data-stu-id="08703-162">Example:</span></span>


```VB
Dim x as IADsLargeInteger
Set o = GetObject("LDAP://DC=Fabrikam,DC=com")
Set x = o.Get("UsnCreated")
Debug.Print x.HighPart
Debug.Print x.LowPart
```



## <a name="octet-string"></a><span data-ttu-id="08703-163">八位字串</span><span class="sxs-lookup"><span data-stu-id="08703-163">Octet String</span></span>


```VB
Syntax Type: ADSTYPE_OCTET_STRING
```



<span data-ttu-id="08703-164">八進位字串會以位元組的變異陣列傳回。</span><span class="sxs-lookup"><span data-stu-id="08703-164">An octet string is returned as a variant array of bytes.</span></span> <span data-ttu-id="08703-165">這包括大小 (八位數) ，後面接著一系列八位。</span><span class="sxs-lookup"><span data-stu-id="08703-165">This consists of a size count (number of octets) followed by a series of octets.</span></span> <span data-ttu-id="08703-166">八位為8位位元組，因此一連串的八位是二進位資料的字串。</span><span class="sxs-lookup"><span data-stu-id="08703-166">An octet is an 8-bit byte, so a series of octets is a string of binary data.</span></span>

## <a name="object-class"></a><span data-ttu-id="08703-167">物件類別</span><span class="sxs-lookup"><span data-stu-id="08703-167">Object Class</span></span>


```VB
Syntax Type: ADSTYPE_CASE_IGNORE_STRING
```



<span data-ttu-id="08703-168">Object 類別是指定之架構類別的唯一物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="08703-168">Object Class is a unique object identifier for a given schema class.</span></span> <span data-ttu-id="08703-169">每個物件實例的類別都是由 **objectClass** 屬性來識別。</span><span class="sxs-lookup"><span data-stu-id="08703-169">The class of each object instance is identified by the **objectClass** attribute.</span></span> <span data-ttu-id="08703-170">建立時，您永遠不能變更物件類別。</span><span class="sxs-lookup"><span data-stu-id="08703-170">When created, you can never change an object class.</span></span> <span data-ttu-id="08703-171">**objectClass** 是多重值屬性。</span><span class="sxs-lookup"><span data-stu-id="08703-171">**objectClass** is a multiple valued attribute.</span></span> <span data-ttu-id="08703-172">它會列出物件的特定類別，以及衍生特定類別之所有結構化或抽象類別類別的類別。</span><span class="sxs-lookup"><span data-stu-id="08703-172">It lists the specific class of the object, and the classes of all structural or abstract classes from which the specific class was derived.</span></span> <span data-ttu-id="08703-173">這包括 Top，也就是所有其他類別最終衍生的類別。</span><span class="sxs-lookup"><span data-stu-id="08703-173">This includes Top, the class from which all other classes are ultimately derived.</span></span> <span data-ttu-id="08703-174">Active Directory 不會列出 **objectClass** 屬性中的輔助類別。</span><span class="sxs-lookup"><span data-stu-id="08703-174">Active Directory does not list auxiliary classes in the **objectClass** attribute.</span></span>

## <a name="security-descriptor"></a><span data-ttu-id="08703-175">安全性描述元</span><span class="sxs-lookup"><span data-stu-id="08703-175">Security Descriptor</span></span>


```VB
Syntax Type: ADSTYPE_NT_SECURITY_DESCRIPTOR
```



<span data-ttu-id="08703-176">存取權限會定義安全性主體嘗試對 Active Directory 物件執行作業時的功能。</span><span class="sxs-lookup"><span data-stu-id="08703-176">Access rights define what abilities a security principal has when it attempts to perform an operation on an Active Directory object.</span></span> <span data-ttu-id="08703-177">安全描述項描述與物件相關聯的存取控制資訊。</span><span class="sxs-lookup"><span data-stu-id="08703-177">A security descriptor describes the access control information associated with an object.</span></span>

<span data-ttu-id="08703-178">在 **nTSecurityDescriptor** 屬性中，安全描述項會儲存為目錄物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="08703-178">The security descriptor is stored as a property of a directory object in the **nTSecurityDescriptor** property.</span></span> <span data-ttu-id="08703-179">當已驗證的使用者嘗試存取目錄物件時，目錄伺服器會根據物件安全描述項，判斷授與或拒絕使用者的存取權。</span><span class="sxs-lookup"><span data-stu-id="08703-179">When an authenticated user attempts to access a directory object, the directory server determines the access granted or denied to the user based on the object security descriptor.</span></span>

<span data-ttu-id="08703-180">[**ADS \_ SD \_ CONTROL \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_sd_control_enum)列舉會指定安全描述項的控制旗標。</span><span class="sxs-lookup"><span data-stu-id="08703-180">The [**ADS\_SD\_CONTROL\_ENUM**](/windows/win32/api/iads/ne-iads-ads_sd_control_enum) enumeration specifies control flags for a security descriptor.</span></span>

<span data-ttu-id="08703-181">下列程式碼範例顯示如何取得安全描述項。</span><span class="sxs-lookup"><span data-stu-id="08703-181">The following code example shows how to obtain a security descriptor.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="08703-182">相關主題</span><span class="sxs-lookup"><span data-stu-id="08703-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08703-183">Active Directory 屬性的語法</span><span class="sxs-lookup"><span data-stu-id="08703-183">Syntaxes for Active Directory Attributes</span></span>](/windows/desktop/AD/syntaxes-for-attributes-in-active-directory-domain-services)
</dt> <dt>

[<span data-ttu-id="08703-184">選擇語法</span><span class="sxs-lookup"><span data-stu-id="08703-184">Choosing a Syntax</span></span>](/windows/desktop/AD/choosing-a-syntax)
</dt> <dt>

[<span data-ttu-id="08703-185">如何指定比較值</span><span class="sxs-lookup"><span data-stu-id="08703-185">How to Specify Comparison Values</span></span>](/windows/desktop/AD/how-to-specify-comparison-values)
</dt> </dl>

 

 