---
description: MBNProfileExt
MS-HAID: WWAN\_profile\_v4.element\_MBNProfileExt
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MBNProfileExt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c47dd7c8b8064d7c9bed24763dfe3ec8fda0ac12
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472124"
---
# <a name="span-idwwan_profile_v4element_mbnprofileextspanmbnprofileext"></a><span id="WWAN_profile_v4.element_MBNProfileExt"></span>MBNProfileExt

**MBNProfileExt** 元素是先前 MBNProfile 專案的延伸模組。 它會以比 MBNProfile 元素更豐富的選項組來識別行動寬頻設定檔。

設定檔中可以有一個以上的 MbnProfileExt 元素，描述一組特定作業條件的設定檔設定。 使用 **MBNProfileExt** 的 [**ProfileConditionedOn**](element-profileconditionedon.md)子項目，以指定哪些作業條件會將特定的設定檔設為使用中的設定檔。

## <a name="element-hierarchy"></a>元素階層

**<MBNProfileExt>**

## <a name="syntax"></a>Syntax

``` syntax
<MBNProfileExt>

  <!-- Child elements -->
  Name,
  Description?,
  ICONFilePath?,
  IsDefault,
  ProfileCreationType?,
  SubscriberID?,
  SimIccID,
  HomeProviderName?,
  AutoConnectOnInternet?,
  ConnectionMode?,
  Context?,
  DataRoamingPartners?,
  PurposeGroups?,
  ProfileConditionedOn?,
  IsProvisioningProfile?,
  ApnID?,
  AdminEnable?,
  AdminRoamControl?,
  IsExclusiveToOther?,
  IsLongStandingAdditionalPdpContextProfile?,
  MmsConfiguration?,
  any element in a non-schema namespace*

</MBNProfileExt>
```

### <a name="key"></a>答案

`?`   選擇性 (零或一) 

`*`   選擇性 (零或多個) 

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性

無。

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目


| 子元素 | Description | 
|---------------|-------------|
| <a href="element-adminenable.md">AdminEnable</a> | <p>指定是否以系統管理員的方式啟用設定檔。這是 v4 的新元素。</p> | 
| <a href="element-adminroamcontrol.md">AdminRoamControl</a> | <p>指定設定檔是否為系統管理漫遊控制。 此元素是 v4 的新專案。 這個元素的值是 <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> 值。 這是選擇性元素;如果未指定任何值，則 <strong>AllRoamAllowed</strong> 為預設值。</p> | 
| <a href="element-apnid.md">ApnID</a> | <p>與此設定檔相關聯的 APN 識別碼。此元素是 v4 中的新元素，而且是選擇性的。</p> | 
| <a href="element-autoconnectoninternet.md">AutoConnectOnInternet</a> | <p>指定行動寬頻裝置是否會自動連接到網路。</p><p>如需詳細資訊，請參閱 v1 <a href="../mbn/schema-autoconnectoninternet-mbnprofile-element.md"><strong>AutoConnectOnInternet</strong></a> 元素的檔。</p> | 
| <a href="element-connectionmode.md">ConnectionMode</a> | <p>指定要用於行動寬頻裝置的自動連線設定。</p><p>如需詳細資訊，請參閱 v1 <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> 元素的檔。</p> | 
| <a href="element-context.md">內容</a> | <p>指定建立資料連線所需的參數。</p> | 
| <a href="element-dataroamingpartners.md">DataRoamingPartners</a> | <p>指定漫遊時的慣用網路提供者清單。</p><p>如需詳細資訊，請參閱 v1 <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>DataRoamingPartners</strong></a> 元素的檔。</p> | 
| <a href="element-description.md">說明</a> | <p>設定檔的描述。</p> | 
| <a href="element-homeprovidername.md">HomeProviderName</a> | <p>給定 SIM/裝置的家用提供者名稱。 如需詳細資訊，請參閱 v1 <a href="../mbn/schema-homeprovidername-mbnprofile-element.md"><strong>HomeProviderName</strong></a> 元素的檔。</p> | 
| <a href="element-iconfilepath.md">ICONFilePath</a> | <p>連接的圖示檔路徑。 當使用此設定檔建立連接時，作業系統連接使用者介面會顯示圖示。</p><p>如需使用此元素的詳細資訊，請參閱 <a href="../mbn/schema-iconfilepath-mbnprofile-element.md"><strong>ICONFilePath</strong></a>的 v1 檔。</p> | 
| <a href="element-isdefault.md">IsDefault</a> | <p>指定此設定檔是否為預設設定檔。</p><p>如需此專案的詳細資訊，請參閱 <a href="../mbn/schema-isdefault-mbnprofile-element.md"><strong>IsDefault</strong></a>的 v1 檔。</p> | 
| <a href="element-isexclusivetoother.md">IsExclusiveToOther</a> | <p>指定此設定檔對於相同設定檔集 (s) 的其他設定檔是專屬的。此元素是 v4 的新專案。</p> | 
| <a href="element-islongstandingadditionalpdpcontextprofile.md">IsLongStandingAdditionalPdpCoNtextProfile</a> | <p>指定此設定檔為長期額外的 PDP 內容設定檔。如果這個元素的值是 <strong>true</strong>，則 <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpCoNtextProfile</strong></a> 也必須設定為 <strong>true</strong>。 這是 v4 的新元素。</p> | 
| <a href="element-isprovisioningprofile.md">IsProvisioningProfile</a> | <p>指定此設定檔僅用於布建。否則，此設定檔並不適用，也無法用來啟用 (PDP) 內容的封包資料通訊協定。 此元素是 v4 的新專案。</p><p>如果 <strong>IsProvisioningProfile</strong> 為 True， <a href="element-isdefault.md"><strong>IsDefault</strong></a> 必須為 false，而且 <a href="element-connectionmode.md"><strong>ConnectionMode</strong></a> 必須是手動。</p> | 
| <a href="element-mmsconfiguration.md">MmsConfiguration</a> | <p>多媒體訊息服務 (MMS) 的設定資訊。</p><p>除了設定此元素內的設定元素之外，MMS 設定檔也必須具有下列設定。</p><ul><li>其 <a href="element-name.md"><strong>Name</strong></a> 元素必須包含全系統的唯一名稱。</li><li>其 <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> 必須設定為 <strong>UserProvisioned</strong>。</li><li>其 <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> 必須包含此設定檔所適用之 SIM 的 ICCID。</li><li>其 <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> 必須設定為 <strong>手動</strong>。</li><li>其 <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> 必須包含 MMS 用途群組的 GUID。</li><li>其 <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpCoNtextProfile</strong></a> 必須設定為 <strong>true</strong>。</li></ul> | 
| <a href="element-name.md">名稱</a> | <p>設定檔的名稱。 如需詳細資訊，請參閱 v1 <a href="../mbn/schema-name-mbnprofile-element.md"><strong>名稱</strong></a> 元素的檔。</p> | 
| <a href="element-profileconditionedon.md">ProfileConditionedOn</a> | <p>指定必須滿足的條件，設定檔才適用。</p><p>此元素是 v4 的新專案。 它可讓您指定在不同條件下套用的多個設定檔，並在適用時自動使用適當的設定檔。 這是選擇性的項目。 如果您未指定，則設定檔一律適用于所列出的條件。</p> | 
| <a href="element-profilecreationtype.md">MBNProfileExt 中的 ProfileCreationType () </a> | <p>指定設定檔的建立者。</p><p>如需此元素的詳細資訊，請參閱 v1 <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> 元素的檔。</p> | 
| <a href="element-purposegroups.md">PurposeGroups</a> | <p>選用的設定檔群組清單，其中每個群組都包含用於一般用途的設定檔。</p><p>此元素是架構 v4 的新專案。</p><p>一個設定檔可以列在多個群組中。</p> | 
| <a href="element-simiccid.md">SimIccID</a> | <p>適用于 GSM 裝置的 SIM Identifcation 號碼。 如需詳細資訊，請參閱 v1 <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> 元素的檔。</p> | 
| <a href="element-subscriberid.md">SubscriberID</a> | <p>識別設定檔的唯一識別碼。</p><p>若為 GSM 網路，這應該包含 SIM 的 IMSI (國際行動使用者身分識別) ，而針對 CDMA 裝置，則應該包含裝置的最小 (行動電話識別碼) 。</p><p>如需詳細資訊，請參閱 v1 <a href="../mbn/schema-subscriberid-mbnprofile-element.md"><strong>SubscriberID</strong></a> 元素的檔。</p> | 


 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素

這個最外層的 (檔) 元素可能不會包含在任何其他專案中。

## <a name="requirements"></a>規格需求


| | | <p>命名空間</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
