---
description: 本節涵蓋環境光線感應器資料的使用，以及使用者介面功能和程式內容如何針對許多光源條件進行優化。
ms.assetid: c84075b2-ae41-4915-a0f6-3a9c017ae0b8
title: 建立 Light-Aware 使用者介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a4b6d404e366cb898114fe61729ab1ad722feb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944749"
---
# <a name="creating-light-aware-user-interfaces"></a><span data-ttu-id="ff349-103">建立 Light-Aware 使用者介面</span><span class="sxs-lookup"><span data-stu-id="ff349-103">Creating Light-Aware User Interfaces</span></span>

<span data-ttu-id="ff349-104">本節涵蓋環境光線感應器資料的使用，以及使用者介面功能和程式內容如何針對許多光源條件進行優化。</span><span class="sxs-lookup"><span data-stu-id="ff349-104">This section covers the use of ambient light sensor data, and how user interface features and program content can be optimized for many lighting conditions.</span></span>

<span data-ttu-id="ff349-105">環境燈光感應器會公開可用來判斷感應器所在之照明條件各方面的資料。</span><span class="sxs-lookup"><span data-stu-id="ff349-105">Ambient light sensors expose data that can be used to determine various aspects of the lighting conditions where the sensor is located.</span></span> <span data-ttu-id="ff349-106">環境光線感應器可以公開環境的整體亮度 (illuminance) 以及周圍照明的其他層面，例如 chromaticity 或色溫。</span><span class="sxs-lookup"><span data-stu-id="ff349-106">Ambient light sensors can expose the overall brightness of an environment (illuminance) and other aspects of the surrounding light, such as chromaticity or color temperature.</span></span>

<span data-ttu-id="ff349-107">當系統回應照明狀況時，電腦可能會有數種方式可發揮效用。</span><span class="sxs-lookup"><span data-stu-id="ff349-107">Computers can be more useful in several ways when the system is responsive to lighting conditions.</span></span> <span data-ttu-id="ff349-108">這些功能包括控制電腦顯示器的亮度 (Windows 7) 的全新、完整支援功能、自動調整發亮鍵盤的照明等級，甚至是其他燈光的亮度控制 (例如按鈕照明、活動燈等) 。</span><span class="sxs-lookup"><span data-stu-id="ff349-108">These include controlling the brightness of the computer display (a new, fully supported feature in Windows 7), automatically adjusting the lighting level of illuminated keyboards, and even brightness control for other lights (such as button illumination, activity lights, and so on).</span></span>

<span data-ttu-id="ff349-109">終端使用者程式也可以從燈光感應器獲益。</span><span class="sxs-lookup"><span data-stu-id="ff349-109">End-user programs can also benefit from light sensors.</span></span> <span data-ttu-id="ff349-110">程式可以套用適用于特定光源條件的主題，例如特定的室外主題和室內主題。</span><span class="sxs-lookup"><span data-stu-id="ff349-110">Programs can apply a theme that is appropriate for a particular lighting condition, such as a specific outdoor theme and indoor theme.</span></span> <span data-ttu-id="ff349-111">也許最重要的一點是，「光線感應器」與「程式」整合的最重要層面，就是根據光源的可讀性和可讀性優化。</span><span class="sxs-lookup"><span data-stu-id="ff349-111">Perhaps the most important aspect of light sensor integration with programs is readability and legibility optimizations that are based on lighting conditions.</span></span>

<span data-ttu-id="ff349-112">感應器 API 可讓您建立這類程式。</span><span class="sxs-lookup"><span data-stu-id="ff349-112">The Sensor API enables you to create such programs.</span></span> <span data-ttu-id="ff349-113">請考慮下列案例。</span><span class="sxs-lookup"><span data-stu-id="ff349-113">Consider the following scenario.</span></span>

## <a name="scenario-using-your-laptop-to-navigate-to-a-restaurant"></a><span data-ttu-id="ff349-114">案例：使用您的膝上型電腦流覽餐廳</span><span class="sxs-lookup"><span data-stu-id="ff349-114">Scenario: Using your Laptop to Navigate to a Restaurant</span></span>

<span data-ttu-id="ff349-115">假設您想要使用電腦協助您流覽至新餐廳。</span><span class="sxs-lookup"><span data-stu-id="ff349-115">Suppose you want to use your computer to help you navigate to a new restaurant.</span></span> <span data-ttu-id="ff349-116">您會在房屋中開始查詢餐廳的位址，並規劃您的路線。</span><span class="sxs-lookup"><span data-stu-id="ff349-116">You start out in your house, looking up the address of the restaurant and planning your route.</span></span> <span data-ttu-id="ff349-117">下列螢幕擷取畫面顯示您的流覽程式如何優化其 UI，以顯示室內照明條件中的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="ff349-117">The following screen shot shows how your navigation program could optimize its UI to show detailed information in indoor lighting conditions.</span></span>

![針對室內照明設計的 ui。](images/nav-normal.png)

<span data-ttu-id="ff349-119">當您移至您的車輛之外時，您會遇到直接的陽光，這會讓膝上型電腦的螢幕難以閱讀。</span><span class="sxs-lookup"><span data-stu-id="ff349-119">When you go outside to your car, you encounter direct sunlight, which makes the laptop's screen difficult to read.</span></span> <span data-ttu-id="ff349-120">下列螢幕擷取畫面顯示您的程式如何改變其 UI，以最大化可讀性/可讀性。</span><span class="sxs-lookup"><span data-stu-id="ff349-120">The following screen shot shows how your program could alter its UI to maximize legibility/readability in direct light.</span></span> <span data-ttu-id="ff349-121">在此觀點中，大部分的詳細資料都已省略，而且對比會最大化。</span><span class="sxs-lookup"><span data-stu-id="ff349-121">In this view, much of the detail has been omitted and contrast is maximized.</span></span>

![專為直接光源條件設計的 ui。](images/nav-contrast.png)

<span data-ttu-id="ff349-123">當您更接近餐廳、夜間的方法，它的範圍會變暗。</span><span class="sxs-lookup"><span data-stu-id="ff349-123">As you get closer to the restaurant, evening approaches and it gets dark outside.</span></span> <span data-ttu-id="ff349-124">在下列螢幕擷取畫面中，已針對輕量的視覺效果優化流覽程式的 UI。</span><span class="sxs-lookup"><span data-stu-id="ff349-124">In the following screen shot, the UI for the navigation program has been optimized for low-light viewing.</span></span> <span data-ttu-id="ff349-125">藉由整體使用較深的色彩，此 UI 很容易就能在深車中一目了然。</span><span class="sxs-lookup"><span data-stu-id="ff349-125">By using darker colors overall, this UI is easy to glance at in the dark car.</span></span>

![針對低度觀賞而設計的 ui。](images/nav-lowlight.png)

<span data-ttu-id="ff349-127">在本節的其餘部分，您將探索一些可為各種光源條件優化程式，以及如何使用感應器 API 來協助啟用淺感知 UI 的事項。</span><span class="sxs-lookup"><span data-stu-id="ff349-127">In the remainder of this section, you will explore some things that you can do to optimize your programs for various lighting conditions and how you can use the Sensor API to help enable light-aware UI.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ff349-128">本節內容</span><span class="sxs-lookup"><span data-stu-id="ff349-128">In This Section</span></span>

-   [<span data-ttu-id="ff349-129">Light-Aware 的使用者介面基礎</span><span class="sxs-lookup"><span data-stu-id="ff349-129">Fundamentals of Light-Aware User Interfaces</span></span>](fundamentals-of-light-aware-user-interfaces.md)
-   [<span data-ttu-id="ff349-130">Light-Aware 使用者介面的範例</span><span class="sxs-lookup"><span data-stu-id="ff349-130">Examples of Light-Aware User Interfaces</span></span>](examples-of-light-aware-user-interfaces.md)
-   [<span data-ttu-id="ff349-131">優化使用者體驗</span><span class="sxs-lookup"><span data-stu-id="ff349-131">Optimizing the User Experience</span></span>](optimizing-the-user-experience.md)
-   [<span data-ttu-id="ff349-132">瞭解和解讀 Lux 值</span><span class="sxs-lookup"><span data-stu-id="ff349-132">Understanding and Interpreting Lux Values</span></span>](understanding-and-interpreting-lux-values.md)
-   [<span data-ttu-id="ff349-133">使用 Light 感應器資料</span><span class="sxs-lookup"><span data-stu-id="ff349-133">Using Light Sensor Data</span></span>](handling-data-from-multiple-light-sensors.md)

 

 



