---
title: 在組織單位中建立新的使用者
description: Terry Adams 是雇用 Fabrikam 銷售組織。 他的直接報告是一 Hines 的派翠克。
ms.assetid: bc31ed04-e505-4d64-9fa3-d06af7351db0
ms.tgt_platform: multiple
keywords:
- 在組織單位中建立新的使用者 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76d62c8d95e7d5e421fc562e38716477ff2dfb8f4097d4652710e2c50715487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118180113"
---
# <a name="creating-new-users-in-the-organizational-unit"></a>在組織單位中建立新的使用者

Terry Adams 是雇用 Fabrikam 銷售組織。 他的直接報告是一 Hines 的派翠克。

如下列程式碼範例所示，Joe Andreshak 企業系統管理員會為他建立新的帳戶。


```VB
Dim salesOU as IADsContainer
Set salesOU = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")
Set usr = salesOU.Create("user", "CN=Terry Adams")
usr.Put "sAMAccountName", "terryadams"
usr.Put "userPrincipalName", "terryadams@fabrikam.com" 
usr.Put "title" "Marketing Manager"
usr.SetInfo

usr.SetPassword "seahorse"
usr.AccountDisabled = False
usr.SetInfo
```



建立新的使用者時，您必須指定 **sAMAccountName**。 這是使用者類別的必要屬性。 在可以建立物件的實例之前，必須先設定所有必要的屬性。 如果未指定新使用者的 SAMAccountName，則會自動產生 **sAMAccountName** 。

建立新的使用者時，必須先在本機快取中設定所有必要的屬性，然後再呼叫 [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) 方法。

Joe 是系統管理員，可以使用 [**IADsUser. SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) 方法指派 Terry 的密碼。 在呼叫 [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo)方法之前， **IADsUser. SetPassword** 方法將無法運作。

然後，Joe 將 [**IADsUser. AccountDisabled**](iadsuser-property-methods.md) 屬性設定為 **FALSE**，以啟用使用者帳戶。

下列程式碼範例示範如何將 Terry 設定為派翠克的經理。


```VB
Set usr = GetObject("LDAP://CN=patrickhines,OU=Sales,DC=Fabrikam,DC=COM")
usr.Put "manager", "CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM"
usr.SetInfo
```



您可能會想要知道 Terry 變更他的姓名、移至不同的組織或離開公司時，會發生什麼事。 神秘維護此管理員-直接報告連結？ 如需詳細資訊，以及此問題的解決方法，請參閱 [重組](reorganization.md)。 因為 Active Directory 架構是可擴充的，所以您可以建立物件的模型，以包含類似的管理員直接報表樣式關聯性。

在繼續進行下一項工作之前，請先查看程式碼範例，其中顯示 Joe 如何審視 Terry 的直屬員工。


```VB
Set usr = GetObject("LDAP://CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM")
reports = usr.GetEx ("directReports")

For each directReport in reports
    Debug.Print directReport
Next
```



在此程式碼範例中，即使從未修改過 **directReports** 屬性，還是會顯示 Terry 的直接報表。 Active Directory 會自動執行此功能。

在目錄世界中，屬性可以有單一或多個值。 因為 **directReports** 有多個值，所以您可以藉由查看架構來取得這項資訊，因此使用 [**IADs GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) 方法會比較容易，因為它會傳回值的陣列，而不論是否傳回單一或多個值。

Active Directory 消費者和電腦嵌入式管理單元可讓您在使用者的 [屬性] 頁面上，查看直接報表和管理員關聯性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將使用者新增至群組](adding-users-to-a-group.md)
</dt> </dl>

 

 




