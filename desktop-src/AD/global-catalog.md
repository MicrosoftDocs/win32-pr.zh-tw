---
title: 通用類別目錄
description: Active Directory Domain Services 所執行的網域可包含許多分割區或命名內容。
ms.assetid: eac02c1f-0c37-4eee-822d-07913ea8775a
ms.tgt_platform: multiple
keywords:
- 通用類別目錄 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4496804d21e53cf2d87947288179e7f96ca75c8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681660"
---
# <a name="global-catalog"></a><span data-ttu-id="e00dc-104">通用類別目錄</span><span class="sxs-lookup"><span data-stu-id="e00dc-104">Global Catalog</span></span>

<span data-ttu-id="e00dc-105">Active Directory Domain Services 所執行的網域可包含許多分割區或命名內容。</span><span class="sxs-lookup"><span data-stu-id="e00dc-105">A Domain run by Active Directory Domain Services can consist of many partitions or naming contexts.</span></span> <span data-ttu-id="e00dc-106">物件的分辨名稱 (DN) 包含足夠的資訊，以找出保存物件之分割區的複本。</span><span class="sxs-lookup"><span data-stu-id="e00dc-106">The distinguished name (DN) of an object includes enough information to locate a replica of the partition that holds the object.</span></span> <span data-ttu-id="e00dc-107">但是，使用者或應用程式不知道目標物件的 DN，或哪個分割區可能包含物件。</span><span class="sxs-lookup"><span data-stu-id="e00dc-107">Many times however, the user or application does not know the DN of the target object or which partition might contain the object.</span></span> <span data-ttu-id="e00dc-108">[*通用類別目錄 (GC)*](/previous-versions/windows/desktop/legacy/ms681905(v=vs.85))可讓使用者和應用程式在指定目標物件的一或多個屬性的 Active Directory 域樹中尋找物件。</span><span class="sxs-lookup"><span data-stu-id="e00dc-108">The [*global catalog (GC)*](/previous-versions/windows/desktop/legacy/ms681905(v=vs.85)) allows users and applications to find objects in an Active Directory domain tree, given one or more attributes of the target object.</span></span>

<span data-ttu-id="e00dc-109">通用類別目錄包含目錄中每個命名內容的部分複本。</span><span class="sxs-lookup"><span data-stu-id="e00dc-109">The global catalog contains a partial replica of every naming context in the directory.</span></span> <span data-ttu-id="e00dc-110">它也包含架構和設定命名內容。</span><span class="sxs-lookup"><span data-stu-id="e00dc-110">It contains the schema and configuration naming contexts as well.</span></span> <span data-ttu-id="e00dc-111">這表示 GC 會保存目錄中每個物件的複本，但只有少數屬性。</span><span class="sxs-lookup"><span data-stu-id="e00dc-111">This means the GC holds a replica of every object in the directory but with only a small number of their attributes.</span></span> <span data-ttu-id="e00dc-112">GC 中的屬性是搜尋作業中最常使用的屬性 (例如使用者的名字和姓氏，或登入名稱) ，以及找出物件完整複本所需的屬性。</span><span class="sxs-lookup"><span data-stu-id="e00dc-112">The attributes in the GC are those most frequently used in search operations (such as a user's first and last names or login names) and those required to locate a full replica of the object.</span></span> <span data-ttu-id="e00dc-113">GC 可讓使用者快速找出感興趣的物件，而不需要知道有哪些網域保存這些物件，而不需要在企業中使用連續的延伸命名空間。</span><span class="sxs-lookup"><span data-stu-id="e00dc-113">The GC allows users to quickly find objects of interest without knowing what domain holds them and without requiring a contiguous extended namespace in the enterprise.</span></span>

<span data-ttu-id="e00dc-114">通用類別目錄是由 Active Directory Domain Services 複寫系統自動建立。</span><span class="sxs-lookup"><span data-stu-id="e00dc-114">The global catalog is built automatically by the Active Directory Domain Services replication system.</span></span> <span data-ttu-id="e00dc-115">系統會自動產生通用類別目錄的複寫拓撲。</span><span class="sxs-lookup"><span data-stu-id="e00dc-115">The replication topology for the global catalog is generated automatically.</span></span> <span data-ttu-id="e00dc-116">複寫到通用類別目錄的屬性包含由 Microsoft 定義的基底集合。</span><span class="sxs-lookup"><span data-stu-id="e00dc-116">The properties replicated into the global catalog include a base set defined by Microsoft.</span></span> <span data-ttu-id="e00dc-117">系統管理員可以指定其他屬性，以符合其安裝的需求。</span><span class="sxs-lookup"><span data-stu-id="e00dc-117">Administrators can specify additional properties to meet the needs of their installation.</span></span>

 

 