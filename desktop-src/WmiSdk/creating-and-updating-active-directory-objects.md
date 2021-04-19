---
description: Active Directory 的物件可以用來找出電腦網路網域中的資源，例如使用者、安全性原則、印表機、分散式元件和其他資源。
ms.assetid: 96f89537-9419-495e-819c-fd07ba546620
ms.tgt_platform: multiple
title: 建立和更新 Active Directory 物件
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0b36a12860ea2c2dc9085b784fdaf85cd95ab87f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106984192"
---
# <a name="creating-and-updating-active-directory-objects"></a><span data-ttu-id="d8b7a-103">建立和更新 Active Directory 物件</span><span class="sxs-lookup"><span data-stu-id="d8b7a-103">Creating and Updating Active Directory Objects</span></span>

<span data-ttu-id="d8b7a-104">Active Directory 的物件可以用來找出電腦網路網域中的資源，例如使用者、安全性原則、印表機、分散式元件和其他資源。</span><span class="sxs-lookup"><span data-stu-id="d8b7a-104">Active Directory objects can be used to locate resources in a computer network domain, such as users, security policies, printers, distributed components, and other resources.</span></span> <span data-ttu-id="d8b7a-105">您可以使用 WMI 來建立和更新 Active Directory 的物件。</span><span class="sxs-lookup"><span data-stu-id="d8b7a-105">Active Directory objects can be created and updated using WMI.</span></span> <span data-ttu-id="d8b7a-106">您可以使用 WMI 事件通知，在物件的新資訊變成可用時，更新 Active Directory 物件。</span><span class="sxs-lookup"><span data-stu-id="d8b7a-106">You can update an Active Directory object when new information about the object becomes available by using WMI event notification.</span></span> <span data-ttu-id="d8b7a-107">例如，建立 Active Directory 使用者物件之後，您可以使用 WMI 中的事件查詢來偵測其建立，而當收到事件時，您可以使用新的資訊來更新物件。</span><span class="sxs-lookup"><span data-stu-id="d8b7a-107">For example, once an Active Directory user object is created, you can detect its creation with an event query in WMI and when the event is received, you can update the object with new information.</span></span>

<span data-ttu-id="d8b7a-108">下列程式碼範例會建立類別的新 WMI 實例，以代表 Active Directory 使用者物件。</span><span class="sxs-lookup"><span data-stu-id="d8b7a-108">The following code example creates a new WMI instance of the class that represents the Active Directory user object.</span></span> <span data-ttu-id="d8b7a-109">此範例顯示如何將值指派給建立新的 Active Directory 使用者實例所需的各種屬性。</span><span class="sxs-lookup"><span data-stu-id="d8b7a-109">The example shows how to assign values to various properties required to create the new Active Directory user instance.</span></span>


```VB
Const cUserID = "WMIUser"
Const cComputerName = "LocalHost"
Const cWMInamespace = "root/directory/LDAP"
Const cWMIclass = "ds_user"

Const ADS_UF_ACCOUNTDISABLE = &h000002

Set objWMILocator = _
    CreateObject("WbemScripting.SWbemLocator")
objWMILocator.Security_.AuthenticationLevel = _
    wbemAuthenticationLevelDefault

Set objWMIServices = objWMILocator. _
    ConnectServer(cComputerName, cWMInamespace, "", "")

Set objWMIClass = objWMIServices.Get(cWMIclass)

Set objWMIInstance = objWMIClass.SpawnInstance_

objWMIInstance.DS_sAMAccountName = userID
objWMIInstance.ADSIPath = "LDAP://CN=" & userID & _
    ",CN=Users,DC=LissWare,DC=Net"

objWMIInstance.Put_ (wbemChangeFlagCreateOrUpdate Or _
    wbemFlagReturnWhenComplete)

WScript.Echo "Active Directory user created."
```



<span data-ttu-id="d8b7a-110">下列程式碼範例會更新 Active Directory 物件的 WMI 實例。</span><span class="sxs-lookup"><span data-stu-id="d8b7a-110">The following code example updates a WMI instance of an Active Directory object.</span></span> <span data-ttu-id="d8b7a-111">在此範例中，displayname 屬性已更新。</span><span class="sxs-lookup"><span data-stu-id="d8b7a-111">In this example, the displayname attribute is updated.</span></span>


```VB
set svc = getObject("Winmgmts:root\directory\ldap")

' A context object is used to tell the provider which
' specific properties are going to be updated.  
' In most cases, when you update a WMI object you do not
' need to specify an additional context object. 
' However,  if a context object is not supplied for a
' directory service provider, the update fails.

set octx = createobject( _
    "wbemscripting.swbemnamedvalueset")
octx.add "__PUT_EXT_PROPERTIES", array("ds_displayname")
octx.add "__PUT_EXTENSIONS", true
octx.add "__PUT_EXT_CLIENT_REQUEST", true


set objEnum = svc.execQuery( _
    "select * from ds_computer where ds_cn = 'userName'", "WQL", 32)

for each obj in objEnum
 obj.ds_DisplayName = "updatedName"
 obj.put_ 1, octx
next

WScript.Echo "Active Directory user successfully updated"
```



 

 



