---
title: 控制物件可見度
description: Active Directory Domain Services 可讓您隱藏物件，使其無法被拒絕特定許可權的使用者使用。
ms.assetid: 3a65ec79-7de0-4d14-b980-1ca6a972ac70
ms.tgt_platform: multiple
keywords:
- 控制物件可見度 Active Directory
- Active Directory Active Directory，使用控制物件可見度
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b1ab364f0711174d5ac1dd1e4fbe98303c50b3
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023275"
---
# <a name="controlling-object-visibility"></a><span data-ttu-id="4b3e0-105">控制物件可見度</span><span class="sxs-lookup"><span data-stu-id="4b3e0-105">Controlling Object Visibility</span></span>

<span data-ttu-id="4b3e0-106">Active Directory Domain Services 可讓您隱藏物件，使其無法被拒絕特定許可權的使用者使用。</span><span class="sxs-lookup"><span data-stu-id="4b3e0-106">Active Directory Domain Services provide the ability to hide objects from users who have been denied certain rights.</span></span> <span data-ttu-id="4b3e0-107">如果隱藏物件，以使用者認證執行的應用程式將無法列舉或系結至物件。</span><span class="sxs-lookup"><span data-stu-id="4b3e0-107">If an object is hidden, an application that is running with a user's credentials will not be able to enumerate or bind to the object.</span></span>

<span data-ttu-id="4b3e0-108">如果使用者被授與廣告直接在容器上 [**\_ \_ ACTRL \_ DS \_ 清單**](/windows/win32/api/iads/ne-iads-ads_rights_enum) 存取控制許可權，使用者可以查看容器的任何子物件。</span><span class="sxs-lookup"><span data-stu-id="4b3e0-108">If a user is granted the [**ADS\_RIGHT\_ACTRL\_DS\_LIST**](/windows/win32/api/iads/ne-iads-ads_rights_enum) access control right on a container, the user can view any of the child objects of the container.</span></span> <span data-ttu-id="4b3e0-109">同樣地，如果使用者被拒，ADS 會直接在容器上 **\_ \_ ACTRL \_ DS \_ 清單** 存取控制，使用者就無法查看容器的任何子物件。</span><span class="sxs-lookup"><span data-stu-id="4b3e0-109">Likewise, if a user is denied the **ADS\_RIGHT\_ACTRL\_DS\_LIST** access control right on a container, the user cannot view any of the child objects of the container.</span></span> <span data-ttu-id="4b3e0-110">這允許隱藏整個容器的內容。</span><span class="sxs-lookup"><span data-stu-id="4b3e0-110">This allows the contents of entire containers to be hidden.</span></span>

<span data-ttu-id="4b3e0-111">Active Directory 伺服器也可以藉由將 [**dSHeuristics**](/windows/desktop/ADSchema/a-dsheuristics) 屬性的第三個字元設定為 "1"，而成為特殊的清單物件模式。</span><span class="sxs-lookup"><span data-stu-id="4b3e0-111">The Active Directory server can also be put into a special list object mode by setting the third character of the [**dSHeuristics**](/windows/desktop/ADSchema/a-dsheuristics) property to "1".</span></span> <span data-ttu-id="4b3e0-112">您可以藉由將 **dSHeuristics** 屬性的第三個字元設定為 "0" 來停用清單物件模式。</span><span class="sxs-lookup"><span data-stu-id="4b3e0-112">The list object mode can be disabled by setting the third character of the **dSHeuristics** property to "0".</span></span> <span data-ttu-id="4b3e0-113">當 Active Directory 伺服器處於 [清單物件] 模式時，如果使用者已被授與父物件的 [**ADS \_ right \_ ACTRL \_ DS \_ 清單**](/windows/win32/api/iads/ne-iads-ads_rights_enum) ，仍會顯示該物件。</span><span class="sxs-lookup"><span data-stu-id="4b3e0-113">When the Active Directory server is in the list object mode, an object will still be visible if the user has been granted the [**ADS\_RIGHT\_ACTRL\_DS\_LIST**](/windows/win32/api/iads/ne-iads-ads_rights_enum) right on the parent object.</span></span> <span data-ttu-id="4b3e0-114">但是，如果使用者已被拒，在父系上的 **ads \_ right \_ ACTRL \_ ds \_ 清單** 中，如果使用者在父系和子物件上被授與 **ads \_ right \_ DS \_ 清單 \_ 物件** ，仍然可以看到特定的子物件。</span><span class="sxs-lookup"><span data-stu-id="4b3e0-114">If, however, the user has been denied the **ADS\_RIGHT\_ACTRL\_DS\_LIST** right on the parent, specific child objects can still be made visible if the user is granted the **ADS\_RIGHT\_DS\_LIST\_OBJECT** right on both the parent and child objects.</span></span> <span data-ttu-id="4b3e0-115">清單物件模式允許系統管理員授與或拒絕使用者或群組個別物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="4b3e0-115">The list object mode allows the system administrator to grant or deny access to individual objects for users or groups.</span></span> <span data-ttu-id="4b3e0-116">應謹慎使用清單物件模式，因為它需要目錄服務所進行的存取檢查呼叫數目明顯較高，以判斷使用者是否可以看到物件。</span><span class="sxs-lookup"><span data-stu-id="4b3e0-116">The list object mode should be used sparingly because it requires a significantly higher number of access check calls to be made by the directory service to determine if an object is visible to a user.</span></span> <span data-ttu-id="4b3e0-117">因此，它可能會對從 Active Directory Domain Services 流覽或讀取物件的效能造成負面影響。</span><span class="sxs-lookup"><span data-stu-id="4b3e0-117">Thus it can have a negative effect on the performance of browsing or reading objects from Active Directory Domain Services.</span></span>

 

 