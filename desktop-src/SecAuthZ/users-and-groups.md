---
description: 說明授權管理員 API 中的使用者和群組定義。
ms.assetid: 783be0b2-7894-4780-900d-98918f824a04
title: 使用者和群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c40ee9234fa8d6259282855011cfc3fc008d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992186"
---
# <a name="users-and-groups"></a>使用者和群組

在授權管理員中，授權原則的收件者會以下列群組表示：

-   Windows 使用者和群組

    這些群組包含安全性主體的使用者、電腦和內建組。

-   LDAP 查詢群組

    這些群組中的成員資格會視需要從輕量型目錄存取協定 (LDAP) 查詢進行動態計算。 LDAP 查詢群組是一種應用程式群組。

-   基本應用程式群組

    這些群組是由 LDAP 查詢群組、Windows 使用者和群組，以及其他基本應用程式群組所組成。

## <a name="windows-users-and-groups"></a>Windows 使用者和群組

這些與整個 Windows 作業系統所使用的使用者和群組相同。

## <a name="ldap-query-groups"></a>LDAP 查詢群組

在授權管理員中，您可以使用 LDAP 查詢，將使用者的屬性與使用者在 Active Directory 中的物件相符。

例如，下列查詢會尋找每個成員，但不包括所有的。


```C++
(&(objectCategory=person)(objectClass=user)(!cn=andy))
```



下列查詢會在 www.fabrikam.com 中尋找某人別名的所有成員。


```C++
(memberOf=CN=someone,OU=litwareinc,DC=Fabrikam,DC=com)
```



## <a name="basic-application-groups"></a>基本應用程式群組

在授權管理員 API 中，應用程式群組是由 [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) 物件表示。 基本應用程式群組是一種應用程式群組。

若要定義基本的應用程式群組成員資格，請定義誰是成員，並定義誰不是成員。 這兩個步驟都是以相同的方式執行。 指定零個或多個 Windows 使用者和群組、先前定義的基本應用程式群組或 LDAP 查詢群組。 基本應用程式群組的成員資格是藉由從群組中移除任何非成員來計算。 授權管理員會在執行時間自動執行此程式。

基本應用程式群組中的 Nonmembership 優先于成員資格。

不允許迴圈成員資格定義;這些錯誤訊息會導致下列錯誤訊息：「無法新增擁有者。 發生下列問題：已偵測到迴圈。」

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 c + + 中定義使用者群組](defining-groups-of-users-in-c--.md)
</dt> </dl>

 

 



