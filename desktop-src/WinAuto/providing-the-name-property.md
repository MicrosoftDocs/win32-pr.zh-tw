---
title: 提供 Name 屬性
description: 在建立預先定義和通用的控制項時，伺服器開發人員必須小心，以確保 Microsoft Active Accessibility 可以公開控制項的 [名稱] 屬性。
ms.assetid: 2b4ec5ae-bda1-41e6-9387-6ee3cb6c3163
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d7a4c30c6bc228785a886d9a41717f8cdb8dda
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933335"
---
# <a name="providing-the-name-property"></a><span data-ttu-id="0355b-103">提供 Name 屬性</span><span class="sxs-lookup"><span data-stu-id="0355b-103">Providing the Name Property</span></span>

<span data-ttu-id="0355b-104">在建立預先定義和通用的控制項時，伺服器開發人員必須小心，以確保 Microsoft Active Accessibility 可以公開控制項的 [ [名稱] 屬性](name-property.md) 。</span><span class="sxs-lookup"><span data-stu-id="0355b-104">Server developers must take care when creating predefined and common controls to ensure that Microsoft Active Accessibility can expose the [Name property](name-property.md) for the control.</span></span> <span data-ttu-id="0355b-105">根據控制項的類型，[名稱] 屬性的文字來自下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="0355b-105">Depending on the type of control, the text for the Name property comes from one of the following:</span></span>

-   <span data-ttu-id="0355b-106">控制項的視窗文字 (或標題) </span><span class="sxs-lookup"><span data-stu-id="0355b-106">The control's window text (or caption)</span></span>
-   <span data-ttu-id="0355b-107">標記控制項的靜態文字</span><span class="sxs-lookup"><span data-stu-id="0355b-107">Static text that labels the control</span></span>

<span data-ttu-id="0355b-108">若要尋找控制項的視窗文字，Microsoft Active Accessibility 將 [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext) 訊息傳送至控制項。</span><span class="sxs-lookup"><span data-stu-id="0355b-108">To find the control's window text, Microsoft Active Accessibility sends the [**WM\_GETTEXT**](/windows/desktop/winmsg/wm-gettext) message to the control.</span></span> <span data-ttu-id="0355b-109">此文字對應至控制項的資源定義語句中的 text 參數。</span><span class="sxs-lookup"><span data-stu-id="0355b-109">This text corresponds to the text parameter in the control's resource definition statement.</span></span> <span data-ttu-id="0355b-110">對於某些控制項（例如按鈕），這是與控制項一起顯示的相同文字。</span><span class="sxs-lookup"><span data-stu-id="0355b-110">For some controls, such as buttons, this is the same text that is displayed with the control.</span></span> <span data-ttu-id="0355b-111">若為其他控制項（例如工具列），則不會顯示此文字。</span><span class="sxs-lookup"><span data-stu-id="0355b-111">For other controls, such as toolbars, this text is not displayed.</span></span> <span data-ttu-id="0355b-112">因此，伺服器開發人員必須在控制項的資源定義語句中提供有意義的文字，以協助用戶端公用程式的使用者識別控制項。</span><span class="sxs-lookup"><span data-stu-id="0355b-112">Therefore, server developers must provide meaningful text in the control's resource definition statement to help users of client utilities identify the control.</span></span>

<span data-ttu-id="0355b-113">若要尋找控制項的標籤，Microsoft Active Accessibility 使用 GW HWNDPREV 旗標呼叫 [**GetWindow**](/windows/desktop/api/winuser/nf-winuser-getwindow) 來搜尋靜態文字控制項 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0355b-113">To find the control's label, Microsoft Active Accessibility searches for a static text control by calling [**GetWindow**](/windows/desktop/api/winuser/nf-winuser-getwindow) with the GW\_HWNDPREV flag.</span></span> <span data-ttu-id="0355b-114">如果找到靜態文字控制項，或如果遇到具有視窗樣式 WS \_ GROUP ws TABSTOP 的控制項，則會停止搜尋 \| \_ 。</span><span class="sxs-lookup"><span data-stu-id="0355b-114">The search is halted if a static text control is found, or if a control is encountered that has the window styles WS\_GROUP \| WS\_TABSTOP.</span></span> <span data-ttu-id="0355b-115">此搜尋順序對應至對話方塊上的反向定位順序。</span><span class="sxs-lookup"><span data-stu-id="0355b-115">This search order corresponds to the reverse tab order on a dialog box.</span></span> <span data-ttu-id="0355b-116">伺服器開發人員必須在建立控制項時觀察定位順序，如此一來，靜態文字控制項就會緊接在其所標記的控制項之前。</span><span class="sxs-lookup"><span data-stu-id="0355b-116">Server developers must observe the tab order when creating controls so that a static text control immediately precedes the control that it labels.</span></span>

<span data-ttu-id="0355b-117">如需 Microsoft Active Accessibility 用來公開 [Name 屬性](name-property.md)之技巧的詳細資訊，請參閱 [消費者介面元素參考](user-interface-element-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="0355b-117">For more information about the techniques that Microsoft Active Accessibility uses to expose the [Name property](name-property.md), see [User Interface Element Reference](user-interface-element-reference.md).</span></span>

 

 