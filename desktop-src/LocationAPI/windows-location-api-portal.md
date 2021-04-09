---
description: .
ms.assetid: 0182461a-df06-46ea-a9c2-7aedbde5033b
title: 位置 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f643565e80f72ffcefe6981c924b3739b1c4f5f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849168"
---
# <a name="location-api"></a><span data-ttu-id="e1419-103">位置 API</span><span class="sxs-lookup"><span data-stu-id="e1419-103">Location API</span></span>

<span data-ttu-id="e1419-104">\[Win32 位置 API，並可在 [需求] 區段中指定的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="e1419-104">\[The Win32 Location API and is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e1419-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="e1419-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="e1419-106">相反地，請使用 [**Windows. 地理位置**](/uwp/api/Windows.Devices.Geolocation) API。</span><span class="sxs-lookup"><span data-stu-id="e1419-106">Instead, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.</span></span> <span data-ttu-id="e1419-107">若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="e1419-107">To access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="e1419-108">\]</span><span class="sxs-lookup"><span data-stu-id="e1419-108">\]</span></span>

## <a name="purpose"></a><span data-ttu-id="e1419-109">目的</span><span class="sxs-lookup"><span data-stu-id="e1419-109">Purpose</span></span>

<span data-ttu-id="e1419-110">現今的電腦比以往更容易移動。</span><span class="sxs-lookup"><span data-stu-id="e1419-110">Computers today are more mobile than ever.</span></span> <span data-ttu-id="e1419-111">從小型膝上型電腦到 Tablet Pc，許多電腦都可以在使用者想要前往的任何地方進行。</span><span class="sxs-lookup"><span data-stu-id="e1419-111">From small laptops to Tablet PCs, many computers can go wherever the user wants to go.</span></span> <span data-ttu-id="e1419-112">利用電腦行動性的程式，可為人們的生活帶來顯著的價值。</span><span class="sxs-lookup"><span data-stu-id="e1419-112">Programs that take advantage of the computer's mobility can add significant value to people's lives.</span></span> <span data-ttu-id="e1419-113">例如，可以找到附近餐廳的程式，以及提供駕駛方向，似乎是可攜式電腦的自然擬合。</span><span class="sxs-lookup"><span data-stu-id="e1419-113">For example, a program that can find nearby restaurants and provide driving directions would seem to be a natural fit for a portable computer.</span></span> <span data-ttu-id="e1419-114">但是，雖然用來判斷使用者目前位置的技術是常見且經濟實惠的，但在這項技術上建立解決方案可能是一項艱巨的工作。</span><span class="sxs-lookup"><span data-stu-id="e1419-114">But while the technology to determine the user's current location is common and affordable, building solutions on this technology can be a daunting task.</span></span>

<span data-ttu-id="e1419-115">若要建立位置感知程式，您可能需要克服各種問題，包括：</span><span class="sxs-lookup"><span data-stu-id="e1419-115">To create a location-aware program, you might need to overcome a variety of issues, including:</span></span>

-   <span data-ttu-id="e1419-116">全球定位系統 (GPS) 使用虛擬 COM 埠的裝置，這一次只提供一個程式的存取權。</span><span class="sxs-lookup"><span data-stu-id="e1419-116">Global positioning system (GPS) devices that use virtual COM ports, which provide access for only one program at a time.</span></span>
-   <span data-ttu-id="e1419-117">瞭解和程式設計通訊協定，例如全國航海電子產品協會 (NMEA) 規格，以及專屬廠商延伸模組。</span><span class="sxs-lookup"><span data-stu-id="e1419-117">Understanding and programming for protocols, such as the National Marine Electronics Association (NMEA) specification, as well as proprietary vendor extensions.</span></span>
-   <span data-ttu-id="e1419-118">受限於已知、垂直硬體解決方案的程式設計。</span><span class="sxs-lookup"><span data-stu-id="e1419-118">Being confined to programming for known, vertical hardware solutions.</span></span>
-   <span data-ttu-id="e1419-119">執行邏輯以處理不同位置提供者之間的轉換，例如 GPS 接收器、連線的網路、行動電話通訊網路、網際網路和使用者設定。</span><span class="sxs-lookup"><span data-stu-id="e1419-119">Implementing logic to handle transitions between various location providers, such as GPS receivers, connected networks, cellular telephone networks, the Internet, and user settings.</span></span>

<span data-ttu-id="e1419-120">本檔說明 (API) 的 Windows 位置應用程式設計介面。</span><span class="sxs-lookup"><span data-stu-id="e1419-120">This documentation describes the Windows Location application programming interface (API).</span></span> <span data-ttu-id="e1419-121">位置 API 可提供一種標準方式來取得使用者位置的相關資料，並將位置資料包表的格式標準化，有助於簡化定位感知程式設計。</span><span class="sxs-lookup"><span data-stu-id="e1419-121">The Location API helps to simplify location-aware programming by providing a standard way to retrieve data about user location and standardizing formats for location data reports.</span></span> <span data-ttu-id="e1419-122">位置 API 會自動處理位置資料提供者之間的轉換，而且一律會為目前的情況選擇最準確的提供者。</span><span class="sxs-lookup"><span data-stu-id="e1419-122">The Location API automatically handles transitions between location data providers and always chooses the most accurate provider for the current situation.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="e1419-123">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="e1419-123">Developer audience</span></span>

<span data-ttu-id="e1419-124">位置 API 會透過一組 COM 介面提供其功能。</span><span class="sxs-lookup"><span data-stu-id="e1419-124">The Location API provides its functionality through a set of COM interfaces.</span></span> <span data-ttu-id="e1419-125">您可以透過 c + + 程式設計語言，或在指令碼語言（如 Microsoft JScript）中使用 COM 物件的程式設計人員，使用位置 API 功能。</span><span class="sxs-lookup"><span data-stu-id="e1419-125">Location API functionality can be used by programmers who are familiar with using COM through the C++ programming language, or with using COM objects in scripting languages, such as Microsoft JScript.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e1419-126">本節內容</span><span class="sxs-lookup"><span data-stu-id="e1419-126">In this section</span></span>

-   [<span data-ttu-id="e1419-127">位置 API c + + 程式設計參考</span><span class="sxs-lookup"><span data-stu-id="e1419-127">Location API C++ Programming Reference</span></span>](windows-location-programming-reference.md)
-   [<span data-ttu-id="e1419-128">位置 API 物件模型參考</span><span class="sxs-lookup"><span data-stu-id="e1419-128">Location API Object Model Reference</span></span>](windows-location-script-programming-reference.md)

 

 
