---
description: 使用 DVD 功能表
ms.assetid: 8c5f8072-b74f-4e15-8991-73bcc4145fd2
title: 使用 DVD 功能表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 113647a37200762b5eaf0a9ac231dea74ad19925
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982120"
---
# <a name="working-with-dvd-menus"></a><span data-ttu-id="85749-103">使用 DVD 功能表</span><span class="sxs-lookup"><span data-stu-id="85749-103">Working With DVD Menus</span></span>

<span data-ttu-id="85749-104">當使用者啟用按鈕時，或當導覽器進入第一個 Play 網域時，DVD 導覽器可能會顯示功能表。</span><span class="sxs-lookup"><span data-stu-id="85749-104">The DVD Navigator might show a menu when the user activates a button, or when the Navigator enters the First Play domain.</span></span> <span data-ttu-id="85749-105">若要以程式設計方式顯示功能表，請呼叫 [**IDvdControl2：： ShowMenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-showmenu) 方法。</span><span class="sxs-lookup"><span data-stu-id="85749-105">To show a menu programmatically, call the [**IDvdControl2::ShowMenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-showmenu) method.</span></span>

<span data-ttu-id="85749-106">有幾種方式可以透過程式設計方式選取功能表按鈕：</span><span class="sxs-lookup"><span data-stu-id="85749-106">There are several ways to select menu buttons programmatically:</span></span>

-   <span data-ttu-id="85749-107">若要依數位選取按鈕，請呼叫 [**IDvdControl2：： SelectButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectbutton)。</span><span class="sxs-lookup"><span data-stu-id="85749-107">To select a button by number, call [**IDvdControl2::SelectButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectbutton).</span></span> <span data-ttu-id="85749-108">按鈕的編號為1到36。</span><span class="sxs-lookup"><span data-stu-id="85749-108">Buttons are numbered 1 to 36.</span></span> <span data-ttu-id="85749-109">[**IDvdInfo2：： GetCurrentButton**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentbutton)方法會傳回可用的按鈕數目。</span><span class="sxs-lookup"><span data-stu-id="85749-109">The [**IDvdInfo2::GetCurrentButton**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentbutton) method returns the number of available buttons.</span></span>
-   <span data-ttu-id="85749-110">若要選取相對於目前所選按鈕位置的按鈕，請呼叫 [**IDvdControl2：： SelectRelativeButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectrelativebutton)。</span><span class="sxs-lookup"><span data-stu-id="85749-110">To select a button relative to the position of the currently selected button, call [**IDvdControl2::SelectRelativeButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectrelativebutton).</span></span> <span data-ttu-id="85749-111">您可以選取 [上]、[下]、[左] 或 [右] 方向的按鈕。</span><span class="sxs-lookup"><span data-stu-id="85749-111">You can select a button in the up, down, left, or right direction.</span></span>
-   <span data-ttu-id="85749-112">若要依視窗內的座標選取按鈕，請呼叫 [**IDvdControl2：： SelectAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectatposition)。</span><span class="sxs-lookup"><span data-stu-id="85749-112">To select a button by its coordinates within the window, call [**IDvdControl2::SelectAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectatposition).</span></span> <span data-ttu-id="85749-113">這個方法會採用相對於影片視窗工作區的 (x，y) 座標。</span><span class="sxs-lookup"><span data-stu-id="85749-113">This method takes (x,y) coordinates relative to the client area of the video window.</span></span> <span data-ttu-id="85749-114"> (無視窗模式，這是應用程式視窗。 ) 如果該位置沒有任何按鈕，此方法會傳回 VFW \_ E \_ DVD \_ no \_ 按鈕。</span><span class="sxs-lookup"><span data-stu-id="85749-114">(For windowless mode, this is the application window.) If there is no button at that location, the method returns VFW\_E\_DVD\_NO\_BUTTON.</span></span>

<span data-ttu-id="85749-115">此外，還有數種方式可以啟用按鈕：</span><span class="sxs-lookup"><span data-stu-id="85749-115">In addition, there are several ways to activate a button:</span></span>

-   <span data-ttu-id="85749-116">若要依數位啟動按鈕，請呼叫 [**IDvdControl2：： SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton)。</span><span class="sxs-lookup"><span data-stu-id="85749-116">To activate a button by number, call [**IDvdControl2::SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton).</span></span>
-   <span data-ttu-id="85749-117">若要依據按鈕的座標啟動按鈕，請呼叫 [**IDvdControl2：： ActivateAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activateatposition)。</span><span class="sxs-lookup"><span data-stu-id="85749-117">To activate a button by its coordinates, call [**IDvdControl2::ActivateAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activateatposition).</span></span>
-   <span data-ttu-id="85749-118">若要啟動目前選取的按鈕，請呼叫 [**IDvdControl2：： ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton)。</span><span class="sxs-lookup"><span data-stu-id="85749-118">To activate the button that is currently selected, call [**IDvdControl2::ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton).</span></span> <span data-ttu-id="85749-119">如果未選取任何按鈕，此方法會傳回 VFW \_ E \_ DVD \_ no \_ 按鈕。</span><span class="sxs-lookup"><span data-stu-id="85749-119">If no button is selected, the method returns VFW\_E\_DVD\_NO\_BUTTON.</span></span>

<span data-ttu-id="85749-120">請記住，選取按鈕只會反白顯示其框線。</span><span class="sxs-lookup"><span data-stu-id="85749-120">Keep in mind that selecting a button merely highlights its borders.</span></span> <span data-ttu-id="85749-121">若要引發相關聯的命令，必須啟用按鈕。</span><span class="sxs-lookup"><span data-stu-id="85749-121">To cause the associated command to be fired, the button must be activated.</span></span> <span data-ttu-id="85749-122">以程式設計方式啟用按鈕可透過各種方式來完成，但您必須一律先選取按鈕，才能啟用它。</span><span class="sxs-lookup"><span data-stu-id="85749-122">Activating a button programmatically can be done in various ways, but the button must always be selected before it can be activated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="85749-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="85749-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85749-124">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="85749-124">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



