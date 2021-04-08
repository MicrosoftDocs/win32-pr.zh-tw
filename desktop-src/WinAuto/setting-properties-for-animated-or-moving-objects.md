---
title: 設定動畫或移動物件的屬性
description: 針對動畫控制項（例如複製檔案時顯示的動畫控制項），請使用「角色 \_ 系統 \_ 動畫」物件角色。
ms.assetid: 8c5ebbc3-4066-452b-8f37-2fb595adea53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1551899305968471bf1425b5cc043be8329c2bd4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021909"
---
# <a name="setting-properties-for-animated-or-moving-objects"></a><span data-ttu-id="4afa3-103">設定動畫或移動物件的屬性</span><span class="sxs-lookup"><span data-stu-id="4afa3-103">Setting Properties for Animated or Moving Objects</span></span>

<span data-ttu-id="4afa3-104">針對動畫控制項（例如複製檔案時顯示的動畫控制項），請使用「 [**角色 \_ 系統 \_ 動畫**](object-roles.md) 」物件角色。</span><span class="sxs-lookup"><span data-stu-id="4afa3-104">For animation controls, such as the animation control displayed when copying files, use the [**ROLE\_SYSTEM\_ANIMATION**](object-roles.md) object role.</span></span> <span data-ttu-id="4afa3-105">針對偶而動畫的圖形，請使用 [**[狀態] 設為**](state-property.md)[[**狀態 \_ 系統 \_ 動畫**](object-state-constants.md)] 的 [**角色 \_ 系統 \_ 圖形**](object-roles.md)物件角色。</span><span class="sxs-lookup"><span data-stu-id="4afa3-105">For graphics that are occasionally animated, use the [**ROLE\_SYSTEM\_GRAPHIC**](object-roles.md) object role with the [**State**](state-property.md) set to [**STATE\_SYSTEM\_ANIMATED**](object-state-constants.md).</span></span>

<span data-ttu-id="4afa3-106">使用「 [**狀態 \_ 系統 \_ 動畫**](object-state-constants.md) 」旗標來標示其外觀會快速變更的物件。</span><span class="sxs-lookup"><span data-stu-id="4afa3-106">Use the [**STATE\_SYSTEM\_ANIMATED**](object-state-constants.md) flag to mark an object whose appearance changes rapidly.</span></span> <span data-ttu-id="4afa3-107">用戶端會使用此旗標，以避免重複通知使用者真正的一系列視覺變更。</span><span class="sxs-lookup"><span data-stu-id="4afa3-107">Clients use this flag to avoid notifying users repeatedly for what is really a single series of visual changes.</span></span>

<span data-ttu-id="4afa3-108">其中一個範例是字幕文字，當它在螢幕上滾動時，會逐漸產生。</span><span class="sxs-lookup"><span data-stu-id="4afa3-108">An example of this is marquee text, which is disclosed progressively as it scrolls across the screen.</span></span> <span data-ttu-id="4afa3-109">系統會為這類物件提供 [**狀態 \_ 系統 \_ 動畫**](object-state-constants.md)的屬性。</span><span class="sxs-lookup"><span data-stu-id="4afa3-109">Such objects are given the attribute of [**STATE\_SYSTEM\_ANIMATED**](object-state-constants.md).</span></span> <span data-ttu-id="4afa3-110">在大部分情況下，物件的 [**值**](value-property.md) 字串會反映整個文字，甚至是目前看不到的部分。</span><span class="sxs-lookup"><span data-stu-id="4afa3-110">In most cases the object's [**Value**](value-property.md) string reflects the entire text, even the portion not currently visible.</span></span> <span data-ttu-id="4afa3-111">不建議經常變更 **值** 字串以對應到目前可見的文字，因為這會導致太多 [**事件 \_ 物件 \_ VALUECHANGE**](event-constants.md) 事件未傳達有用的資訊。</span><span class="sxs-lookup"><span data-stu-id="4afa3-111">Changing the **Value** string frequently to correspond to the text currently visible is not recommended because it results in far too many [**EVENT\_OBJECT\_VALUECHANGE**](event-constants.md) events that do not convey useful information.</span></span>

<span data-ttu-id="4afa3-112">例如，在包含矩形區域的視窗中，顯示 "Yes！" 這個字。</span><span class="sxs-lookup"><span data-stu-id="4afa3-112">For example, in a window that contains a rectangular region that shows the word "Yes!"</span></span> <span data-ttu-id="4afa3-113">在圖8模式中移動， [**角色**](role-property.md) 是 [**角色 \_ 系統 \_ 圖形**](object-roles.md)， [**值**](value-property.md) 屬性是顯示的字串， [**Location**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) 屬性是文字周圍的周框，並且會設定 [**狀態 \_ 系統 \_ 動畫**](object-state-constants.md) 屬性旗標。</span><span class="sxs-lookup"><span data-stu-id="4afa3-113">moving in a figure-eight pattern, the [**Role**](role-property.md) is [**ROLE\_SYSTEM\_GRAPHIC**](object-roles.md), the [**Value**](value-property.md) property is the string displayed, the [**Location**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) property is the bounding rectangle around the text, and the [**STATE\_SYSTEM\_ANIMATED**](object-state-constants.md) attribute flag is set.</span></span> <span data-ttu-id="4afa3-114">[**描述**](description-property.md)為「沒錯！」這個字</span><span class="sxs-lookup"><span data-stu-id="4afa3-114">The [**Description**](description-property.md) is "The word 'Yes!'</span></span> <span data-ttu-id="4afa3-115">在畫面上移動8個模式。」</span><span class="sxs-lookup"><span data-stu-id="4afa3-115">is moving around the screen in a figure-eight pattern."</span></span> <span data-ttu-id="4afa3-116">當物件啟動或停止動畫時，伺服器只會產生 [**事件 \_ 物件 \_ STATECHANGE**](event-constants.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="4afa3-116">The server generates only [**EVENT\_OBJECT\_STATECHANGE**](event-constants.md) events when the object starts or ceases animation.</span></span>

 

 




