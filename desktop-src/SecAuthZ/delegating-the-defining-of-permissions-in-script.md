---
description: 您可以將儲存在 Active Directory 中的授權原則存放區委派給管理。
ms.assetid: a7b43dfe-f03e-4795-bbd3-746eb3449fd0
title: 委派腳本中的許可權定義
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a9569f82271642a610919db8246cc6389daba309
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319599"
---
# <a name="delegating-the-defining-of-permissions-in-script"></a>委派腳本中的許可權定義

您可以將儲存在 Active Directory 中的授權原則存放區委派給管理。 系統管理可以委派給存放區、應用程式或範圍層級的使用者和群組。

每個層級都有一份系統管理員和讀者的清單。 存放區、應用程式或範圍的系統管理員可以讀取和修改委派層級的原則存放區。 讀取器可以讀取委派層級的原則存放區，但無法修改存放區。

屬於系統管理員或應用程式讀取者的使用者或群組，也必須新增為包含該應用程式之原則存放區的委派使用者。 同樣地，必須將屬於系統管理員或範圍讀取者的使用者或群組新增為包含該範圍之應用程式的委派使用者。

**委派範圍的管理**

1.  藉由呼叫包含範圍之 [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore)物件的 [**AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser)方法，將使用者或群組新增至包含範圍之存放區的委派使用者清單中。
2.  藉由呼叫包含範圍之 [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication)物件的 [**AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser)方法，將使用者或群組新增至包含範圍的應用程式的委派使用者清單中。
3.  藉由呼叫 [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope)物件的 [**AddPolicyAdministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator)方法，將使用者或群組新增至範圍的系統管理員清單。

> [!Note]  
> 以 XML 為基礎的原則存放區不支援任何層級的委派。

 

如果儲存在 Active Directory 中的授權存放內的範圍包含包含授權規則的授權規則或角色定義的工作定義，則無法委派該範圍。

下列範例顯示如何委派應用程式的管理。 此範例假設指定的位置有現有的 Active Directory 授權原則存放區，此原則存放區包含名為 Expense 的應用程式，且此應用程式未包含任何含有商務規則腳本的工作。


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, _
    "msldap://CN=MyStore,CN=Program Data,DC=authmanager,DC=com"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Add a delegated policy user to the store.
AzManStore.AddDelegatedPolicyUserName("ExampleDomain\\UserName")

'  Add the user as an administrator of the application.
expenseApp.AddPolicyAdministratorName("ExampleDomain\\UserName")

'  Save changes to the store.
AzManStore.Submit
```



 

 



