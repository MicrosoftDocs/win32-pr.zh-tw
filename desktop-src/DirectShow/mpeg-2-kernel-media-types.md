---
description: 針對數個 MPEG-2 媒體類型 Guid，Windows DDK 會定義與 DirectShow 中使用的名稱不同的名稱。 下表顯示 (在 Ksuuids 中定義的 DirectShow 名稱) ，以及在 Ksmedia 中定義 (的對應核心模式名稱) 。
ms.assetid: ecf94552-5a0f-464c-9f9b-4861faa38d05
title: 'MPEG-2 核心媒體類型 (Dshow .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37b03e6d3cbc32c987110ceac98e6aeef6617d6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993442"
---
# <a name="mpeg-2-kernel-media-types"></a><span data-ttu-id="8e1e7-104">MPEG-2 核心媒體類型</span><span class="sxs-lookup"><span data-stu-id="8e1e7-104">MPEG-2 Kernel Media Types</span></span>

<span data-ttu-id="8e1e7-105">針對數個 MPEG-2 媒體類型 Guid，Windows DDK 會定義與 DirectShow 中使用的名稱不同的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e1e7-105">For several MPEG-2 media type GUIDs, the Windows DDK defines names that differ from the names used in DirectShow.</span></span> <span data-ttu-id="8e1e7-106">下表顯示 (在 Ksuuids 中定義的 DirectShow 名稱) ，以及在 Ksmedia 中定義 (的對應核心模式名稱) 。</span><span class="sxs-lookup"><span data-stu-id="8e1e7-106">The following table shows the DirectShow names (defined in Ksuuids.h) and the corresponding kernel-mode names (defined in Ksmedia.h).</span></span>



| <span data-ttu-id="8e1e7-107">Ksuuids 中的名稱</span><span class="sxs-lookup"><span data-stu-id="8e1e7-107">Name in Ksuuids.h</span></span>              | <span data-ttu-id="8e1e7-108">Ksmedia 中的名稱</span><span class="sxs-lookup"><span data-stu-id="8e1e7-108">Name in Ksmedia.h</span></span>                          |
|--------------------------------|--------------------------------------------|
| <span data-ttu-id="8e1e7-109">格式 \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="8e1e7-109">FORMAT\_WaveFormatEx</span></span>           | <span data-ttu-id="8e1e7-110">KSDATAFORMAT \_ 規範 \_ WAVEFORMATEX</span><span class="sxs-lookup"><span data-stu-id="8e1e7-110">KSDATAFORMAT\_SPECIFIER\_WAVEFORMATEX</span></span>      |
| <span data-ttu-id="8e1e7-111">格式 \_ MPEG2Video</span><span class="sxs-lookup"><span data-stu-id="8e1e7-111">FORMAT\_MPEG2Video</span></span>             | <span data-ttu-id="8e1e7-112">KSDATAFORMAT \_ 規範 \_ MPEG2 \_ 影片</span><span class="sxs-lookup"><span data-stu-id="8e1e7-112">KSDATAFORMAT\_SPECIFIER\_MPEG2\_VIDEO</span></span>      |
| <span data-ttu-id="8e1e7-113">MEDIASUBTYPE \_ ATSC \_ SI</span><span class="sxs-lookup"><span data-stu-id="8e1e7-113">MEDIASUBTYPE\_ATSC\_SI</span></span>         | <span data-ttu-id="8e1e7-114">KSDATAFORMAT \_ 子類型 \_ ATSC \_ SI</span><span class="sxs-lookup"><span data-stu-id="8e1e7-114">KSDATAFORMAT\_SUBTYPE\_ATSC\_SI</span></span>            |
| <span data-ttu-id="8e1e7-115">MEDIASUBTYPE \_ 杜 \_ AC3</span><span class="sxs-lookup"><span data-stu-id="8e1e7-115">MEDIASUBTYPE\_DOLBY\_AC3</span></span>       | <span data-ttu-id="8e1e7-116">KSDATAFORMAT \_ 子類型 \_ AC3 \_ 音訊</span><span class="sxs-lookup"><span data-stu-id="8e1e7-116">KSDATAFORMAT\_SUBTYPE\_AC3\_AUDIO</span></span>          |
| <span data-ttu-id="8e1e7-117">MEDIASUBTYPE \_ DVB-T \_ SI</span><span class="sxs-lookup"><span data-stu-id="8e1e7-117">MEDIASUBTYPE\_DVB\_SI</span></span>          | <span data-ttu-id="8e1e7-118">KSDATAFORMAT \_ 子類型 \_ DVB-T \_ SI</span><span class="sxs-lookup"><span data-stu-id="8e1e7-118">KSDATAFORMAT\_SUBTYPE\_DVB\_SI</span></span>             |
| <span data-ttu-id="8e1e7-119">MEDIASUBTYPE \_ DVD \_ LPCM \_ 音訊</span><span class="sxs-lookup"><span data-stu-id="8e1e7-119">MEDIASUBTYPE\_DVD\_LPCM\_AUDIO</span></span> | <span data-ttu-id="8e1e7-120">KSDATAFORMAT \_ 子類型 \_ LPCM \_ 音訊</span><span class="sxs-lookup"><span data-stu-id="8e1e7-120">KSDATAFORMAT\_SUBTYPE\_LPCM\_AUDIO</span></span>         |
| <span data-ttu-id="8e1e7-121">MEDIASUBTYPE \_ MPEG2 \_ 音訊</span><span class="sxs-lookup"><span data-stu-id="8e1e7-121">MEDIASUBTYPE\_MPEG2\_AUDIO</span></span>     | <span data-ttu-id="8e1e7-122">KSDATAFORMAT \_ 子類型 \_ MPEG2 \_ 音訊</span><span class="sxs-lookup"><span data-stu-id="8e1e7-122">KSDATAFORMAT\_SUBTYPE\_MPEG2\_AUDIO</span></span>        |
| <span data-ttu-id="8e1e7-123">MEDIASUBTYPE \_ MPEG2 \_ 計畫</span><span class="sxs-lookup"><span data-stu-id="8e1e7-123">MEDIASUBTYPE\_MPEG2\_PROGRAM</span></span>   | <span data-ttu-id="8e1e7-124">靜態 \_ KSDATAFORMAT \_ 類型 \_ MPEG2 \_ 程式</span><span class="sxs-lookup"><span data-stu-id="8e1e7-124">STATIC\_KSDATAFORMAT\_TYPE\_MPEG2\_PROGRAM</span></span> |
| <span data-ttu-id="8e1e7-125">MEDIASUBTYPE \_ MPEG2 \_ 傳輸</span><span class="sxs-lookup"><span data-stu-id="8e1e7-125">MEDIASUBTYPE\_MPEG2\_TRANSPORT</span></span> | <span data-ttu-id="8e1e7-126">KSDATAFORMAT \_ 類型 \_ MPEG2 \_ 傳輸</span><span class="sxs-lookup"><span data-stu-id="8e1e7-126">KSDATAFORMAT\_TYPE\_MPEG2\_TRANSPORT</span></span>       |
| <span data-ttu-id="8e1e7-127">MEDIASUBTYPE \_ MPEG2 \_ 影片</span><span class="sxs-lookup"><span data-stu-id="8e1e7-127">MEDIASUBTYPE\_MPEG2\_VIDEO</span></span>     | <span data-ttu-id="8e1e7-128">KSDATAFORMAT \_ 子類型的 \_ MPEG2 \_ 影片</span><span class="sxs-lookup"><span data-stu-id="8e1e7-128">KSDATAFORMAT\_SUBTYPE\_MPEG2\_VIDEO</span></span>        |
| <span data-ttu-id="8e1e7-129">媒體的 \_ MPEG2 \_ 區段</span><span class="sxs-lookup"><span data-stu-id="8e1e7-129">MEDIATYPE\_MPEG2\_SECTIONS</span></span>     | <span data-ttu-id="8e1e7-130">KSDATAFORMAT \_ 類型 \_ MPEG2 \_ 區段</span><span class="sxs-lookup"><span data-stu-id="8e1e7-130">KSDATAFORMAT\_TYPE\_MPEG2\_SECTIONS</span></span>        |
| <span data-ttu-id="8e1e7-131">媒體 \_ 媒體</span><span class="sxs-lookup"><span data-stu-id="8e1e7-131">MEDIATYPE\_Audio</span></span>               | <span data-ttu-id="8e1e7-132">KSDATAFORMAT \_ 類型 \_ 音訊</span><span class="sxs-lookup"><span data-stu-id="8e1e7-132">KSDATAFORMAT\_TYPE\_AUDIO</span></span>                  |
| <span data-ttu-id="8e1e7-133">媒體媒體的 \_ MPEG2 \_ pe</span><span class="sxs-lookup"><span data-stu-id="8e1e7-133">MEDIATYPE\_MPEG2\_PES</span></span>          | <span data-ttu-id="8e1e7-134">KSDATAFORMAT \_ 類型 \_ MPEG2 \_ pe</span><span class="sxs-lookup"><span data-stu-id="8e1e7-134">KSDATAFORMAT\_TYPE\_MPEG2\_PES</span></span>             |
| <span data-ttu-id="8e1e7-135">媒體 \_ 媒體</span><span class="sxs-lookup"><span data-stu-id="8e1e7-135">MEDIATYPE\_Video</span></span>               | <span data-ttu-id="8e1e7-136">KSDATAFORMAT \_ 型別 \_ 影片</span><span class="sxs-lookup"><span data-stu-id="8e1e7-136">KSDATAFORMAT\_TYPE\_VIDEO</span></span>                  |



 

## <a name="requirements"></a><span data-ttu-id="8e1e7-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e1e7-137">Requirements</span></span>



| <span data-ttu-id="8e1e7-138">需求</span><span class="sxs-lookup"><span data-stu-id="8e1e7-138">Requirement</span></span> | <span data-ttu-id="8e1e7-139">值</span><span class="sxs-lookup"><span data-stu-id="8e1e7-139">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8e1e7-140">標頭</span><span class="sxs-lookup"><span data-stu-id="8e1e7-140">Header</span></span><br/> | <dl> <span data-ttu-id="8e1e7-141"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="8e1e7-141"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e1e7-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8e1e7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e1e7-143">MPEG-2 媒體類型</span><span class="sxs-lookup"><span data-stu-id="8e1e7-143">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 




