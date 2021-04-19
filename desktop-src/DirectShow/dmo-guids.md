---
description: 下表列出 (Guid) 針對 Microsoft DirectX 媒體物件 (的) 類別目錄定義的全域唯一識別碼。 這些 Guid 會定義在標頭檔 Dmoreg 中，並由 Dmoguids .lib 程式庫匯出。
ms.assetid: d67debd0-8ecb-41ab-bc6c-b27cba97c65a
title: 'SQL-DMO Guid (Dmoreg .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c10d5bd917d6368d398362e76ffa9ea8255933ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994272"
---
# <a name="dmo-guids"></a><span data-ttu-id="fa8cd-104">SQL-DMO Guid</span><span class="sxs-lookup"><span data-stu-id="fa8cd-104">DMO GUIDs</span></span>

<span data-ttu-id="fa8cd-105">下表列出 (Guid) 針對 Microsoft DirectX 媒體物件 (的) 類別目錄定義的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="fa8cd-105">The following table lists the globally unique identifiers (GUIDs) defined for Microsoft DirectX Media Object (DMO) categories.</span></span> <span data-ttu-id="fa8cd-106">這些 Guid 會定義在標頭檔 Dmoreg 中，並由 Dmoguids .lib 程式庫匯出。</span><span class="sxs-lookup"><span data-stu-id="fa8cd-106">These GUIDs are defined in the header file Dmoreg.h and exported by the Dmoguids.lib library.</span></span>

<span data-ttu-id="fa8cd-107">若要列舉分類中註冊的 DMOs，請將對應的 GUID 傳遞給 [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) 函式。</span><span class="sxs-lookup"><span data-stu-id="fa8cd-107">To enumerate the DMOs registered in a category, pass the corresponding GUID to the [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) function.</span></span>



| <span data-ttu-id="fa8cd-108">GUID</span><span class="sxs-lookup"><span data-stu-id="fa8cd-108">GUID</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="fa8cd-109">Description</span><span class="sxs-lookup"><span data-stu-id="fa8cd-109">Description</span></span>                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------|
| <span id="DMOCATEGORY_AUDIO_DECODER"></span><span id="dmocategory_audio_decoder"></span><dl> <span data-ttu-id="fa8cd-110"><dt>**DMOCATEGORY \_ 音訊 \_ 解碼器**</dt></span><span class="sxs-lookup"><span data-stu-id="fa8cd-110"><dt>**DMOCATEGORY\_AUDIO\_DECODER**</dt></span></span> </dl>                       | <span data-ttu-id="fa8cd-111">音訊解碼器</span><span class="sxs-lookup"><span data-stu-id="fa8cd-111">Audio decoder</span></span><br/>        |
| <span id="DMOCATEGORY_AUDIO_EFFECT"></span><span id="dmocategory_audio_effect"></span><dl> <span data-ttu-id="fa8cd-112"><dt>**DMOCATEGORY \_ 音訊 \_ 效果**</dt></span><span class="sxs-lookup"><span data-stu-id="fa8cd-112"><dt>**DMOCATEGORY\_AUDIO\_EFFECT**</dt></span></span> </dl>                          | <span data-ttu-id="fa8cd-113">音訊效果</span><span class="sxs-lookup"><span data-stu-id="fa8cd-113">Audio effect</span></span><br/>         |
| <span id="DMOCATEGORY_AUDIO_ENCODER"></span><span id="dmocategory_audio_encoder"></span><dl> <span data-ttu-id="fa8cd-114"><dt>**DMOCATEGORY \_ 音訊 \_ 編碼器**</dt></span><span class="sxs-lookup"><span data-stu-id="fa8cd-114"><dt>**DMOCATEGORY\_AUDIO\_ENCODER**</dt></span></span> </dl>                       | <span data-ttu-id="fa8cd-115">音訊編碼器</span><span class="sxs-lookup"><span data-stu-id="fa8cd-115">Audio encoder</span></span><br/>        |
| <span id="DMOCATEGORY_VIDEO_DECODER"></span><span id="dmocategory_video_decoder"></span><dl> <span data-ttu-id="fa8cd-116"><dt>**DMOCATEGORY \_ 影片 \_ 解碼器**</dt></span><span class="sxs-lookup"><span data-stu-id="fa8cd-116"><dt>**DMOCATEGORY\_VIDEO\_DECODER**</dt></span></span> </dl>                       | <span data-ttu-id="fa8cd-117">影片解碼</span><span class="sxs-lookup"><span data-stu-id="fa8cd-117">Video decoder</span></span><br/>        |
| <span id="DMOCATEGORY_VIDEO_EFFECT"></span><span id="dmocategory_video_effect"></span><dl> <span data-ttu-id="fa8cd-118"><dt>**DMOCATEGORY \_ 影片 \_ 效果**</dt></span><span class="sxs-lookup"><span data-stu-id="fa8cd-118"><dt>**DMOCATEGORY\_VIDEO\_EFFECT**</dt></span></span> </dl>                          | <span data-ttu-id="fa8cd-119">影片效果</span><span class="sxs-lookup"><span data-stu-id="fa8cd-119">Video effect</span></span><br/>         |
| <span id="DMOCATEGORY_VIDEO_ENCODER"></span><span id="dmocategory_video_encoder"></span><dl> <span data-ttu-id="fa8cd-120"><dt>**DMOCATEGORY \_ 影片 \_ 編碼器**</dt></span><span class="sxs-lookup"><span data-stu-id="fa8cd-120"><dt>**DMOCATEGORY\_VIDEO\_ENCODER**</dt></span></span> </dl>                       | <span data-ttu-id="fa8cd-121">影片編碼器</span><span class="sxs-lookup"><span data-stu-id="fa8cd-121">Video encoder</span></span><br/>        |
| <span id="DMOCATEGORY_AUDIO_CAPTURE_EFFECT"></span><span id="dmocategory_audio_capture_effect"></span><dl> <span data-ttu-id="fa8cd-122"><dt>**DMOCATEGORY \_ 音訊 \_ 捕獲 \_ 效果**</dt></span><span class="sxs-lookup"><span data-stu-id="fa8cd-122"><dt>**DMOCATEGORY\_AUDIO\_CAPTURE\_EFFECT**</dt></span></span> </dl> | <span data-ttu-id="fa8cd-123">音訊捕獲效果</span><span class="sxs-lookup"><span data-stu-id="fa8cd-123">Audio capture effect</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="fa8cd-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa8cd-124">Requirements</span></span>



| <span data-ttu-id="fa8cd-125">需求</span><span class="sxs-lookup"><span data-stu-id="fa8cd-125">Requirement</span></span> | <span data-ttu-id="fa8cd-126">值</span><span class="sxs-lookup"><span data-stu-id="fa8cd-126">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fa8cd-127">標頭</span><span class="sxs-lookup"><span data-stu-id="fa8cd-127">Header</span></span><br/> | <dl> <span data-ttu-id="fa8cd-128"><dt>Dmoreg。h</dt></span><span class="sxs-lookup"><span data-stu-id="fa8cd-128"><dt>Dmoreg.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa8cd-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa8cd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa8cd-130">SQL-DMO 常數</span><span class="sxs-lookup"><span data-stu-id="fa8cd-130">DMO Constants</span></span>](dmo-constants.md)
</dt> </dl>

 

 




