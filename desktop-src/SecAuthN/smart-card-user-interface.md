---
description: 智慧卡使用者介面 (UI) 是單一的通用對話方塊，可讓使用者指定或搜尋智慧卡來開啟 (也就是在應用程式) 中連接和使用。
ms.assetid: a64a617a-b2ae-471f-a88f-a73f0fc3a791
title: 智慧卡消費者介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc558446516149529e9a98d28aa9fe94f80b2777
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988934"
---
# <a name="smart-card-user-interface"></a><span data-ttu-id="498ef-103">智慧卡消費者介面</span><span class="sxs-lookup"><span data-stu-id="498ef-103">Smart Card User Interface</span></span>

<span data-ttu-id="498ef-104">智慧卡 [*使用者介面*](../secgloss/u-gly.md) (UI) 是單一的 [*通用對話方塊*](../secgloss/s-gly.md) ，可讓使用者指定或搜尋智慧卡來開啟 (也就是在應用程式) 中連接和使用。</span><span class="sxs-lookup"><span data-stu-id="498ef-104">The smart card [*user interface*](../secgloss/u-gly.md) (UI) is a single [*common dialog box*](../secgloss/s-gly.md) that lets the user specify or search for a smart card to open (that is, connect to and use in an application).</span></span>

<span data-ttu-id="498ef-105">以下是您可以使用 [一般] 對話方塊的兩種方式。</span><span class="sxs-lookup"><span data-stu-id="498ef-105">Following are two ways you can use the common dialog box.</span></span> <span data-ttu-id="498ef-106">兩者都假設將顯示對話方塊 UI。</span><span class="sxs-lookup"><span data-stu-id="498ef-106">Both assume that the dialog box UI will be displayed.</span></span> <span data-ttu-id="498ef-107">如需詳細資訊，請參閱 [**OPENCARDNAME**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea)。</span><span class="sxs-lookup"><span data-stu-id="498ef-107">For more information, see [**OPENCARDNAME**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea).</span></span>

<span data-ttu-id="498ef-108">**若要選取要開啟的智慧卡**</span><span class="sxs-lookup"><span data-stu-id="498ef-108">**To select a smart card to open**</span></span>

1.  <span data-ttu-id="498ef-109">宣告 **OPENCARDNAME** 型別的變數。</span><span class="sxs-lookup"><span data-stu-id="498ef-109">Declare a variable of type **OPENCARDNAME**.</span></span>
2.  <span data-ttu-id="498ef-110">在 [一般] 對話方塊中提供足夠的資訊，以縮小呼叫應用程式所要尋找之智慧卡的搜尋範圍。</span><span class="sxs-lookup"><span data-stu-id="498ef-110">Provide enough information in the common dialog box to narrow the search for a smart card that the calling application is looking for.</span></span> <span data-ttu-id="498ef-111">這包括指定 **lpstrGroupNames**、 **lpstrCardNames** 和 **rgguidInterfaces**。</span><span class="sxs-lookup"><span data-stu-id="498ef-111">This includes specifying **lpstrGroupNames**, **lpstrCardNames**, and **rgguidInterfaces**.</span></span> <span data-ttu-id="498ef-112">這也包括指定慣用的共用模式，以及當通用對話方塊使用 [**OPENCARDNAME**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea)結構的 **dwShareMode** 和 **dwPreferredProtocols** 成員連接到卡片時所要使用的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="498ef-112">This also includes specifying a preferred share mode and protocol to use when the common dialog box connects to the card by using the **dwShareMode** and **dwPreferredProtocols** members of the [**OPENCARDNAME**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea) structure.</span></span>
3.  <span data-ttu-id="498ef-113">呼叫 [**GetOpenCardName**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) 函式，向使用者顯示通用對話方塊。</span><span class="sxs-lookup"><span data-stu-id="498ef-113">Call the [**GetOpenCardName**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) function to display the common dialog box to the user.</span></span> <span data-ttu-id="498ef-114">系統將會顯示簡單的說明資訊行，而且如果找到其中一個所要求的卡片，則會在顯示中反白顯示該卡片。</span><span class="sxs-lookup"><span data-stu-id="498ef-114">A simple help information line will be displayed, and if one of the cards being requested is found, the card will be highlighted in the display.</span></span> <span data-ttu-id="498ef-115">針對多個卡片名稱搜尋，會反白顯示包含其中一個慣用卡片的第一個讀取器。</span><span class="sxs-lookup"><span data-stu-id="498ef-115">For multiple card name searches, the first reader that contains one of the preferred cards will be highlighted.</span></span>
4.  <span data-ttu-id="498ef-116">使用者接著選取卡片，然後按一下 **[確定]**，連接到智慧卡。</span><span class="sxs-lookup"><span data-stu-id="498ef-116">The user then selects a card, clicks **OK**, and connects to the smart card.</span></span>

<span data-ttu-id="498ef-117">**搜尋特定卡片**</span><span class="sxs-lookup"><span data-stu-id="498ef-117">**To search for a specific card**</span></span>

1.  <span data-ttu-id="498ef-118">宣告 **OPENCARDNAME** 型別的變數。</span><span class="sxs-lookup"><span data-stu-id="498ef-118">Declare a variable of type **OPENCARDNAME**.</span></span>
2.  <span data-ttu-id="498ef-119">在 [一般] 對話方塊中提供足夠的資訊，以縮小呼叫應用程式所要尋找之智慧卡的搜尋範圍。</span><span class="sxs-lookup"><span data-stu-id="498ef-119">Provide enough information in the common dialog box to narrow the search for a smart card that the calling application is looking for.</span></span> <span data-ttu-id="498ef-120">這包括指定 **lpstrGroupNames**、 **lpstrCardNames** 和 **rgguidInterfaces**。</span><span class="sxs-lookup"><span data-stu-id="498ef-120">This includes specifying **lpstrGroupNames**, **lpstrCardNames**, and **rgguidInterfaces**.</span></span>
3.  <span data-ttu-id="498ef-121">建立 **Connect**、 **Check** 和 **Disconnect** 回呼函數，並適當地設定 **lpfnConnect**、 **lpfnCheck** 和 **lpfnDisconnect** 資料成員。</span><span class="sxs-lookup"><span data-stu-id="498ef-121">Create the **Connect**, **Check**, and **Disconnect** callback functions, and set the **lpfnConnect**, **lpfnCheck**, and **lpfnDisconnect** data members appropriately.</span></span>
    > [!Note]  
    > <span data-ttu-id="498ef-122">以這種方式使用通用對話方塊時，所有三個函數和成員都必須可用。</span><span class="sxs-lookup"><span data-stu-id="498ef-122">All three functions and members must be available when using the common dialog box in this way.</span></span>

     

4.  <span data-ttu-id="498ef-123">呼叫 [**GetOpenCardName**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) 通用對話方塊函數。</span><span class="sxs-lookup"><span data-stu-id="498ef-123">Call the [**GetOpenCardName**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) common dialog box function.</span></span>
5.  <span data-ttu-id="498ef-124">[一般] 對話方塊接著會搜尋要求的卡片。</span><span class="sxs-lookup"><span data-stu-id="498ef-124">The common dialog box will then search for the requested cards.</span></span> <span data-ttu-id="498ef-125">如果找到相符的卡片名稱或 [*ATR 字串*](../secgloss/a-gly.md) ，就會依序呼叫 **Connect**、 **Check** 和 **Disconnect** 回呼函數。</span><span class="sxs-lookup"><span data-stu-id="498ef-125">If a matching card name or [*ATR string*](../secgloss/a-gly.md) is found, the **Connect**, **Check**, and **Disconnect** callback functions will be called in sequence.</span></span> <span data-ttu-id="498ef-126">如果卡片通過 **檢查** 常式 (亦即， **檢查** 回呼會傳回 **TRUE**) ，則會在顯示中將此卡片反白顯示給使用者。</span><span class="sxs-lookup"><span data-stu-id="498ef-126">If a card passes the **Check** routine (that is, the **Check** callback returns **TRUE**), this card is highlighted in the display to the user.</span></span>
    > [!Note]  
    > <span data-ttu-id="498ef-127">如果指定了多個卡片名稱，則第一個包含其中一個要求之卡片的讀取器，並通過 **檢查** 常式將會是選取的卡片。</span><span class="sxs-lookup"><span data-stu-id="498ef-127">If multiple card names are given, the first reader that contains one of the requested cards and passes the **Check** routine will be the selected card.</span></span>

     

6.  <span data-ttu-id="498ef-128">如果找不到相符專案，則會出現通用對話方塊。</span><span class="sxs-lookup"><span data-stu-id="498ef-128">If no matches are found, a common dialog box will appear.</span></span>

 

 
