---
title: 'IWMPClosedCaption (VB 和 C ) 介面 (h.264. h) '
description: 提供一種方式，可包含包含數位媒體檔案的標題。 字幕文字位於已同步處理的可存取媒體交換 (薩米) 檔。
ms.assetid: 927f6fe4-5847-439e-9df0-19cc910d887d
keywords:
- IWMPClosedCaption (VB 和 C ) 介面 Windows Media Player
- IWMPClosedCaption (VB 和 C ) 介面 Windows Media Player，說明
topic_type:
- apiref
api_name:
- IWMPClosedCaption (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ce3f697fc5c651a47f257a61bd9841987f54478
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989825"
---
# <a name="iwmpclosedcaption-vb-and-c-interface"></a><span data-ttu-id="83311-106">IWMPClosedCaption (VB 和 c # ) 介面</span><span class="sxs-lookup"><span data-stu-id="83311-106">IWMPClosedCaption (VB and C#) interface</span></span>

<span data-ttu-id="83311-107">提供一種方式，可包含包含數位媒體檔案的標題。</span><span class="sxs-lookup"><span data-stu-id="83311-107">Provides a way to include captions with a digital media file.</span></span> <span data-ttu-id="83311-108">字幕文字位於已同步處理的可存取媒體交換 (薩米) 檔。</span><span class="sxs-lookup"><span data-stu-id="83311-108">The captioning text is in a Synchronized Accessible Media Interchange (SAMI) file.</span></span>

## <a name="members"></a><span data-ttu-id="83311-109">成員</span><span class="sxs-lookup"><span data-stu-id="83311-109">Members</span></span>

<span data-ttu-id="83311-110">**IWMPClosedCaption (VB 和 c # )** 介面不會定義任何成員。</span><span class="sxs-lookup"><span data-stu-id="83311-110">The **IWMPClosedCaption (VB and C#)** interface does not define any members.</span></span>

<span data-ttu-id="83311-111">**IWMPClosedCaption** 介面會公開下列屬性。</span><span class="sxs-lookup"><span data-stu-id="83311-111">The **IWMPClosedCaption** interface exposes the following properties.</span></span>



| <span data-ttu-id="83311-112">屬性</span><span class="sxs-lookup"><span data-stu-id="83311-112">Property</span></span>                                                                             | <span data-ttu-id="83311-113">描述</span><span class="sxs-lookup"><span data-stu-id="83311-113">Description</span></span>                                                                                |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="83311-114">captioningId</span><span class="sxs-lookup"><span data-stu-id="83311-114">captioningId</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-captioningid--vb-and-c.md) | <span data-ttu-id="83311-115">取得或設定顯示字幕的 HTML 元素名稱。</span><span class="sxs-lookup"><span data-stu-id="83311-115">Gets or sets the name of the HTML element displaying the captioning.</span></span>                       |
| [<span data-ttu-id="83311-116">SAMIFileName</span><span class="sxs-lookup"><span data-stu-id="83311-116">SAMIFileName</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samifilename--vb-and-c.md) | <span data-ttu-id="83311-117">取得或設定包含隱藏式輔助字幕所需資訊的檔案名。</span><span class="sxs-lookup"><span data-stu-id="83311-117">Gets or sets the name of the file containing the information needed for closed captioning.</span></span> |
| [<span data-ttu-id="83311-118">SAMILang</span><span class="sxs-lookup"><span data-stu-id="83311-118">SAMILang</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)         | <span data-ttu-id="83311-119">取得或設定針對隱藏式輔助字幕所顯示的語言。</span><span class="sxs-lookup"><span data-stu-id="83311-119">Gets or sets the language displayed for closed captioning.</span></span>                                 |
| [<span data-ttu-id="83311-120">SAMIStyle</span><span class="sxs-lookup"><span data-stu-id="83311-120">SAMIStyle</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)       | <span data-ttu-id="83311-121">取得或設定隱藏式輔助字幕樣式。</span><span class="sxs-lookup"><span data-stu-id="83311-121">Gets or sets the closed captioning style.</span></span>                                                  |



 

<span data-ttu-id="83311-122">使用下列屬性來取得 **IWMPClosedCaption** 介面。</span><span class="sxs-lookup"><span data-stu-id="83311-122">Get an **IWMPClosedCaption** interface by using the following property.</span></span>



| <span data-ttu-id="83311-123">Object</span><span class="sxs-lookup"><span data-stu-id="83311-123">Object</span></span>                                                            | <span data-ttu-id="83311-124">屬性</span><span class="sxs-lookup"><span data-stu-id="83311-124">Property</span></span>                                                                   |
|-------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="83311-125">AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="83311-125">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="83311-126">closedCaption</span><span class="sxs-lookup"><span data-stu-id="83311-126">closedCaption</span></span>](axwmplib-axwindowsmediaplayer-closedcaption--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="83311-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="83311-127">Requirements</span></span>



| <span data-ttu-id="83311-128">需求</span><span class="sxs-lookup"><span data-stu-id="83311-128">Requirement</span></span> | <span data-ttu-id="83311-129">值</span><span class="sxs-lookup"><span data-stu-id="83311-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="83311-130">標頭</span><span class="sxs-lookup"><span data-stu-id="83311-130">Header</span></span><br/> | <dl> <span data-ttu-id="83311-131"><dt>Wmp。h</dt></span><span class="sxs-lookup"><span data-stu-id="83311-131"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83311-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="83311-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83311-133">**將隱藏式輔助字幕新增至數位媒體**</span><span class="sxs-lookup"><span data-stu-id="83311-133">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="83311-134">**適用于 Visual Basic .NET 和 C 的介面#**</span><span class="sxs-lookup"><span data-stu-id="83311-134">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="83311-135">**IWMPClosedCaption2 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="83311-135">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





