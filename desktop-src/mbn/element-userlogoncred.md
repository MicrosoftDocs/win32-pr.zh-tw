---
description: 'MBNProfileExt \/ ... \/UserLogonCred (v4) '
MS-HAID: WWAN\_profile\_v4.element\_UserLogonCred
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: UserLogonCred
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 12a65d91-1917-49d4-9b58-68c60464c857
api_name:
- UserLogonCred
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d28c0d275b722dbba6ebc1be3363cfa3e2f6d300
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985391"
---
# <a name="span-idwwan_profile_v4element_userlogoncredspanmbnprofileextuserlogoncred-v4"></a><span id="WWAN_profile_v4.element_UserLogonCred"></span>MBNProfileExt \/ ... \/UserLogonCred (v4) 

連接的登入認證。

## <a name="element-hierarchy"></a>元素階層

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<UserLogonCred\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-1-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<UserLogonCred\>**

## <a name="syntax"></a>Syntax

``` syntax
<UserLogonCred>

  <!-- Child elements -->
  UserName,
  IgnorePassword?,
  Password?

</UserLogonCred>
```

### <a name="key"></a>答案

`?`   選擇性 (零或一) 

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性

無。

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目


| 子元素 | Description | 
|---------------|-------------|
| <a href="element-ignorepassword.md">IgnorePassword</a> | <p>指定升級設定檔時密碼的處理方式。</p><p>如果設定為 <strong>TRUE</strong> 且在更新作業時存在具有相同名稱的設定檔，則會採用該設定檔中的密碼，並將其儲存在新的設定檔中。</p><p>如需詳細資訊，請參閱 v1 <a href="../mbn/schema-ignorepassword-userlogoncred-element.md"><strong>IgnorePassword</strong></a> 元素的檔。</p> | 
| <a href="element-password.md">密碼</a> | <p>指定用來驗證使用者的密碼。</p><p>如需詳細資訊，請參閱 v1 <a href="../mbn/schema-password-userlogoncred-element.md"><strong>密碼</strong></a> 元素的檔。</p> | 
| <a href="element-username.md">使用者名稱</a> | <p>用於登入的使用者名稱。</p><p>如需詳細資訊，請參閱 v1 使用者 <a href="../mbn/schema-username-userlogoncred-element.md"><strong>名稱</strong></a> 元素的檔。</p> | 


 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素


| Parent 項目 | 描述 | 
|----------------|-------------|
| <a href="element-context.md">內容</a> | <p>指定建立資料連線所需的參數。</p> | 


 

## <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p>命名空間</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 



