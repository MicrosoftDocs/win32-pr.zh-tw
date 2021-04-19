---
description: 'MBNProfileExt \/ ... \/AuthProtocol (v4) '
MS-HAID: WWAN\_profile\_v4.element\_AuthProtocol
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: AuthProtocol
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8274effe-1fcc-43f8-a609-795fe19a1c4f
api_name:
- AuthProtocol
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 90b3b64c5052a16f18c0a1b9fd154e2e73acd714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972848"
---
# <a name="span-idwwan_profile_v4element_authprotocolspanmbnprofileextauthprotocol-v4"></a><span id="WWAN_profile_v4.element_AuthProtocol"></span>MBNProfileExt \/ ... \/AuthProtocol (v4) 

>指定要用於啟用封包資料通訊協定 (PDP) 內容的驗證通訊協定。

請注意，在 v4 中，此元素有新的列舉值。 **AutoSelection** 表示驗證通訊協定是由較低層 (s) 挑選。

如需詳細資訊，請參閱 v1 [**AuthProtocol**](./schema-authprotocol-contexttype-element.md) 元素的檔。

## <a name="element-hierarchy"></a>元素階層

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<AuthProtocol\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<AuthProtocol\>**

## <a name="syntax"></a>Syntax

``` syntax
<AuthProtocol>

  "NONE" | "PAP" | "CHAP" | "MsCHAPv2" | "AutoSelection"

</AuthProtocol>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性

無。

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目

無。

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parent 項目</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-context.md">內容</a></td>
<td><p>指定建立資料連線所需的參數。</p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a>規格需求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>命名空間</p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
