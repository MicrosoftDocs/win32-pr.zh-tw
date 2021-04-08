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
# <a name="querying-for-groups-in-a-domain"></a><span data-ttu-id="b1704-105">查詢網域中的群組</span><span class="sxs-lookup"><span data-stu-id="b1704-105">Querying for Groups in a Domain</span></span>

<span data-ttu-id="b1704-106">群組可以放在網域的任何容器或組織單位中，也可以放在網域的根目錄中。</span><span class="sxs-lookup"><span data-stu-id="b1704-106">Groups can be placed in any container or organizational unit in a domain as well as the root of the domain.</span></span> <span data-ttu-id="b1704-107">群組不一定會位於一個容器中。</span><span class="sxs-lookup"><span data-stu-id="b1704-107">Groups may not always be in one container.</span></span> <span data-ttu-id="b1704-108">因此，必須搜尋整個網域以尋找網域中的所有群組。</span><span class="sxs-lookup"><span data-stu-id="b1704-108">Therefore, it is necessary to search the entire domain to find all groups in the domain.</span></span>

<span data-ttu-id="b1704-109">若要搜尋網域中的所有群組，請將搜尋起點設定為網域的根目錄、將搜尋範圍設定為子樹，並搜尋具有 [**objectClass**](/windows/desktop/ADSchema/a-objectclass) 值 "group" 的所有物件。</span><span class="sxs-lookup"><span data-stu-id="b1704-109">To search for all groups in a domain, set the search start point to the root of the domain, set the search scope to subtree and search for all objects that have an [**objectClass**](/windows/desktop/ADSchema/a-objectclass) value of "group".</span></span>

<span data-ttu-id="b1704-110">如果必須找到包含特定 [**ADS \_ 群組 \_ 類型 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) 值的群組，則可以使用 **LDAP \_ 比對 \_ 規則 \_ 位 \_ 和比** 對規則運算子來搜尋在 [**groupType**](/windows/desktop/ADSchema/a-grouptype) 屬性中設定特定位的群組。</span><span class="sxs-lookup"><span data-stu-id="b1704-110">If groups that contain particular [**ADS\_GROUP\_TYPE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) values must be found, the **LDAP\_MATCHING\_RULE\_BIT\_AND** matching rule operator can be used to search for groups that have particular bits set in the [**groupType**](/windows/desktop/ADSchema/a-grouptype) attribute.</span></span> <span data-ttu-id="b1704-111">如需使用相符規則的詳細資訊，請參閱 [搜尋篩選語法](/windows/desktop/ADSI/search-filter-syntax)。</span><span class="sxs-lookup"><span data-stu-id="b1704-111">For more information about using matching rules, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span>

<span data-ttu-id="b1704-112">如需詳細資訊和示範如何在定義域中搜尋群組的程式碼範例，請參閱 [在網域中搜尋群組的範例程式碼](example-code-for-performing-a-query-in-a-domain.md)。</span><span class="sxs-lookup"><span data-stu-id="b1704-112">For more information and a code example that shows how to search for groups in a domain, see [Example Code for Searching for Groups in a Domain](example-code-for-performing-a-query-in-a-domain.md).</span></span>

 

 