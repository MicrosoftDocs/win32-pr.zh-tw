---
description: GetKaraokeChannelContent 方法會抓取值，指出指定之資料流程中指定之卡拉別通道的內容類型。
ms.assetid: e36a88b8-7184-44a4-8e02-204440f651bc
title: GetKaraokeChannelContent 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd35705f1fba65eaf5c6f7c67ea55078c68e5036
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106988051"
---
# <a name="getkaraokechannelcontent-method"></a><span data-ttu-id="4ef2b-103">GetKaraokeChannelContent 方法</span><span class="sxs-lookup"><span data-stu-id="4ef2b-103">GetKaraokeChannelContent Method</span></span>

> [!Note]  
> <span data-ttu-id="4ef2b-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="4ef2b-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="4ef2b-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="4ef2b-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="4ef2b-106">`GetKaraokeChannelContent`方法會抓取值，指出指定之資料流程中指定之卡拉別通道的內容類型。</span><span class="sxs-lookup"><span data-stu-id="4ef2b-106">The `GetKaraokeChannelContent` method retrieves a value that indicates the type of content in the specified karaoke channel in the specified stream.</span></span>

``` syntax
[ iContent = ] MSWebDVD.GetKaraokeChannelContent(iStream, iChannel)
```

## <a name="parameters"></a><span data-ttu-id="4ef2b-107">參數</span><span class="sxs-lookup"><span data-stu-id="4ef2b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ef2b-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="4ef2b-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="4ef2b-109">將音訊串流指定為整數。</span><span class="sxs-lookup"><span data-stu-id="4ef2b-109">Specifies the audio stream as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="4ef2b-110"><span id="iChannel"></span><span id="ichannel"></span><span id="ICHANNEL"></span>*iChannel*</span><span class="sxs-lookup"><span data-stu-id="4ef2b-110"><span id="iChannel"></span><span id="ichannel"></span><span id="ICHANNEL"></span>*iChannel*</span></span>
</dt> <dd>

<span data-ttu-id="4ef2b-111">將通道指定為整數。</span><span class="sxs-lookup"><span data-stu-id="4ef2b-111">Specifies the channel as an Integer.</span></span> <span data-ttu-id="4ef2b-112">每個通道的可能值為：</span><span class="sxs-lookup"><span data-stu-id="4ef2b-112">The possible values for each channel are:</span></span>



| <span data-ttu-id="4ef2b-113">值</span><span class="sxs-lookup"><span data-stu-id="4ef2b-113">Value</span></span>  | <span data-ttu-id="4ef2b-114">描述</span><span class="sxs-lookup"><span data-stu-id="4ef2b-114">Description</span></span>    |
|--------|----------------|
| <span data-ttu-id="4ef2b-115">0x0001</span><span class="sxs-lookup"><span data-stu-id="4ef2b-115">0x0001</span></span> | <span data-ttu-id="4ef2b-116">指南關切這個領域1</span><span class="sxs-lookup"><span data-stu-id="4ef2b-116">Guide Vocal 1</span></span>  |
| <span data-ttu-id="4ef2b-117">0x0002</span><span class="sxs-lookup"><span data-stu-id="4ef2b-117">0x0002</span></span> | <span data-ttu-id="4ef2b-118">指南關切這個領域2</span><span class="sxs-lookup"><span data-stu-id="4ef2b-118">Guide Vocal 2</span></span>  |
| <span data-ttu-id="4ef2b-119">0x0004</span><span class="sxs-lookup"><span data-stu-id="4ef2b-119">0x0004</span></span> | <span data-ttu-id="4ef2b-120">指南旋律1</span><span class="sxs-lookup"><span data-stu-id="4ef2b-120">Guide Melody 1</span></span> |
| <span data-ttu-id="4ef2b-121">0x0008</span><span class="sxs-lookup"><span data-stu-id="4ef2b-121">0x0008</span></span> | <span data-ttu-id="4ef2b-122">指南旋律2</span><span class="sxs-lookup"><span data-stu-id="4ef2b-122">Guide Melody 2</span></span> |
| <span data-ttu-id="4ef2b-123">0x0010</span><span class="sxs-lookup"><span data-stu-id="4ef2b-123">0x0010</span></span> | <span data-ttu-id="4ef2b-124">指南旋律</span><span class="sxs-lookup"><span data-stu-id="4ef2b-124">Guide Melody A</span></span> |
| <span data-ttu-id="4ef2b-125">0x0020</span><span class="sxs-lookup"><span data-stu-id="4ef2b-125">0x0020</span></span> | <span data-ttu-id="4ef2b-126">指南旋律 B</span><span class="sxs-lookup"><span data-stu-id="4ef2b-126">Guide Melody B</span></span> |
| <span data-ttu-id="4ef2b-127">0x0040</span><span class="sxs-lookup"><span data-stu-id="4ef2b-127">0x0040</span></span> | <span data-ttu-id="4ef2b-128">音效效果 A</span><span class="sxs-lookup"><span data-stu-id="4ef2b-128">Sound Effect A</span></span> |
| <span data-ttu-id="4ef2b-129">0x0080</span><span class="sxs-lookup"><span data-stu-id="4ef2b-129">0x0080</span></span> | <span data-ttu-id="4ef2b-130">音效效果 B</span><span class="sxs-lookup"><span data-stu-id="4ef2b-130">Sound Effect B</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ef2b-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="4ef2b-131">Return Value</span></span>

<span data-ttu-id="4ef2b-132">傳回整數值，其個別位指定卡拉 ok 通道的內容。</span><span class="sxs-lookup"><span data-stu-id="4ef2b-132">Returns an integer value whose individual bits specify the contents of the karaoke channel.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ef2b-133">備註</span><span class="sxs-lookup"><span data-stu-id="4ef2b-133">Remarks</span></span>

<span data-ttu-id="4ef2b-134">DVD-音訊頻道編號是以零為基礎，因此通道2、3和4是輔助的卡拉卡拉器通道。</span><span class="sxs-lookup"><span data-stu-id="4ef2b-134">DVD audio channel numbering is zero-based, so channels 2, 3, and 4 are the auxiliary karaoke channels.</span></span> <span data-ttu-id="4ef2b-135">在方法傳回之後，請在 *iContent* 上執行位 and 運算，以判斷每個通道的內容。</span><span class="sxs-lookup"><span data-stu-id="4ef2b-135">After the method returns, perform a bitwise AND operation on *iContent* to determine the contents of each channel.</span></span> <span data-ttu-id="4ef2b-136">由於單一通道可能會在其上記錄一個以上的內容，因此您應該測試所有可能的值，即使在找到相符的之後也是一樣。</span><span class="sxs-lookup"><span data-stu-id="4ef2b-136">Because a single channel might have more than one type of content recorded on it, you should test for all the possible values even after a match is found.</span></span>

<span data-ttu-id="4ef2b-137">當使用者知道每個頻道的內容之後，他或她必須能夠視需要調整音量，或開啟或關閉個別頻道。</span><span class="sxs-lookup"><span data-stu-id="4ef2b-137">After the user knows the contents of each channel, he or she must be able to adjust the volume or turn the individual channels on or off as needed.</span></span> <span data-ttu-id="4ef2b-138">使用 [**KaraokeAudioPresentationMode**](karaokeaudiopresentationmode-property.md) 屬性，在您的應用程式中執行這項功能。</span><span class="sxs-lookup"><span data-stu-id="4ef2b-138">Implement this functionality in your application by using the [**KaraokeAudioPresentationMode**](karaokeaudiopresentationmode-property.md) property.</span></span>

> [!Note]  
> <span data-ttu-id="4ef2b-139">若要播放卡拉卡拉5光碟，使用者系統上的音訊解碼器必須與 DirectShow 8 卡拉卡拉的執行相容。</span><span class="sxs-lookup"><span data-stu-id="4ef2b-139">To play karaoke discs, the audio decoder on the user's system must be compatible with the DirectShow 8 karaoke implementation.</span></span>

 

 

 



