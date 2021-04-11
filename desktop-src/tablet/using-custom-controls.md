---
description: 針對 Tablet PC 使用客戶控制項的說明。
ms.assetid: 43d78acd-1f02-417d-97be-1682e90a81a2
title: 使用自訂控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c713d2b3912d2bbe4a689c7d8d05d4d977a6eb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847979"
---
# <a name="using-custom-controls"></a><span data-ttu-id="68fa6-103">使用自訂控制項</span><span class="sxs-lookup"><span data-stu-id="68fa6-103">Using Custom Controls</span></span>

<span data-ttu-id="68fa6-104">您可以自訂標準控制項，方法是使用主控描繪來變更控制項的外觀，並建立超類別或子類別來變更控制項的行為。</span><span class="sxs-lookup"><span data-stu-id="68fa6-104">You can customize standard controls by using owner-drawing to change the control's appearance and establishing a superclass or subclass to change the control's behavior.</span></span> <span data-ttu-id="68fa6-105">在每個案例中，標準控制項類型的基礎系統程式碼會處理基本的控制函數。</span><span class="sxs-lookup"><span data-stu-id="68fa6-105">In each case, the underlying system code for the standard control type handles basic control functions.</span></span> <span data-ttu-id="68fa6-106">如果您正確地使用這些控制項，就可以存取這些控制項。</span><span class="sxs-lookup"><span data-stu-id="68fa6-106">Most of these controls can be accessible if you use them properly.</span></span>

<span data-ttu-id="68fa6-107">以標準控制項為基礎的主控描繪控制項，會顯示為輔助功能輔助的標準控制項，並支援 Microsoft Active Accessibility;不過，它有自訂的外觀。</span><span class="sxs-lookup"><span data-stu-id="68fa6-107">An owner-drawn control that is based on a standard control appears as the standard control to accessibility aids and supports Microsoft Active Accessibility; however, it has a customized appearance.</span></span> <span data-ttu-id="68fa6-108">有些應用程式會使用自訂控制項來變更控制項的外觀，但主控描繪的控制項是更容易存取的方案。</span><span class="sxs-lookup"><span data-stu-id="68fa6-108">Some applications use custom controls to change the appearance of a control, but owner-drawn controls are a more accessible solution.</span></span> <span data-ttu-id="68fa6-109">如需如何定義主控描繪功能表和公開主控描繪控制項的詳細資訊，請參閱 [協助工具](../accessibility/accessibility.md)。</span><span class="sxs-lookup"><span data-stu-id="68fa6-109">For more information about how to define owner-drawn menus and expose owner-drawn controls, see [Accessibility](../accessibility/accessibility.md).</span></span>

<span data-ttu-id="68fa6-110">建立超級類別或子類別是自訂現有控制項行為的技巧。</span><span class="sxs-lookup"><span data-stu-id="68fa6-110">Establishing a superclass or subclass is a technique for customizing the behavior of existing controls.</span></span> <span data-ttu-id="68fa6-111">視控制項的新行為而定，可能需要補充其公開的協助工具資訊。</span><span class="sxs-lookup"><span data-stu-id="68fa6-111">Depending on the new behavior of the control, it may be necessary to supplement the accessibility information that it exposes.</span></span> <span data-ttu-id="68fa6-112">例如，應用程式可以使用主控描繪的控制項，在選取的核取方塊中顯示 X，而不是以圖片（而非單字）標示命令按鈕。</span><span class="sxs-lookup"><span data-stu-id="68fa6-112">For example, an application can use an owner-drawn control to display an X in a selected check box, rather than a check mark, or label a command button with a picture instead of a word.</span></span>

<span data-ttu-id="68fa6-113">使用屬於超類別或子類別的擁有者繪製控制項時：</span><span class="sxs-lookup"><span data-stu-id="68fa6-113">When using owner-drawn controls that are either a superclass or a subclass:</span></span>

-   <span data-ttu-id="68fa6-114">提供所有控制項的標籤，即使在畫面上看不到標籤。</span><span class="sxs-lookup"><span data-stu-id="68fa6-114">Provide labels for all controls, even when the labels are not visible on the screen.</span></span> <span data-ttu-id="68fa6-115">如果您自訂控制項，使標準標題無法顯示 (例如，具有圖形面的按鈕) ，並將標題保留為空白字串，協助工具輔助程式就無法取得標題並使用它來識別控制項。</span><span class="sxs-lookup"><span data-stu-id="68fa6-115">If you customize a control so that the standard caption is not visible (for example, a button with a graphic face) and leave the caption as a blank string, the accessibility aid is not able to get the caption and use it to identify the control.</span></span>
-   <span data-ttu-id="68fa6-116">確定支援 [**WM \_ GETTEXT**](../winmsg/wm-gettext.md) 。</span><span class="sxs-lookup"><span data-stu-id="68fa6-116">Ensure that [**WM\_GETTEXT**](../winmsg/wm-gettext.md) is supported.</span></span>
-   <span data-ttu-id="68fa6-117">確定支援所有類別特定的訊息。</span><span class="sxs-lookup"><span data-stu-id="68fa6-117">Ensure that all class-specific messages are supported.</span></span> <span data-ttu-id="68fa6-118">更重要的是，支援如 [**CB \_ GETLBTEXT**](../controls/cb-getlbtext.md) 和 [**LB \_ GETTEXT**](../controls/lb-gettext.md)等文字抓取訊息。</span><span class="sxs-lookup"><span data-stu-id="68fa6-118">It is especially important to support text-retrieval messages such as [**CB\_GETLBTEXT**](../controls/cb-getlbtext.md) and [**LB\_GETTEXT**](../controls/lb-gettext.md).</span></span> <span data-ttu-id="68fa6-119">設定適當的樣式位，例如 **CBS \_ HASSTRINGS** 和 **磅 \_ HASSTRINGS**，以指出控制項支援這些訊息。</span><span class="sxs-lookup"><span data-stu-id="68fa6-119">Set the appropriate style bits, such as **CBS\_HASSTRINGS** and **LBS\_HASSTRINGS**, to indicate the control supports those messages.</span></span>

 

 
