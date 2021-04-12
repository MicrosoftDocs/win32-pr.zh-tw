---
title: WM/MediaClassSecondaryID
description: WM/MediaClassSecondaryID 屬性包含次要媒體類別的 GUID。
ms.assetid: 3d1429bc-f168-4b25-9d26-c1c28b852160
keywords:
- WM/MediaClassSecondaryID windows Media 格式
topic_type:
- apiref
api_name:
- WM/MediaClassSecondaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a5923ff0ff0545f1feb769973f2528bd82e351e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373257"
---
# <a name="wmmediaclasssecondaryid"></a><span data-ttu-id="80808-104">WM/MediaClassSecondaryID</span><span class="sxs-lookup"><span data-stu-id="80808-104">WM/MediaClassSecondaryID</span></span>

<span data-ttu-id="80808-105">**WM/MediaClassSecondaryID** 屬性包含次要媒體類別的 GUID。</span><span class="sxs-lookup"><span data-stu-id="80808-105">The **WM/MediaClassSecondaryID** attribute contains the GUID of the secondary media class.</span></span>

## <a name="global-constant"></a><span data-ttu-id="80808-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="80808-106">Global Constant</span></span>

<span data-ttu-id="80808-107">g \_ wszWMMediaClassSecondaryID</span><span class="sxs-lookup"><span data-stu-id="80808-107">g\_wszWMMediaClassSecondaryID</span></span>

## <a name="data-type"></a><span data-ttu-id="80808-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="80808-108">Data Type</span></span>

<span data-ttu-id="80808-109">**WMT \_ 類型 \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="80808-109">**WMT\_TYPE\_GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="80808-110">備註</span><span class="sxs-lookup"><span data-stu-id="80808-110">Remarks</span></span>

<span data-ttu-id="80808-111">這個屬性應該設定為下表中的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="80808-111">This attribute should be set to one of the values in the following table.</span></span>



| <span data-ttu-id="80808-112">次要類別 GUID</span><span class="sxs-lookup"><span data-stu-id="80808-112">Secondary class GUID</span></span>                   | <span data-ttu-id="80808-113">Description</span><span class="sxs-lookup"><span data-stu-id="80808-113">Description</span></span>                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80808-114">"E0236BEB-C281-4EDE-A36D-7AF76A3D45B5"</span><span class="sxs-lookup"><span data-stu-id="80808-114">"E0236BEB-C281-4EDE-A36D-7AF76A3D45B5"</span></span> | <span data-ttu-id="80808-115">用於音訊書籍檔案。</span><span class="sxs-lookup"><span data-stu-id="80808-115">Use for audio book files.</span></span>                                                                                                                                                               |
| <span data-ttu-id="80808-116">"3A172A13-2BD9-4831-835B-114F6A95943F"</span><span class="sxs-lookup"><span data-stu-id="80808-116">"3A172A13-2BD9-4831-835B-114F6A95943F"</span></span> | <span data-ttu-id="80808-117">適用于包含語音文字的音訊檔案，但不是音訊叢書。</span><span class="sxs-lookup"><span data-stu-id="80808-117">Use for audio files that contain spoken word, but are not audio books.</span></span> <span data-ttu-id="80808-118">例如，喜劇常式。</span><span class="sxs-lookup"><span data-stu-id="80808-118">For example, stand-up comedy routines.</span></span>                                                                           |
| <span data-ttu-id="80808-119">"6677DB9B-E5A0-4063-A1AD-ACEB52840CF1"</span><span class="sxs-lookup"><span data-stu-id="80808-119">"6677DB9B-E5A0-4063-A1AD-ACEB52840CF1"</span></span> | <span data-ttu-id="80808-120">用於與新聞相關的音訊檔案。</span><span class="sxs-lookup"><span data-stu-id="80808-120">Use for audio files related to news.</span></span>                                                                                                                                                    |
| <span data-ttu-id="80808-121">"1B824A67-3F80-4E3E-9CDE-F7361B0F5F1B"</span><span class="sxs-lookup"><span data-stu-id="80808-121">"1B824A67-3F80-4E3E-9CDE-F7361B0F5F1B"</span></span> | <span data-ttu-id="80808-122">用於具有交談顯示內容的音訊檔案。</span><span class="sxs-lookup"><span data-stu-id="80808-122">Use for audio files with talk show content.</span></span>                                                                                                                                             |
| <span data-ttu-id="80808-123">"1FE2E091-4E1E-40CE-B22D-348C732E0B10"</span><span class="sxs-lookup"><span data-stu-id="80808-123">"1FE2E091-4E1E-40CE-B22D-348C732E0B10"</span></span> | <span data-ttu-id="80808-124">用於與新聞相關的影片檔案。</span><span class="sxs-lookup"><span data-stu-id="80808-124">Use for video files related to news.</span></span>                                                                                                                                                    |
| <span data-ttu-id="80808-125">"D6DE1D88-C77C-4593-BFBC-9C61E8C373E3"</span><span class="sxs-lookup"><span data-stu-id="80808-125">"D6DE1D88-C77C-4593-BFBC-9C61E8C373E3"</span></span> | <span data-ttu-id="80808-126">用於包含以網路為基礎的節目、短片、影片結尾等的影片檔案。</span><span class="sxs-lookup"><span data-stu-id="80808-126">Use for video files containing Web-based shows, short films, movie trailers, and so on.</span></span> <span data-ttu-id="80808-127">這是不適合另一個類別的影片娛樂一般識別碼。</span><span class="sxs-lookup"><span data-stu-id="80808-127">This is the general identifier for video entertainment that does not fit into another category.</span></span> |
| <span data-ttu-id="80808-128">"00033368-5009-4AC3-A820-5D2D09A4E7C1"</span><span class="sxs-lookup"><span data-stu-id="80808-128">"00033368-5009-4AC3-A820-5D2D09A4E7C1"</span></span> | <span data-ttu-id="80808-129">用於包含遊戲音訊剪輯的音訊檔案。</span><span class="sxs-lookup"><span data-stu-id="80808-129">Use for audio files containing sound clips from games.</span></span>                                                                                                                                  |
| <span data-ttu-id="80808-130">"F24FF731-96FC-4D0F-A2F5-5A3483682B1A"</span><span class="sxs-lookup"><span data-stu-id="80808-130">"F24FF731-96FC-4D0F-A2F5-5A3483682B1A"</span></span> | <span data-ttu-id="80808-131">用於包含遊戲音效軌完整歌曲的音訊檔案。</span><span class="sxs-lookup"><span data-stu-id="80808-131">Use for audio files containing complete songs from game sound tracks.</span></span> <span data-ttu-id="80808-132">如果檔案中只編碼一部分的歌曲，請改用遊戲音訊剪輯的識別碼。</span><span class="sxs-lookup"><span data-stu-id="80808-132">If only part of a song is encoded in the file, use the identifier for game sound clips instead.</span></span>                   |
| <span data-ttu-id="80808-133">"E3E689E2-BA8C-4330-96DF-A0EEEFFA6876"</span><span class="sxs-lookup"><span data-stu-id="80808-133">"E3E689E2-BA8C-4330-96DF-A0EEEFFA6876"</span></span> | <span data-ttu-id="80808-134">用於包含音樂影片的影片檔案。</span><span class="sxs-lookup"><span data-stu-id="80808-134">Use for video files containing music videos.</span></span>                                                                                                                                            |
| <span data-ttu-id="80808-135">"B76628F4-300D-443D-9CB5-01C285109DAF"</span><span class="sxs-lookup"><span data-stu-id="80808-135">"B76628F4-300D-443D-9CB5-01C285109DAF"</span></span> | <span data-ttu-id="80808-136">用於包含一般家用影片的影片檔案。</span><span class="sxs-lookup"><span data-stu-id="80808-136">Use for video files containing general home video.</span></span>                                                                                                                                      |
| <span data-ttu-id="80808-137">"A9B87FC9-BD47-4BF0-AC4F-655B89F7D868"</span><span class="sxs-lookup"><span data-stu-id="80808-137">"A9B87FC9-BD47-4BF0-AC4F-655B89F7D868"</span></span> | <span data-ttu-id="80808-138">用於包含功能短片的影片檔案。</span><span class="sxs-lookup"><span data-stu-id="80808-138">Use for video files containing feature films.</span></span>                                                                                                                                           |
| <span data-ttu-id="80808-139">"BA7F258A-62F7-47A9-B21F-4651C42A000E"</span><span class="sxs-lookup"><span data-stu-id="80808-139">"BA7F258A-62F7-47A9-B21F-4651C42A000E"</span></span> | <span data-ttu-id="80808-140">用於包含電視節目的影片檔案。</span><span class="sxs-lookup"><span data-stu-id="80808-140">Use for video files containing television shows.</span></span> <span data-ttu-id="80808-141">如果是以 Web 為基礎的節目，請使用更多的一般識別碼。</span><span class="sxs-lookup"><span data-stu-id="80808-141">For Web-based shows, use the more generic identifier.</span></span>                                                                                  |
| <span data-ttu-id="80808-142">"44051B5B-B103-4B5C-92AB-93060A9463F0"</span><span class="sxs-lookup"><span data-stu-id="80808-142">"44051B5B-B103-4B5C-92AB-93060A9463F0"</span></span> | <span data-ttu-id="80808-143">用於包含公司影片的影片檔案。</span><span class="sxs-lookup"><span data-stu-id="80808-143">Use for video files containing corporate video.</span></span> <span data-ttu-id="80808-144">例如，錄製的會議或訓練影片。</span><span class="sxs-lookup"><span data-stu-id="80808-144">For example, recorded meetings or training videos.</span></span>                                                                                      |
| <span data-ttu-id="80808-145">"0B710218-8C0C-475E-AF73-4C41C0C8F8CE"</span><span class="sxs-lookup"><span data-stu-id="80808-145">"0B710218-8C0C-475E-AF73-4C41C0C8F8CE"</span></span> | <span data-ttu-id="80808-146">用於包含從相片製作之家用影片的影片檔案。</span><span class="sxs-lookup"><span data-stu-id="80808-146">Use for video files containing home video made from photographs.</span></span>                                                                                                                        |



 

<span data-ttu-id="80808-147">指定次要類別識別碼時，檔案也應該包含主要類別識別碼屬性。</span><span class="sxs-lookup"><span data-stu-id="80808-147">When specifying a secondary class identifier, the file should also contain a primary class identifier attribute.</span></span>

## <a name="see-also"></a><span data-ttu-id="80808-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="80808-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80808-149">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="80808-149">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="80808-150">**WM/MediaClassPrimaryID**</span><span class="sxs-lookup"><span data-stu-id="80808-150">**WM/MediaClassPrimaryID**</span></span>](wm-mediaprimaryid.md)
</dt> </dl>

 

 




