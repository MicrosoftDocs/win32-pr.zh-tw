---
title: 播放。狀態
description: Status 屬性會抓取值，指出 Windows Media Player 的狀態。
ms.assetid: 781c44d0-15cf-4be2-9e83-76706ce1cb85
keywords:
- Player. 狀態 Windows Media Player
topic_type:
- apiref
api_name:
- Player.status
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d54c71e6ab8ece61fb97960bd2956393b1ae584
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986182"
---
# <a name="playerstatus"></a><span data-ttu-id="0ad01-104">播放。狀態</span><span class="sxs-lookup"><span data-stu-id="0ad01-104">Player.status</span></span>

<span data-ttu-id="0ad01-105">**Status** 屬性會抓取值，指出 Windows Media Player 的狀態。</span><span class="sxs-lookup"><span data-stu-id="0ad01-105">The **status** property retrieves a value indicating the status of Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ad01-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ad01-106">Syntax</span></span>

<span data-ttu-id="0ad01-107">*玩家* 。**狀態**</span><span class="sxs-lookup"><span data-stu-id="0ad01-107">*player* .**status**</span></span>

## <a name="possible-values"></a><span data-ttu-id="0ad01-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="0ad01-108">Possible Values</span></span>

<span data-ttu-id="0ad01-109">這個屬性是唯讀字串。</span><span class="sxs-lookup"><span data-stu-id="0ad01-109">This property is a read-only String.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ad01-110">備註</span><span class="sxs-lookup"><span data-stu-id="0ad01-110">Remarks</span></span>

<span data-ttu-id="0ad01-111">這個屬性中包含的值隨時可能會變更，而且僅供顯示之用。</span><span class="sxs-lookup"><span data-stu-id="0ad01-111">The values contained in this property are subject to change at any time, and should be used for display purposes only.</span></span>

<span data-ttu-id="0ad01-112">每當這個屬性變更值時，就會引發 **StatusChange** 事件。</span><span class="sxs-lookup"><span data-stu-id="0ad01-112">The **StatusChange** event is fired whenever this property changes value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ad01-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="0ad01-113">Requirements</span></span>



| <span data-ttu-id="0ad01-114">需求</span><span class="sxs-lookup"><span data-stu-id="0ad01-114">Requirement</span></span> | <span data-ttu-id="0ad01-115">值</span><span class="sxs-lookup"><span data-stu-id="0ad01-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0ad01-116">版本</span><span class="sxs-lookup"><span data-stu-id="0ad01-116">Version</span></span><br/> | <span data-ttu-id="0ad01-117">Windows Media Player 7.0 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="0ad01-117">Windows Media Player 7.0 or later.</span></span><br/>                                      |
| <span data-ttu-id="0ad01-118">DLL</span><span class="sxs-lookup"><span data-stu-id="0ad01-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="0ad01-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ad01-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ad01-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0ad01-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ad01-121">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="0ad01-121">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="0ad01-122">**StatusChange 事件**</span><span class="sxs-lookup"><span data-stu-id="0ad01-122">**Player.StatusChange Event**</span></span>](player-player-statuschange.md)
</dt> </dl>

 

 





