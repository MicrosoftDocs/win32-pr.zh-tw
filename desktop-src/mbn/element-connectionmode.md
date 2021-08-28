---
description: ConnectionMode
MS-HAID: WWAN\_profile\_v4.element\_ConnectionMode
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ConnectionMode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55af96a96bfae012e77093688cf8665c3763fb65
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879904"
---
# <a name="span-idwwan_profile_v4element_connectionmodespanconnectionmode"></a><span id="WWAN_profile_v4.element_ConnectionMode"></span>ConnectionMode

指定要用於行動寬頻裝置的自動連線設定。

如需詳細資訊，請參閱 v1 [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) 元素的檔。

## <a name="element-hierarchy"></a>元素階層

[&lt;MBNProfileExt&gt;](element-mbnprofileext.md)  
**&lt;ConnectionMode&gt;**

## <a name="syntax"></a>Syntax

``` syntax
<ConnectionMode>

  "manual" | "auto" | "auto-home"

</ConnectionMode>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性

無。

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目

無。

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素


| Parent 項目 | 描述 | 
|----------------|-------------|
| <a href="element-mbnprofileext.md">MBNProfileExt</a> | <p><strong>MBNProfileExt</strong>元素是先前 MBNProfile 專案的延伸模組。 它會以比 MBNProfile 元素更豐富的選項組來識別行動寬頻設定檔。</p><p>設定檔中可以有一個以上的 MbnProfileExt 元素，描述一組特定作業條件的設定檔設定。 使用<strong>MBNProfileExt</strong>的<a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a>子項目，以指定哪些作業條件會將特定的設定檔設為使用中的設定檔。</p> | 


 

## <a name="requirements"></a>規格需求


| | | <p>命名空間</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
