---
title: 建立組織單位
description: 現在您已有網域物件，可以開始建立組織單位。
ms.assetid: c9955b44-5ca1-4b4b-85c8-e0d55a4304ca
ms.tgt_platform: multiple
keywords:
- 建立組織單位 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78ec0da1efe78d54eba8bc0dc05a998717aaf91f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931849"
---
# <a name="creating-an-organizational-unit"></a>建立組織單位

現在您已有網域物件，可以開始建立組織單位。 Fabrikam 有兩個部門：銷售和生產。 公司計畫雇用兩部 Windows 2000 系統管理員來管理每個部門。 Joe Worden 是企業系統管理員，將在 Fabrikam 網域下建立兩個新的組織單位。 藉由建立組織單位，Joe 可以將多個物件群組在一起，讓其他人管理這些物件。 下列程式碼範例會建立 (OU) 的銷售組織單位。


```VB
Dim dom as IADsContainer
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
Set salesOrg = dom.Create("organizationalUnit", "OU=Sales")
salesOrg.Put "description", "Sales Headquarter,SF"
salesOrg.Put "wwwHomePage", "https://fabrikam.com/sales"
salesOrg.SetInfo
```



[**IADsContainer**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create)方法會接受類別名稱和新物件的名稱。 此時不會將物件認可至 Active Directory。 不過，您在用戶端上將會有 ADSI/COM 物件參考。 使用這個 ADSI 物件，您可以使用 [**IADs**](/windows/desktop/api/Iads/nf-iads-iads-put) 方法來設定或修改屬性。 **IADs** 方法會接受屬性名稱和屬性的值。 但是，不會對目錄認可任何內容;所有專案都會在用戶端快取。 當您呼叫 [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) 方法時，就會將變更（在此案例中為物件建立和屬性修改）認可至目錄。 這些變更都是交易的，也就是說，您會看到新的物件具有您設定的所有屬性，或完全沒有物件。

您也可以嵌套組織單位。 下列程式碼範例假設銷售部門會進一步細分為東部和西部區域。


```VB
Set east = salesOrg.Create("organizationalUnit", "OU=East")
east.SetInfo
```



這也適用于西部區域。

若要直接系結至銷售組織中的東部區域，請指定辨別名稱。


```VB
Set east = GetObject("LDAP://OU=East,OU=Sales,DC=Fabrikam,DC=COM")
Debug.Print east.Get "description"
east.Put "wwwHomePage", "https://fabrikam.com/sales/east"
```



如果您已經系結至父物件 (Sales) ，您可以使用子物件的相對名稱，系結至父物件 (東部) 的子物件。


```VB
Set east = salesOU.GetObject("organizationalUnit", "OU=East")
```



若要確定已建立物件，請使用 Active Directory 消費者和電腦 MMC 嵌入式管理單元來查看新的組織單位。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將現有的使用者移至組織單位](moving-existing-users-to-the-organizational-unit.md)
</dt> </dl>

 

 




