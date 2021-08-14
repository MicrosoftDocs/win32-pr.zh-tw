---
title: 搜尋定義域內容
description: 在討論要系結到何處開始搜尋網域中的物件之前，請先瞭解資料如何儲存在 Active Directory Domain Services 中。
ms.assetid: fd0b4556-465b-4338-87cb-375450590c44
ms.tgt_platform: multiple
keywords:
- 網域內容 Active Directory
- 搜尋定義域內容 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51f775e199cd269eec8a67054ca26bcd69e11eacaa6436781f4481083d11e60d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118183866"
---
# <a name="searching-domain-contents"></a>搜尋定義域內容

在討論要系結到何處開始搜尋網域中的物件之前，請先瞭解資料如何儲存在 Active Directory Domain Services 中。

如果您有一個具有多個網域的樹系，Active Directory Domain Services 不會將所有物件資料儲存在單一網域控制站上，因為效能、擴充性和可靠性的原因。 網域控制站只會保存其所屬網域的所有資訊 (它具有網域) 的完整複本。 但網域控制站不會保存任何其他網域的完整資訊。

如果您系結至已關閉參考追蹤的網域物件，則可以搜尋該網域中的任何物件，而且只搜尋該網域。 如需有關參考追蹤的詳細資訊，請參閱 [參考](referrals.md)。 搜尋可以取得任何屬性，而且可以使用包含任何屬性的查詢篩選準則。

在樹系中，網域會以階層方式排列為網域樹狀結構。 網域樹狀結構可以是單一網域或具有一個或多個子網域的網域。 這些子域接著可以有子定義域。 網域樹狀結構也是連續的命名空間。 連續的命名空間表示子定義域是命名階層的接續。 例如，網域 fabrikam.com (或 DC = Fabrikam，DC = COM) 可以有一個名為 mydivision (mydivision.fabrikam.com 或 DC = mydivision，DC = Fabrikam，DC = COM) 的子域，而該網域接著可能會有一個名為 mydev 的子域 (mydev.mydivision.fabrikam.com 或 DC = mydev，DC = mydivision，DC = Fabrikam，DC = COM) 。

如果您系結至網域物件 (並針對網域樹狀結構中的網域開啟) 的參考追蹤，您將會在其中搜尋該網域和整個階層。 搜尋可以取得任何屬性，而且可以使用包含任何屬性的查詢篩選準則。

如果網域控制站只包含其專屬網域的完整複本，您可以在網域樹狀目錄上執行子樹搜尋。 網域保存其子定義域的參考。 當網域控制站針對其本身的網域處理子樹搜尋要求時，網域控制站會搜尋該網域，然後將對其每個子域的參考傳回給用戶端。 參考是指目錄伺服器通訊的方式，它不包含完成要求所需的資訊 (例如查詢) 但是參考可能包含必要資訊的伺服器。 在樹系搜尋網域樹狀結構的案例中，會傳回每個直接子域的參考，以便在每個子網域中的網域控制站繼續搜尋。 如果開啟了參考追蹤，LDAP 用戶端程式庫 (Wldap32.dll) 會使用這些參照來系結至每個子網域中的網域控制站，然後繼續搜尋。 如果關閉了參考追蹤，LDAP 用戶端便無法解析參考，且搜尋已完成。

如果子域的網域控制站連線速度很慢，子樹會在已開啟參考追蹤的網域樹狀目錄上搜尋，可能會很耗時。 如果您只想要搜尋單一網域，您應該關閉參考追蹤，以避免不必要地搜尋子域。

 

 




