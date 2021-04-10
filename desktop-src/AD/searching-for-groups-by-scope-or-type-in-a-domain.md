---
title: 依範圍或輸入網域來搜尋群組
description: 在 Windows 2000 網域中，有一個名為 [群組] 的類別，用於所有群組範圍 (網域本機、全域、通用) 和類型 (安全性、散發) 。
ms.assetid: e32629d9-aa62-4953-aa49-43af726b7deb
ms.tgt_platform: multiple
keywords:
- 依網域 AD 中的範圍或類型搜尋群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ee9aae5e2c7be7b9cba590f9bc80f0517bca918
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681639"
---
# <a name="searching-for-groups-by-scope-or-type-in-a-domain"></a><span data-ttu-id="80688-104">依範圍或輸入網域來搜尋群組</span><span class="sxs-lookup"><span data-stu-id="80688-104">Searching for Groups by Scope or Type in a Domain</span></span>

<span data-ttu-id="80688-105">在 Windows 2000 網域中，有一個名為 [ [**群組**](/windows/desktop/ADSchema/c-group) ] 的類別，用於所有群組範圍 (網域本機、全域、通用) 和類型 (安全性、散發) 。</span><span class="sxs-lookup"><span data-stu-id="80688-105">In Windows 2000 domains, there is single class called [**group**](/windows/desktop/ADSchema/c-group) for all group scopes (Domain Local, Global, Universal) and types (security, distribution).</span></span> <span data-ttu-id="80688-106">Group 物件的 [**groupType**](/windows/desktop/ADSchema/a-grouptype) 屬性會指定群組類型和範圍。</span><span class="sxs-lookup"><span data-stu-id="80688-106">The [**groupType**](/windows/desktop/ADSchema/a-grouptype) attribute of the group object specifies the group type and scope.</span></span>

<span data-ttu-id="80688-107">若要使用類型或範圍來搜尋 Windows 2000 網域上的群組，請使用包含 [**groupType**](/windows/desktop/ADSchema/a-grouptype) 屬性之相符規則的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="80688-107">To use type or scope to search for groups on Windows 2000 domains, use a filter that contains a matching rule for the [**groupType**](/windows/desktop/ADSchema/a-grouptype) attribute.</span></span> <span data-ttu-id="80688-108">如需相符規則的詳細資訊，請參閱 [搜尋篩選語法](/windows/desktop/ADSI/search-filter-syntax)。</span><span class="sxs-lookup"><span data-stu-id="80688-108">For more information about matching rules, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span>

<span data-ttu-id="80688-109">如需詳細資訊和示範如何在定義域中搜尋群組的程式碼範例，請參閱 [在網域中搜尋群組的範例程式碼](example-code-for-performing-a-query-in-a-domain.md)。</span><span class="sxs-lookup"><span data-stu-id="80688-109">For more information and a code example that shows how to search for groups in a domain, see [Example Code for Searching for Groups in a Domain](example-code-for-performing-a-query-in-a-domain.md).</span></span>

## <a name="example-ldap-query-strings"></a><span data-ttu-id="80688-110">範例 LDAP 查詢字串</span><span class="sxs-lookup"><span data-stu-id="80688-110">Example LDAP Query Strings</span></span>

<span data-ttu-id="80688-111">下列查詢字串範例顯示如何建立用來搜尋或篩選特定群組類型的 LDAP 查詢字串。</span><span class="sxs-lookup"><span data-stu-id="80688-111">The following query string examples show how to construct an LDAP query string used to search for or filter specific group types.</span></span>

<span data-ttu-id="80688-112">下列查詢字串會搜尋安全性群組。</span><span class="sxs-lookup"><span data-stu-id="80688-112">The following query string will search for security groups.</span></span> <span data-ttu-id="80688-113">此範例使用 "-2147483648" 做為 **ADS \_ 群組 \_ 類型 \_ 安全性 \_ 啟用** 旗標的十進位對等專案。</span><span class="sxs-lookup"><span data-stu-id="80688-113">This example uses "-2147483648" as the decimal equivalent of the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** flag.</span></span>


```C++
(&(objectCategory=group)(groupType:1.2.840.113556.1.4.803:=-2147483648))
```



<span data-ttu-id="80688-114">下列查詢字串會搜尋通用通訊群組;亦即，包含 **ads \_ 群組 \_ 類型 \_ 通用 \_ 組** 旗標的群組，且不包含 **ads \_ 群組 \_ 類型 \_ 安全性 \_ 啟用** 旗標。</span><span class="sxs-lookup"><span data-stu-id="80688-114">The following query string will search for universal distribution groups; that is, groups that contain the **ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP** flag and do not contain the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** flag.</span></span> <span data-ttu-id="80688-115">此範例會使用 "8" 作為 **ads \_ 群組 \_ 類型 \_ 通用 \_ 組類型** 的十進位對等專案，並使用 "-2147483648" 做為 **ads \_ 群組 \_ 類型 \_ 安全性 \_ 啟用** 旗標的十進位對等專案。</span><span class="sxs-lookup"><span data-stu-id="80688-115">This example uses "8" as the decimal equivalent of **ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP** and "-2147483648" as the decimal equivalent of the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** flag.</span></span>


```C++
(&(objectCategory=group)((&(groupType:1.2.840.113556.1.4.803:=8)(!(groupType:1.2.840.113556.1.4.803:=-2147483648)))))
```



 

 