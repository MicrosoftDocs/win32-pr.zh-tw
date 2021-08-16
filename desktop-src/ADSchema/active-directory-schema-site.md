---
title: Active Directory 架構術語
description: 下列詞彙通常是用來參考 Active Directory 架構。
ms.assetid: 22c5756f-d663-4cb7-aab0-956b22a01e9d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2b48256d1df8f9c344fe0acceb2fb6a70ed3033260baea4db7df44dd71e1c3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117836434"
---
# <a name="active-directory-schema-terminology"></a>Active Directory 架構術語

下列詞彙通常是用來參考 Active Directory 架構。


<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>屬性
</dt> <dd>

用來描述架構中所定義之類別所代表之物件的資料項目。 屬性是在架構中與類別分開定義;這可讓您將單一屬性定義套用至許多類別。 例如， [**Description**](a-description.md) 是可套用至架構中任何類別的屬性。 **Description** 屬性會在架構中定義一次，以確保一致性，而不是對使用者的 **描述** 和印表機 **描述** 具有不同的定義。

> [!Note]  
> Term *屬性* 通常會與 term *屬性* 交換使用。

 

</dd> <dt>

<span id="Attribute_Instance"></span><span id="attribute_instance"></span><span id="ATTRIBUTE_INSTANCE"></span>屬性實例
</dt> <dd>

架構中所定義之屬性的出現位置。 這個詞彙是用來區別屬性的定義和屬性的離散出現。 例如，儲存 "Jeff Smith" 的使用者物件，並將 [**Common name**](a-cn.md) 屬性設定為 "jeff smith"，就會建立 [**共同名稱**](a-cn.md)的實例。

</dd> <dt>

<span id="Class"></span><span id="class"></span><span id="CLASS"></span>類
</dt> <dd>

目錄服務中所儲存之離散、可識別類型之物件的正式描述。 例如， [**使用者**](c-user.md)、 [**列印佇列**](c-printqueue.md)和 [**群組**](c-group.md) 都是類別。 此外，還有三個不同類別的類別： [結構化類別](classes-structural.md)、 [抽象類別](classes-abstract.md)和 [輔助類別](classes-auxiliary.md)。

</dd> <dt>

<span id="Class_Instance"></span><span id="class_instance"></span><span id="CLASS_INSTANCE"></span>類別實例
</dt> <dd>

架構中所定義之類別的出現位置。 這個詞彙是用來區分類別的定義和個別出現的類別。 例如，在目錄服務中儲存 "Jeff Smith" 的 [**使用者**](c-user.md) 物件時，會建立 [**使用者**](c-user.md)的實例。

</dd> <dt>

<span id="Content_Rules"></span><span id="content_rules"></span><span id="CONTENT_RULES"></span>內容規則
</dt> <dd>

目錄服務中儲存之類別實例的可能內容定義。 在 NT 目錄服務中 (NTDS) ，在 Active Directory 為基礎時，內容規則會以每個類別之架構定義的 [ [**必須包含**](a-mustcontain.md) ] 和 [ [**可能-包含**](a-maycontain.md) ] 屬性完全表示。

</dd> <dt>

<span id="Derivation"></span><span id="derivation"></span><span id="DERIVATION"></span>推導
</dt> <dd>

請參閱 *繼承*。

</dd> <dt>

<span id="Directory_Information_Tree"></span><span id="directory_information_tree"></span><span id="DIRECTORY_INFORMATION_TREE"></span>目錄資訊樹狀目錄
</dt> <dd>

目錄本身，以樹狀結構表示，其中頂點是 (類別實例的目錄專案) ，而連接線則是專案之間的父子式關聯性。

</dd> <dt>

<span id="DIT"></span><span id="dit"></span>DIT
</dt> <dd>

請參閱 *目錄資訊樹狀目錄*。

</dd> <dt>

<span id="Control_Access_Rights"></span><span id="control_access_rights"></span><span id="CONTROL_ACCESS_RIGHTS"></span>控制存取權限
</dt> <dd>

類別，描述未系結至資源但動作的存取權。 例如，可以授與使用者建立相對識別碼值的許可權。

</dd> <dt>

<span id="Inheritance"></span><span id="inheritance"></span><span id="INHERITANCE"></span>繼承
</dt> <dd>

能夠從現有的物件類別建立新的物件類別。 新物件會定義為父物件的子 *類別* 。 父物件變成新物件的 *超級類別* 。 子類別會繼承父系的屬性，包括結構規則和內容規則。

</dd> <dt>

<span id="LDAP"></span><span id="ldap"></span>LDAP
</dt> <dd>

請參閱 *輕量型目錄存取協定*。

</dd> <dt>

<span id="Lightweight_Directory_Access_Protocol"></span><span id="lightweight_directory_access_protocol"></span><span id="LIGHTWEIGHT_DIRECTORY_ACCESS_PROTOCOL"></span>輕量型目錄存取協定
</dt> <dd>

用來與 NTDS 通訊的標準網際網路通訊協定。 支援 LDAP 第2版和第3版。

</dd> <dt>

<span id="NT_Security_Descriptor"></span><span id="nt_security_descriptor"></span><span id="NT_SECURITY_DESCRIPTOR"></span>NT 安全描述項
</dt> <dd>

請參閱 *安全描述項*。

</dd> <dt>

<span id="Object"></span><span id="object"></span><span id="OBJECT"></span>物件
</dt> <dd>

目錄服務中的資料儲存體單位。 目錄服務物件不會與 COM 物件或其他具有可執行元件和執行時間行為的物件導向系統物件混淆。 目錄服務物件僅包含資料。 目錄服務物件是由類別 [**架構**](c-classschema.md)物件和 [**類別架構**](c-classschema.md)物件所參考的一組 [**屬性架構**](c-attributeschema.md)物件所定義。

[**類別架構**](c-classschema.md) 和 [**屬性架構**](c-attributeschema.md) 物件本身是目錄服務物件，且架構中的定義與任何其他物件一樣。 請參閱 *類別*。

</dd> <dt>

<span id="Object_Identifier"></span><span id="object_identifier"></span><span id="OBJECT_IDENTIFIER"></span>物件識別碼
</dt> <dd>

由各種發行授權單位所發行的唯一數值，可唯一識別資料元素、語法，以及分散式應用程式的各種其他部分。 在 OSI 應用程式、x.500 目錄、SNMP 和其他重要的應用程式中，都可以找到 (Oid) 的物件識別碼。 Oid 是以樹狀結構為基礎，在此結構中，較高的發行授權單位（例如 ISO）會將樹狀結構的分支配置給子授權單位，進而配置子分支。

NTDS 中的 Oid 包括由 ISO 針對 X. 500 類別和屬性簽發的部分，以及某些由 Microsoft 發出的 Oid。 OID 標記法是數位的點字串，例如 "1.2.840.113556.1.5.4"，它會轉譯成下列清單所列的字串。 

| 值  | 描述                                                                                  |
|--------|----------------------------------------------------------------------------------------------|
| 1      | ISO-「根授權單位」，發行了 "1.2" 至 ANSI，後者接著 .。。                           |
| 2      | ANSI。。。發給美國的 "1.2.840"，也就是 .。。                                            |
| 840    | 美國。。。已向 Microsoft 發出 "1.2.840.113556" .。。                                               |
| 113556 | 微軟。。。其中 Microsoft 會在 "1.2.840.113556" 下管理數個 OID 分支。 |
| 1      | Microsoft DS                                                                                 |
| 5      | NTDS 類別                                                                                 |
| 4      | Builtin-Domain                                                                               |



 

</dd> <dt>

<span id="OID"></span><span id="oid"></span>老
</dt> <dd>

請參閱 *物件識別碼*。

</dd> <dt>

<span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>模式
</dt> <dd>

目錄服務內容和結構的正式定義。 架構會定義所有的屬性和類別。 針對每個類別，會定義 [**Poss-Superiors**](a-posssuperiors.md)、 [**必須包含**](a-mustcontain.md)，而且 [**可能包含**](a-maycontain.md) 屬性。 [**Poss-Superiors**](a-posssuperiors.md) 藉由指定哪些類別可以是任何指定類別的父系，來定義目錄服務的可能樹狀結構。 [**必須包含**](a-mustcontain.md) 且 [**可能包含**](a-maycontain.md) 類別的屬性，這些屬性必須存在才能儲存類別，以及選擇性的其他屬性可能會出現。

</dd> <dt>

<span id="Security_Descriptor"></span><span id="security_descriptor"></span><span id="SECURITY_DESCRIPTOR"></span>安全描述項
</dt> <dd>

物件擁有權的相關資訊，以及其他使用者對該物件的許可權。 架構專案的 [**NT-Security-描述**](a-ntsecuritydescriptor.md) 元屬性包含表示物件安全描述項的字串。 如需此欄位中資訊格式的詳細資訊，請參閱 [安全描述項字串格式](/windows/desktop/SecAuthZ/security-descriptor-string-format)。

</dd> <dt>

<span id="Structure_Rules"></span><span id="structure_rules"></span><span id="STRUCTURE_RULES"></span>結構規則
</dt> <dd>

可能的樹狀結構或結構的定義。 在 NTDS 中，結構規則會以 Poss superiors 屬性（存在於每個 [**類別架構**](c-classschema.md) 物件上）完全表示。 請參閱 *架構*。

</dd> <dt>

<span id="Subclass"></span><span id="subclass"></span><span id="SUBCLASS"></span>類
</dt> <dd>

繼承自另一個 [**類別架構**](c-classschema.md)物件的 [**類別架構**](c-classschema.md)物件。 請參閱 *繼承*。

</dd> <dt>

<span id="Superclass"></span><span id="superclass"></span><span id="SUPERCLASS"></span>超級
</dt> <dd>

一個或多個其他 [**類別架構**](c-classschema.md)物件所繼承的 [**類別架構**](c-classschema.md)物件。 請參閱 *繼承*。

</dd> <dt>

<span id="Tree"></span><span id="tree"></span><span id="TREE"></span>樹
</dt> <dd>

請參閱 *目錄資訊樹狀目錄*。

</dd> <dt>

<span id="X.500"></span><span id="x.500"></span>X. 500
</dt> <dd>

由 ISO 和 ITU 共同開發的標準系列（先前稱為 CCITT），可指定目錄服務的命名、資料表示和通訊協定。

</dd> </dl>

 

 