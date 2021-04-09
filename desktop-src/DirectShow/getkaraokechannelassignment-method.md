---
description: GetKaraokeChannelAssignment 方法會抓取一個值，指出如何將卡拉卡拉板通道指派給喇叭。
ms.assetid: 08e35fa6-fa1b-4f9f-8f56-d953c4422226
title: GetKaraokeChannelAssignment 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dafe1217e08f3dc4f55aeec42424b1ebf9d86d22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846876"
---
# <a name="getkaraokechannelassignment-method"></a><span data-ttu-id="5a40c-103">GetKaraokeChannelAssignment 方法</span><span class="sxs-lookup"><span data-stu-id="5a40c-103">GetKaraokeChannelAssignment Method</span></span>

> [!Note]  
> <span data-ttu-id="5a40c-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="5a40c-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="5a40c-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="5a40c-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="5a40c-106">`GetKaraokeChannelAssignment`方法會抓取一個值，指出如何將卡拉卡拉板通道指派給喇叭。</span><span class="sxs-lookup"><span data-stu-id="5a40c-106">The `GetKaraokeChannelAssignment` method retrieves a value that indicates how the karaoke channels are assigned to the speakers.</span></span>

``` syntax
[ iAssignment = ] MSWebDVD.GetKaraokeChannelAssignment(iStream)
```

## <a name="parameters"></a><span data-ttu-id="5a40c-107">參數</span><span class="sxs-lookup"><span data-stu-id="5a40c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a40c-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="5a40c-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="5a40c-109">將音訊串流指定為整數。</span><span class="sxs-lookup"><span data-stu-id="5a40c-109">Specifies the audio stream as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a40c-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="5a40c-110">Return Value</span></span>

<span data-ttu-id="5a40c-111">傳回整數，表示指定之資料流程的喇叭指派。</span><span class="sxs-lookup"><span data-stu-id="5a40c-111">Returns an integer indicating the speaker assignment for the specified stream.</span></span>



| <span data-ttu-id="5a40c-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5a40c-112">Return code</span></span> | <span data-ttu-id="5a40c-113">描述</span><span class="sxs-lookup"><span data-stu-id="5a40c-113">Description</span></span>                                                             |
|-------------|-------------------------------------------------------------------------|
| <span data-ttu-id="5a40c-114">2</span><span class="sxs-lookup"><span data-stu-id="5a40c-114">2</span></span>           | <span data-ttu-id="5a40c-115">資料流程會指派給左邊和右邊的喇叭。</span><span class="sxs-lookup"><span data-stu-id="5a40c-115">The stream is assigned to the left and right speakers.</span></span>                  |
| <span data-ttu-id="5a40c-116">3</span><span class="sxs-lookup"><span data-stu-id="5a40c-116">3</span></span>           | <span data-ttu-id="5a40c-117">資料流程會指派給左、右和中間說話者。</span><span class="sxs-lookup"><span data-stu-id="5a40c-117">The stream is assigned to the left, right, and middle speakers.</span></span>         |
| <span data-ttu-id="5a40c-118">4</span><span class="sxs-lookup"><span data-stu-id="5a40c-118">4</span></span>           | <span data-ttu-id="5a40c-119">資料流程會指派給左、右和 audio1 喇叭。</span><span class="sxs-lookup"><span data-stu-id="5a40c-119">The stream is assigned to the left, right, and audio1 speakers.</span></span>         |
| <span data-ttu-id="5a40c-120">5</span><span class="sxs-lookup"><span data-stu-id="5a40c-120">5</span></span>           | <span data-ttu-id="5a40c-121">資料流程會指派給左、右、中間和 audio1 喇叭。</span><span class="sxs-lookup"><span data-stu-id="5a40c-121">The stream is assigned to the left, right, middle, and audio1 speakers.</span></span> |
| <span data-ttu-id="5a40c-122">6</span><span class="sxs-lookup"><span data-stu-id="5a40c-122">6</span></span>           | <span data-ttu-id="5a40c-123">資料流程會指派給左、右和 audio2 喇叭。</span><span class="sxs-lookup"><span data-stu-id="5a40c-123">The stream is assigned to the left, right, and audio2 speakers.</span></span>         |
| <span data-ttu-id="5a40c-124">7</span><span class="sxs-lookup"><span data-stu-id="5a40c-124">7</span></span>           | <span data-ttu-id="5a40c-125">資料流程會指派給左、右、中間和 audio2 喇叭。</span><span class="sxs-lookup"><span data-stu-id="5a40c-125">The stream is assigned to the left, right, middle, and audio2 speakers.</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="5a40c-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5a40c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a40c-127">**KaraokeAudioPresentationMode**</span><span class="sxs-lookup"><span data-stu-id="5a40c-127">**KaraokeAudioPresentationMode**</span></span>](karaokeaudiopresentationmode-property.md)
</dt> </dl>

 

 



