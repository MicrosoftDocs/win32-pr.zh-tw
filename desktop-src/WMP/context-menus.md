---
title: 操作功能表
description: 操作功能表
ms.assetid: d1ea899a-9087-4502-8825-5cef1a87ef03
keywords:
- Windows Media Player 線上商店，內容功能表
- 線上商店、內容功能表
- 輸入1個線上商店、內容功能表
- Windows Media Player 線上商店、自訂內容功能表
- 線上商店、自訂內容功能表
- 輸入1個線上商店、自訂內容功能表
- 內容功能表
- 自訂內容功能表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba3ed52b408651607cb1f6dab1a04f53282d3ef
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374378"
---
# <a name="context-menus"></a><span data-ttu-id="5eeed-111">操作功能表</span><span class="sxs-lookup"><span data-stu-id="5eeed-111">Context Menus</span></span>

<span data-ttu-id="5eeed-112">線上商店可以提供自訂的內容功能表。</span><span class="sxs-lookup"><span data-stu-id="5eeed-112">Online stores can provide custom context menus.</span></span> <span data-ttu-id="5eeed-113">若要這樣做，線上商店外掛程式會執行 [IWMPContentPartner：： GetCommands](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands) 方法。</span><span class="sxs-lookup"><span data-stu-id="5eeed-113">To do this, the online store plug-in implements the [IWMPContentPartner::GetCommands](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands) method.</span></span> <span data-ttu-id="5eeed-114">Windows Media Player 會呼叫這個方法，以提供使用者介面中顯示內容功能表之位置的相關資訊， (使用者以滑鼠右鍵按一下) 。</span><span class="sxs-lookup"><span data-stu-id="5eeed-114">Windows Media Player calls this method to provide information about the location in the user interface where the context menu is displayed (where the user right-clicked).</span></span> <span data-ttu-id="5eeed-115">外掛程式會傳回一組描述每個內容功能表項目的 [WMPCoNtextMenuInfo](/previous-versions/windows/desktop/api/contentpartner/ns-contentpartner-wmpcontextmenuinfo) 結構，包括每個內容功能表項目的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="5eeed-115">The plug-in returns an array of [WMPContextMenuInfo](/previous-versions/windows/desktop/api/contentpartner/ns-contentpartner-wmpcontextmenuinfo) structures that describe each context menu item, including a command ID for each.</span></span>

<span data-ttu-id="5eeed-116">在 Windows Media Player 取出陣列之後，播放程式會使用陣列來建立使用者所看到的內容功能表。</span><span class="sxs-lookup"><span data-stu-id="5eeed-116">After Windows Media Player has retrieved the array, the Player uses the array to build the context menu the user sees.</span></span> <span data-ttu-id="5eeed-117">當使用者按一下內容功能表中的專案時，播放程式會呼叫 [IWMPContentPartner：： InvokeCommand](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand)，並透過 *dwCommandID* 參數傳遞與功能表項目相關聯的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="5eeed-117">When the user clicks an item in the context menu, the Player calls [IWMPContentPartner::InvokeCommand](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand), passing the command ID associated with the menu item through the *dwCommandID* parameter.</span></span> <span data-ttu-id="5eeed-118">播放程式也會傳遞程式庫位置值和識別碼陣列，代表功能表叫用的專案，例如追蹤識別碼的陣列。</span><span class="sxs-lookup"><span data-stu-id="5eeed-118">The Player also passes a library location value and an array of IDs that represents the items the menu was invoked upon, such as an array of track IDs.</span></span> <span data-ttu-id="5eeed-119">藉由使用這項資訊，外掛程式可以啟動任何適當的進程，以回應使用者的滑鼠點擊。</span><span class="sxs-lookup"><span data-stu-id="5eeed-119">By using this information, the plug-in can start any appropriate process in response to the user's mouse click.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5eeed-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="5eeed-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5eeed-121">**關於類型1線上商店**</span><span class="sxs-lookup"><span data-stu-id="5eeed-121">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> </dl>

 

 




