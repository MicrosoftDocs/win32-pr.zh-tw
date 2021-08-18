---
title: 決定要搜尋的位置
description: 本主題說明可以在 Active Directory Domain Services 中執行的不同搜尋。
ms.assetid: 4b7428c8-c246-41fc-8811-892220c4270f
ms.tgt_platform: multiple
keywords:
- 決定要在哪裡搜尋 AD
- Active Directory AD、搜尋、決定要搜尋的位置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6984a79bb761c1926b6735a91209c9f387ac45619ffc752daef253a74f5e587a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024316"
---
# <a name="deciding-where-to-search"></a>決定要搜尋的位置

本主題說明可以在 Active Directory Domain Services 中執行的不同搜尋。

所有搜尋都是在下列其中一個命名內容中執行：

-   網域，包括應用程式目錄分割
-   架構容器
-   設定容器
-   通用類別目錄

## <a name="searching-a-domain"></a>搜尋定義域

網域包含大部分高度使用的物件，例如使用者、連絡人、群組、組織單位、電腦等等。 大部分的查詢都會搜尋網域。 如需搜尋網域的詳細資訊，請參閱 [搜尋定義域內容](searching-domain-contents.md)。

## <a name="searching-the-schema-container"></a>搜尋架構容器

架構容器包含 [**classSchema**](/windows/desktop/ADSchema/c-classschema) 和 [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) 物件，這些物件會提供可存在於 Active Directory Domain Services 中的每個類別和屬性的正式定義。 若要搜尋架構容器中的物件，請系結至任何網域控制站上的架構容器。 架構容器可在所有網域控制站上使用。 架構容器的分辨名稱是從 rootDSE 的 **schemaNamingCoNtext** 屬性取得。 如需 rootDSE 和 **schemaNamingCoNtext** 屬性的詳細資訊，請參閱 [無伺服器系結和 rootDSE](serverless-binding-and-rootdse.md)。

如需有關從架構或抽象架構容器讀取的詳細資訊，請參閱系結 [至架構的指導方針](guidelines-for-binding-to-the-schema.md)。

## <a name="searching-the-configuration-container"></a>搜尋設定容器

Configuration 容器包含整個樹系的設定資訊，例如網站、服務和顯示規範。 若要搜尋設定容器中的物件，請系結至任何網域控制站上的設定容器。 Configuration 容器可在所有網域控制站上使用。 設定容器的分辨名稱是從 rootDSE 的 **configurationNamingCoNtext** 屬性取得。 如需 rootDSE 和 **configurationNamingCoNtext** 屬性的詳細資訊，請參閱 [無伺服器系結和 rootDSE](serverless-binding-and-rootdse.md)。

## <a name="searching-the-global-catalog"></a>搜尋通用類別目錄

通用類別目錄會在 Active Directory Domain Services 中保存每個物件的複本，但其屬性只有少數幾個。 通用類別目錄中的屬性是搜尋作業中最常使用的屬性，例如使用者的名字和姓氏、登入名稱等等。 如需有關搜尋通用類別目錄的詳細資訊，請參閱 [搜尋通用類別目錄](searching-global-catalog-contents.md)。

 

 