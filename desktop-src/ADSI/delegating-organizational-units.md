---
title: 委派組織單位
description: Fabrikam 公司雇用兩位系統管理員（Mike 和 Paul），分別管理東部和西部組織單位。
ms.assetid: ecf71ae6-9b6f-4e3c-878a-2c6fd193da33
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9928884c8be19f9668d6f81ed9462f6fb757286f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "107001061"
---
# <a name="delegating-organizational-units"></a>委派組織單位

Fabrikam 公司雇用兩位系統管理員（Mike 和 Paul），分別管理東部和西部組織單位。 Joe 將他的管理責任委派給他們，讓他們可以在各自的組織單位中建立和刪除使用者。

在瞭解如何在 Mike 和 Paul 下設定這些組織單位之前，您必須瞭解如何在 Active Directory 中設定物件的存取權。 Active Directory 中的每個物件都有安全描述項。 有了安全描述項，您就可以修改物件的許可權、傳播許可權、啟用審核等等。 安全描述項本身有兩個存取控制清單 (Acl) ：任意 ACL (DACL) 和系統 ACL (SACL) 。 每個 ACL 可以包含 (Ace) 的存取控制專案。 您可以使用 ACE 來設定物件的允許或拒絕存取。 此外，您可以指定要允許或拒絕的特定動作。 動作範例包括「建立子系」、「刪除子系」、「讀取屬性」和「寫入」屬性。 這些許可權是使用 [**AccessMask**](iadsaccesscontrolentry-property-methods.md)指定的。

接著，您可以指定與此 ACE 相關聯的類別或屬性。 在接下來的 Fabrikam 範例中，Joe 挑選使用者類別，讓每位系統管理員可以將使用者新增至系統。 接下來，您必須回答下列問題：「誰將是此 ACE 的受益人？」 Joe 將指定 Mike。

最後，您可以設定 ACE 繼承行為，例如，您可以指定 Ace 來向下傳播階層。 總而言之，上述範例將會導致 Mike 能夠在東部銷售組織單位下建立和刪除使用者物件。

Joe 使用下列程式碼範例，在東部組織單位上設定 Ace 和 Acl。


```VB
Set ou = GetObject("LDAP://OU=East, OU=Sales, DC=Fabrikam,DC=COM")
Set sec = ou.Get("ntSecurityDescriptor")
Set acl = sec.DiscretionaryAcl

Set ace = CreateObject("AccessControlEntry") 
' You can also use Set ace = new ADsAccessControlEntry.

' Grant access to the object.
ace.AceType = ADS_ACETYPE_ACCESS_ALLOWED_OBJECT 

' Create and delete child objects.
ace.AccessMask = ADS_RIGHT_DS_CREATE_CHILD Or ADS_RIGHT_DS_DELETE_CHILD 
' Create the user object with the user schema IDGUID.
ace.ObjectType = "{BF967ABA-0DE6-11D0-A285-00AA003049E2}" 
' Propagate the ACE down.  
ace.AceFlags = ADS_ACEFLAG_INHERIT_ACE
' Provide an option that notifies that the objectType is filled.
ace.Flags = ADS_FLAG_OBJECT_TYPE_PRESENT 
' Show the beneficiary of this ACE.
ace.Trustee = "FABRIKAM\Mike" 
acl.AddAce ace

sec.DiscretionaryAcl = acl
ou.Put "ntSecurityDescriptor", Array(sec)
' Use SetInfo to commit the data to Active Directory.
ou.SetInfo 

' Release the objects.
Set ace = Nothing
Set acl  = Nothing
Set sec = Nothing
```



下圖顯示在程式碼執行之後 Active Directory **建立新的視圖** 功能表。 當 Joe （系統管理員）登入時，他看到了數個可以建立的類別。 不過，當 Mike 登入時，他只能夠建立使用者物件。

![建立新的視圖選項功能表](images/adadsi5.png)

如需詳細資訊，請參閱 [ADSI 安全性模型](adsi-security-model.md)。

 

 




