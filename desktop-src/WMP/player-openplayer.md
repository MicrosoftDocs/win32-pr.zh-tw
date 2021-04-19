---
title: OpenPlayer 方法
description: OpenPlayer 方法會使用指定的 URL 開啟 Windows Media Player。 |OpenPlayer 方法
ms.assetid: 9ddd63c9-f4a0-490a-8543-51ad0fa74a26
keywords:
- openPlayer 方法 Windows Media Player
- openPlayer 方法 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，openPlayer 方法
topic_type:
- apiref
api_name:
- Player.openPlayer
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3378df48f961f1aa5e3fccec72e79b7f1c26ff08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989566"
---
# <a name="playeropenplayer-method"></a><span data-ttu-id="f3498-107">OpenPlayer 方法</span><span class="sxs-lookup"><span data-stu-id="f3498-107">Player.openPlayer method</span></span>

<span data-ttu-id="f3498-108">**OpenPlayer** 方法會使用指定的 URL 開啟 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="f3498-108">The **openPlayer** method opens Windows Media Player using the specified URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3498-109">語法</span><span class="sxs-lookup"><span data-stu-id="f3498-109">Syntax</span></span>


```JScript
Player.openPlayer(
  URL
)
```



## <a name="parameters"></a><span data-ttu-id="f3498-110">參數</span><span class="sxs-lookup"><span data-stu-id="f3498-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3498-111">*URL* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3498-111">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3498-112">代表要播放之媒體專案之 URL 的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="f3498-112">**String** representing the URL of the media item to play.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3498-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3498-113">Return value</span></span>

<span data-ttu-id="f3498-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f3498-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3498-115">備註</span><span class="sxs-lookup"><span data-stu-id="f3498-115">Remarks</span></span>

<span data-ttu-id="f3498-116">這個方法會啟動 Windows Media Player，並將指定的 URL 設定為目前的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="f3498-116">This method launches Windows Media Player with the specified URL set as the current media item.</span></span> <span data-ttu-id="f3498-117">如果播放程式之前是在面板模式中關閉，則會使用使用者最後選擇的面板來開啟。</span><span class="sxs-lookup"><span data-stu-id="f3498-117">If the Player was previously closed in skin mode it will open using the skin last chosen by the user.</span></span> <span data-ttu-id="f3498-118">否則，播放會以完整模式開啟。</span><span class="sxs-lookup"><span data-stu-id="f3498-118">Otherwise, the Player opens in full mode.</span></span>

<span data-ttu-id="f3498-119">如果從內嵌于遠端模式的 Windows Media PlayerActiveX 控制項呼叫這個方法，其行為就會與 *PlayerApplication* 相同。**switchToPlayerApplication** 方法。</span><span class="sxs-lookup"><span data-stu-id="f3498-119">If this method is called from a Windows Media PlayerActiveX control embedded in remote mode, its behavior is identical to the *PlayerApplication*.**switchToPlayerApplication** method.</span></span>

<span data-ttu-id="f3498-120">**Windows Media Player 10** 行動裝置版：不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="f3498-120">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3498-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3498-121">Requirements</span></span>



| <span data-ttu-id="f3498-122">需求</span><span class="sxs-lookup"><span data-stu-id="f3498-122">Requirement</span></span> | <span data-ttu-id="f3498-123">值</span><span class="sxs-lookup"><span data-stu-id="f3498-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f3498-124">版本</span><span class="sxs-lookup"><span data-stu-id="f3498-124">Version</span></span><br/> | <span data-ttu-id="f3498-125">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="f3498-125">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="f3498-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f3498-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="f3498-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3498-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3498-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3498-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3498-129">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="f3498-129">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="f3498-130">**PlayerApplication.switchToPlayerApplication**</span><span class="sxs-lookup"><span data-stu-id="f3498-130">**PlayerApplication.switchToPlayerApplication**</span></span>](playerapplication-switchtoplayerapplication.md)
</dt> </dl>

 

 





