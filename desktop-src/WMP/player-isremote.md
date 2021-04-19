---
title: IsRemote
description: IsRemote 屬性會抓取值，指出 Windows Media Player 控制項是否在遠端模式中執行。
ms.assetid: bfeab968-affb-4d5d-b88b-5caf50d34cee
keywords:
- IsRemote Windows Media Player
topic_type:
- apiref
api_name:
- Player.isRemote
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7c8d97ba212e032db16b43299d2a3a8a836f9b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990038"
---
# <a name="playerisremote"></a><span data-ttu-id="b0002-104">IsRemote</span><span class="sxs-lookup"><span data-stu-id="b0002-104">Player.isRemote</span></span>

<span data-ttu-id="b0002-105">**IsRemote** 屬性會抓取值，指出 Windows Media Player 控制項是否在遠端模式中執行。</span><span class="sxs-lookup"><span data-stu-id="b0002-105">The **isRemote** property retrieves a value indicating whether the Windows Media Player control is running in remote mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0002-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0002-106">Syntax</span></span>

<span data-ttu-id="b0002-107">*玩家* 。**isRemote**</span><span class="sxs-lookup"><span data-stu-id="b0002-107">*player* .**isRemote**</span></span>

## <a name="possible-values"></a><span data-ttu-id="b0002-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="b0002-108">Possible Values</span></span>

<span data-ttu-id="b0002-109">這個屬性是唯讀的 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="b0002-109">This property is a read-only **Boolean**.</span></span>



| <span data-ttu-id="b0002-110">值</span><span class="sxs-lookup"><span data-stu-id="b0002-110">Value</span></span> | <span data-ttu-id="b0002-111">描述</span><span class="sxs-lookup"><span data-stu-id="b0002-111">Description</span></span>                                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="b0002-112">true</span><span class="sxs-lookup"><span data-stu-id="b0002-112">true</span></span>  | <span data-ttu-id="b0002-113">播放機控制項以遠端模式執行。</span><span class="sxs-lookup"><span data-stu-id="b0002-113">The Player control is running in remote mode.</span></span> |
| <span data-ttu-id="b0002-114">false</span><span class="sxs-lookup"><span data-stu-id="b0002-114">false</span></span> | <span data-ttu-id="b0002-115">播放機控制項是在原生模式中執行。</span><span class="sxs-lookup"><span data-stu-id="b0002-115">The Player control is running in local mode.</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="b0002-116">備註</span><span class="sxs-lookup"><span data-stu-id="b0002-116">Remarks</span></span>

<span data-ttu-id="b0002-117">**Windows Media Player 10** 行動裝置版：此屬性一律會傳回 false。</span><span class="sxs-lookup"><span data-stu-id="b0002-117">**Windows Media Player 10 Mobile:** This property always returns false.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0002-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0002-118">Requirements</span></span>



| <span data-ttu-id="b0002-119">需求</span><span class="sxs-lookup"><span data-stu-id="b0002-119">Requirement</span></span> | <span data-ttu-id="b0002-120">值</span><span class="sxs-lookup"><span data-stu-id="b0002-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b0002-121">版本</span><span class="sxs-lookup"><span data-stu-id="b0002-121">Version</span></span><br/> | <span data-ttu-id="b0002-122">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="b0002-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="b0002-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b0002-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="b0002-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0002-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0002-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b0002-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0002-126">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="b0002-126">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="b0002-127">**遠端處理 Windows Media Player 控制項**</span><span class="sxs-lookup"><span data-stu-id="b0002-127">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





