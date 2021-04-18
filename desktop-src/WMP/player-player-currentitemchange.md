---
title: CurrentItemChange 事件
description: CurrentItem 變更時，就會發生 CurrentItemChange 事件。
ms.assetid: e6f68aeb-d7e7-460b-adc9-647f28c678a1
keywords:
- CurrentItemChange 事件 Windows Media Player
- CurrentItemChange 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，CurrentItemChange 事件
topic_type:
- apiref
api_name:
- Player.CurrentItemChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4c425184bf4b338177ec892ed5362c085dd8cb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996474"
---
# <a name="playercurrentitemchange-event"></a><span data-ttu-id="d4692-106">CurrentItemChange 事件</span><span class="sxs-lookup"><span data-stu-id="d4692-106">Player.CurrentItemChange event</span></span>

<span data-ttu-id="d4692-107">當 *控制項* 時，就會發生 **CurrentItemChange** 事件。**currentItem** 變更。</span><span class="sxs-lookup"><span data-stu-id="d4692-107">The **CurrentItemChange** event occurs when *Controls*.**currentItem** changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4692-108">語法</span><span class="sxs-lookup"><span data-stu-id="d4692-108">Syntax</span></span>


```JScript
Player.CurrentItemChange()
```



## <a name="parameters"></a><span data-ttu-id="d4692-109">參數</span><span class="sxs-lookup"><span data-stu-id="d4692-109">Parameters</span></span>

<span data-ttu-id="d4692-110">此事件沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d4692-110">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d4692-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d4692-111">Return value</span></span>

<span data-ttu-id="d4692-112">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d4692-112">This event does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="d4692-113">範例</span><span class="sxs-lookup"><span data-stu-id="d4692-113">Examples</span></span>

<span data-ttu-id="d4692-114">下列 JScript 範例示範 *播放* 程式的事件處理常式。**currentItemChange** 事件。</span><span class="sxs-lookup"><span data-stu-id="d4692-114">The following JScript example demonstrates an event handler for the *Player*.**currentItemChange** event.</span></span> <span data-ttu-id="d4692-115">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="d4692-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an HTML text box to display the media item name. -->
<INPUT TYPE="TEXT" NAME="MEDIA">

<!-- Create an event handler. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player EVENT = currentItemChange()>

   // Display the name of the new media item.
   MEDIA.value = Player.currentMedia.name;

</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="d4692-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4692-116">Requirements</span></span>



| <span data-ttu-id="d4692-117">需求</span><span class="sxs-lookup"><span data-stu-id="d4692-117">Requirement</span></span> | <span data-ttu-id="d4692-118">值</span><span class="sxs-lookup"><span data-stu-id="d4692-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d4692-119">版本</span><span class="sxs-lookup"><span data-stu-id="d4692-119">Version</span></span><br/> | <span data-ttu-id="d4692-120">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="d4692-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d4692-121">DLL</span><span class="sxs-lookup"><span data-stu-id="d4692-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="d4692-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4692-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4692-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4692-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4692-124">**CurrentItem**</span><span class="sxs-lookup"><span data-stu-id="d4692-124">**Controls.currentItem**</span></span>](controls-currentitem.md)
</dt> <dt>

[<span data-ttu-id="d4692-125">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="d4692-125">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





