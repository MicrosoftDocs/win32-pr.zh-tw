---
title: 查詢使用者
description: 若要查詢使用者，查詢必須包含搜尋運算式 \ 0034; ( (objectClass 使用者)  (objectCategory person) ) \ 0034;。
ms.assetid: a9f12de4-e1e2-41bb-b2cc-ff9c9fa1c39a
ms.tgt_platform: multiple
keywords:
- 使用者廣告，查詢使用者
- Active Directory、使用、使用者、查詢使用者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ae6939cef858c3dfc108611a1b0e7ab0367c302a091ca436c9c69b2fb5277b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025316"
---
# <a name="querying-for-users"></a>查詢使用者

若要查詢使用者，查詢必須包含搜尋運算式 " (& (objectClass = user)  (objectCategory = person) ) "。

由於 computer 類別是使用者的子類別，因此只包含 (objectClass = user) 的查詢會傳回使用者物件和電腦物件。 此外，使用者物件的物件類別是 person (不是使用者) ;因此， (objectCategory = user) 的運算式不會傳回任何使用者。 如果您使用運算式 (objectCategory = person) ，查詢會傳回使用者物件和 contact 物件。

使用者可以放在網域的任何容器或組織單位中，也可以放在網域的根目錄中。 這表示使用者可以位於目錄階層中的多個位置。 您可以執行 " (objectCategory = user) " 的深層搜尋，以尋找容器、組織單位、網域、網域樹狀結構或樹系中的所有使用者，視您所使用的 [**>idirectorysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) 指標所系結至的物件而定。

 

 