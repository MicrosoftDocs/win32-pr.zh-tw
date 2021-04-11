---
description: 列舉裝置和篩選器
ms.assetid: 334bba2a-7477-4115-9ce0-d4495c1fc290
title: 列舉裝置和篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e69997a4af4f3160f0b338bc9c595adea83a5354
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846600"
---
# <a name="enumerating-devices-and-filters"></a><span data-ttu-id="9924c-103">列舉裝置和篩選器</span><span class="sxs-lookup"><span data-stu-id="9924c-103">Enumerating Devices and Filters</span></span>

<span data-ttu-id="9924c-104">有時候，應用程式必須在使用者的系統上找出特定的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="9924c-104">Sometimes an application needs to locate a particular filter on the user's system.</span></span> <span data-ttu-id="9924c-105">例如，影片捕獲應用程式可能會顯示可用的捕獲裝置清單。</span><span class="sxs-lookup"><span data-stu-id="9924c-105">For example, a video capture application might display a list of available capture devices.</span></span> <span data-ttu-id="9924c-106">因為 DirectShow 使用以元件為基礎的架構，所以您無法在設計階段得知使用者系統上安裝了哪些篩選器。</span><span class="sxs-lookup"><span data-stu-id="9924c-106">Because DirectShow uses a component-based architecture, you cannot know at design time which filters are installed on the user's system.</span></span> <span data-ttu-id="9924c-107">這特別適用于代表硬體裝置的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="9924c-107">This is particularly true for filters that represent hardware devices.</span></span> <span data-ttu-id="9924c-108">DirectShow 提供兩個元件來尋找已註冊的篩選：</span><span class="sxs-lookup"><span data-stu-id="9924c-108">DirectShow provides two components that locate registered filters:</span></span>

-   <span data-ttu-id="9924c-109">[系統裝置列舉](system-device-enumerator.md)值會依類別目錄來尋找篩選。</span><span class="sxs-lookup"><span data-stu-id="9924c-109">The [System Device Enumerator](system-device-enumerator.md) finds filters by their category.</span></span>
-   <span data-ttu-id="9924c-110">[篩選器](filter-mapper.md)對應程式會根據應用程式所提供的搜尋條件來尋找篩選。</span><span class="sxs-lookup"><span data-stu-id="9924c-110">The [Filter Mapper](filter-mapper.md) finds filters according to search criteria supplied by the application.</span></span>

<span data-ttu-id="9924c-111">本節中所討論的列舉值會遵循 COM 列舉介面所使用的標準格式。</span><span class="sxs-lookup"><span data-stu-id="9924c-111">The enumerators discussed in this section follow the standard form used by COM enumeration interfaces.</span></span> <span data-ttu-id="9924c-112">如需詳細資訊，請參閱 Microsoft 平臺軟體發展工具組 (SDK) 中的「IEnumXXXX」主題。</span><span class="sxs-lookup"><span data-stu-id="9924c-112">For more information, see the "IEnumXXXX" topic in the Microsoft Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="9924c-113">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="9924c-113">This section contains the following topics:</span></span>

-   [<span data-ttu-id="9924c-114">使用系統裝置列舉值</span><span class="sxs-lookup"><span data-stu-id="9924c-114">Using the System Device Enumerator</span></span>](using-the-system-device-enumerator.md)
-   [<span data-ttu-id="9924c-115">使用篩選器對應程式</span><span class="sxs-lookup"><span data-stu-id="9924c-115">Using the Filter Mapper</span></span>](using-the-filter-mapper.md)

## <a name="related-topics"></a><span data-ttu-id="9924c-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="9924c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9924c-117">基本的 DirectShow 工作</span><span class="sxs-lookup"><span data-stu-id="9924c-117">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> </dl>

 

 



