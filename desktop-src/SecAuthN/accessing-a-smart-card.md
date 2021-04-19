---
description: 說明應用程式或服務提供者可以使用智慧卡子系統連接到智慧卡的方式。
ms.assetid: 27f8f25f-1883-4070-94a4-0d3c51032378
title: 存取智慧卡
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b155d467c9de28b1e02dea01511ea1e71d574eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987575"
---
# <a name="accessing-a-smart-card"></a><span data-ttu-id="4d64c-103">存取智慧卡</span><span class="sxs-lookup"><span data-stu-id="4d64c-103">Accessing a Smart Card</span></span>

<span data-ttu-id="4d64c-104">[*智慧卡*](/windows/desktop/SecGloss/s-gly)子系統提供數種方法，讓應用程式或 [*服務提供者*](/windows/desktop/SecGloss/c-gly)連接到智慧卡：</span><span class="sxs-lookup"><span data-stu-id="4d64c-104">The [*smart card*](/windows/desktop/SecGloss/s-gly) subsystem provides several means for an application or [*service provider*](/windows/desktop/SecGloss/c-gly) to connect to a smart card:</span></span>

-   <span data-ttu-id="4d64c-105">應用程式可以呼叫 [**SCardConnect**](/windows/desktop/api/Winscard/nf-winscard-scardconnecta) ，以連接到位於指定讀取器中的卡片。</span><span class="sxs-lookup"><span data-stu-id="4d64c-105">An application can call [**SCardConnect**](/windows/desktop/api/Winscard/nf-winscard-scardconnecta) to connect to a card that resides in a given reader.</span></span> <span data-ttu-id="4d64c-106">這是與智慧卡建立通訊的最簡單方式。</span><span class="sxs-lookup"><span data-stu-id="4d64c-106">This is the simplest way to establish communication with a smart card.</span></span>
-   <span data-ttu-id="4d64c-107">應用程式可以在指定的讀者群組內搜尋特定的智慧卡。</span><span class="sxs-lookup"><span data-stu-id="4d64c-107">An application can search for a specific smart card within a given reader group.</span></span> <span data-ttu-id="4d64c-108">應用程式會依其顯示名稱來識別卡片，並指定卡片可能出現的讀取器清單。</span><span class="sxs-lookup"><span data-stu-id="4d64c-108">The application identifies the card by its display name, and specifies a list of readers in which the card may appear.</span></span> <span data-ttu-id="4d64c-109">[*資源管理員*](/windows/desktop/SecGloss/r-gly)會在讀取器清單中搜尋 [*ATR 字串*](/windows/desktop/SecGloss/a-gly)符合命名卡，並將狀態資訊傳回給應用程式的所有卡片。</span><span class="sxs-lookup"><span data-stu-id="4d64c-109">The [*resource manager*](/windows/desktop/SecGloss/r-gly) searches the list of readers for any cards with an [*ATR string*](/windows/desktop/SecGloss/a-gly) that matches the named card, and returns status information to the application.</span></span> <span data-ttu-id="4d64c-110">[*智慧卡子系統*](/windows/desktop/SecGloss/s-gly)絕對不會在取得 ATR 字串的情況下，使用 GUI 或與卡片互動。</span><span class="sxs-lookup"><span data-stu-id="4d64c-110">The [*smart card subsystem*](/windows/desktop/SecGloss/s-gly) never puts up a GUI or interacts with the card beyond obtaining the ATR string.</span></span> <span data-ttu-id="4d64c-111">但是，它會提供足夠的資訊給應用程式或通用控制項，讓使用者能夠透過尋找所需的卡片或卡片類型來引導使用者。</span><span class="sxs-lookup"><span data-stu-id="4d64c-111">It does, however, supply sufficient information for the application or a common control to be able to walk the user through locating the desired card or card type.</span></span> <span data-ttu-id="4d64c-112">這會導致將要求對應至特定讀取器，以進一步的 i/o 導向。</span><span class="sxs-lookup"><span data-stu-id="4d64c-112">This results in mapping the request to a specific reader, to which further I/O is directed.</span></span>
-   <span data-ttu-id="4d64c-113">應用程式可以要求支援一組指定智慧卡介面的卡片清單。</span><span class="sxs-lookup"><span data-stu-id="4d64c-113">An application can request a list of cards supporting a given set of smart card interfaces.</span></span> <span data-ttu-id="4d64c-114">然後，應用程式可以使用先前案例中的清單。</span><span class="sxs-lookup"><span data-stu-id="4d64c-114">The application can then use the list in the previous case.</span></span> <span data-ttu-id="4d64c-115">這可讓應用程式根據其功能連接到卡片，而不考慮其名稱。</span><span class="sxs-lookup"><span data-stu-id="4d64c-115">This allows applications to connect to cards based on their capabilities, without regard to their names.</span></span>

<span data-ttu-id="4d64c-116">當應用程式尋找卡片時，它會提供要在其中查看的讀者名稱陣列。</span><span class="sxs-lookup"><span data-stu-id="4d64c-116">When an application looks for a card, it supplies an array of reader names in which to look.</span></span> <span data-ttu-id="4d64c-117">資源管理員會針對陣列中的每個讀取器元素提供下列資訊：</span><span class="sxs-lookup"><span data-stu-id="4d64c-117">For each reader element in the array, the resource manager supplies the following information:</span></span>

-   <span data-ttu-id="4d64c-118">此應用程式是否可使用讀取器。</span><span class="sxs-lookup"><span data-stu-id="4d64c-118">Whether the reader is available for use by this application.</span></span>
-   <span data-ttu-id="4d64c-119">是否有卡片插入此讀取器，如果有的話，它的 ATR 字串是什麼。</span><span class="sxs-lookup"><span data-stu-id="4d64c-119">Whether there is a card inserted into this reader, and if so, what its ATR string is.</span></span>
-   <span data-ttu-id="4d64c-120">卡片的 ATR 字串是否符合任何要求的卡片 ATR 字串。</span><span class="sxs-lookup"><span data-stu-id="4d64c-120">Whether the card's ATR string matches any of the requested cards' ATR strings.</span></span>

<span data-ttu-id="4d64c-121">應用程式會使用傳回的資訊，將進一步的篩選套用到卡片，或提示使用者選取所需的卡片。</span><span class="sxs-lookup"><span data-stu-id="4d64c-121">The application uses the returned information to apply further filters to the cards or to prompt the user to select the desired card.</span></span> <span data-ttu-id="4d64c-122">請注意，可能會開啟一或多個已傳回的讀取器清單，供其他應用程式使用，因此不保證無法存取這份讀取器清單。</span><span class="sxs-lookup"><span data-stu-id="4d64c-122">Note that one or more of the returned list of readers may be opened for exclusive use by other applications, so access to this list of readers is not guaranteed.</span></span>

 

 
