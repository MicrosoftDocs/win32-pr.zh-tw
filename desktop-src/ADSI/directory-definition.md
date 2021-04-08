---
title: 目錄定義
description: 範例提供者元件使用相當簡單的目錄設計來說明元件之間的關聯性，以及顯示成為 ADSI 提供者所需的最低需求。
ms.assetid: d8dcd255-4a17-4c80-a749-61c1af605dba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6156f2e1ab89b34f009f1a86e5de011c20cf9503
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839208"
---
# <a name="directory-definition"></a><span data-ttu-id="7b61c-103">目錄定義</span><span class="sxs-lookup"><span data-stu-id="7b61c-103">Directory Definition</span></span>

<span data-ttu-id="7b61c-104">範例提供者元件使用相當簡單的目錄設計來說明元件之間的關聯性，以及顯示成為 ADSI 提供者所需的最低需求。</span><span class="sxs-lookup"><span data-stu-id="7b61c-104">The example provider component uses a relatively simple directory design to clarify the relationship between components and to show the minimum requirements necessary to be an ADSI provider.</span></span>

<span data-ttu-id="7b61c-105">範例提供者元件的「目錄」包含兩個根節點：「西雅圖」和「多倫多」。</span><span class="sxs-lookup"><span data-stu-id="7b61c-105">The "directory" for the example provider component consists of two root nodes: "Seattle" and "Toronto".</span></span> <span data-ttu-id="7b61c-106">西雅圖還包含兩個子級別：「Bellevue」和「Redmond」。</span><span class="sxs-lookup"><span data-stu-id="7b61c-106">Seattle contains two more sublevels, "Bellevue" and "Redmond".</span></span> <span data-ttu-id="7b61c-107">其中每個專案都包含數個使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="7b61c-107">Each of these entries contains several user accounts.</span></span> <span data-ttu-id="7b61c-108">「多倫多」專案沒有進一步的子層級，但直接包含數個使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="7b61c-108">The "Toronto" entry has no further sublevels, but directly contains several user accounts.</span></span> <span data-ttu-id="7b61c-109">下圖顯示兩個連接到網路的根節點。</span><span class="sxs-lookup"><span data-stu-id="7b61c-109">The following figure shows these two root nodes connected to a network.</span></span>

![目錄定義](images/dssmdo.png)

<span data-ttu-id="7b61c-111">在階層式詞彙中，命名空間節點包含「西雅圖」和「多倫多」。</span><span class="sxs-lookup"><span data-stu-id="7b61c-111">In hierarchical terms, the Namespace node contains "Seattle" and "Toronto".</span></span> <span data-ttu-id="7b61c-112">「西雅圖」包含「Bellevue」和「Redmond」。</span><span class="sxs-lookup"><span data-stu-id="7b61c-112">"Seattle" contains "Bellevue" and "Redmond".</span></span> <span data-ttu-id="7b61c-113">"Bellevue" 和 "Redmond" 各包含一組使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="7b61c-113">"Bellevue" and "Redmond" each contain a set of user accounts.</span></span> <span data-ttu-id="7b61c-114">「多倫多」直接包含沒有中繼組織節點的使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="7b61c-114">"Toronto" directly contains the user accounts with no intermediate organizational nodes.</span></span>

<span data-ttu-id="7b61c-115">範例提供者元件只會以兩個 Active Directory 物件類型來表示此結構：容器物件和分葉物件。</span><span class="sxs-lookup"><span data-stu-id="7b61c-115">The example provider component represents this structure with only two Active Directory object types: a container object and a leaf object.</span></span> <span data-ttu-id="7b61c-116">「西雅圖」、「多倫多」、「Bellevue」和「Redmond」是容器物件，而每個使用者帳戶都是分葉物件。</span><span class="sxs-lookup"><span data-stu-id="7b61c-116">"Seattle", "Toronto", "Bellevue", and "Redmond" are container objects and each user account is a leaf object.</span></span>

<span data-ttu-id="7b61c-117">範例提供者元件會建立名為「組織單位」的架構類別做為容器物件類型，並為使用者帳戶建立名為 "User" 的架構類別。</span><span class="sxs-lookup"><span data-stu-id="7b61c-117">The example provider component creates a schema class called "Organizational Unit" for a container object type and a schema class called "User" for a user account.</span></span>

<span data-ttu-id="7b61c-118">每個架構類別的屬性、其方法以及管理這些物件之內含專案關聯性的規則全都定義在 [架構管理](schema-management.md)中。</span><span class="sxs-lookup"><span data-stu-id="7b61c-118">The properties for each schema class, their methods, and the rules that govern the containment relationships for these objects are all defined in [Schema Management](schema-management.md).</span></span>

 

 




