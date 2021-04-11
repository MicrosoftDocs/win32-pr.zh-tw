---
title: 列舉包含許多成員的群組
description: 群組的成員會儲存在名為 member 的多重值屬性中。
ms.assetid: 78f81b09-2223-4b74-b8d5-7a97494c0324
ms.tgt_platform: multiple
keywords:
- 列舉包含許多成員的群組 Active Directory
- 群組 Active Directory，列舉具有許多成員的群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe2d9a5c9abc6e77ac72672379789d1028f92c3f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104092638"
---
# <a name="enumerating-groups-that-contain-many-members"></a><span data-ttu-id="1f0b5-105">列舉包含許多成員的群組</span><span class="sxs-lookup"><span data-stu-id="1f0b5-105">Enumerating Groups That Contain Many Members</span></span>

<span data-ttu-id="1f0b5-106">群組的成員會儲存在名為 **member** 的多重值屬性中。</span><span class="sxs-lookup"><span data-stu-id="1f0b5-106">The members of a group are stored in a multi-value attribute called **member**.</span></span> <span data-ttu-id="1f0b5-107">**成員** 屬性可以包含大量的值。</span><span class="sxs-lookup"><span data-stu-id="1f0b5-107">The **member** attribute can contain a large number of values.</span></span> <span data-ttu-id="1f0b5-108">當多重值屬性中的值數目變大時，列舉成員可能會沒有效率。</span><span class="sxs-lookup"><span data-stu-id="1f0b5-108">Enumerating members can be inefficient when the number of values in a multi-valued attribute becomes large.</span></span> <span data-ttu-id="1f0b5-109">伺服器也會限制可在單一查詢中取出的最大值數目。</span><span class="sxs-lookup"><span data-stu-id="1f0b5-109">The server will also limit the maximum number of values that can be retrieved in a single query.</span></span> <span data-ttu-id="1f0b5-110">這表示，如果群組的成員可能超過伺服器所能提供的成員，列舉所有成員的唯一方法就是使用資料的累加抓取，稱為 *範圍* 抓取。</span><span class="sxs-lookup"><span data-stu-id="1f0b5-110">This means that if a group may have more members than can be supplied by the server, the only way to enumerate all members is to use incremental retrieval of data, known as *range retrieval*.</span></span>

<span data-ttu-id="1f0b5-111">範圍抓取需要在單一查詢中要求有限數目的屬性值。</span><span class="sxs-lookup"><span data-stu-id="1f0b5-111">Range retrieval involves requesting a limited number of attribute values in a single query.</span></span> <span data-ttu-id="1f0b5-112">要求的值數目必須小於或等於伺服器支援的最大值數目。</span><span class="sxs-lookup"><span data-stu-id="1f0b5-112">The number of values requested must be less than, or equal to, the maximum number of values supported by the server.</span></span> <span data-ttu-id="1f0b5-113">若要減少查詢必須與伺服器聯繫的次數，要求的值數目應該盡可能接近此最大值。</span><span class="sxs-lookup"><span data-stu-id="1f0b5-113">To reduce the number of times the query must contact the server, the number of values requested should be as close, as possible, to this maximum.</span></span> <span data-ttu-id="1f0b5-114">若要讓應用程式能夠在所有伺服器上正常運作，應使用最大的1000數目。</span><span class="sxs-lookup"><span data-stu-id="1f0b5-114">To enable an application to work correctly with all servers, a maximum number of 1000 should be used.</span></span>

<span data-ttu-id="1f0b5-115">提供所要求資料的伺服器版本會決定可在單一查詢中取出的最大值數目。</span><span class="sxs-lookup"><span data-stu-id="1f0b5-115">The version of the server that supplies the requested data determines the maximum number of values that can be retrieved in a single query.</span></span> <span data-ttu-id="1f0b5-116">下表列出可在單一查詢中取出的伺服器版本和最大值數目。</span><span class="sxs-lookup"><span data-stu-id="1f0b5-116">The following table lists the server version and the maximum number of values that can be retrieved in a single query.</span></span>



| <span data-ttu-id="1f0b5-117">伺服器作業系統版本</span><span class="sxs-lookup"><span data-stu-id="1f0b5-117">Server operating system version</span></span> | <span data-ttu-id="1f0b5-118">已抓取的最大值</span><span class="sxs-lookup"><span data-stu-id="1f0b5-118">Maximum values retrieved</span></span> |
|---------------------------------|--------------------------|
| <span data-ttu-id="1f0b5-119">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="1f0b5-119">Windows 2000</span></span>                    | <span data-ttu-id="1f0b5-120">1000</span><span class="sxs-lookup"><span data-stu-id="1f0b5-120">1000</span></span>                     |
| <span data-ttu-id="1f0b5-121">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1f0b5-121">Windows Server 2003</span></span>             | <span data-ttu-id="1f0b5-122">1500</span><span class="sxs-lookup"><span data-stu-id="1f0b5-122">1500</span></span>                     |



 

<span data-ttu-id="1f0b5-123">如需使用 ADSI 來抓取屬性值範圍的詳細資訊，請參閱 [屬性範圍](/windows/desktop/ADSI/attribute-range-retrieval)抓取。</span><span class="sxs-lookup"><span data-stu-id="1f0b5-123">For more information about retrieving ranges of attribute values with ADSI, see [Attribute Range Retrieval](/windows/desktop/ADSI/attribute-range-retrieval).</span></span>

<span data-ttu-id="1f0b5-124">如需有關使用 [DirectoryServices](/dotnet/api/system.directoryservices)來抓取屬性值範圍的詳細資訊，請參閱 [列舉大型群組中的成員](https://msdn.microsoft.com/library/ms180907(v=VS.80).aspx)。</span><span class="sxs-lookup"><span data-stu-id="1f0b5-124">For more information about retrieving ranges of attribute values with [System.DirectoryServices](/dotnet/api/system.directoryservices), see [Enumerating Members in a Large Group](https://msdn.microsoft.com/library/ms180907(v=VS.80).aspx).</span></span>

 

 