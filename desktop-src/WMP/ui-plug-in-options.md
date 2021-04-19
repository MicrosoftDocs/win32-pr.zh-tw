---
title: UI 外掛程式選項
description: UI 外掛程式選項
ms.assetid: 3c188506-865c-4e0c-965d-1429eafd01ef
keywords:
- Windows Media Player 外掛程式，選項
- 外掛程式，選項
- 使用者介面外掛程式，選項
- UI 外掛程式，選項
- 設定區域外掛程式
- 背景外掛程式
- 分隔視窗外掛程式
- 中繼資料區域外掛程式
- 顯示區域外掛程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281dd0679e6a975b1c867624f2f652f2b3e6b9ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967608"
---
# <a name="ui-plug-in-options"></a><span data-ttu-id="c4fe5-112">UI 外掛程式選項</span><span class="sxs-lookup"><span data-stu-id="c4fe5-112">UI Plug-in Options</span></span>

<span data-ttu-id="c4fe5-113">五個 UI 外掛程式類型的任一個都可以有屬性頁，讓使用者可以在其中修改外掛程式設定。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-113">Any of the five UI plug-in types can have a property page where the user can modify plug-in settings.</span></span> <span data-ttu-id="c4fe5-114">這個屬性頁可以設定為第一次載入外掛程式時自動顯示。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-114">This property page can be set to display automatically when a plug-in is loaded for the first time.</span></span> <span data-ttu-id="c4fe5-115">也可以從 [選項] 對話方塊的 [外掛程式] 索引標籤存取。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-115">It can also be accessed from the Plug-ins tab of the Options dialog box.</span></span>

<span data-ttu-id="c4fe5-116">當 Windows Media Player 啟動時，可以將 UI 外掛程式設定為自動載入。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-116">A UI plug-in can be set to load automatically after installation when Windows Media Player is started.</span></span> <span data-ttu-id="c4fe5-117">如果沒有自動啟動，則使用者可以從 [**工具**] 功能表上的 [**外掛程式]** 清單中選取它來載入它。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-117">If it is not started automatically, the user can load it by selecting it from the **Plug-ins** list on the **Tools** menu.</span></span>

<span data-ttu-id="c4fe5-118">顯示區域外掛程式可以有多個預設值，也就是外掛程式可讓使用者使用的不同視圖。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-118">A display area plug-in can have multiple presets, which are different views that the plug-in can make available to the user.</span></span> <span data-ttu-id="c4fe5-119">使用者可以變更預設值，方法是從 [ **View** ] 功能表上的 [**視覺效果和流覽** 器] 清單中選取不同的專案，或使用狀態訊息和傳輸控制項正上方的 [**目前播放**] 窗格底部提供的箭號按鈕。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-119">The user can change the preset by selecting a different entry from the **Visualizations and Views** list on the **View** menu, or by using the arrow buttons provided at the bottom of the **Now Playing** pane just above the status message and transport controls.</span></span>

<span data-ttu-id="c4fe5-120">背景和個別的視窗 UI 外掛程式可進行程式設計，以接受使用者傳送給它的媒體專案或播放清單。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-120">Background and separate window UI plug-ins can be programmed to accept a media item or playlist that the user sends to it.</span></span> <span data-ttu-id="c4fe5-121">如果外掛程式支援這項功能，其名稱會出現在播放清單控制項或程式庫的快捷方式功能表中的 [ **傳送到** ] 清單上。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-121">If a plug-in supports this feature, its name will appear on the **Send to** list available from the shortcut menu of the playlist control or the library.</span></span>

<span data-ttu-id="c4fe5-122">UI 外掛程式可進行程式設計，以在具有鍵盤焦點時攔截鍵盤快速鍵。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-122">A UI plug-in can be programmed to intercept keyboard shortcuts when it has the keyboard focus.</span></span> <span data-ttu-id="c4fe5-123">載入多個攔截相同鍵盤快速鍵的 UI 外掛程式時，需要鍵盤焦點以防止發生衝突。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-123">Keyboard focus is required to prevent conflicts when multiple UI plug-ins that intercept the same keyboard shortcut are loaded.</span></span> <span data-ttu-id="c4fe5-124">雖然這樣會造成衝突，但也會對使用者造成混淆。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-124">Although this prevents conflicts, it can also cause confusion to end users.</span></span> <span data-ttu-id="c4fe5-125">基於這個理由，不建議使用具有 UI 外掛程式的鍵盤快速鍵。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-125">For this reason, the use of keyboard shortcuts with UI plug-ins is not recommended.</span></span> <span data-ttu-id="c4fe5-126">不過，使用這些方法時，不應攔截 Windows Media Player 所使用的任何鍵盤快速鍵。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-126">When they are used, however, they should not intercept any keyboard shortcuts that are used by Windows Media Player.</span></span> <span data-ttu-id="c4fe5-127">如需播放程式所使用之鍵盤快速鍵的完整清單，請參閱 Windows Media Player 說明。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-127">For a complete list of keyboard shortcuts used by the Player, see Windows Media Player Help.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4fe5-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="c4fe5-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4fe5-129">**UI 外掛程式總覽**</span><span class="sxs-lookup"><span data-stu-id="c4fe5-129">**UI Plug-in Overview**</span></span>](ui-plug-in-overview.md)
</dt> </dl>

 

 




