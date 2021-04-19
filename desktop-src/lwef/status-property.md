---
title: Status 屬性
description: Status 屬性
ms.assetid: vs|msagent|~\pacontrol_8xd6.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402e88185e1024aa5958d06936a6529ae4012622
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968434"
---
# <a name="status-property"></a><span data-ttu-id="be59b-103">Status 屬性</span><span class="sxs-lookup"><span data-stu-id="be59b-103">Status Property</span></span>

<span data-ttu-id="be59b-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="be59b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="be59b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="be59b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="be59b-106">傳回音訊輸出通道的狀態。</span><span class="sxs-lookup"><span data-stu-id="be59b-106">Returns the status of the audio output channel.</span></span>

</dd> <dt>

<span data-ttu-id="be59b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="be59b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="be59b-108">*代理程式 \* \* *。AudioOutput。狀態**</span><span class="sxs-lookup"><span data-stu-id="be59b-108">*agent\*\*\*.AudioOutput.Status*\*</span></span>



| <span data-ttu-id="be59b-109">值</span><span class="sxs-lookup"><span data-stu-id="be59b-109">Value</span></span> | <span data-ttu-id="be59b-110">描述</span><span class="sxs-lookup"><span data-stu-id="be59b-110">Description</span></span>                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be59b-111">0</span><span class="sxs-lookup"><span data-stu-id="be59b-111">0</span></span>     | <span data-ttu-id="be59b-112">音訊輸出通道可用 () 不會忙碌。</span><span class="sxs-lookup"><span data-stu-id="be59b-112">The audio output channel is available (not busy).</span></span>                                                                 |
| <span data-ttu-id="be59b-113">1</span><span class="sxs-lookup"><span data-stu-id="be59b-113">1</span></span>     | <span data-ttu-id="be59b-114">不支援音訊輸出;例如，因為沒有音效卡。</span><span class="sxs-lookup"><span data-stu-id="be59b-114">There is no support for audio output; for example, because there is no sound card.</span></span>                                |
| <span data-ttu-id="be59b-115">2</span><span class="sxs-lookup"><span data-stu-id="be59b-115">2</span></span>     | <span data-ttu-id="be59b-116">無法開啟音訊輸出通道 (忙碌中) ;例如，因為有些其他應用程式現正播放音訊。</span><span class="sxs-lookup"><span data-stu-id="be59b-116">The audio output channel can't be opened (is busy); for example, because some other application is playing audio.</span></span> |
| <span data-ttu-id="be59b-117">3</span><span class="sxs-lookup"><span data-stu-id="be59b-117">3</span></span>     | <span data-ttu-id="be59b-118">音訊輸出通道忙碌中，因為伺服器正在處理使用者語音輸入。</span><span class="sxs-lookup"><span data-stu-id="be59b-118">The audio output channel is busy because the server is processing user speech input.</span></span>                              |
| <span data-ttu-id="be59b-119">4</span><span class="sxs-lookup"><span data-stu-id="be59b-119">4</span></span>     | <span data-ttu-id="be59b-120">音訊輸出通道正在忙碌中，因為字元目前正在說話中。</span><span class="sxs-lookup"><span data-stu-id="be59b-120">The audio output channel is busy because a character is currently speaking.</span></span>                                       |
| <span data-ttu-id="be59b-121">5</span><span class="sxs-lookup"><span data-stu-id="be59b-121">5</span></span>     | <span data-ttu-id="be59b-122">音訊輸出通道不在忙碌中，但正在等候使用者語音輸入。</span><span class="sxs-lookup"><span data-stu-id="be59b-122">The audio output channel is not busy, but it is waiting for user speech input.</span></span>                                    |
| <span data-ttu-id="be59b-123">6</span><span class="sxs-lookup"><span data-stu-id="be59b-123">6</span></span>     | <span data-ttu-id="be59b-124">嘗試存取音訊輸出通道時發生一些其他 (未知的) 問題。</span><span class="sxs-lookup"><span data-stu-id="be59b-124">There was some other (unknown) problem in attempting to access the audio output channel.</span></span>                          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be59b-125">備註</span><span class="sxs-lookup"><span data-stu-id="be59b-125">Remarks</span></span>

<span data-ttu-id="be59b-126">這項設定可讓您的用戶端應用程式查詢音訊輸出通道，並傳回整數值以指出音訊輸出通道的狀態。</span><span class="sxs-lookup"><span data-stu-id="be59b-126">This setting enables your client application to query the audio output channel, returning an Integer value that indicates the status of the audio output channel.</span></span> <span data-ttu-id="be59b-127">您可以使用此資訊來判斷是否適合讓您的字元說話，或是否適合嘗試使用 [**接聽**](listen-method.md) 方法) 來開啟接聽模式 (。</span><span class="sxs-lookup"><span data-stu-id="be59b-127">You can use this to determine whether it is appropriate to have your character speak or whether it is appropriate to try to turn on Listening mode (using the [**Listen**](listen-method.md) method).</span></span>

## <a name="see-also"></a><span data-ttu-id="be59b-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="be59b-128">See Also</span></span>

[<span data-ttu-id="be59b-129">**ListenComplete 事件**</span><span class="sxs-lookup"><span data-stu-id="be59b-129">**ListenComplete event**</span></span>](listencomplete-event.md)


 

 




