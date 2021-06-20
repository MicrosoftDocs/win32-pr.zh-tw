---
title: 列舉群組中的成員
description: 瞭解如何列舉 Azure Active Directory 群組中的成員。 群組的成員會儲存在名為 member 的多重值屬性中。
ms.assetid: 28cafdbe-e599-4b1d-a384-264f41d81c79
ms.tgt_platform: multiple
keywords:
- 列舉群組中的成員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 916b988cd26ee4df59eaf27cc5ffd690bca1458a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407421"
---
# <a name="enumerating-members-in-a-group"></a><span data-ttu-id="81108-105">列舉群組中的成員</span><span class="sxs-lookup"><span data-stu-id="81108-105">Enumerating Members in a Group</span></span>

<span data-ttu-id="81108-106">群組的成員會儲存在名為 **member** 的多重值屬性中。</span><span class="sxs-lookup"><span data-stu-id="81108-106">The members of a group are stored in a multi-value attribute called **member**.</span></span> <span data-ttu-id="81108-107">對於具有小型到中型成員資格的群組，請使用 [**IADsGroup**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) 來取得 [**IADsMembers**](/windows/desktop/api/iads/nn-iads-iadsmembers) 物件的指標，其中包含所有成員的清單。</span><span class="sxs-lookup"><span data-stu-id="81108-107">For groups with a small to medium-sized membership, use the [**IADsGroup.Members**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) method to get a pointer to an [**IADsMembers**](/windows/desktop/api/iads/nn-iads-iadsmembers) object that contains the list of all members.</span></span> <span data-ttu-id="81108-108">然後使用 [**IADsMembers：： get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum)取得列舉值物件，您可以用來列舉成員。</span><span class="sxs-lookup"><span data-stu-id="81108-108">Then use the [**IADsMembers::get\_\_NewEnum**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum) to get an enumerator object that you can use to enumerate the members.</span></span>

<span data-ttu-id="81108-109">如果預期的群組成員資格將是1000或更多成員，請使用範圍，一次取出一個範圍的使用者。</span><span class="sxs-lookup"><span data-stu-id="81108-109">If the anticipated group membership will be 1000 or more members, use ranging to retrieve users one range at a time.</span></span> <span data-ttu-id="81108-110">如需使用範圍列舉成員的詳細資訊，請參閱 [列舉包含許多成員的群組](enumerating-groups-that-contain-many-members.md)。</span><span class="sxs-lookup"><span data-stu-id="81108-110">For more information about using ranging to enumerate members, see [Enumerating Groups That Contain Many Members](enumerating-groups-that-contain-many-members.md).</span></span>

 

 