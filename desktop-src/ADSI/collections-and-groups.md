---
title: 集合和群組
description: ADSI 會使用集合物件來代表目錄服務中可使用相同資料類型表示的任意一組專案。
ms.assetid: 03257cc9-f354-4e1c-8880-936a7acac3ef
ms.tgt_platform: multiple
keywords:
- ADSI ADSI、使用、集合和群組
- 集合 ADSI
- 群組 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9f0f4d699d8dde0c3d70c7449dfe146212b2b30
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933599"
---
# <a name="collections-and-groups"></a><span data-ttu-id="dcbec-106">集合和群組</span><span class="sxs-lookup"><span data-stu-id="dcbec-106">Collections and Groups</span></span>

<span data-ttu-id="dcbec-107">ADSI 會使用集合物件來代表目錄服務中可使用相同資料類型表示的任意一組專案。</span><span class="sxs-lookup"><span data-stu-id="dcbec-107">ADSI uses collection objects to represent any arbitrary set of items in a directory service that can be represented using the same data type.</span></span> <span data-ttu-id="dcbec-108">集合物件會定義為一組 **VARIANT** 值，表示任何有效的 Automation 資料類型。</span><span class="sxs-lookup"><span data-stu-id="dcbec-108">Collection objects are defined as a set of **VARIANT** values, representing any of the valid Automation data types.</span></span> <span data-ttu-id="dcbec-109">集合物件可以同時代表持續性資訊，例如存取控制清單和暫時性資訊，例如列印佇列中的列印工作。</span><span class="sxs-lookup"><span data-stu-id="dcbec-109">Collection objects can represent both persistent information such as access-control lists and volatile information such as print jobs in a print queue.</span></span>

<span data-ttu-id="dcbec-110">列出集合 (或容器) 物件內容的標準 COM 慣例是建立支援 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)的列舉值物件，此物件有方法可以逐步執行集合物件的清單。</span><span class="sxs-lookup"><span data-stu-id="dcbec-110">The standard COM convention for listing the contents of a collection (or container) object is to create an enumerator object that supports [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), which has methods to step through the list of collection objects.</span></span> <span data-ttu-id="dcbec-111">ADSI 中提供 **get \_ \_ NewEnum** 方法的介面 (記下兩個底線) 為 [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)、 [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)和 [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection)。</span><span class="sxs-lookup"><span data-stu-id="dcbec-111">The interfaces in ADSI that supply the **get\_\_NewEnum** method (note the two underscores) are [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) and [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection).</span></span> <span data-ttu-id="dcbec-112">ADSI 也提供 C 和 c + + 程式的 helper 函式 [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) 和 [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) ，以簡化列舉。</span><span class="sxs-lookup"><span data-stu-id="dcbec-112">ADSI also supplies the helper functions [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) and [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) for C and C++ programs to simplify enumeration.</span></span> <span data-ttu-id="dcbec-113">Automation 用戶端在 **For** 迴圈中呼叫 **Next** 時，會隱含地使用列舉。</span><span class="sxs-lookup"><span data-stu-id="dcbec-113">Automation clients use enumeration implicitly when they call **Next** in a **For** loop.</span></span>

<span data-ttu-id="dcbec-114">群組只是支援 [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) 介面的物件集合。</span><span class="sxs-lookup"><span data-stu-id="dcbec-114">Groups are simply collections of objects supporting the [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) interface.</span></span>

 

 