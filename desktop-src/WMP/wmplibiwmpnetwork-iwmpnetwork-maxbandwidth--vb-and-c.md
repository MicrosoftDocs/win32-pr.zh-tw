---
title: IWMPNetwork maxBandwidth 屬性
description: MaxBandwidth 屬性會取得或設定允許的最大頻寬。
ms.assetid: ff7548d8-b80f-4cb4-bdd6-86d585fef329
keywords:
- maxBandwidth 屬性 Windows Media Player
- maxBandwidth 屬性 Windows Media Player，IWMPNetwork 介面
- IWMPNetwork 介面 Windows Media Player，maxBandwidth 屬性
topic_type:
- apiref
api_name:
- IWMPNetwork.maxBandwidth
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3620d609db0f1786da673923f54d726b3c99994a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994152"
---
# <a name="iwmpnetworkmaxbandwidth-property"></a><span data-ttu-id="67a58-106">IWMPNetwork：： maxBandwidth 屬性</span><span class="sxs-lookup"><span data-stu-id="67a58-106">IWMPNetwork::maxBandwidth property</span></span>

<span data-ttu-id="67a58-107">**MaxBandwidth** 屬性會取得或設定允許的最大頻寬。</span><span class="sxs-lookup"><span data-stu-id="67a58-107">The **maxBandwidth** property gets or sets the maximum allowed bandwidth.</span></span>

## <a name="syntax"></a><span data-ttu-id="67a58-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="67a58-108">Syntax</span></span>


```CSharp
public System.Int32 maxBandwidth {get; set;}
```


```VB

Public Property maxBandwidth As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="67a58-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="67a58-109">Property value</span></span>

<span data-ttu-id="67a58-110">最大頻寬的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="67a58-110">A **System.Int32** that is the maximum bandwidth.</span></span>

## <a name="remarks"></a><span data-ttu-id="67a58-111">備註</span><span class="sxs-lookup"><span data-stu-id="67a58-111">Remarks</span></span>

<span data-ttu-id="67a58-112">這個屬性沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="67a58-112">This property does not have a default value.</span></span> <span data-ttu-id="67a58-113">當 Windows Media Player 現正播放時，可以指定此值，但在目前的媒體專案發行之前，您可以開啟另一個媒體專案，或呼叫 **AxWindowsMediaPlayer**，變更將不會生效。</span><span class="sxs-lookup"><span data-stu-id="67a58-113">The value can be specified while Windows Media Player is playing, but the change will not take effect until the current media item is released by opening another one or by calling **AxWindowsMediaPlayer.close**.</span></span> <span data-ttu-id="67a58-114">Windows Media Player 嘗試達到可能的最高頻寬。</span><span class="sxs-lookup"><span data-stu-id="67a58-114">Windows Media Player attempts to achieve the highest bandwidth possible.</span></span> <span data-ttu-id="67a58-115">除非已設定此值，否則不會刻意減少頻寬。</span><span class="sxs-lookup"><span data-stu-id="67a58-115">No intentional reduction of bandwidth will occur unless this value is set.</span></span>

<span data-ttu-id="67a58-116">這項設定有助於減少使用的頻寬量，特別是在多位元率 (MBR) 串流的情況下。</span><span class="sxs-lookup"><span data-stu-id="67a58-116">This setting is useful for reducing the amount of bandwidth used, particularly in the case of a multiple bit rate (MBR) stream.</span></span> <span data-ttu-id="67a58-117">MBR 資料流程包含多個具有不同位速率的資料流程。</span><span class="sxs-lookup"><span data-stu-id="67a58-117">An MBR stream contains multiple streams with different bit rates.</span></span> <span data-ttu-id="67a58-118">在某些情況下，您可能會想要使用比用戶端所需的位元速率低的資料流程。</span><span class="sxs-lookup"><span data-stu-id="67a58-118">In some cases, it may be desirable to use a stream with a lower bit rate than the client requires.</span></span> <span data-ttu-id="67a58-119">在此情況下，使用 **IWMPNetwork. maxBandwidth** 屬性指定較低的位元速率，將會選取較低的位元速率串流。</span><span class="sxs-lookup"><span data-stu-id="67a58-119">In this case, specifying a lower bit rate with the **IWMPNetwork.maxBandwidth** property will select a lower bit-rate stream.</span></span> <span data-ttu-id="67a58-120">例如，MBR 串流可能包含以每秒 20 kb 編碼的資料流程 (Kbps) 、37 Kbps 和 200 Kbps。</span><span class="sxs-lookup"><span data-stu-id="67a58-120">For example, an MBR stream might include streams encoded at 20 kilobits per second (Kbps), 37 Kbps, and 200 Kbps.</span></span> <span data-ttu-id="67a58-121">使用 **IWMPNetwork** 來指定 50000 (50 Kbps 的位元速率) 將會選取 37 kbps 資料流程，而不是 200 kbps 串流。</span><span class="sxs-lookup"><span data-stu-id="67a58-121">Using **IWMPNetwork.maxBandwidth** to specify a bit rate of 50,000 (50 Kbps) will select the 37 Kbps stream instead of the 200 Kbps stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="67a58-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="67a58-122">Requirements</span></span>



| <span data-ttu-id="67a58-123">需求</span><span class="sxs-lookup"><span data-stu-id="67a58-123">Requirement</span></span> | <span data-ttu-id="67a58-124">值</span><span class="sxs-lookup"><span data-stu-id="67a58-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67a58-125">版本</span><span class="sxs-lookup"><span data-stu-id="67a58-125">Version</span></span><br/>   | <span data-ttu-id="67a58-126">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="67a58-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="67a58-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="67a58-127">Namespace</span></span><br/> | <span data-ttu-id="67a58-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="67a58-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="67a58-129">組件</span><span class="sxs-lookup"><span data-stu-id="67a58-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="67a58-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="67a58-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67a58-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67a58-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67a58-132">**AxWindowsMediaPlayer. close (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="67a58-132">**AxWindowsMediaPlayer.close (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-close.md)
</dt> <dt>

[<span data-ttu-id="67a58-133">**IWMPNetwork 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="67a58-133">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





