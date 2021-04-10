---
title: 關於 Player 物件
description: 關於 Player 物件
ms.assetid: db995e75-d4e3-4f50-a34a-cc1b2f2c5db5
keywords:
- Windows Media Player，Player 物件
- Windows Media Player 物件模型、Player 物件
- 物件模型、Player 物件
- Windows Media Player ActiveX 控制項、Player 物件
- ActiveX 控制項、Player 物件
- Windows Media Player Mobile ActiveX 控制項、Player 物件
- Windows Media Player Mobile，Player 物件
- Player 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c030d42cd6fd65811c41af7401ec3e60c8c7801
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092309"
---
# <a name="about-the-player-object"></a><span data-ttu-id="858d5-111">關於 Player 物件</span><span class="sxs-lookup"><span data-stu-id="858d5-111">About the Player Object</span></span>

<span data-ttu-id="858d5-112">**Player** 物件是 Windows Media Player 控制項的核心物件。</span><span class="sxs-lookup"><span data-stu-id="858d5-112">The **Player** object is the core object for the Windows Media Player control.</span></span> <span data-ttu-id="858d5-113">所有其他相關物件都會透過傳回物件的特定屬性連接到這個物件。</span><span class="sxs-lookup"><span data-stu-id="858d5-113">All other related objects are connected to this object through specific properties that return the object.</span></span> <span data-ttu-id="858d5-114">例如，您可以透過 [**設定**] 屬性來存取 **設定** 物件。</span><span class="sxs-lookup"><span data-stu-id="858d5-114">For example, the **Settings** object is accessed through the **settings** property.</span></span> <span data-ttu-id="858d5-115">**Player** 物件提供與 Windows Media Player 核心功能相關的方法、屬性和事件。</span><span class="sxs-lookup"><span data-stu-id="858d5-115">The **Player** object provides methods, properties, and events that relate to the core functionality of Windows Media Player.</span></span>

<span data-ttu-id="858d5-116">因為此參考也可用於外觀程式設計，所以 **播放** 程式物件的識別碼將會是 "player"，以取得語法範例。</span><span class="sxs-lookup"><span data-stu-id="858d5-116">Because this reference is also to be used for skins programming, the ID of the **Player** object will be "player" for syntax examples.</span></span>

<span data-ttu-id="858d5-117">使用面板定義檔內的 **media player** 全域屬性，可讓您存取 **player** 物件以在腳本中使用。</span><span class="sxs-lookup"><span data-stu-id="858d5-117">Using the **player** global attribute within a skin definition file gives access to the **Player** object for use in scripting.</span></span> <span data-ttu-id="858d5-118">透過 **Player** 物件，Windows Media Player 控制項中的其他所有物件也都可供腳本使用。</span><span class="sxs-lookup"><span data-stu-id="858d5-118">Through the **Player** object, all other objects in the Windows Media Player control become accessible to scripts as well.</span></span> <span data-ttu-id="858d5-119">**Player** 物件和 **URL** 屬性的事件也可以在設計階段使用 [播放](player-element.md)程式面板元素來指定。</span><span class="sxs-lookup"><span data-stu-id="858d5-119">The events of the **Player** object and the **URL** property can also be specified at design time using the [PLAYER](player-element.md) skin element.</span></span> <span data-ttu-id="858d5-120">如需詳細資訊，請參閱 [Windows Media Player 的外觀](windows-media-player-skins.md)。</span><span class="sxs-lookup"><span data-stu-id="858d5-120">For more information, see [Windows Media Player Skins](windows-media-player-skins.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="858d5-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="858d5-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="858d5-122">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="858d5-122">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="858d5-123">**指令碼語言的播放程式物件模型**</span><span class="sxs-lookup"><span data-stu-id="858d5-123">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




