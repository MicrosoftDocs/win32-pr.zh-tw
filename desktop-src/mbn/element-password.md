---
description: 'MBNProfileExt \/ ... \/ (v4 的密碼) '
MS-HAID: WWAN\_profile\_v4.element\_Password
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 密碼
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5d8816c7-a3be-4a9c-a3e0-5c12230dc06f
api_name:
- Password
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 62426b97c7714bfb483adb8883e6f6167618c35e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469635"
---
# <a name="span-idwwan_profile_v4element_passwordspanmbnprofileextpassword-v4"></a><span id="WWAN_profile_v4.element_Password"></span>MBNProfileExt \/ ... \/ (v4 的密碼) 

指定用來驗證使用者的密碼。

如需詳細資訊，請參閱 v1 [**密碼**](./schema-password-userlogoncred-element.md) 元素的檔。

## <a name="element-hierarchy"></a>元素階層

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<Password\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-1-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<Password\>**

## <a name="syntax"></a>Syntax

``` syntax
<Password>

  string

</Password>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性

無。

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目

無。

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素


| Parent 項目 | Description | 
|----------------|-------------|
| <a href="element-userlogoncred.md">UserLogonCred</a> | <p>連接的登入認證。</p> | 


 

## <a name="requirements"></a>規格需求


| | | <p>命名空間</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
