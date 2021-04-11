---
title: 當您產生參考時
description: 參考是目錄伺服器通訊的方式，它不包含完成查詢所需的資料，而是參考可能包含必要資料的伺服器。
ms.assetid: 2c11a52a-26e2-4a50-a0a3-5463a0852b27
ms.tgt_platform: multiple
keywords:
- 參考世代 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e47c1e172f3eaed34dad452aa46847980cd66f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842015"
---
# <a name="when-referrals-are-generated"></a>當您產生參考時

參考是目錄伺服器通訊的方式，它不包含完成查詢所需的資料，而是參考可能包含必要資料的伺服器。 請注意，參考不是由查詢要求所產生。

下列作業可能會導致一個或多個參考：

-   系結至不包含所要求之辨別名稱所指定之物件的伺服器，但其資料可能包含該物件的伺服器或網域。 在 ADSI 中，如果應用程式呼叫 [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject) 或 [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) 來系結至樹系中另一個網域 (內部參考) 或與樹系 (外部參考) 完全分開的命名內容，就會發生這種情況。 針對 LDAP API，執行加入、修改、刪除或搜尋作業時，可能會發生這種情況，此作業會指定存在於樹系中其他網域的物件 (內部參考) 或與樹系 (外部參考) 完全分開的命名內容。

    如果名稱解析在本機找不到物件，且該部分的命名空間沒有可 **交叉** 參考的物件，則網域控制站將嘗試根據辨別名稱的網域元件來建立外部參考。 例如，如果搜尋是以 "CN = a，CN = b，DC = c，DC = d，DC = e" 為基礎，網域控制站將會在 DNS 位址 "c." 上建立對 LDAP 伺服器的參考。

    所有 Windows 2000 網域控制站 (僅支援 DC = 命名上層元件) 彼此辨識，而且用戶端不需要外部交互參照，就能從一個樹系系結至另一個樹系。 如果其他非 Windows 2000 目錄伺服器（例如 Netscape 伺服器）使用 DC = 命名，並且在 DNS 中登錄了適當的 SRV RR，則也會獲得自動參考的優點。 如果不是，則必須手動加入外部 **交叉引用** 物件。

-   在包含樹系或次級外部網域、架構或設定容器之次級網域的網域上執行子樹搜尋。 將會建立從屬網域、外部網域、架構或設定容器的參考。 如果已啟用參考追蹤，對呼叫端的參考將會是透明的。

 

 