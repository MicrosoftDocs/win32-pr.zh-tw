---
title: 現用屬性
description: 現用屬性
ms.assetid: 76ada073-782a-4355-b4e8-42dd84d0139b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061fe5fea7d94586c9f9d5c12b3a3b11ffbd7c3f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183499"
---
# <a name="active-property"></a><span data-ttu-id="28f7e-103">現用屬性</span><span class="sxs-lookup"><span data-stu-id="28f7e-103">Active Property</span></span>

<span data-ttu-id="28f7e-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="28f7e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="28f7e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="28f7e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="28f7e-106">傳回您的應用程式是否為字元的作用中用戶端，以及字元是否最上層。</span><span class="sxs-lookup"><span data-stu-id="28f7e-106">Returns whether your application is the active client of the character and whether the character is topmost.</span></span>

</dd> <dt>

<span data-ttu-id="28f7e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="28f7e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="28f7e-108">*代理程式。\*\*\*字元 \* \*\*\*\* \* \* (」CharacterID \* \* \* ) 。* 作用中 \*  \[  =  *狀態*\]</span><span class="sxs-lookup"><span data-stu-id="28f7e-108">*agent.\*\*\*Characters\*\*\*\*("*\*\* CharacterID\***").Active** \[ = *State*\]</span></span>



| <span data-ttu-id="28f7e-109">部分</span><span class="sxs-lookup"><span data-stu-id="28f7e-109">Part</span></span>    | <span data-ttu-id="28f7e-110">描述</span><span class="sxs-lookup"><span data-stu-id="28f7e-110">Description</span></span>                                                                                                                                                                                                |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28f7e-111">*state*</span><span class="sxs-lookup"><span data-stu-id="28f7e-111">*state*</span></span> | <span data-ttu-id="28f7e-112">整數運算式，指定用戶端應用程式的狀態。</span><span class="sxs-lookup"><span data-stu-id="28f7e-112">An integer expression specifying the state of your client application.</span></span> <span data-ttu-id="28f7e-113">0不是作用中的用戶端。</span><span class="sxs-lookup"><span data-stu-id="28f7e-113">0 Not the active client.</span></span><br/> <span data-ttu-id="28f7e-114">1個作用中用戶端。</span><span class="sxs-lookup"><span data-stu-id="28f7e-114">1 The active client.</span></span> <br/> <span data-ttu-id="28f7e-115">2輸入-主動用戶端。</span><span class="sxs-lookup"><span data-stu-id="28f7e-115">2 The input-active client.</span></span> <span data-ttu-id="28f7e-116"> (最上方的字元。 ) </span><span class="sxs-lookup"><span data-stu-id="28f7e-116">(The topmost character.)</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="28f7e-117">備註</span><span class="sxs-lookup"><span data-stu-id="28f7e-117">Remarks</span></span>

<span data-ttu-id="28f7e-118">當多個用戶端應用程式共用相同的字元時，字元的作用中用戶端會收到滑鼠輸入 (例如，Microsoft Agent control [**Click**](click-event.md) 或 [DragStart](dragstart-event.md) events) 。</span><span class="sxs-lookup"><span data-stu-id="28f7e-118">When multiple client applications share the same character, the active client of the character receives mouse input (for example, Microsoft Agent control [**Click**](click-event.md) or [DragStart](dragstart-event.md) events).</span></span> <span data-ttu-id="28f7e-119">同樣地，當顯示多個字元時，最上層字元的作用中用戶端 (也稱為輸入-主動用戶端) 接收命令事件。</span><span class="sxs-lookup"><span data-stu-id="28f7e-119">Similarly, when multiple characters are displayed, the active client of the topmost character (also known as the input-active client) receives Command events.</span></span>

<span data-ttu-id="28f7e-120">您可以使用 [**啟動**](activate-method.md)方法來設定您的應用程式是字元的作用中用戶端，還是讓您的應用程式成為輸入使用中的用戶端 (也會讓字元) 最上層。</span><span class="sxs-lookup"><span data-stu-id="28f7e-120">You can use the [**Activate**](activate-method.md)method to set whether your application is the active client of the character or to make your application the input active client (which also makes the character topmost).</span></span>

## <a name="see-also"></a><span data-ttu-id="28f7e-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28f7e-121">See Also</span></span>

[<span data-ttu-id="28f7e-122">啟動 \* \* 方法 \* \*</span><span class="sxs-lookup"><span data-stu-id="28f7e-122">\*\*\*\*Activate\*\* method\*\*</span></span>](activate-method.md)


 

 





