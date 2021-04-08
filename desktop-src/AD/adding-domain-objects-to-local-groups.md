---
title: 將網域物件新增至本機群組
description: 屬於網域的使用者和群組可以新增至本機電腦上的群組，以將許可權授與該特定電腦上的網域使用者或群組。
ms.assetid: 07287190-88a1-4d4d-a91c-1e95d9903a4d
ms.tgt_platform: multiple
keywords:
- Active Directory 範例 Active Directory，將網域物件新增至本機群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52e956d1cf076f4c33c46700e52798463b7e1d2c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681698"
---
# <a name="adding-domain-objects-to-local-groups"></a>將網域物件新增至本機群組

當成員伺服器或在 Windows 2000 Professional 上執行的電腦是 Windows 2000 網域的成員時，屬於該網域的使用者和群組可以新增至本機電腦上的群組，以授與該特定電腦上網域使用者或群組的許可權。

使用 ADSI 管理 Windows 2000 網域上的網域本機群組時，通常會使用 LDAP 提供者。 不過，在成員伺服器上管理本機群組和執行 Windows 2000 Professional 的電腦時，必須使用 WinNT 提供者。

只有本機群組可以在成員伺服器和 Windows 2000 Professional 上建立。 不過，本機群組可包含：

-   樹系中的通用和全域群組，其中包含電腦所屬的網域。
-   來自該電腦網域的網域本機群組。
-   樹系中任何網域的使用者。

**將網域物件新增至本機群組**

1.  系結至電腦的 [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) 介面，其中包含要新增成員的本機群組。 系結必須使用具有足夠許可權的帳戶來執行，才能存取該電腦。 系結字串的格式必須是 "WinNT:// <computer name> ，computer"，其中 " &lt; computer name &gt; " 是要新增成員的電腦群組名。 "，Computer" 參數會指示 ADSI 系結至電腦。 ADSI 會將此資料公開給 WinNT 提供者的剖析器，讓它可以略過一些明確的解析查詢，以判斷您要系結到的物件類型。 這可以讓使用者有5到20秒的時間來解決不明確的問題。
2.  使用 [**IADsContainer**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) 做為類別的 "group"，並使用本機群組名稱作為要系結至群組的物件名稱。
3.  系結至將加入成員之本機群組的 [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) 介面。
4.  以 "WinNT://" 形式來建立要新增至本機群組之物件的 ADsPath <domain> / <name> ，其中 " &lt; domain &gt; " 是包含要加入之物件的功能變數名稱，而 " &lt; name &gt; " 是要加入之物件的名稱。
5.  使用 [**IADsGroup**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) 將使用者或群組新增至本機群組，並傳遞在步驟4中所建立的 ADsPath。

如需詳細資訊和示範如何將網域使用者或群組物件新增到本機群組的程式碼範例，請參閱 [將網域使用者或群組新增至本機群組的範例程式碼](example-code-for-adding-a-domain-user-or-group-to-a-local-group.md)。

 

 