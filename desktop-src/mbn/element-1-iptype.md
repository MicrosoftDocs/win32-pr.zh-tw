---
description: 'ModemDMConfigProfile \/ ... \/IPType (v4) '
MS-HAID: WWAN\_profile\_v4.element\_1\_IPType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPType (v4) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f655d2f8592613fdb4953cbda32841dc9beaec0d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479974"
---
# <a name="span-idwwan_profile_v4element_1_iptypespanmodemdmconfigprofileiptype-v4"></a><span id="WWAN_profile_v4.element_1_IPType"></span>ModemDMConfigProfile \/ ... \/IPType (v4) 

指定要用於此資料連線的 IP 類型。

此元素是架構 v4 中的新專案。 元素可以具有下列其中一個值。

| 值   | 意義                                       |
|---------|-----------------------------------------------|
| 預設 | IP 類型是由較低層 () 所挑選     |
| IPv4    | 使用 IPv4                                      |
| IPv6    | 使用 IPv6                                      |
| IPv4v6  | 使用 IPv4 和（或） IPv6 （如有提供）。           |
| XLAT    | 使用464XLAT 透過 IPv6 網路將 IPv4 通道 |

 

## <a name="element-hierarchy"></a>元素階層

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<IPType\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<IPType\>**

## <a name="syntax"></a>Syntax

``` syntax
<IPType>

  "Default" | "IPv4" | "IPv6" | "IPv4v6" | "XLAT"

</IPType>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性

無。

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目

無。

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素


| Parent 項目 | 描述 | 
|----------------|-------------|
| <a href="element-1-context.md">內容</a> | <p>指定建立資料連線所需的參數。</p> | 


 

## <a name="requirements"></a>規格需求


| | | <p>命名空間</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 



