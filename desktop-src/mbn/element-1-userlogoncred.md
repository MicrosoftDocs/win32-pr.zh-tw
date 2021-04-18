---
description: 'ModemDMConfigProfile \/ ... \/UserLogonCred (v4) '
MS-HAID: WWAN\_profile\_v4.element\_1\_UserLogonCred
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'UserLogonCred (v4) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6d563cf8-ea40-46b3-a74e-ec7640ca9824
api_name:
- UserLogonCred
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: aea2cdfda61e557ff790b59e7af2a05d914d3403
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/05/2021
ms.locfileid: "106996547"
---
# <a name="span-idwwan_profile_v4element_1_userlogoncredspanmodemdmconfigprofileuserlogoncred-v4"></a><span data-ttu-id="f3101-103"><span id="WWAN_profile_v4.element_1_UserLogonCred"></span>ModemDMConfigProfile \/ ... \/UserLogonCred (v4) </span><span class="sxs-lookup"><span data-stu-id="f3101-103"><span id="WWAN_profile_v4.element_1_UserLogonCred"></span>ModemDMConfigProfile\/...\/UserLogonCred (v4)</span></span>

<span data-ttu-id="f3101-104">連接的登入認證。</span><span class="sxs-lookup"><span data-stu-id="f3101-104">Logon credentials for a connection.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="f3101-105">元素階層</span><span class="sxs-lookup"><span data-stu-id="f3101-105">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<UserLogonCred\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-1-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<UserLogonCred\>**

## <a name="syntax"></a><span data-ttu-id="f3101-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3101-106">Syntax</span></span>

``` syntax
<UserLogonCred>

  <!-- Child elements -->
  UserName,
  IgnorePassword?,
  Password?

</UserLogonCred>
```

### <a name="key"></a><span data-ttu-id="f3101-107">答案</span><span class="sxs-lookup"><span data-stu-id="f3101-107">Key</span></span>

<span data-ttu-id="f3101-108">`?`   選擇性 (零或一) </span><span class="sxs-lookup"><span data-stu-id="f3101-108">`?`   optional (zero or one)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="f3101-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素</span><span class="sxs-lookup"><span data-stu-id="f3101-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="f3101-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="f3101-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="f3101-111">無。</span><span class="sxs-lookup"><span data-stu-id="f3101-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="f3101-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目</span><span class="sxs-lookup"><span data-stu-id="f3101-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f3101-113">子元素</span><span class="sxs-lookup"><span data-stu-id="f3101-113">Child Element</span></span></th>
<th><span data-ttu-id="f3101-114">Description</span><span class="sxs-lookup"><span data-stu-id="f3101-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f3101-115"><a href="element-1-ignorepassword.md">IgnorePassword</a></span><span class="sxs-lookup"><span data-stu-id="f3101-115"><a href="element-1-ignorepassword.md">IgnorePassword</a></span></span></td>
<td><p><span data-ttu-id="f3101-116">指定升級設定檔時密碼的處理方式。</span><span class="sxs-lookup"><span data-stu-id="f3101-116">Specifies how passwords are handled when upgrading profiles.</span></span></p>
<p><span data-ttu-id="f3101-117">如果設定為 <strong>TRUE</strong> 且在更新作業時存在具有相同名稱的設定檔，則會採用該設定檔中的密碼，並將其儲存在新的設定檔中。</span><span class="sxs-lookup"><span data-stu-id="f3101-117">If set to <strong>TRUE</strong> and a profile with the same name exists at the time of the update operation, then the password from that profile will be taken and stored in the new profile.</span></span></p>
<p><span data-ttu-id="f3101-118">如需詳細資訊，請參閱 v1 <a href="../mbn/schema-ignorepassword-userlogoncred-element.md"><strong>IgnorePassword</strong></a> 元素的檔。</span><span class="sxs-lookup"><span data-stu-id="f3101-118">For more details, see the documentation for the v1 <a href="../mbn/schema-ignorepassword-userlogoncred-element.md"><strong>IgnorePassword</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3101-119"><a href="element-1-password.md">密碼</a></span><span class="sxs-lookup"><span data-stu-id="f3101-119"><a href="element-1-password.md">Password</a></span></span></td>
<td><p><span data-ttu-id="f3101-120">指定用來驗證使用者的密碼。</span><span class="sxs-lookup"><span data-stu-id="f3101-120">Specifies the password used to authenticate a user.</span></span></p>
<p><span data-ttu-id="f3101-121">如需詳細資訊，請參閱 v1 <a href="../mbn/schema-password-userlogoncred-element.md"><strong>密碼</strong></a> 元素的檔。</span><span class="sxs-lookup"><span data-stu-id="f3101-121">For more information, see the documentation for the v1 <a href="../mbn/schema-password-userlogoncred-element.md"><strong>Password</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3101-122"><a href="element-1-username.md">使用者名稱</a></span><span class="sxs-lookup"><span data-stu-id="f3101-122"><a href="element-1-username.md">UserName</a></span></span></td>
<td><p><span data-ttu-id="f3101-123">用於登入的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="f3101-123">The user name to use for logon.</span></span></p>
<p><span data-ttu-id="f3101-124">如需詳細資訊，請參閱 v1 使用者 <a href="../mbn/schema-username-userlogoncred-element.md"><strong>名稱</strong></a> 元素的檔。</span><span class="sxs-lookup"><span data-stu-id="f3101-124">For more details, see the documentation for the v1 <a href="../mbn/schema-username-userlogoncred-element.md"><strong>UserName</strong></a> element.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="f3101-125"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素</span><span class="sxs-lookup"><span data-stu-id="f3101-125"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f3101-126">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="f3101-126">Parent Element</span></span></th>
<th><span data-ttu-id="f3101-127">描述</span><span class="sxs-lookup"><span data-stu-id="f3101-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f3101-128"><a href="element-1-context.md">內容</a></span><span class="sxs-lookup"><span data-stu-id="f3101-128"><a href="element-1-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="f3101-129">指定建立資料連線所需的參數。</span><span class="sxs-lookup"><span data-stu-id="f3101-129">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="f3101-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3101-130">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3101-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="f3101-131">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



