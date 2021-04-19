---
title: " (AD DS) 的推薦"
description: Active Directory Domain Services 在設定容器中的資料分割容器 (crossRefContainer) 中，維護所儲存之交叉參考物件中的參考資料。
ms.assetid: e4d6cc8a-9c2c-4e0f-acca-e9ecdd5e879b
ms.tgt_platform: multiple
keywords:
- 參考廣告
- Active Directory，推薦
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63c87fb0248d85ab20191296f9659eb58e460f6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "106965637"
---
# <a name="referrals-ad-ds"></a> (AD DS) 的推薦

Active Directory Domain Services 在設定容器中的資料分割容器 ([**crossRefContainer**](/windows/desktop/ADSchema/c-crossrefcontainer)) 中，維護所儲存之 [**交叉**](/windows/desktop/ADSchema/c-crossref)參考物件中的參考資料。 在 [決定要搜尋的位置](where-to-search.md) 主題時，會在域樹內的網域內容中討論參考，以及在子樹搜尋上產生從屬網域的參考。

Active Directory Domain Services 建立和維護樹系中所有網域的 [**交叉引用**](/windows/desktop/ADSchema/c-crossref) 物件。 此外，也有設定和架構容器的 **交叉引用** 物件。 這些 **交叉** 參考物件可用來產生參考，以回應要求有關樹系中之物件的資料，但不包含在處理要求的目錄伺服器上的查詢。 這些稱為 *內部交互參考*，因為它們參考樹系內的網域、架構和設定容器。

如果未啟用參考追蹤，且執行子樹搜尋，則搜尋會傳回符合搜尋準則之指定網域內的所有物件。 搜尋也會將參考傳回給任何屬於目錄伺服器網域的直接下階的次級網域。 用戶端必須藉由系結至參考所指定的路徑並提交另一個查詢，來解析參考。

如果開啟了參考追蹤並執行子樹搜尋，則基礎 LDAP API 會自動嘗試系結至任何參考，並將搜尋結果新增至結果集。 在大多數情況下，呼叫端的參考追蹤將會是透明的。 如果是參考不同網域或樹系中的物件，基礎 LDAP API 將會嘗試使用目前的認證來系結至參考的目標。 如果成功，則參考追蹤將會是透明的。 如果不成功，則會傳回參考和參考錯誤碼。

如需設定「參考追蹤」搜尋喜好設定的詳細資訊，請參閱 [指定其他搜尋選項](specifying-other-search-options.md)。

除了 [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) (網域的 DNS 名稱) 和 [**nCName**](/windows/desktop/ADSchema/a-ncname) (網域) 屬性的分辨名稱之外，[**交叉引用**](/windows/desktop/ADSchema/c-crossref)物件也包含網域 (的 **nETBIOSName**) NetBIOS 名稱，以及代表網域的直接父系網域 (屬性之 **交叉引用** 物件的 **trustParent**) 辨別名稱。

Active Directory Domain Services 也可以有參考樹系外部物件的 *外部交互參考* 。 外部交互參照必須由系統管理員明確加入。 請注意，外部交互參考的目標伺服器必須有 DNS 根目錄;也就是說，它必須遵守 RFC 2247。

外部交互參考是指任何其他樹系上的物件，只要名稱在目標樹系中是唯一的。 例如，貴公司所使用的 LDAP 用戶端應用程式可以將作業提交至您的目錄伺服器以進行 Fabrikam.com。 您可以建立 Fabrikam.com 的 [**交叉引用**](/windows/desktop/ADSchema/c-crossref) 物件。 現在，您的目錄伺服器可以將參考傳回給 Fabrikam.com 網域中的物件，而用戶端可以重新尋找參考，而不是傳回「找不到物件」錯誤。 例如，如果您有一個具有下列辨別名稱的物件：


```C++
CN=SomeObject,OU=SomeOU,DC=Fabrikam,DC=Com
```



您可以為名稱為 "ChildOfSomeObject" 的物件加入外部交互參考。


```C++
CN=ChildOfSomeObject,CN=SomeObject,OU=SomeOU,DC=Fabrikam,DC=Com
```



包含 "SomeObject" 的子樹搜尋也會傳回 "ChildOfSomeObject" 的參考。 請注意，在參照所指定的位址上必須有 LDAP 伺服器 ([**交叉**](/windows/desktop/ADSchema/c-crossref) 參考物件) 的其中一個屬性，而且此 ldap 伺服器必須提供 "ChildOfSomeObject" 所識別的命名空間。

由於 [**交叉引用**](/windows/desktop/ADSchema/c-crossref) 物件儲存在設定容器中，因此每個網域控制站 (DC) 都有所有 **交叉交叉** 物件的複本。 因此，每個 DC 都包含樹系中每個網域以及其高階/附屬關聯性的相關資料。 這可讓每個 DC 為樹系中的任何網域產生參考，以及在子樹搜尋上未探索從屬網域、架構或設定容器的參考。

如需有關參考的詳細資訊，請參閱：

-   [當您產生參考時](when-referrals-are-generated.md)
-   [建立外部參考](creating-an-external-referral.md)

如需詳細資訊和示範如何取得分割區容器之辨別名稱的程式碼範例，請參閱 [尋找分割區容器的範例程式碼](example-code-for-locating-the-partitions-container.md)。

 

 