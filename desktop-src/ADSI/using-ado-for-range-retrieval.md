---
title: 使用 ADO 進行範圍抓取
description: 如果使用自動化語言，則應該使用 (ADO) 的 ActiveX 目錄物件，以抓取屬性值的範圍。使用 ADO 進行範圍抓取時，有一個必須特別解決的問題。
ms.assetid: ca06169d-7de7-4552-aa7d-e9427353e49e
ms.tgt_platform: multiple
keywords:
- 使用 ADO 進行範圍抓取 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb8950a71708bd9c824c90842f043808c897554
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671111"
---
# <a name="using-ado-for-range-retrieval"></a><span data-ttu-id="36fe6-104">使用 ADO 進行範圍抓取</span><span class="sxs-lookup"><span data-stu-id="36fe6-104">Using ADO for Range Retrieval</span></span>

<span data-ttu-id="36fe6-105">如果使用自動化語言，則應該使用 (ADO) 的 ActiveX 目錄物件，以抓取屬性值的範圍。</span><span class="sxs-lookup"><span data-stu-id="36fe6-105">If an automation language is used, the ActiveX Directory Objects (ADO) should be used to retrieve a range of property values.</span></span>

<span data-ttu-id="36fe6-106">使用 ADO 進行範圍抓取時，有一個必須特別解決的問題。</span><span class="sxs-lookup"><span data-stu-id="36fe6-106">When using ADO for range retrieval, there is one problem that must be specifically addressed.</span></span> <span data-ttu-id="36fe6-107">當查詢屬性值的最後一個群組時，ADO 物件將會取出零個物件，即使有更多的物件也一樣。</span><span class="sxs-lookup"><span data-stu-id="36fe6-107">When querying for the final group of property values, the ADO object will retrieve zero objects, even though more remain.</span></span> <span data-ttu-id="36fe6-108">若要取得其餘的值，請使用範圍萬用字元 ' \* '。</span><span class="sxs-lookup"><span data-stu-id="36fe6-108">To retrieve the remaining values, use the range wildcard '\*'.</span></span> <span data-ttu-id="36fe6-109">例如，如果群組包含150成員，則可以使用範圍抓取來正常地取出成員值0-100。</span><span class="sxs-lookup"><span data-stu-id="36fe6-109">For example, if a group contains 150 members, member values 0-100 can be retrieved normally using ranged retrieval.</span></span> <span data-ttu-id="36fe6-110">如果接著要求範圍101-200，ADO 物件將會傳回零個物件。</span><span class="sxs-lookup"><span data-stu-id="36fe6-110">If range 101-200 is then requested, the ADO object will return zero objects.</span></span> <span data-ttu-id="36fe6-111">此時，必須將查詢修改為要求範圍 101- \* 。</span><span class="sxs-lookup"><span data-stu-id="36fe6-111">At this point, it is necessary to modify the query to request range 101-\*.</span></span> <span data-ttu-id="36fe6-112">這會將值從101取出至150。</span><span class="sxs-lookup"><span data-stu-id="36fe6-112">This will retrieve values from 101 to 150.</span></span> <span data-ttu-id="36fe6-113">如需詳細資訊和程式碼範例，請參閱 [使用範圍取得群組成員的範例程式碼](example-code-for-using-ranging-to-retrieve-members-of-a-group.md)。</span><span class="sxs-lookup"><span data-stu-id="36fe6-113">For more information and a code example, see [Example Code for Using Ranging to Retrieve Members of a Group](example-code-for-using-ranging-to-retrieve-members-of-a-group.md).</span></span>

<span data-ttu-id="36fe6-114">如需使用 ADO 進行範圍抓取的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="36fe6-114">For more information about using ADO for range retrieval, see:</span></span>

-   [<span data-ttu-id="36fe6-115">ADO LDAP 範圍方言</span><span class="sxs-lookup"><span data-stu-id="36fe6-115">ADO LDAP Ranging Dialect</span></span>](ado-ldap-ranging-dialect.md)
-   [<span data-ttu-id="36fe6-116">ADO SQL 範圍方言</span><span class="sxs-lookup"><span data-stu-id="36fe6-116">ADO SQL Ranging Dialect</span></span>](ado-sql-ranging-dialect.md)
-   [<span data-ttu-id="36fe6-117">使用範圍取得群組成員的範例程式碼</span><span class="sxs-lookup"><span data-stu-id="36fe6-117">Example Code for Using Ranging to Retrieve Members of a Group</span></span>](example-code-for-using-ranging-to-retrieve-members-of-a-group.md)

 

 




