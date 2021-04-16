---
description: 這行概念在經過一段時間後就已演變出來，並已部分由位址和終端概念取代。 TAPI 3 不直接使用 line 的概念，但 TAPI 2 仍繼續納入此範例。
ms.assetid: 3e457c7d-da2e-4667-aade-053610abbb8a
title: 線條
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8275555e0cb34f5831ce671e22a89a1499fb1796
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567809"
---
# <a name="line"></a><span data-ttu-id="91df0-104">線條</span><span class="sxs-lookup"><span data-stu-id="91df0-104">Line</span></span>

<span data-ttu-id="91df0-105">這行概念在經過一段時間後就已演變出來，並已部分由位址和終端概念取代。</span><span class="sxs-lookup"><span data-stu-id="91df0-105">The line concept has evolved over time and been partly superseded by the Address and Terminal concepts.</span></span> <span data-ttu-id="91df0-106">TAPI 3 不直接使用 line 的概念，但 TAPI 2 仍繼續納入此範例。</span><span class="sxs-lookup"><span data-stu-id="91df0-106">TAPI 3 does not directly use the concept of line, but TAPI 2 continues to incorporate this paradigm.</span></span>

<span data-ttu-id="91df0-107">*線路裝置* 是一種實體裝置，例如傳真板、數據機或連接到網路的 ISDN 卡。</span><span class="sxs-lookup"><span data-stu-id="91df0-107">A *line device* is a physical device such as a fax board, a modem, or an ISDN card that is connected to a network.</span></span> <span data-ttu-id="91df0-108">裝置可能未實際連接到 TAPI 應用程式執行所在的電腦，例如伺服器上的數據機集區。</span><span class="sxs-lookup"><span data-stu-id="91df0-108">The device may not be physically connected to the computer on which the TAPI application is running, such as a modem pool on a server.</span></span> <span data-ttu-id="91df0-109">線路裝置可讓應用程式將資訊傳送至網路或從中接收資訊，藉此支援通訊功能。</span><span class="sxs-lookup"><span data-stu-id="91df0-109">Line devices support communications capabilities by allowing applications to send information to or receive information from a network.</span></span> <span data-ttu-id="91df0-110">線路裝置包含一組一或多個可用於建立呼叫的同質通道。</span><span class="sxs-lookup"><span data-stu-id="91df0-110">A line device contains a set of one or more homogeneous channels that can be used to establish calls.</span></span>

<span data-ttu-id="91df0-111">在 TAPI 2.x 應用程式中，線路裝置是實體電話裝置的邏輯標記法。</span><span class="sxs-lookup"><span data-stu-id="91df0-111">Within TAPI 2.x applications, a line device is the logical representation of a physical telephone device.</span></span> <span data-ttu-id="91df0-112">雖然「行」通常會使用兩個端點來意味著某個專案，但您可以將線路裝置抽象化成單一點，因為 TAPI 會將它視為進入交換器的行進入點。</span><span class="sxs-lookup"><span data-stu-id="91df0-112">Although "line" often connotes something with two endpoints, it is possible to abstract a line device to a single point because TAPI views it only as a point of entry to the line that leads to the switch.</span></span>

![線路裝置](images/ch0501.png)

<span data-ttu-id="91df0-114">雖然上圖中的三行是由不同的硬體所組成，而且用於不同的函式，但它們會抽象化為相同的裝置類型，並受到相同的規則控管。</span><span class="sxs-lookup"><span data-stu-id="91df0-114">Although the three lines in the preceding illustration are composed of different hardware and used for different functions, they are abstracted to the same device type and governed by the same rules.</span></span> <span data-ttu-id="91df0-115">電話不代表電話裝置，而是用於語音通話的線路裝置。</span><span class="sxs-lookup"><span data-stu-id="91df0-115">The telephone represents not a phone device but a line device used for voice calls.</span></span> <span data-ttu-id="91df0-116">當使用此線路裝置進行傳入或傳出的呼叫時，應用程式也需要開啟並控制電話裝置類別的實例，在稍後的章節中會有詳細說明。</span><span class="sxs-lookup"><span data-stu-id="91df0-116">When using this line device for incoming or outgoing calls, the application would also need to open and control an instance of the phone-device class, which is described in detail in later sections.</span></span>

<span data-ttu-id="91df0-117">線路裝置類別是與裝置無關的實體線路裝置（如數據機）標記法。</span><span class="sxs-lookup"><span data-stu-id="91df0-117">The line device class is a device-independent representation of a physical line device, such as a modem.</span></span> <span data-ttu-id="91df0-118">它可包含一或多個相同的通道 (用於在應用程式與交換器或網路之間) 的信號及/或資訊。</span><span class="sxs-lookup"><span data-stu-id="91df0-118">It can contain one or more identical communications channels (used for signaling and/or information) between the application and the switch or network.</span></span> <span data-ttu-id="91df0-119">因為屬於一行的通道具有相同的功能，所以它們是可互換的。</span><span class="sxs-lookup"><span data-stu-id="91df0-119">Because channels belonging to a single line have identical capabilities, they are interchangeable.</span></span> <span data-ttu-id="91df0-120">在許多情況下 (與「POTS) 」一樣，服務提供者會將一行模型為只有一個通道。</span><span class="sxs-lookup"><span data-stu-id="91df0-120">In many cases (as with POTS), a service provider will model a line as having only one channel.</span></span> <span data-ttu-id="91df0-121">其他技術（例如 ISDN）會提供更多的通道，而服務提供者應適當地加以處理。</span><span class="sxs-lookup"><span data-stu-id="91df0-121">Other technologies, like ISDN, offer more channels, and the service provider should treat them accordingly.</span></span>

<span data-ttu-id="91df0-122">**TAPI 2.x：** 應用程式使用 [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) 函式探索行功能。</span><span class="sxs-lookup"><span data-stu-id="91df0-122">**TAPI 2.x:** Applications discover line capabilities using the [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) function.</span></span> <span data-ttu-id="91df0-123">使用 [**lineNegotiateAPIVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateapiversion) [**lineNegotiateExtVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateextversion) 函式的版本協商必須先前已被呼叫。</span><span class="sxs-lookup"><span data-stu-id="91df0-123">Version negotiation using the [**lineNegotiateAPIVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateapiversion) [**lineNegotiateExtVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateextversion) functions must have been previously called.</span></span>

<span data-ttu-id="91df0-124">**TAPI 3.x：** 應用程式主要依賴位址概念。</span><span class="sxs-lookup"><span data-stu-id="91df0-124">**TAPI 3.x:** Applications rely primarily on the address concept.</span></span>

 

 
