---
title: 附錄 B 標準對話方塊管理員支援
description: Microsoft Active Accessibility 提供標準對話方塊管理員 (SDM) 對話方塊控制項的完整支援。
ms.assetid: cdec2dbd-943b-4160-ae22-c16198cc192a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a710b7f35a242badbff6295d1af0d08cada13fa7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673444"
---
# <a name="appendix-b-standard-dialog-manager-support"></a><span data-ttu-id="5e604-103">附錄 B：標準對話方塊管理員支援</span><span class="sxs-lookup"><span data-stu-id="5e604-103">Appendix B: Standard Dialog Manager Support</span></span>

<span data-ttu-id="5e604-104">Microsoft Active Accessibility 提供標準對話方塊管理員 (SDM) 對話方塊控制項的完整支援。</span><span class="sxs-lookup"><span data-stu-id="5e604-104">Microsoft Active Accessibility provides complete support for Standard Dialog Manager (SDM) dialog box controls.</span></span> <span data-ttu-id="5e604-105">SDM 是 Microsoft 的內部程式碼程式庫，可為 Microsoft 應用程式提供與 Macintosh 和 Microsoft Windows 作業系統之間的差異程度的獨立性。</span><span class="sxs-lookup"><span data-stu-id="5e604-105">SDM is an internal Microsoft code library that provides Microsoft applications with a degree of independence from the differences between the Macintosh and Microsoft Windows operating systems.</span></span> <span data-ttu-id="5e604-106">SDM 主要用於 Microsoft Excel 和 Microsoft Word 中的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="5e604-106">SDM is primarily used for dialog boxes in Microsoft Excel and Microsoft Word.</span></span>

<span data-ttu-id="5e604-107">SDM 會顯示協助工具協助工具的問題，因為它使用了非標準的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="5e604-107">SDM presents problems for accessibility aids because it uses nonstandard implementations of dialog boxes.</span></span> <span data-ttu-id="5e604-108">例如，[SDM] 對話方塊按鈕不會使用 windows 控制碼，與標準使用者介面元素的方式相同。</span><span class="sxs-lookup"><span data-stu-id="5e604-108">For example, SDM dialog box buttons do not use window handles the same way that the standard user interface elements do.</span></span> <span data-ttu-id="5e604-109">您無法將訊息傳送至視窗清單中未包含的按鈕和按鈕。</span><span class="sxs-lookup"><span data-stu-id="5e604-109">You cannot send messages to buttons and buttons are not contained in the window list.</span></span> <span data-ttu-id="5e604-110">使用 SDM 的應用程式會透過私用介面與控制項通訊。</span><span class="sxs-lookup"><span data-stu-id="5e604-110">An application using SDM communicates with the control through a private interface.</span></span>

<span data-ttu-id="5e604-111">下圖顯示 Word 的範例對話方塊。</span><span class="sxs-lookup"><span data-stu-id="5e604-111">The following illustration shows a sample dialog box from Word.</span></span> <span data-ttu-id="5e604-112">雖然它看起來像是使用索引標籤控制項的一般 Windows 對話方塊，但它其實是一個 SDM 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="5e604-112">Although it looks like a regular Windows dialog box that uses the tab control, it is really an SDM dialog box.</span></span>

![選取 [視圖] 索引標籤之 [選項] 對話方塊的螢幕擷取畫面](images/dialog.gif)

 

 




