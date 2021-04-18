---
description: 'MBNProfileExt \/ ... \/IgnorePassword (v4) '
MS-HAID: WWAN\_profile\_v4.element\_IgnorePassword
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IgnorePassword
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc73050a01f6f0f9799290ba267b8ecaaee1003a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191451"
---
# <a name="span-idwwan_profile_v4element_ignorepasswordspanmbnprofileextignorepassword-v4"></a><span data-ttu-id="56a88-103"><span id="WWAN_profile_v4.element_IgnorePassword"></span>MBNProfileExt \/ ... \/IgnorePassword (v4) </span><span class="sxs-lookup"><span data-stu-id="56a88-103"><span id="WWAN_profile_v4.element_IgnorePassword"></span>MBNProfileExt\/...\/IgnorePassword (v4)</span></span>

<span data-ttu-id="56a88-104">指定升級設定檔時密碼的處理方式。</span><span class="sxs-lookup"><span data-stu-id="56a88-104">Specifies how passwords are handled when upgrading profiles.</span></span>

<span data-ttu-id="56a88-105">如果設定為 **TRUE** 且在更新作業時存在具有相同名稱的設定檔，則會採用該設定檔中的密碼，並將其儲存在新的設定檔中。</span><span class="sxs-lookup"><span data-stu-id="56a88-105">If set to **TRUE** and a profile with the same name exists at the time of the update operation, then the password from that profile will be taken and stored in the new profile.</span></span>

<span data-ttu-id="56a88-106">如需詳細資訊，請參閱 v1 [**IgnorePassword**](./schema-ignorepassword-userlogoncred-element.md) 元素的檔。</span><span class="sxs-lookup"><span data-stu-id="56a88-106">For more details, see the documentation for the v1 [**IgnorePassword**](./schema-ignorepassword-userlogoncred-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="56a88-107">元素階層</span><span class="sxs-lookup"><span data-stu-id="56a88-107">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<IgnorePassword\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-1-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<IgnorePassword\>**

## <a name="syntax"></a><span data-ttu-id="56a88-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="56a88-108">Syntax</span></span>

``` syntax
<IgnorePassword>

  boolean

</IgnorePassword>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="56a88-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素</span><span class="sxs-lookup"><span data-stu-id="56a88-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="56a88-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="56a88-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="56a88-111">無。</span><span class="sxs-lookup"><span data-stu-id="56a88-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="56a88-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目</span><span class="sxs-lookup"><span data-stu-id="56a88-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="56a88-113">無。</span><span class="sxs-lookup"><span data-stu-id="56a88-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="56a88-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素</span><span class="sxs-lookup"><span data-stu-id="56a88-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="56a88-115">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="56a88-115">Parent Element</span></span></th>
<th><span data-ttu-id="56a88-116">Description</span><span class="sxs-lookup"><span data-stu-id="56a88-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="56a88-117"><a href="element-userlogoncred.md">UserLogonCred</a></span><span class="sxs-lookup"><span data-stu-id="56a88-117"><a href="element-userlogoncred.md">UserLogonCred</a></span></span></td>
<td><p><span data-ttu-id="56a88-118">連接的登入認證。</span><span class="sxs-lookup"><span data-stu-id="56a88-118">Logon credentials for a connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="56a88-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="56a88-119">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56a88-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="56a88-120">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
