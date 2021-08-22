---
description: 提供將 WMI 類別對應至 Active Directory 的規則。
ms.assetid: 295d3233-5729-4eb0-9fa3-1cf64fef2909
ms.tgt_platform: multiple
title: 對應 Active Directory 類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc38e91d52b59a206a0b64465d0f9710f6d515c9487853824477b7f4f6a126aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992898"
---
# <a name="mapping-active-directory-classes"></a>對應 Active Directory 類別

由於 Active Directory 有各種可能的物件，因此 WMI 無法建立直接的一對一對應。 相反地，目錄服務提供者會使用規則來對應兩個技術之間的類別。

本主題將討論下列各節：

-   [對應類別](#mapping-classes)
-   [對應屬性](#mapping-attributes)
-   [關聯類別](#association-classes)

> [!Note]  
> 如需有關在特定作業系統上支援和安裝此元件的詳細資訊，請參閱 [WMI 元件的作業系統可用性](operating-system-availability-of-wmi-components.md)。

 

## <a name="mapping-classes"></a>對應類別

下列清單描述目錄服務提供者用來將 Active Directory 類別對應至 WMI 類別的指導方針：

-   Active Directory 架構中的每個抽象類別都會對應至 WMI 架構中的一個抽象類別。

    在 WMI 架構中，每個抽象類別的前面都會加上 DS \_ 。 例如，Active Directory 架構中的 **person** 類別會對應到 **DS \_ person** WMI 類別。

-   Active Directory 架構中的每個非抽象類別別都會對應至 WMI 架構中的下列兩個類別：

    -   第一個對應的類別前面會加上 ADS \_ 。 這些是抽象類別，根據下列規則進行對應。
    -   第二個對應類別是具有 DS 名稱前置詞的非抽象類別別 \_ 。 此類別衍生自 ADS \_ 抽象類別，並加入了 [**提供者**](/windows/desktop/api/Provider/nl-provider-provider) 辨識符號。

    例如，Active Directory 架構中的 **user** 類別會對應到兩個類別。 第一個類別是 **ADS \_ 使用者** 抽象類別，根據下列規則進行對應。 第二個類別是 **DS \_ 使用者** 非抽象類別別。 它衍生自 **ADS \_ 使用者** ，並具有新增的 [**提供者**](/windows/desktop/api/Provider/nl-provider-provider) 辨識符號。

-   除非另有指定，否則對應類別的名稱是 Active Directory 類別中 **LDAP 顯示名稱** 屬性的已損壞值。
-   如果 Active Directory 類別上有 **子類別的** 屬性，則 WMI 對應的類別會衍生自指定的類別。

    如果不存在 **子類別的** 屬性，則 WMI 對應類別會衍生自「 **DS \_ LDAP \_ 根 \_ 類別** 」類別，如 MOF 檔案中所指定。

    > [!Note]  
    > 此類別具有 **ADSIPath** 索引鍵屬性，其類型為 **VT \_ BSTR**。 這是識別此實例的唯一 ADSI 路徑。 Active Directory 僅支援單一繼承，因此可正常運作。

     

-   會為每個類別建立 **VT \_ BOOL** 類型的 **動態** 限定詞，並 `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` 設定為 **TRUE** 。 這是標準的 WMI 辨識符號，表示會動態提供這個類別的實例。
-   如果類別不是抽象的，則提供者會為每個類別建立類型為 **VT \_ BSTR BOOL** 的 [**提供者**](/windows/desktop/api/Provider/nl-provider-provider)辨識符號，以及 `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` 設定為 "DS Instance provider" 的辨識符號。 這是標準的 WMI 辨識符號，表示提供者的名稱會動態提供這個類別的實例。

ADSI 屬性的其餘部分會根據下列資料表對應至類別限定詞和屬性。 具有限定詞旗標值的所有限定詞對應 `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` 。

以下列出 Active Directory 類別的對應資訊，其中顯示每個 Active Directory 屬性的 WMI 辨識符號和 WMI 辨識符號類型。

<dl> <dt>

**一般名稱**
</dt> <dd>

**CN** (**VT \_ BSTR**) 

直接從字串值對應。

</dd> <dt>

**預設-物件-類別**
</dt> <dd>

**DefaultObjectCategory** (**VT \_ BSTR**) 

直接從字串值對應。

</dd> <dt>

**預設-安全性-描述元**
</dt> <dd>

**DefaultSecurityDescriptor** (**VT \_ BSTR**) 

直接從字串值對應。

</dd> <dt>

**控管-識別碼**
</dt> <dd>

**GovernsId** (**VT \_ BSTR**) 

從 OID 的字串表示進行對應;例如，"{1 3 3 6}"。

</dd> <dt>

**物件類別**
</dt> <dd>

N/A

未對應。

</dd> <dt>

**物件類別-類別目錄**
</dt> <dd>

**ObjectClassCategory** (**VT \_ I4**) 

直接從整數值對應。 此外，如果此值為 Abstract (2) ，則也會建立標準 **VT \_ BOOL** CIM 辨識符號（稱為「 **抽象** 」限定詞）。

</dd> <dt>

**RDN-ATT-ID**
</dt> <dd>

**RDNATTID** (**VT \_ BSTR**) 

從 OID 值的字串標記法對應;例如，"{1 3 3 6}"。 此外，此處識別的屬性會標注標準的 **索引** CIM 辨識符號設定為 **TRUE**。

</dd> <dt>

**僅限系統**
</dt> <dd>

**SystemOnly** (**VT \_ BOOL**) 

直接從布林值對應。

</dd> </dl>

 

以下列出對應至 WMI 類別屬性的 Active Directory 類別屬性。

<dl> <dt>

**可能包含**
</dt> <dd>

此清單中的每個屬性都會對應至 WMI 屬性。

</dd> <dt>

**必須包含**
</dt> <dd>

此清單中的每個屬性都會對應至 WMI 屬性。 這每一個都是針對上述各項建立標準 **非 \_ Null** CIM 限定詞。

</dd> <dt>

**系統-可能包含**
</dt> <dd>

此清單中的每個屬性都會對應至 WMI 屬性。 此外，每個屬性都會以 **系統** 限定詞標注，設定為 **TRUE**。

</dd> <dt>

**系統-必須包含**
</dt> <dd>

此清單中的每個屬性都會對應至 WMI 屬性。 這每一個都是針對上述各項建立標準 **非 \_ Null** CIM 限定詞。 此外，每個屬性都會以 **系統** 限定詞標注，設定為 **TRUE**。

</dd> </dl>

## <a name="mapping-attributes"></a>對應屬性

目錄服務提供者會根據本節中的規則，將 Active Directory 類別的每個屬性對應到相對應 WMI 類別的一個屬性。 一般情況下，目錄服務提供者會將 WMI 屬性命名為 Active Directory 屬性的 **LDAP 顯示名稱** 值的損壞版本。

如果 Active Directory 屬性 **為-單一值** 為 **FALSE**，則此 WMI 屬性會與 OR 運算子結合 **CIM 旗標 \_ \_ 陣列**。 請注意，每個屬性都會以 **VT \_ BSTR** 辨識符號（ **ADSyntax**）標記。 它代表基礎 Active Directory 語法。

下表列出 Active Directory 語法與 WMI 屬性資料類型的對應。



| Active Directory 元素                                      | WMI 資料類型                                                           |
|---------------------------------------------------------------|-------------------------------------------------------------------------|
| [**存取點**](/windows/desktop/ADSchema/s-object-access-point)            | **CIM \_ 字串**                                                         |
| [**Boolean**](/windows/desktop/ADSchema/s-boolean)                             | **CIM \_ 布林值**                                                        |
| **不區分大小寫的字串**                                   | **CIM \_ 字串**                                                         |
| [**區分大小寫的字串**](/windows/desktop/ADSchema/s-string-case-sensitive) | **CIM \_ 字串**                                                         |
| [**辨別名稱**](/windows/desktop/ADSchema/s-object-ds-dn)             | **CIM \_ 字串**                                                         |
| [**DN-二進位**](/windows/desktop/ADSchema/s-object-dn-binary)                  | 類別 DN 的內嵌 **物件 \_ ， \_** 定義如下的二進位檔。<br/> |
| [**DN-字串**](/windows/desktop/ADSchema/s-object-dn-string)                  | 類別 DN 的內嵌 **物件 \_ ， \_ 具有** 以下定義的字串。<br/> |
| [**列舉型別**](/windows/desktop/ADSchema/s-enumeration)                     | **CIM \_ SINT32**                                                         |
| [**列舉型別**](/windows/desktop/ADSchema/s-enumeration)                     | **CIM \_ 字串**                                                         |
| [**整數**](/windows/desktop/ADSchema/s-integer)                             | **CIM \_ SINT32**                                                         |
| [**LargeInteger**](/windows/desktop/ADSchema/s-largeinteger)                   | **CIM \_ 字串**                                                         |
| 安全性描述元                                           | 以下定義之類別 **Uint8Array** 的内嵌物件。<br/>       |
| 數值字串                                                | **CIM \_ 字串**                                                         |
| 物件識別碼                                                     | **CIM \_ 字串**                                                         |
| 八位字串                                                  | 以下定義之類別 **Uint8Array** 的内嵌物件。<br/>       |
| 或名稱                                                       | **CIM \_ 字串**                                                         |
| Presentation-Address                                          | 以下定義之類別 **Uint8Array** 的内嵌物件。<br/>       |
| 列印案例字串                                             | **CIM \_ 字串**                                                         |
| 複本連結                                                  | 以下定義之類別 **Uint8Array** 的内嵌物件。<br/>       |
| [**(Sid) 的字串**](/windows/desktop/ADSchema/s-string-sid)                      | 以下定義之類別 **Uint8Array** 的内嵌物件。<br/>       |
| 時間                                                          | **CIM \_ DATETIME**                                                       |
| UTC 編碼時間                                                | **CIM \_ DATETIME**                                                       |
| Unicode 字串                                                | **CIM \_ 字串**                                                         |



 

八位字串語法（參考 **uint8** 值的陣列）會在對應至 WMI 時呈現問題，因為 wmi 允許 **uint8** 類型的屬性和 **uint8** 的陣列，而 Active Directory 則允許類型為八進位字串的屬性，以及八位字串的陣列。

下列範例顯示的目錄服務提供者類別，用來對應八位字串型別屬性的陣列。

``` syntax
Class Uint8Array 
{
    uint8 values[];
    uint32 numberOfValues;
};
```

WMI 會將所有的八位字串 Active Directory 屬性值對應至 **Uint8Array** 的內嵌實例。 同樣地，WMI 會將八位字串的陣列對應至內嵌 **Uint8Array** 物件的陣列。

下列範例顯示 WMI 對應的類別，以 DN-Binary 和 DN-String DS 屬性值。

``` syntax
Class DN_With_String
{
    string dnString;
    string value;
};

Class DN_With_Binary
{
    string dnString;
    uint8 value[];
};
```

下表列出 WMI 如何將 Active Directory 屬性介面屬性的其餘部分對應至 WMI 屬性限定詞。



| Active Directory 屬性-屬性名稱 | WMI 辨識符號       | 資料類型    | 對應資訊                               |
|------------------------------------------|---------------------|--------------|---------------------------------------------------|
| **屬性語法**                     | **AttributeSyntax** | **VT \_ BSTR** | 從 OID 的字串表示進行對應。 |
| **一般名稱**                          | **CN**              | **VT \_ BSTR** | 從字串值對應。                     |
| **僅限系統**                          | **系統**          | **VT \_ BOOL** | 從布林值對應。                    |



 

> [!Note]  
> WMI 會將所有 Active Directory 限定詞對應到辨識符號的類別 `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` 。

 

## <a name="association-classes"></a>關聯類別

目錄服務基本上是物件的階層式存放區。 這些物件可以出現在階層中的非分葉層級上，稱為「容器」。 此階層的結構會進一步由架構中類別的 "Poss-Superiors" 和 "Poss-Superiors" 屬性控制。 這些會一起建立，並指定一組類別，其實例可以包含在容器類別的實例中。

下列範例會將 CIM 關聯模型為靜態關聯類別的 [**DS \_ LDAP \_ 類別 \_**](/previous-versions/windows/desktop/dsprov/ds-ldap-class-containment)內含專案的實例。

``` syntax
//  DS Class Associations Provider 

// Create a class of which instances are
// provided by this provider

[
  Association : ToInstance,
  dynamic,
  HasClassRefs,
  Provider("Microsoft|DSLDAPClassAssociationProvider|V1.0")
]
class DS_LDAP_Class_Containment
{
    [key, classref{"DS_LDAP_Root_Class"} : ToInstance ToSubClass]
    object Ref ChildClass;

    [key, classref{"DS_LDAP_Root_Class"} : ToInstance ToSubClass] 
    object Ref ParentClass; // The parent DS Class
};


// Create an instance of the provider class for registration
instance of __Win32Provider as $AssociationsProvider
{
    Name = "Microsoft|DSLDAPClassAssociationProvider|V1.0";
    Clsid = "{33831ED4-42B8-11d2-93AD-00805F853771}";
    ImpersonationLevel = 1;
};    

// Specification of the instances and operation
// provided by the provider
instance of __InstanceProviderRegistration
{
    Provider = $AssociationsProvider;
    SupportsGet = TRUE;
    SupportsPut = FALSE;
    SupportsDelete = FALSE;
    SupportsEnumeration = TRUE;
};
```

Association 類別提供者支援 [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) 和 [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) 方法。

 

