---
title: Player。錯誤事件
description: 發生錯誤情況時，就會發生錯誤事件。
ms.assetid: 1e418a56-ae81-4ff0-b721-3390be08970d
keywords:
- 錯誤事件 Windows Media Player
- 錯誤事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，錯誤事件
topic_type:
- apiref
api_name:
- Player.Error
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a99411773994ad012155eea5a203ed341d50b460
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001902"
---
# <a name="playererror-event"></a><span data-ttu-id="5302b-106">Player。錯誤事件</span><span class="sxs-lookup"><span data-stu-id="5302b-106">Player.Error event</span></span>

<span data-ttu-id="5302b-107">發生錯誤情況時，就會發生 **錯誤** 事件。</span><span class="sxs-lookup"><span data-stu-id="5302b-107">The **Error** event occurs when there is an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="5302b-108">語法</span><span class="sxs-lookup"><span data-stu-id="5302b-108">Syntax</span></span>


```JScript
Player.Error()
```



## <a name="parameters"></a><span data-ttu-id="5302b-109">參數</span><span class="sxs-lookup"><span data-stu-id="5302b-109">Parameters</span></span>

<span data-ttu-id="5302b-110">此事件沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="5302b-110">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5302b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="5302b-111">Return value</span></span>

<span data-ttu-id="5302b-112">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="5302b-112">This event does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="5302b-113">範例</span><span class="sxs-lookup"><span data-stu-id="5302b-113">Examples</span></span>

<span data-ttu-id="5302b-114">下列 JScript 範例會建立事件處理常式，以顯示錯誤佇列中第一個錯誤的描述文字。</span><span class="sxs-lookup"><span data-stu-id="5302b-114">The following JScript example creates an event handler to display the description text for the first error in the error queue.</span></span> <span data-ttu-id="5302b-115">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="5302b-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the description of the first error. 
var errDesc = Player.error.item(0).errorDescription;

// Display the error description.
alert(errDesc);

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="5302b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="5302b-116">Requirements</span></span>



| <span data-ttu-id="5302b-117">需求</span><span class="sxs-lookup"><span data-stu-id="5302b-117">Requirement</span></span> | <span data-ttu-id="5302b-118">值</span><span class="sxs-lookup"><span data-stu-id="5302b-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5302b-119">版本</span><span class="sxs-lookup"><span data-stu-id="5302b-119">Version</span></span><br/> | <span data-ttu-id="5302b-120">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="5302b-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5302b-121">DLL</span><span class="sxs-lookup"><span data-stu-id="5302b-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="5302b-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5302b-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5302b-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5302b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5302b-124">**ErrorItem. errorDescription**</span><span class="sxs-lookup"><span data-stu-id="5302b-124">**ErrorItem.errorDescription**</span></span>](erroritem-errordescription.md)
</dt> <dt>

[<span data-ttu-id="5302b-125">**錯誤。專案**</span><span class="sxs-lookup"><span data-stu-id="5302b-125">**Error.item**</span></span>](error-item.md)
</dt> <dt>

[<span data-ttu-id="5302b-126">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="5302b-126">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





