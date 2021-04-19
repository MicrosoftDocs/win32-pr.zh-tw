---
title: EnableCoNtextMenu
description: EnableCoNtextMenu 屬性會指定或抓取值，指出是否要啟用操作功能表，這會在按下滑鼠右鍵時顯示。
ms.assetid: 736c8714-5650-4912-9e97-914a20137b91
keywords:
- EnableCoNtextMenu Windows Media Player
topic_type:
- apiref
api_name:
- Player.enableContextMenu
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 324ab0f14b83621651869e715c1fd4a882ceb650
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106988667"
---
# <a name="playerenablecontextmenu"></a><span data-ttu-id="ebd6c-104">EnableCoNtextMenu</span><span class="sxs-lookup"><span data-stu-id="ebd6c-104">Player.enableContextMenu</span></span>

<span data-ttu-id="ebd6c-105">**EnableCoNtextMenu** 屬性會指定或抓取值，指出是否要啟用操作功能表，這會在按下滑鼠右鍵時顯示。</span><span class="sxs-lookup"><span data-stu-id="ebd6c-105">The **enableContextMenu** property specifies or retrieves a value indicating whether to enable the context menu, which appears when the right mouse button is clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebd6c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ebd6c-106">Syntax</span></span>

<span data-ttu-id="ebd6c-107">*玩家*。**enableCoNtextMenu**</span><span class="sxs-lookup"><span data-stu-id="ebd6c-107">*player*.**enableContextMenu**</span></span>

## <a name="possible-values"></a><span data-ttu-id="ebd6c-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="ebd6c-108">Possible Values</span></span>

<span data-ttu-id="ebd6c-109">這個屬性是讀取/寫入布林值。</span><span class="sxs-lookup"><span data-stu-id="ebd6c-109">This property is a read/write Boolean.</span></span>



| <span data-ttu-id="ebd6c-110">值</span><span class="sxs-lookup"><span data-stu-id="ebd6c-110">Value</span></span> | <span data-ttu-id="ebd6c-111">描述</span><span class="sxs-lookup"><span data-stu-id="ebd6c-111">Description</span></span>                       |
|-------|-----------------------------------|
| <span data-ttu-id="ebd6c-112">true</span><span class="sxs-lookup"><span data-stu-id="ebd6c-112">true</span></span>  | <span data-ttu-id="ebd6c-113">預設值。</span><span class="sxs-lookup"><span data-stu-id="ebd6c-113">Default.</span></span> <span data-ttu-id="ebd6c-114">啟用內容功能表。</span><span class="sxs-lookup"><span data-stu-id="ebd6c-114">Enable the context menu.</span></span> |
| <span data-ttu-id="ebd6c-115">false</span><span class="sxs-lookup"><span data-stu-id="ebd6c-115">false</span></span> | <span data-ttu-id="ebd6c-116">請勿啟用內容功能表。</span><span class="sxs-lookup"><span data-stu-id="ebd6c-116">Do not enable the context menu.</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="ebd6c-117">備註</span><span class="sxs-lookup"><span data-stu-id="ebd6c-117">Remarks</span></span>

<span data-ttu-id="ebd6c-118">在全螢幕播放期間，Windows Media Player 會在 **enableCoNtextMenu** 等於 False 且 **uiMode** 等於 "none" 時隱藏滑鼠游標。</span><span class="sxs-lookup"><span data-stu-id="ebd6c-118">During full-screen playback, Windows Media Player hides the mouse cursor when **enableContextMenu** equals false and **uiMode** equals "none".</span></span>

<span data-ttu-id="ebd6c-119">**Windows Media Player 10** 行動裝置版：不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="ebd6c-119">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebd6c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="ebd6c-120">Requirements</span></span>



| <span data-ttu-id="ebd6c-121">需求</span><span class="sxs-lookup"><span data-stu-id="ebd6c-121">Requirement</span></span> | <span data-ttu-id="ebd6c-122">值</span><span class="sxs-lookup"><span data-stu-id="ebd6c-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ebd6c-123">版本</span><span class="sxs-lookup"><span data-stu-id="ebd6c-123">Version</span></span><br/> | <span data-ttu-id="ebd6c-124">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="ebd6c-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="ebd6c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ebd6c-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="ebd6c-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebd6c-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebd6c-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ebd6c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebd6c-128">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="ebd6c-128">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





