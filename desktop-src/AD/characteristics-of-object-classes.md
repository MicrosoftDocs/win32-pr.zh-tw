---
title: 物件類別的特性
description: Active Directory Domain Services 中的每個物件類別都是由架構容器中的 classSchema 物件所定義。
ms.assetid: 88a2b2a3-e8e2-4be1-9784-9709cbea08d6
ms.tgt_platform: multiple
keywords:
- 物件類別 AD 的特性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00c7e750d53597d1532d48c3c463315f8a48bd6d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681690"
---
# <a name="characteristics-of-object-classes"></a>物件類別的特性

Active Directory Domain Services 中的每個物件類別都是由架構容器中的 **classSchema** 物件所定義。 **ClassSchema** 物件的屬性會指定類別的特性，例如：

-   類別識別碼：類別有數個識別碼，包括 **ldapDisplayName**，LDAP 用戶端會使用這些識別碼來識別搜尋篩選準則中的類別，以及使用 **schemaIDGUID**（用於安全描述項）來控制對類別的存取。
-   可能的屬性：物件類別定義包含可在類別的實例上設定的強制和選擇性屬性清單。
-   可能的父系：除了目錄階層的根目錄之外，每個物件實例都只有一個父系。 物件類別定義包含可能的父系清單，也就是可以包含類別實例的物件類別。
-   超類和輔助類別：除了 [*top*](/previous-versions/windows/desktop/legacy/ms681941(v=vs.85))) 之外，每個物件類別 (都是衍生自另一個類別。 類別會繼承類別階層架構中其上類別的可能屬性和可能的父系。 類別也可以有任意數目的輔助類別，從中繼承可能屬性的清單。 如需詳細資訊，請參閱 [Active Directory 架構中的類別繼承](class-inheritance-in-the-active-directory-schema.md)。

下表列出 **classSchema** 物件之索引鍵屬性的 **lDAPDisplayName** 和描述。 如需詳細資訊，以及 **classSchema** 物件的強制和選擇性屬性完整清單，請參閱 [**classSchema**](/windows/desktop/ADSchema/c-classschema)。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>lDAPDisplayName</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>cn</strong></td>
<td>Active Directory Domain Services 中的每個物件都有一個命名屬性，其相對辨別名稱 (RDN) 形成。 <strong>ClassSchema</strong>物件的命名屬性是<strong>Cn</strong> (一般名稱) 。 指派給 <strong>cn</strong> 的值是物件類別將擁有做為其 RDN 的值。 例如， <strong>organizationalUnit</strong>物件類別的<strong>Cn</strong>是組織單位，它會以「cn = 組織單位」的分辨名稱顯示。 <strong>Cn</strong>在架構容器中必須是唯一的。</td>
</tr>
<tr class="even">
<td><strong>lDAPDisplayName</strong></td>
<td>LDAP 用戶端（例如 ADSI LDAP 提供者）所使用的名稱，用來參考類別，例如在搜尋篩選準則中指定類別。 類別的 <strong>lDAPDisplayName</strong> 在架構容器中必須是唯一的，這表示它在所有 <strong>classSchema</strong> 和 <strong>attributeSchema</strong> 物件中必須是唯一的。 如需針對新類別撰寫 <strong>cn</strong> 和 <strong>lDAPDisplayName</strong> 的詳細資訊，請參閱 <a href="naming-attributes-and-classes.md">命名屬性和類別</a>。</td>
</tr>
<tr class="odd">
<td><strong>schemaIDGUID</strong></td>
<td>儲存為八位字串的 GUID。 此 GUID 可唯一識別類別。 此 GUID 可以用在存取控制專案中，以控制對這個類別之物件的存取。 如需詳細資訊，請參閱 <a href="setting-permissions-on-child-object-operations.md">設定子物件作業的許可權</a>。 建立 <strong>classSchema</strong> 物件時，如果未指定，Active Directory 伺服器會產生這個值。 如果您建立新的類別，請為每個類別產生您自己的 GUID，讓擴充功能的所有安裝都使用相同的 <strong>schemaIDGUID</strong> 來參考類別。<br/></td>
</tr>
<tr class="even">
<td><strong>adminDisplayName</strong></td>
<td>在 [系統管理工具] 中使用之類別的顯示名稱。 如果在建立類別時未指定 <strong>adminDisplayName</strong> ，系統會使用 Common-Name 值作為顯示名稱。 只有當對應不存在於類別的顯示規範的 <strong>classDisplayName</strong> 屬性中時，才會使用此顯示名稱。 如需詳細資訊，請參閱 <a href="display-specifiers.md">顯示</a> 規範和 <a href="class-and-attribute-display-names.md">類別和屬性顯示名稱</a>。<br/></td>
</tr>
<tr class="odd">
<td><strong>governsID</strong></td>
<td>類別的 OID。 此值在所有<strong>classSchema</strong>物件的<strong>governsIDs</strong>中必須是唯一的，而且所有<strong>attributeSchema</strong>物件的<strong>attributeIDs</strong>都必須是唯一的。 如需詳細資訊，請參閱 <a href="object-identifiers.md">物件識別碼</a>。</td>
</tr>
<tr class="even">
<td><strong>rDnAttId</strong></td>
<td>識別命名屬性（attribute），此屬性（attribute）會提供這個類別的 RDN （如果不同于預設的 (<strong>cn</strong>) ）。 不建議使用 <strong>cn</strong> 以外的命名屬性。 命名屬性應該從已知的集合中繪製， (OU、CN、O、L 和 DC) ，而這些都是由所有 LDAP 第3版用戶端瞭解。 如需詳細資訊，請參閱<a href="syntaxes-for-attributes-in-active-directory-domain-services.md">Active Directory Domain Services 中屬性的</a><a href="object-names-and-identities.md">物件名稱和</a>識別和語法。 命名屬性必須有目錄字串語法。 如需詳細資訊，請參閱 <a href="syntaxes-for-attributes-in-active-directory-domain-services.md">Active Directory Domain Services 中的屬性語法</a>。<br/></td>
</tr>
<tr class="odd">
<td><strong>mustContain</strong>、 <strong>systemMustContain</strong></td>
<td>一對多重值屬性，這些屬性會指定必須存在於這個類別的實例上的屬性。 這些是必要的屬性，必須在建立期間存在，而且無法在建立後清除。 建立類別之後，就無法變更這些屬性。 類別的完整強制屬性集是這個類別上的 <strong>systemMustContain</strong> 和 <strong>mustContain</strong> 值與所有繼承類別的聯集。<br/></td>
</tr>
<tr class="even">
<td><strong>mayContain</strong>、 <strong>systemMayContain</strong></td>
<td>一對多重值屬性，這些屬性會指定可能存在於此類別的實例上的屬性。 這些是非強制性的選擇性屬性，因此不一定會出現在這個類別的實例上。 您可以新增或移除現有類別1或類別 2 <strong>classSchema</strong>物件中的<strong>mayContain</strong>值。 從<strong>classSchema</strong>物件移除<strong>mayContain</strong>值之前，您應該先搜尋物件類別的實例，並清除您要移除之屬性的任何值。 建立類別之後， <strong>systemMayContain</strong> 屬性就無法變更類別的一組完整的選擇性屬性，就是這個類別和所有繼承類別上的 <strong>systemMayContain</strong> 和 <strong>mayContain</strong> 值的聯集。<br/></td>
</tr>
<tr class="odd">
<td><strong>possSuperiors</strong>、 <strong>systemPossSuperiors</strong></td>
<td>一對多重值的屬性，這些屬性會指定可以成為這個類別之實例合法父系的結構化類別。 一組完整的可能 superiors 是這個類別上的 <strong>systemPossSuperiors</strong> 和 <strong>possSuperiors</strong> 值的聯集，以及任何繼承的結構或抽象類別。 <strong>systemPossSuperiors</strong> 和 <strong>possSuperiors</strong> 值不會繼承自輔助類別。 您可以新增或移除現有類別1或類別 2 <strong>classSchema</strong>物件中的<strong>possSuperiors</strong>值。 建立類別之後，就無法變更 <strong>systemPossSuperiors</strong> 屬性。<br/></td>
</tr>
<tr class="even">
<td><strong>objectClassCategory</strong></td>
<td>指定類別類別目錄的整數值，它可以是下列其中一項：
<ul>
<li>結構化，表示它可以在目錄中具現化。</li>
<li>Abstract，表示類別提供類別的基本定義，可用來形成結構類別。</li>
<li>輔助，表示可以使用類別來擴充繼承自它的類別定義，但不能用它本身來形成類別。</li>
</ul>
如需詳細資訊，請參閱 <a href="structural-abstract-and-auxiliary-classes.md">結構化、抽象概念和輔助類別</a>。<br/></td>
</tr>
<tr class="odd">
<td><strong>subClassOf</strong></td>
<td>這個類別之立即超類別的 OID，也就是衍生這個類別的類別。 針對結構化類別， <strong>subClassOf</strong> 可以是結構化或抽象類別。<br/> 針對抽象類別， <strong>subClassOf</strong> 只能是抽象類別。<br/> 針對輔助類別， <strong>subClassOf</strong> 可以是抽象或輔助類別。<br/> 如果您定義新的類別，請確定 <strong>subClassOf</strong> 類別存在，或在新類別寫入目錄時存在。 如果類別不存在，則不會將 <strong>classSchema</strong> 物件新增至目錄。<br/></td>
</tr>
<tr class="even">
<td><strong>auxiliaryClass</strong>、 <strong>systemAuxiliaryClass</strong></td>
<td>一對多重值的屬性，這些屬性會指定此類別繼承自的輔助類別。 一組完整的輔助類別是這個類別上的 <strong>systemAuxiliaryClass</strong> 和 <strong>auxiliaryClass</strong> 值與所有繼承類別的聯集。 針對現有的 <strong>classSchema</strong> 物件，可以將值加入至 <strong>auxiliaryClass</strong> 屬性，但不能移除。 建立類別之後，就無法變更 <strong>systemAuxiliaryClass</strong> 屬性。<br/></td>
</tr>
<tr class="odd">
<td><strong>defaultObjectCategory</strong></td>
<td>此物件類別或其中一個超類的分辨名稱。 建立此物件類別的實例時，系統會將新實例的 <strong>objectCategory</strong> 屬性設定為其物件類別之 <strong>defaultObjectCategory</strong> 屬性中指定的值。 <strong>ObjectCategory</strong>屬性是用來提高物件類別搜尋效率的索引屬性。 如果在建立類別時未指定 <strong>defaultObjectCategory</strong> ，系統會將它設定為此類別之 <strong>CLASSSCHEMA</strong> 物件 (DN) 的分辨名稱。 如果這個物件會經常由超類別的值（而不是物件本身的類別）進行查詢，您可以將 <strong>defaultObjectCategory</strong> 設定為超級類別的 DN。 例如，如果您要子類別化預先定義的 (類別 1) 類別，最佳作法是將 <strong>defaultObjectCategory</strong> 設定為與超級類別相同的值。 這可讓標準 UI &quot; 尋找您的子 &quot; 類別。<br/> 如需詳細資訊，請參閱 <a href="object-class-and-object-category.md">物件類別和物件類別</a>。<br/></td>
</tr>
<tr class="even">
<td><strong>defaultHidingValue</strong></td>
<td>布林值，指定這個類別之新實例的 <strong>showInAdvancedViewOnly</strong> 屬性預設設定。 許多目錄物件對終端使用者而言都不感興趣。 為了讓這些物件不會雜亂 UI，每個物件都有一個稱為 <strong>showInAdvancedViewOnly</strong>的布林值屬性。 如果 <strong>defaultHidingValue</strong> 設定為 <strong>TRUE</strong>，則會在系統管理嵌入式管理單元和 Windows shell 中隱藏新的物件實例。 即使在物件類別的<strong>displaySpecifier</strong>物件上設定適當的建立 wizard 屬性，物件類別的功能表項目也不會出現在系統管理嵌入式管理單元的<strong>新</strong>操作功能表中。<br/> 如果 <strong>defaultHidingValue</strong> 設定為 <strong>FALSE</strong>，則會在系統管理嵌入式管理單元和 Windows shell 中顯示物件的新實例。 將此屬性設定為 <strong>FALSE</strong> ，可在系統管理嵌入式管理單元和 shell 中查看類別的實例，並在系統管理嵌入式管理單元的 [ <strong>新增</strong> ] 功能表中啟用建立嚮導和其功能表項目。<br/> 如果未設定 <strong>defaultHidingValue</strong> 值，預設值為 <strong>TRUE</strong>。<br/></td>
</tr>
<tr class="odd">
<td><strong>systemFlags</strong></td>
<td>整數值，包含定義類別之其他屬性的旗標。 0x10 位會識別類別1類別 (類別，這是系統) 中所包含之基底架構的一部分。 您無法設定此位，這表示不會在類別2類別中設定位， (是架構) 的延伸。</td>
</tr>
<tr class="even">
<td><strong>systemOnly</strong></td>
<td>布林值，這個值會指定是否只有 Active Directory 伺服器可以修改類別。 只有 (DSA) 的目錄服務代理程式才能建立或刪除僅限系統的類別。 系統專用類別是系統相依于正常作業的類別。</td>
</tr>
<tr class="odd">
<td><strong>defaultSecurityDescriptor</strong></td>
<td>為這個類別的新物件指定預設安全描述項。 如需詳細資訊，請參閱 <a href="default-security-descriptor.md">預設安全描述項</a> ，以及 <a href="how-security-descriptors-are-set-on-new-directory-objects.md">如何在新的目錄物件上設定安全描述項</a>。</td>
</tr>
<tr class="even">
<td><strong>isDefunct</strong></td>
<td>指出類別是否無用的布林值。 如需詳細資訊，請參閱 <a href="disabling-existing-classes-and-attributes.md">停用現有的類別和屬性</a>。</td>
</tr>
<tr class="odd">
<td><strong>description</strong></td>
<td>供系統管理應用程式使用之類別的文字描述。</td>
</tr>
<tr class="even">
<td><strong>objectClass</strong></td>
<td>識別此物件為其實例的物件類別，這是所有類別定義的 <strong>classSchema</strong> 物件類別，以及所有屬性定義的 <strong>attributeSchema</strong> 物件類別。</td>
</tr>
</tbody>
</table>



 

 

