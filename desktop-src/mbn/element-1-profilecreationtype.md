---
description: 'ModemDMConfigProfile 中的 ProfileCreationType () '
MS-HAID: WWAN\_profile\_v4.element\_1\_ProfileCreationType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'ModemDMConfigProfile 中的 ProfileCreationType () '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbd0a4a3a634a892f81f4be54093f51638d6c4ca
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885098"
---
# <a name="span-idwwan_profile_v4element_1_profilecreationtypespanprofilecreationtype-in-modemdmconfigprofile"></a><span id="WWAN_profile_v4.element_1_ProfileCreationType"></span>ModemDMConfigProfile 中的 ProfileCreationType () 

指定此數據機 DM 設定檔的建立方式。

這個值是用來決定使用者是否可以刪除設定檔。 使用者只能刪除 **UserProvisioned** 設定檔。

## <a name="element-hierarchy"></a>元素階層

[&lt;ModemDMConfigProfile&gt;](element-modemdmconfigprofile.md)  
**&lt;ProfileCreationType&gt;**

## <a name="syntax"></a>Syntax

``` syntax
<ProfileCreationType>

  "UserProvisioned" | "AdminProvisioned" | "OperatorProvisioned" | "DeviceProvisioned"

</ProfileCreationType>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性

無。

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目

無。

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素


| Parent 項目 | 說明 | 
|----------------|-------------|
| <a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a> | <p>數據機 DM 設定檔。</p> | 


 

## <a name="related-elements"></a>相關元素

下列專案的名稱與這個專案的名稱相同，但內容或屬性不同：

-   **[MBNProfileExt 中的 ProfileCreationType ()](element-profilecreationtype.md)**

## <a name="requirements"></a>規格需求


| | | <p>命名空間</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 



