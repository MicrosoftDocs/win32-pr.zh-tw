---
description: ModemDMConfigProfile
MS-HAID: WWAN\_profile\_v4.element\_ModemDMConfigProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ModemDMConfigProfile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58ea408fb35fef5b9b2f89255e6ecb28f59b2370
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882900"
---
# <a name="span-idwwan_profile_v4element_modemdmconfigprofilespanmodemdmconfigprofile"></a><span id="WWAN_profile_v4.element_ModemDMConfigProfile"></span>ModemDMConfigProfile

數據機 DM 設定檔。

## <a name="element-hierarchy"></a>元素階層

**&lt;ModemDMConfigProfile&gt;**

## <a name="syntax"></a>Syntax

``` syntax
<ModemDMConfigProfile>

  <!-- Child elements -->
  Name,
  SimIccID,
  ApnID,
  OemConnectionId,
  RoamApplicability?,
  Context,
  AdminEnable,
  AdminRoamControl,
  ProfileCreationType?,
  any element in a non-schema namespace*

</ModemDMConfigProfile>
```

### <a name="key"></a>答案

`?`   選擇性 (零或一) 

`*`   選擇性 (零或多個) 

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性

無。

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目


| 子元素 | 說明 | 
|---------------|-------------|
| <a href="element-1-adminenable.md">AdminEnable</a> | <p>指定是否以系統管理員的方式啟用設定檔。這是 v4 的新元素。</p> | 
| <a href="element-1-adminroamcontrol.md">AdminRoamControl</a> | <p>指定設定檔是否為系統管理漫遊控制。 此元素是 v4 的新專案。 這個元素的值是 <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> 值。 這是選擇性元素;如果未指定任何值，則 <strong>AllRoamAllowed</strong> 為預設值。</p> | 
| <a href="element-1-apnid.md">ApnID</a> | <p>與此設定檔相關聯的 APN 識別碼。此元素是 v4 中的新元素，而且是選擇性的。</p> | 
| <a href="element-1-context.md">內容</a> | <p>指定建立資料連線所需的參數。</p> | 
| <a href="element-1-name.md">名稱</a> | <p>設定檔的名稱。 如需詳細資訊，請參閱 v1 <a href="../mbn/schema-name-mbnprofile-element.md"><strong>名稱</strong></a> 元素的檔。</p> | 
| <a href="element-oemconnectionid.md">OemConnectionId</a> | <p>數據機 DM 設定的 OEM 連接識別碼。</p> | 
| <a href="element-1-profilecreationtype.md">ModemDMConfigProfile 中的 ProfileCreationType () </a> | <p>指定此數據機 DM 設定檔的建立方式。</p><p>這個值是用來決定使用者是否可以刪除設定檔。 使用者只能刪除 <strong>UserProvisioned</strong> 設定檔。</p> | 
| <a href="element-1-roamapplicability.md">RoamApplicability</a> | <p>指定只有在目前的漫遊條件是指定的漫遊條件時，才會使用此設定檔。 否則，此設定檔並不適用，也無法用來啟用 (PDP) 內容的封包資料通訊協定。 這個元素的值必須是有效的 <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> 值。</p> | 
| <a href="element-1-simiccid.md">SimIccID</a> | <p>適用于 GSM 裝置的 SIM Identifcation 號碼。 如需詳細資訊，請參閱 v1 <a href="../mbn/schema-simiccid-mbnprofile-element.md"><strong>SimIccID</strong></a> 元素的檔。</p> | 


 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素

這個最外層的 (檔) 元素可能不會包含在任何其他專案中。

## <a name="requirements"></a>規格需求


| | | <p>命名空間</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 



