---
title: StretchToFit
description: StretchToFit 屬性會指定或抓取值，指出當影片視窗大於影片影像的尺寸時，Windows Media Player 控制項所顯示的影片是否會自動調整大小以符合影片視窗。
ms.assetid: 9ea02959-602e-4bac-a8aa-dce502d1bb54
keywords:
- StretchToFit Windows Media Player
topic_type:
- apiref
api_name:
- Player.stretchToFit
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb7b68042cf2a5bd0e7f718d1e19641edecdf548
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977407"
---
# <a name="playerstretchtofit"></a><span data-ttu-id="ca129-104">StretchToFit</span><span class="sxs-lookup"><span data-stu-id="ca129-104">Player.stretchToFit</span></span>

<span data-ttu-id="ca129-105">**StretchToFit** 屬性會指定或抓取值，指出當影片視窗大於影片影像的尺寸時，Windows Media Player 控制項所顯示的影片是否會自動調整大小以符合影片視窗。</span><span class="sxs-lookup"><span data-stu-id="ca129-105">The **stretchToFit** property specifies or retrieves a value indicating whether video displayed by the Windows Media Player control automatically sizes to fit the video window, when the video window is larger than the dimensions of the video image.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca129-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca129-106">Syntax</span></span>

<span data-ttu-id="ca129-107">*玩家*。**stretchToFit**</span><span class="sxs-lookup"><span data-stu-id="ca129-107">*player*.**stretchToFit**</span></span>

## <a name="possible-values"></a><span data-ttu-id="ca129-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="ca129-108">Possible Values</span></span>

<span data-ttu-id="ca129-109">這個屬性是讀取/寫入 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="ca129-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="ca129-110">值</span><span class="sxs-lookup"><span data-stu-id="ca129-110">Value</span></span> | <span data-ttu-id="ca129-111">描述</span><span class="sxs-lookup"><span data-stu-id="ca129-111">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="ca129-112">true</span><span class="sxs-lookup"><span data-stu-id="ca129-112">true</span></span>  | <span data-ttu-id="ca129-113">影片將會延展以符合視窗。</span><span class="sxs-lookup"><span data-stu-id="ca129-113">The video will stretch to fit the window.</span></span>              |
| <span data-ttu-id="ca129-114">false</span><span class="sxs-lookup"><span data-stu-id="ca129-114">false</span></span> | <span data-ttu-id="ca129-115">預設值。</span><span class="sxs-lookup"><span data-stu-id="ca129-115">Default.</span></span> <span data-ttu-id="ca129-116">影片將不會延展以符合視窗。</span><span class="sxs-lookup"><span data-stu-id="ca129-116">The video will not stretch to fit the window.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ca129-117">備註</span><span class="sxs-lookup"><span data-stu-id="ca129-117">Remarks</span></span>

<span data-ttu-id="ca129-118">當 **stretchToFit** 設定為 true 時，Windows Media Player 控制項會維持影片的原始外觀比例。</span><span class="sxs-lookup"><span data-stu-id="ca129-118">When **stretchToFit** is set to true, the Windows Media Player control maintains the original aspect ratio of the video.</span></span> <span data-ttu-id="ca129-119">如果影片的長寬比與影片視窗的外觀比例不相符，則可能會在影片影像的頂端和底部或左邊和右邊出現黑色遮罩區域。</span><span class="sxs-lookup"><span data-stu-id="ca129-119">If the aspect ratio of the video does not match the aspect ratio of the video window, black mask areas may appear on either the top and the bottom, or left and right, of the video image.</span></span>

<span data-ttu-id="ca129-120">只有當內嵌在網頁中時，此屬性才會套用至 Windows Media Player 控制項。</span><span class="sxs-lookup"><span data-stu-id="ca129-120">This property applies to the Windows Media Player control only when embedded in a webpage.</span></span>

<span data-ttu-id="ca129-121">**Windows Media Player 10** 行動裝置版：不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="ca129-121">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca129-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="ca129-122">Requirements</span></span>



| <span data-ttu-id="ca129-123">需求</span><span class="sxs-lookup"><span data-stu-id="ca129-123">Requirement</span></span> | <span data-ttu-id="ca129-124">值</span><span class="sxs-lookup"><span data-stu-id="ca129-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ca129-125">版本</span><span class="sxs-lookup"><span data-stu-id="ca129-125">Version</span></span><br/> | <span data-ttu-id="ca129-126">Windows Media Player 7.1 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="ca129-126">Windows Media Player version 7.1 or later.</span></span><br/>                              |
| <span data-ttu-id="ca129-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ca129-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="ca129-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca129-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca129-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ca129-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca129-130">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="ca129-130">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





