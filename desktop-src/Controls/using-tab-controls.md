---
title: 使用索引標籤控制項
description: 本主題包含兩個使用索引標籤控制項的範例。
ms.assetid: 29cc2f47-5667-4b03-8af8-51995a90a3dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78432e24f85ed3fa6a3c71a056ae25ede920f6e0
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "104463841"
---
# <a name="using-tab-controls"></a><span data-ttu-id="aff6b-103">使用索引標籤控制項</span><span class="sxs-lookup"><span data-stu-id="aff6b-103">Using Tab Controls</span></span>

<span data-ttu-id="aff6b-104">本主題包含兩個使用索引標籤控制項的範例。</span><span class="sxs-lookup"><span data-stu-id="aff6b-104">This topic contains two examples that use tab controls.</span></span> <span data-ttu-id="aff6b-105">第一個範例示範如何使用索引標籤控制項，在應用程式主視窗中的多個文字頁面之間切換。</span><span class="sxs-lookup"><span data-stu-id="aff6b-105">The first example demonstrates how to use a tab control to switch between multiple pages of text in an application's main window.</span></span> <span data-ttu-id="aff6b-106">第二個範例示範如何使用索引標籤控制項，在對話方塊中的多個控制項頁面之間切換。</span><span class="sxs-lookup"><span data-stu-id="aff6b-106">The second example demonstrates how to use a tab control to switch between multiple pages of controls in a dialog box.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="aff6b-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="aff6b-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aff6b-108">主題</span><span class="sxs-lookup"><span data-stu-id="aff6b-108">Topic</span></span></th>
<th><span data-ttu-id="aff6b-109">描述</span><span class="sxs-lookup"><span data-stu-id="aff6b-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aff6b-110"><a href="create-a-tab-control-in-the-main-window.md">如何在主視窗中建立索引標籤控制項</a></span><span class="sxs-lookup"><span data-stu-id="aff6b-110"><a href="create-a-tab-control-in-the-main-window.md">How to Create a Tab Control in the Main Window</a></span></span><br/></td>
<td><span data-ttu-id="aff6b-111">本節中的範例將示範如何建立索引標籤控制項，並將其顯示在應用程式主視窗的工作區中。</span><span class="sxs-lookup"><span data-stu-id="aff6b-111">The example in this section demonstrates how to create a tab control and display it in the client area of the application's main window.</span></span> <span data-ttu-id="aff6b-112">應用程式會在索引標籤控制項的顯示區域中，顯示 (靜態控制項) 的第三個視窗。</span><span class="sxs-lookup"><span data-stu-id="aff6b-112">The application displays a third window (a static control) in the display area of the tab control.</span></span> <span data-ttu-id="aff6b-113">父視窗在處理 <a href="/windows/desktop/winmsg/wm-size"><strong>WM_SIZE</strong></a> 訊息時，會定位並調整索引標籤控制項和靜態控制項的大小。</span><span class="sxs-lookup"><span data-stu-id="aff6b-113">The parent window positions and sizes the tab control and static control when it processes the <a href="/windows/desktop/winmsg/wm-size"><strong>WM_SIZE</strong></a> message.</span></span> <br/> <span data-ttu-id="aff6b-114">此範例中有七個索引標籤，一周的每一天都有一個。</span><span class="sxs-lookup"><span data-stu-id="aff6b-114">There are seven tabs in this example, one for each day of the week.</span></span> <span data-ttu-id="aff6b-115">當使用者選取索引標籤時，應用程式會在靜態控制項中顯示對應日期的名稱。</span><span class="sxs-lookup"><span data-stu-id="aff6b-115">When the user selects a tab, the application displays the name of the corresponding day in the static control.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aff6b-116"><a href="create-a-tabbed-dialog-box.md">如何建立索引標籤式對話方塊</a></span><span class="sxs-lookup"><span data-stu-id="aff6b-116"><a href="create-a-tabbed-dialog-box.md">How to Create a Tabbed Dialog Box</a></span></span><br/></td>
<td><span data-ttu-id="aff6b-117">本節中的範例將示範如何建立使用 tab 鍵來提供多個控制項頁面的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="aff6b-117">The example in this section demonstrates how to create a dialog box that uses tabs to provide multiple pages of controls.</span></span> <span data-ttu-id="aff6b-118">主要對話方塊是強制回應對話方塊。</span><span class="sxs-lookup"><span data-stu-id="aff6b-118">The main dialog box is a modal dialog box.</span></span> <span data-ttu-id="aff6b-119">每一頁的控制項都是由具有 <a href="/windows/desktop/winmsg/window-styles"><strong>WS_CHILD</strong></a> 樣式的對話方塊範本所定義。</span><span class="sxs-lookup"><span data-stu-id="aff6b-119">Each page of controls is defined by a dialog box template that has the <a href="/windows/desktop/winmsg/window-styles"><strong>WS_CHILD</strong></a> style.</span></span> <span data-ttu-id="aff6b-120">選取索引標籤時，就會為傳入頁面建立非強制回應對話方塊，並終結傳出頁面的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="aff6b-120">When a tab is selected, a modeless dialog box is created for the incoming page and the dialog box for the outgoing page is destroyed.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="aff6b-121">在許多情況下，您可以使用屬性工作表更輕鬆地執行多頁對話方塊。</span><span class="sxs-lookup"><span data-stu-id="aff6b-121">In many cases, you can implement multiple-page dialog boxes more easily by using property sheets.</span></span> <span data-ttu-id="aff6b-122">如需屬性工作表的詳細資訊，請參閱 <a href="property-sheets.md">關於屬性工作表</a>。</span><span class="sxs-lookup"><span data-stu-id="aff6b-122">For more information about property sheets, see <a href="property-sheets.md">About Property Sheets</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="aff6b-123">主要對話方塊的範本只會定義兩個按鈕控制項。</span><span class="sxs-lookup"><span data-stu-id="aff6b-123">The template for the main dialog box simply defines two button controls.</span></span> <span data-ttu-id="aff6b-124">處理 <a href="/windows/desktop/dlgbox/wm-initdialog"><strong>WM_INITDIALOG</strong></a> 訊息時，對話方塊程式會建立一個索引標籤控制項，並為每個子對話方塊載入對話方塊範本資源。</span><span class="sxs-lookup"><span data-stu-id="aff6b-124">When processing the <a href="/windows/desktop/dlgbox/wm-initdialog"><strong>WM_INITDIALOG</strong></a> message, the dialog box procedure creates a tab control and loads the dialog box template resources for each of the child dialog boxes.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

