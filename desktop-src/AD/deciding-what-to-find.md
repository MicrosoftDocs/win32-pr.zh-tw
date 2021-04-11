---
title: 決定要尋找的內容
description: 搜尋目錄之前，請先考慮您的搜尋將如何根據您的方法執行。 要傳回的資料和屬性會影響您系結以開始搜尋的位置、搜尋的深度、查詢篩選和搜尋效能。
ms.assetid: 788fa12c-9086-4d8b-bd2e-e96a494a26ad
ms.tgt_platform: multiple
keywords:
- 搜尋準則 Active Directory
- 決定要尋找哪些 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 818b0f9be56830a836453c5e52ceadd52928a522
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020870"
---
# <a name="deciding-what-to-find"></a><span data-ttu-id="79f40-106">決定要尋找的內容</span><span class="sxs-lookup"><span data-stu-id="79f40-106">Deciding What to Find</span></span>

<span data-ttu-id="79f40-107">搜尋目錄之前，請先考慮您的搜尋將如何根據您的方法執行。</span><span class="sxs-lookup"><span data-stu-id="79f40-107">Before you search a directory, consider how your search will perform based on your approach.</span></span> <span data-ttu-id="79f40-108">要傳回的資料和屬性會影響您系結以開始搜尋的位置、搜尋的深度、查詢篩選和搜尋效能。</span><span class="sxs-lookup"><span data-stu-id="79f40-108">The data and properties to be returned affect where you bind to start a search, the depth of your search, your query filter, and search performance.</span></span>

<span data-ttu-id="79f40-109">例如，如果您想要使用姓氏 Smith 搜尋所有的使用者物件：</span><span class="sxs-lookup"><span data-stu-id="79f40-109">For example, if you want search for all user objects with surname Smith:</span></span>



| <span data-ttu-id="79f40-110">區域</span><span class="sxs-lookup"><span data-stu-id="79f40-110">Area</span></span>                       | <span data-ttu-id="79f40-111">描述</span><span class="sxs-lookup"><span data-stu-id="79f40-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79f40-112">搜尋位置</span><span class="sxs-lookup"><span data-stu-id="79f40-112">Where to search</span></span>            | <span data-ttu-id="79f40-113">特定的容器或組織單位 (OU) 在網域、特定網域、特定網域樹狀結構或整個樹系內。</span><span class="sxs-lookup"><span data-stu-id="79f40-113">A specific container or organizational unit (OU) within a domain, a specific domain, a specific domain tree, or the entire forest.</span></span> <span data-ttu-id="79f40-114">如果您在特定容器或網域內搜尋物件，搜尋查詢會以直接系結至該容器或網域的方式執行，而不是在域樹上執行子樹搜尋。</span><span class="sxs-lookup"><span data-stu-id="79f40-114">If you search for objects within a specific container or domain, the search query will perform better by binding directly to that container or domain   instead of performing a subtree search on a domain tree.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="79f40-115">搜尋類型</span><span class="sxs-lookup"><span data-stu-id="79f40-115">Type of search</span></span>             | <span data-ttu-id="79f40-116">如果您確認是否存在，或抓取具有分辨名稱 (DN) 的特定物件屬性，您應該執行基底搜尋，只搜尋您所系結的物件。</span><span class="sxs-lookup"><span data-stu-id="79f40-116">If you verify the existence of, or retrieve the properties of a particular object that has a distinguished name (DN) you already know, you should perform a base search, which searches only the object you have bound to.</span></span><br/> <span data-ttu-id="79f40-117">如果您知道某個物件是特定容器的直接子系，請系結至該容器，並進行一層級的搜尋 (**attributeSchema** 和 **classSchema** 中的架構容器中的物件，以及延伸許可權容器中的擴充權限物件，是) 的良好範例。</span><span class="sxs-lookup"><span data-stu-id="79f40-117">If you know an object is a direct descendant of a particular container, bind to that container and do a one-level search (**attributeSchema** and **classSchema** objects in the schema container and extended-right objects in the extended-rights container are good examples).</span></span><br/> <span data-ttu-id="79f40-118">如果您不知道物件的確切位置，或是想要搜尋您所系結的物件和目錄階層中的所有子物件，請執行子樹搜尋。</span><span class="sxs-lookup"><span data-stu-id="79f40-118">If you do not know exactly where the object is, or if you want to search the object you have bound to and all the child objects below it in the directory hierarchy, perform a subtree search.</span></span><br/>                                                       |
| <span data-ttu-id="79f40-119">盡可能使用索引</span><span class="sxs-lookup"><span data-stu-id="79f40-119">Use indexes where possible</span></span> | <span data-ttu-id="79f40-120">最後，如果您尋找特定類別的物件，則查詢篩選準則應該有運算式可評估針對該類別定義的屬性。</span><span class="sxs-lookup"><span data-stu-id="79f40-120">Finally, if you look for a specific class of object, the query filter should have expressions that evaluate properties that are defined for that class.</span></span><br/> <span data-ttu-id="79f40-121">若要搜尋群組物件，請在篩選中包含 (objectCategory = group) 的運算式。</span><span class="sxs-lookup"><span data-stu-id="79f40-121">To search for group objects, include the expression (objectCategory=group) in the filter.</span></span> <span data-ttu-id="79f40-122">若要搜尋使用者物件，請指定 (& (objectClass = user)  (objectCategory = person) ) ，因為 computer 類別衍生自 user 類別，所以 (objectClass = user) 會同時傳回使用者和電腦，因此， (objectCategory = person) 會傳回使用者和連絡人。</span><span class="sxs-lookup"><span data-stu-id="79f40-122">To search for user objects, specify (&(objectClass=user)(objectCategory=person)) because the computer class derives from the user class, so (objectClass=user) would return both users and computers and also because both contact and user objects have an **objectCategory** of person, so (objectCategory=person) would return both users and contacts.</span></span><br/> <span data-ttu-id="79f40-123">如需詳細資訊，請參閱 [物件類別和物件類別目錄](object-class-and-object-category.md) 和 [索引屬性](indexed-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="79f40-123">For more information, see [Object Class and Object Category](object-class-and-object-category.md) and [Indexed Attributes](indexed-attributes.md).</span></span><br/> |



 

 

 





