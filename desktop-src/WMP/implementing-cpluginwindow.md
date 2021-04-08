---
title: 執行 CPluginWindow
description: 執行 CPluginWindow
ms.assetid: b22723ce-f373-43b1-a098-86a8dbcf485e
keywords:
- Windows Media Player 外掛程式、CPluginWindow 類別
- 外掛程式，CPluginWindow 類別
- 使用者介面外掛程式、CPluginWindow 類別
- UI 外掛程式、CPluginWindow 類別
- CPluginWindow 類別
- 程式設計指南，使用者介面外掛程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe282b0c6cefbcac8fbce76ca53f8e0efaf64874
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672248"
---
# <a name="implementing-cpluginwindow"></a><span data-ttu-id="3e4ce-109">執行 CPluginWindow</span><span class="sxs-lookup"><span data-stu-id="3e4ce-109">Implementing CPluginWindow</span></span>

<span data-ttu-id="3e4ce-110">CPluginWindow 類別會提供使用者介面給外掛程式。</span><span class="sxs-lookup"><span data-stu-id="3e4ce-110">The CPluginWindow class provides the UI to the plug-in.</span></span> <span data-ttu-id="3e4ce-111">在搜尋 UI 外掛程式的案例中，這個類別包含 [ **搜尋** ] 按鈕的程式碼，以及按一下按鈕時啟動搜尋頁面的程式碼。</span><span class="sxs-lookup"><span data-stu-id="3e4ce-111">In the case of the Search UI plug-in, this class contains the code for the **Search** button and the code that launches the search page when the button is clicked.</span></span>

<span data-ttu-id="3e4ce-112">Wizard 在 CPluginWindow .h 標頭檔中提供 CPluginWindow 的基本執行。</span><span class="sxs-lookup"><span data-stu-id="3e4ce-112">The wizard provides a basic implementation of CPluginWindow in the CPluginWindow.h header file.</span></span> <span data-ttu-id="3e4ce-113">為了簡單起見，搜尋 UI 外掛程式會直接修改這個檔案，雖然通常會在個別的 CPluginWindow .cpp 檔案中放置廣泛的新增專案。</span><span class="sxs-lookup"><span data-stu-id="3e4ce-113">To keep things simple, the Search UI plug-in will modify this file directly, although extensive additions would normally be placed in a separate CPluginWindow.cpp file.</span></span>

<span data-ttu-id="3e4ce-114">下列各節說明執行 CPluginWindow 所需執行的動作：</span><span class="sxs-lookup"><span data-stu-id="3e4ce-114">The following sections describe what you need to do to implement CPluginWindow:</span></span>

-   [<span data-ttu-id="3e4ce-115">訊息對應</span><span class="sxs-lookup"><span data-stu-id="3e4ce-115">The Message Map</span></span>](the-message-map.md)
-   [<span data-ttu-id="3e4ce-116">函數</span><span class="sxs-lookup"><span data-stu-id="3e4ce-116">The Constructor</span></span>](the-constructor.md)
-   [<span data-ttu-id="3e4ce-117">OnPaint 方法</span><span class="sxs-lookup"><span data-stu-id="3e4ce-117">The OnPaint Method</span></span>](the-onpaint-method.md)
-   [<span data-ttu-id="3e4ce-118">>oncreate 方法</span><span class="sxs-lookup"><span data-stu-id="3e4ce-118">The OnCreate Method</span></span>](the-oncreate-method.md)
-   [<span data-ttu-id="3e4ce-119">OnSearch 方法</span><span class="sxs-lookup"><span data-stu-id="3e4ce-119">The OnSearch Method</span></span>](the-onsearch-method.md)
-   [<span data-ttu-id="3e4ce-120">LaunchPage 方法</span><span class="sxs-lookup"><span data-stu-id="3e4ce-120">The LaunchPage Method</span></span>](the-launchpage-method.md)

## <a name="related-topics"></a><span data-ttu-id="3e4ce-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="3e4ce-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e4ce-122">**消費者介面外掛程式程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="3e4ce-122">**User Interface Plug-ins Programming Guide**</span></span>](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




