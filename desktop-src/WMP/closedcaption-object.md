---
title: ClosedCaption 物件
description: ClosedCaption 物件提供一種方式，可包含媒體剪輯的標題。 字幕文字位於已同步處理的可存取媒體交換 (薩米) 檔。
ms.assetid: 5e192aa4-0ecd-4bda-8dad-1750039c7898
keywords:
- ClosedCaption 物件 Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 85e53468e8d5cc2694555b9a05d8b207d1660618
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "104022693"
---
# <a name="closedcaption-object"></a><span data-ttu-id="e427f-105">ClosedCaption 物件</span><span class="sxs-lookup"><span data-stu-id="e427f-105">ClosedCaption Object</span></span>

<span data-ttu-id="e427f-106">**ClosedCaption** 物件提供一種方式，可包含媒體剪輯的標題。</span><span class="sxs-lookup"><span data-stu-id="e427f-106">The **ClosedCaption** object provides a way to include captions with a media clip.</span></span> <span data-ttu-id="e427f-107">字幕文字位於已同步處理的可存取媒體交換 (薩米) 檔。</span><span class="sxs-lookup"><span data-stu-id="e427f-107">The captioning text is in a Synchronized Accessible Media Interchange (SAMI) file.</span></span>

<span data-ttu-id="e427f-108">**ClosedCaption** 物件支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="e427f-108">The **ClosedCaption** object supports the following properties.</span></span>



| <span data-ttu-id="e427f-109">屬性</span><span class="sxs-lookup"><span data-stu-id="e427f-109">Property</span></span>                                           | <span data-ttu-id="e427f-110">描述</span><span class="sxs-lookup"><span data-stu-id="e427f-110">Description</span></span>                                                                                          |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e427f-111">captioningID</span><span class="sxs-lookup"><span data-stu-id="e427f-111">captioningID</span></span>](closedcaption-captioningid.md)     | <span data-ttu-id="e427f-112">指定或抓取顯示字幕的框架或控制項名稱。</span><span class="sxs-lookup"><span data-stu-id="e427f-112">Specifies or retrieves the name of the frame or control displaying the captioning.</span></span>                   |
| [<span data-ttu-id="e427f-113">SAMIFileName</span><span class="sxs-lookup"><span data-stu-id="e427f-113">SAMIFileName</span></span>](closedcaption-samifilename.md)     | <span data-ttu-id="e427f-114">指定或抓取包含隱藏式輔助字幕所需資訊的檔案名。</span><span class="sxs-lookup"><span data-stu-id="e427f-114">Specifies or retrieves the name of the file containing the information needed for closed captioning.</span></span> |
| [<span data-ttu-id="e427f-115">SAMILang</span><span class="sxs-lookup"><span data-stu-id="e427f-115">SAMILang</span></span>](closedcaption-samilang.md)             | <span data-ttu-id="e427f-116">指定或抓取隱藏式輔助字幕所顯示的語言。</span><span class="sxs-lookup"><span data-stu-id="e427f-116">Specifies or retrieves the language displayed for closed captioning.</span></span>                                 |
| [<span data-ttu-id="e427f-117">SAMILangCount</span><span class="sxs-lookup"><span data-stu-id="e427f-117">SAMILangCount</span></span>](closedcaption-samilangcount.md)   | <span data-ttu-id="e427f-118">抓取目前的薩米文檔案所支援的語言數目。</span><span class="sxs-lookup"><span data-stu-id="e427f-118">Retrieves the number of languages supported by the current SAMI file.</span></span>                                |
| [<span data-ttu-id="e427f-119">SAMIStyle</span><span class="sxs-lookup"><span data-stu-id="e427f-119">SAMIStyle</span></span>](closedcaption-samistyle.md)           | <span data-ttu-id="e427f-120">指定或抓取隱藏式輔助字幕樣式。</span><span class="sxs-lookup"><span data-stu-id="e427f-120">Specifies or retrieves the closed captioning style.</span></span>                                                  |
| [<span data-ttu-id="e427f-121">SAMIStyleCount</span><span class="sxs-lookup"><span data-stu-id="e427f-121">SAMIStyleCount</span></span>](closedcaption-samistylecount.md) | <span data-ttu-id="e427f-122">抓取目前的薩米文檔案所支援的樣式數目。</span><span class="sxs-lookup"><span data-stu-id="e427f-122">Retrieves the number of styles supported by the current SAMI file.</span></span>                                   |



 

<span data-ttu-id="e427f-123">**ClosedCaption** 物件支援下列方法。</span><span class="sxs-lookup"><span data-stu-id="e427f-123">The **ClosedCaption** object supports the following methods.</span></span>



| <span data-ttu-id="e427f-124">方法</span><span class="sxs-lookup"><span data-stu-id="e427f-124">Method</span></span>                                                 | <span data-ttu-id="e427f-125">描述</span><span class="sxs-lookup"><span data-stu-id="e427f-125">Description</span></span>                                                                              |
|--------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e427f-126">getSAMILangID</span><span class="sxs-lookup"><span data-stu-id="e427f-126">getSAMILangID</span></span>](closedcaption-getsamilangid.md)       | <span data-ttu-id="e427f-127">抓取目前薩米文檔案所支援之語言 (LCID) 的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="e427f-127">Retrieves the locale identifier (LCID) of a language supported by the current SAMI file.</span></span> |
| [<span data-ttu-id="e427f-128">getSAMILangName</span><span class="sxs-lookup"><span data-stu-id="e427f-128">getSAMILangName</span></span>](closedcaption-getsamilangname.md)   | <span data-ttu-id="e427f-129">抓取目前的薩米文檔案所支援的語言名稱。</span><span class="sxs-lookup"><span data-stu-id="e427f-129">Retrieves the name of a language supported by the current SAMI file.</span></span>                     |
| [<span data-ttu-id="e427f-130">getSAMIStyleName</span><span class="sxs-lookup"><span data-stu-id="e427f-130">getSAMIStyleName</span></span>](closedcaption-getsamistylename.md) | <span data-ttu-id="e427f-131">抓取目前的薩米文檔案所支援的樣式名稱。</span><span class="sxs-lookup"><span data-stu-id="e427f-131">Retrieves the name of a style supported by the current SAMI file.</span></span>                        |



 

<span data-ttu-id="e427f-132">**ClosedCaption** 物件是透過下列屬性來存取。</span><span class="sxs-lookup"><span data-stu-id="e427f-132">The **ClosedCaption** object is accessed through the following property.</span></span>



| <span data-ttu-id="e427f-133">Object</span><span class="sxs-lookup"><span data-stu-id="e427f-133">Object</span></span>                      | <span data-ttu-id="e427f-134">屬性</span><span class="sxs-lookup"><span data-stu-id="e427f-134">Property</span></span>                                  |
|-----------------------------|-------------------------------------------|
| [<span data-ttu-id="e427f-135">球員</span><span class="sxs-lookup"><span data-stu-id="e427f-135">Player</span></span>](player-object.md) | [<span data-ttu-id="e427f-136">closedCaption</span><span class="sxs-lookup"><span data-stu-id="e427f-136">closedCaption</span></span>](player-closedcaption.md) |



 

## <a name="see-also"></a><span data-ttu-id="e427f-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e427f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e427f-138">**將隱藏式輔助字幕新增至數位媒體**</span><span class="sxs-lookup"><span data-stu-id="e427f-138">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="e427f-139">**腳本的物件模型參考**</span><span class="sxs-lookup"><span data-stu-id="e427f-139">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




