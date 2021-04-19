---
title: OpenPlaylistSwitch 事件
description: 當 DVD 上的標題開始播放時，就會發生 OpenPlaylistSwitch 事件。 |OpenPlaylistSwitch 事件
ms.assetid: 97d69716-602f-4522-b743-83f2dbc852a2
keywords:
- OpenPlaylistSwitch 事件 Windows Media Player
- OpenPlaylistSwitch 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，OpenPlaylistSwitch 事件
topic_type:
- apiref
api_name:
- Player.OpenPlaylistSwitch
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d35d4568356365cc9276c13ea33f866e937da1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992156"
---
# <a name="playeropenplaylistswitch-event"></a><span data-ttu-id="bf321-107">OpenPlaylistSwitch 事件</span><span class="sxs-lookup"><span data-stu-id="bf321-107">Player.OpenPlaylistSwitch event</span></span>

<span data-ttu-id="bf321-108">當 DVD 上的標題開始播放時，就會發生 **OpenPlaylistSwitch** 事件。</span><span class="sxs-lookup"><span data-stu-id="bf321-108">The **OpenPlaylistSwitch** event occurs when a title on a DVD begins playing.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf321-109">語法</span><span class="sxs-lookup"><span data-stu-id="bf321-109">Syntax</span></span>


```JScript
Player.OpenPlaylistSwitch(
  pItem
)
```



## <a name="parameters"></a><span data-ttu-id="bf321-110">參數</span><span class="sxs-lookup"><span data-stu-id="bf321-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf321-111">*pItem*</span><span class="sxs-lookup"><span data-stu-id="bf321-111">*pItem*</span></span> 
</dt> <dd>

<span data-ttu-id="bf321-112">代表標題的 **播放清單** 物件。</span><span class="sxs-lookup"><span data-stu-id="bf321-112">**Playlist** object representing the title.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf321-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="bf321-113">Return value</span></span>

<span data-ttu-id="bf321-114">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="bf321-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf321-115">備註</span><span class="sxs-lookup"><span data-stu-id="bf321-115">Remarks</span></span>

<span data-ttu-id="bf321-116">事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。</span><span class="sxs-lookup"><span data-stu-id="bf321-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="bf321-117">此參數名稱的類型必須完全如所示，包括大小寫。</span><span class="sxs-lookup"><span data-stu-id="bf321-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf321-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf321-118">Requirements</span></span>



| <span data-ttu-id="bf321-119">需求</span><span class="sxs-lookup"><span data-stu-id="bf321-119">Requirement</span></span> | <span data-ttu-id="bf321-120">值</span><span class="sxs-lookup"><span data-stu-id="bf321-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bf321-121">版本</span><span class="sxs-lookup"><span data-stu-id="bf321-121">Version</span></span><br/> | <span data-ttu-id="bf321-122">適用于 Windows XP 或更新版本的 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="bf321-122">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="bf321-123">DLL</span><span class="sxs-lookup"><span data-stu-id="bf321-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="bf321-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf321-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf321-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bf321-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf321-126">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="bf321-126">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





