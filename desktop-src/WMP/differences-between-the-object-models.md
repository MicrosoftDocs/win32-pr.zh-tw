---
title: 物件模型之間的差異
description: 物件模型之間的差異
ms.assetid: a6d2a2d5-2892-461a-aa6d-7e11b504b2af
keywords:
- Windows Media Player，物件模型
- Windows Media Player 物件模型，版本差異
- 物件模型，版本差異
- Windows Media Player ActiveX 控制項，版本差異
- ActiveX 控制項，版本差異
- Windows Media Player 的行動 ActiveX 控制項，版本差異
- Windows Media Player 行動裝置，物件模型
- 遷移指南，版本差異
- Windows Media Player 的版本，物件模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a5341067e2daad0f44fbdd7075f0f543bac2fd4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969471"
---
# <a name="differences-between-the-object-models"></a><span data-ttu-id="addac-112">物件模型之間的差異</span><span class="sxs-lookup"><span data-stu-id="addac-112">Differences Between the Object Models</span></span>

<span data-ttu-id="addac-113">Windows Media Player 6.4 物件模型和 Windows Media Player 7 或更新版本的物件模型之間有兩個主要差異。</span><span class="sxs-lookup"><span data-stu-id="addac-113">There are two primary differences between the Windows Media Player 6.4 object model and the Windows Media Player 7 or later object model.</span></span>

-   <span data-ttu-id="addac-114">**CLSID** Windows Media Player 7 或更新版本的物件模型完全離開6.4 版物件模型。</span><span class="sxs-lookup"><span data-stu-id="addac-114">**CLSID** The Windows Media Player 7 or later object model is a complete departure from the version 6.4 object model.</span></span> <span data-ttu-id="addac-115">元件物件模型 (COM) 規格需要所有現有的介面都必須在新版本的 COM 元件中繼續運作。</span><span class="sxs-lookup"><span data-stu-id="addac-115">The Component Object Model (COM) specification requires that all existing interfaces must continue to function in new versions of a COM component.</span></span> <span data-ttu-id="addac-116">這表示新介面可以新增至 COM 元件，但永遠不會改變現有的介面，以確保較舊的用戶端程式代碼一律會使用其設計所使用的特定元件。</span><span class="sxs-lookup"><span data-stu-id="addac-116">This means that new interfaces can be added to a COM component, but existing interfaces must never be altered, ensuring older client code will always work with the particular component it was designed to use.</span></span> <span data-ttu-id="addac-117">因此，Windows Media Player 7 或更新版本的 ActiveX 控制項有新的類別識別碼：6BF52A52-394A-11D3-B153-00C04F79FAA6。</span><span class="sxs-lookup"><span data-stu-id="addac-117">Therefore, the Windows Media Player 7 or later ActiveX control has a new class ID: 6BF52A52-394A-11D3-B153-00C04F79FAA6.</span></span> <span data-ttu-id="addac-118">如果您想要利用此版本之控制項的新功能，則必須變更您的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="addac-118">If you want to take advantage of the new functionality of the control for this version, you must change your CLSID.</span></span>
-   <span data-ttu-id="addac-119">**階層式物件模型** 如果您已經使用 Windows Media Player 6.4 ActiveX 控制項，可能已經注意到所有屬性、方法和事件都是透過相同的物件來存取： **Player** 物件。</span><span class="sxs-lookup"><span data-stu-id="addac-119">**Hierarchical Object Model** If you've been using the Windows Media Player 6.4 ActiveX control, you may have noticed that all the properties, methods, and events are accessed through the same object: the **Player** object.</span></span> <span data-ttu-id="addac-120">相反地，Windows Media Player 7 或更新版本的物件模型會組織為物件的階層。</span><span class="sxs-lookup"><span data-stu-id="addac-120">By contrast, the Windows Media Player 7 or later object model is organized as a hierarchy of objects.</span></span> <span data-ttu-id="addac-121">**Player** 物件仍然是根物件，但函式現在可透過各種子物件來存取。</span><span class="sxs-lookup"><span data-stu-id="addac-121">The **Player** object is still the root object, but functions are now accessed through a variety of child objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="addac-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="addac-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="addac-123">**物件模型遷移指南**</span><span class="sxs-lookup"><span data-stu-id="addac-123">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> </dl>

 

 




