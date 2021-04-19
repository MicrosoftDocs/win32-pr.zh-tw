---
title: MediaChange 事件
description: 當媒體專案變更時，就會發生 MediaChange 事件。 |MediaChange 事件
ms.assetid: c4bdd2ae-c51f-4577-b762-bc84aaf52f76
keywords:
- MediaChange 事件 Windows Media Player
- MediaChange 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，MediaChange 事件
topic_type:
- apiref
api_name:
- Player.MediaChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99a63e087356b5d39ae8d751236b8128330c4f3c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995446"
---
# <a name="playermediachange-event"></a><span data-ttu-id="5d419-107">MediaChange 事件</span><span class="sxs-lookup"><span data-stu-id="5d419-107">Player.MediaChange event</span></span>

<span data-ttu-id="5d419-108">當媒體專案變更時，就會發生 **MediaChange** 事件。</span><span class="sxs-lookup"><span data-stu-id="5d419-108">The **MediaChange** event occurs when a media item changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d419-109">語法</span><span class="sxs-lookup"><span data-stu-id="5d419-109">Syntax</span></span>


```JScript
Player.MediaChange(
  Item
)
```



## <a name="parameters"></a><span data-ttu-id="5d419-110">參數</span><span class="sxs-lookup"><span data-stu-id="5d419-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d419-111">*Item*</span><span class="sxs-lookup"><span data-stu-id="5d419-111">*Item*</span></span> 
</dt> <dd>

<span data-ttu-id="5d419-112">代表已變更之專案的 **媒體** 物件。</span><span class="sxs-lookup"><span data-stu-id="5d419-112">**Media** object representing the item that changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d419-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5d419-113">Return value</span></span>

<span data-ttu-id="5d419-114">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="5d419-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d419-115">備註</span><span class="sxs-lookup"><span data-stu-id="5d419-115">Remarks</span></span>

<span data-ttu-id="5d419-116">事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。</span><span class="sxs-lookup"><span data-stu-id="5d419-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="5d419-117">此參數名稱的類型必須完全如所示，包括大小寫。</span><span class="sxs-lookup"><span data-stu-id="5d419-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="5d419-118">**Windows Media Player 10** 行動裝置版：不支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="5d419-118">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="5d419-119">範例</span><span class="sxs-lookup"><span data-stu-id="5d419-119">Examples</span></span>

<span data-ttu-id="5d419-120">下列 JScript 範例會使用名為 MediaName 的 HTML DIV 元素，來顯示目前媒體專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d419-120">The following JScript example uses an HTML DIV element, named MediaName, to display the name of the current media item.</span></span> <span data-ttu-id="5d419-121">程式碼會更新 DIV 中每次出現 **mediaChange** 事件的文字。</span><span class="sxs-lookup"><span data-stu-id="5d419-121">The code updates the text in the DIV with each occurrence of the **mediaChange** event.</span></span> <span data-ttu-id="5d419-122">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="5d419-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for media change. -->
<SCRIPT FOR = "Player" EVENT = "mediaChange(Item)">
   // Test whether a valid currentMedia object exists.
   if (Player.currentMedia){
      // Display the name of the current media item.
      MediaName.innerHTML = Player.currentMedia.name;
   }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="5d419-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d419-123">Requirements</span></span>



| <span data-ttu-id="5d419-124">需求</span><span class="sxs-lookup"><span data-stu-id="5d419-124">Requirement</span></span> | <span data-ttu-id="5d419-125">值</span><span class="sxs-lookup"><span data-stu-id="5d419-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5d419-126">版本</span><span class="sxs-lookup"><span data-stu-id="5d419-126">Version</span></span><br/> | <span data-ttu-id="5d419-127">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="5d419-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5d419-128">DLL</span><span class="sxs-lookup"><span data-stu-id="5d419-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="5d419-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d419-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d419-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d419-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d419-131">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="5d419-131">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





