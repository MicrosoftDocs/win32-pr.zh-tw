---
description: 公開自訂控制項的 substandard 技術描述。
ms.assetid: 107968c6-c3b3-462d-b488-96c69f2b3b14
title: 公開自訂控制項的 Substandard 技術
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1194614474596b55e0b1cf0530a07f9b3c411f6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988903"
---
# <a name="substandard-techniques-for-exposing-custom-controls"></a><span data-ttu-id="606c2-103">公開自訂控制項的 Substandard 技術</span><span class="sxs-lookup"><span data-stu-id="606c2-103">Substandard Techniques for Exposing Custom Controls</span></span>

<span data-ttu-id="606c2-104">如果應用程式不支援 Microsoft Active Accessibility，則可能無法完全存取。</span><span class="sxs-lookup"><span data-stu-id="606c2-104">If an application does not support Microsoft Active Accessibility, it may not be fully accessible.</span></span> <span data-ttu-id="606c2-105">下列技巧轉譯控制項的部分相容：</span><span class="sxs-lookup"><span data-stu-id="606c2-105">The following techniques render controls partially compatible:</span></span>

-   <span data-ttu-id="606c2-106">使用 WM GETTEXT 訊息來查詢控制項時，傳回描述性字串 \_ 。</span><span class="sxs-lookup"><span data-stu-id="606c2-106">Return a descriptive string when the control is queried by using the WM\_GETTEXT message.</span></span> <span data-ttu-id="606c2-107">例如，允許對等按鈕控制項標示為 "Print" 的自訂對等專案傳回「列印按鈕」字串。</span><span class="sxs-lookup"><span data-stu-id="606c2-107">For example, allow a custom equivalent of a button control labeled "Print" to return the string "Print button."</span></span> <span data-ttu-id="606c2-108">這會識別控制項類型和標籤。</span><span class="sxs-lookup"><span data-stu-id="606c2-108">This identifies both control type and label.</span></span> <span data-ttu-id="606c2-109">相同的字串適用于標籤不是文字（例如印表機的圖形）的按鈕。</span><span class="sxs-lookup"><span data-stu-id="606c2-109">The same string is appropriate for a button with a label that is something other than text, such as a graphic of a printer.</span></span> <span data-ttu-id="606c2-110">同樣地，您可以讓行為類似核取方塊的自訂控制項傳回標題字串「已啟用列印」核取方塊。</span><span class="sxs-lookup"><span data-stu-id="606c2-110">Similarly, allow a custom control that behaves like a check box to return the caption string "Printing Enabled check box, checked."</span></span>
-   <span data-ttu-id="606c2-111">支援 WM \_ GETDLGCODE 訊息，識別支援的鍵盤輸入。</span><span class="sxs-lookup"><span data-stu-id="606c2-111">Support the WM\_GETDLGCODE message, identifying the keyboard input that is supported.</span></span> <span data-ttu-id="606c2-112">例如，允許編輯控制項的自訂對等，藉由傳回 \_ DLGC HASSETSEL 來處理 WM GETDLGCODE，方法是在 \_ 處理訊息來設定選取專案時，DLGC \_ WANTARROWS （如果它使用方向鍵），而 DLGC \_ WANTCHARS 表示它使用字元輸入。</span><span class="sxs-lookup"><span data-stu-id="606c2-112">For example, allow a custom equivalent of an edit control to handle WM\_GETDLGCODE by returning DLGC\_HASSETSEL if it handles messages to set the selection, DLGC\_WANTARROWS if it uses arrow keys, and DLGC\_WANTCHARS to indicate that it uses character input.</span></span>
    > [!Note]  
    > <span data-ttu-id="606c2-113">只有具有自己的視窗控制碼的控制項可以回應 WM \_ GETTEXT 和 wm \_ GETDLGCODE 訊息。</span><span class="sxs-lookup"><span data-stu-id="606c2-113">Only controls that have their own window handles can respond to the WM\_GETTEXT and WM\_GETDLGCODE messages.</span></span>

     

<span data-ttu-id="606c2-114">為了避免協助工具協助工具的相容性問題，您應該在設計自訂控制項時，仔細遵循 Active Accessibility 的指導方針。</span><span class="sxs-lookup"><span data-stu-id="606c2-114">To avoid compatibility problems with accessibility aids, you should follow Active Accessibility guidelines closely when designing custom controls.</span></span> <span data-ttu-id="606c2-115">如需有關如何避免相容性問題與協助工具輔助的詳細資訊，請參閱 [協助工具](../accessibility/accessibility.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="606c2-115">For more information about how to avoid compatibility problems with accessibility aids, see the [Accessibility](../accessibility/accessibility.md) section.</span></span>

 

 
