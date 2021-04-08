---
title: 查詢網域中的群組
description: 群組可以放在網域的任何容器或組織單位中，也可以放在網域的根目錄中。
ms.assetid: 338a93dd-445d-4f74-a6d6-e5c8ba2e765e
ms.tgt_platform: multiple
keywords:
- 查詢網域 AD 中的群組
- 群組 AD，查詢網域中的群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a3abd4ec393fbeca1308ed59e08131b9b73e6b1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842036"
---
# <a name="querying-for-groups-in-a-domain"></a>查詢網域中的群組

群組可以放在網域的任何容器或組織單位中，也可以放在網域的根目錄中。 群組不一定會位於一個容器中。 因此，必須搜尋整個網域以尋找網域中的所有群組。

若要搜尋網域中的所有群組，請將搜尋起點設定為網域的根目錄、將搜尋範圍設定為子樹，並搜尋具有 [**objectClass**](/windows/desktop/ADSchema/a-objectclass) 值 "group" 的所有物件。

如果必須找到包含特定 [**ADS \_ 群組 \_ 類型 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) 值的群組，則可以使用 **LDAP \_ 比對 \_ 規則 \_ 位 \_ 和比** 對規則運算子來搜尋在 [**groupType**](/windows/desktop/ADSchema/a-grouptype) 屬性中設定特定位的群組。 如需使用相符規則的詳細資訊，請參閱 [搜尋篩選語法](/windows/desktop/ADSI/search-filter-syntax)。

如需詳細資訊和示範如何在定義域中搜尋群組的程式碼範例，請參閱 [在網域中搜尋群組的範例程式碼](example-code-for-performing-a-query-in-a-domain.md)。

 

 