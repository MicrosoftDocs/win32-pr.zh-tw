---
description: 憑證的數目、憑證撤銷清單 (Crl) ，以及使用者集合中 (Ctl) 的憑證信任清單成長時，這些憑證的組織就會變成問題。
ms.assetid: 13e7e077-e8be-4ba4-99e1-08421fd2452e
title: 集合存放區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66d783aafe6d0ff22cd990195f6bce5ce433f2f01595bed2cf20c5c41ea3a24e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876910"
---
# <a name="collection-stores"></a>集合存放區

[*憑證的數目、*](../secgloss/c-gly.md)[*憑證撤銷清單*](../secgloss/c-gly.md) (crl) ，以及使用者集合中 (ctl) 的 [*憑證信任清單*](../secgloss/c-gly.md)成長時，這些憑證的組織就會變成問題。 其中一個可能的解決方法是建立不同的憑證存放區，以保留不同類型的憑證。 此解決方案會建立新的問題，因為應用程式可能需要搜尋數個不同的商店來尋找特定的憑證。 使用邏輯或集合存放區可解決此問題。

[*邏輯存放區*](../secgloss/l-gly.md)和集合憑證存放區是以單一存放區形式出現在應用程式中的實體存放區群組。 您可以使用對 [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) 或 [**CertEnumCertificatesInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore)的單一函數呼叫來搜尋或列舉邏輯或集合存放區的所有成員存放區。

使用「邏輯」或「收集」存放區也可提供難以使用紙張記錄來達成的彈性。 單一實體存放區中的憑證可能必須是數個不同邏輯群組的成員。 因此，個別的實體存放區可以是一個以上的邏輯或集合存放區成員，如下圖所示。

![集合存放區](images/mancert.png)

下圖顯示下列基本的邏輯憑證存放區概念：

-   集合憑證存放區有指向該集合存放區之第一個指標區塊的指標。
-   集合存放區的每個指標區塊都有指向同級存放區的指標，以及該集合下一個指標區塊的指標。
-   集合中的每個同級存放區都是簡單的實體憑證存放區。
-   簡單的憑證存放區可以是許多不同收集存放區中的成員同級存放區。
-   新增至集合存放區的憑證會實際新增至集合中的其中一個同級存放區。
-   在同級存放區中的憑證，可以由任何屬於該成員的集合存放區存取。

收集存放區是在應用程式內建立的，方法是使用 [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) 開啟集合存放區，然後使用 [**CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection) 將開啟的同級存放區加入至集合存放區。 您可以藉由呼叫 [**CertRemoveStoreFromCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certremovestorefromcollection)，從集合存放區刪除同級存放區。

 

 
