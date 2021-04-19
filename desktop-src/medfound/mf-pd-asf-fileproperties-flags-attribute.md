---
description: 指定 Advanced 系統格式 (ASF) 檔案是否為廣播或可搜尋。 此值會對應至在 ASF 規格中定義之檔案屬性物件的旗標欄位。
ms.assetid: 427f0dca-f945-4c89-a87a-a7c86291b1c5
title: 'MF_PD_ASF_FILEPROPERTIES_FLAGS 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee294642188a0f2e22143feeca6791fea591cbb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977075"
---
# <a name="mf_pd_asf_fileproperties_flags-attribute"></a><span data-ttu-id="5f793-104">MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 旗標屬性</span><span class="sxs-lookup"><span data-stu-id="5f793-104">MF\_PD\_ASF\_FILEPROPERTIES\_FLAGS attribute</span></span>

<span data-ttu-id="5f793-105">指定 Advanced 系統格式 (ASF) 檔案是否為廣播或可搜尋。</span><span class="sxs-lookup"><span data-stu-id="5f793-105">Specifies whether an Advanced Systems Format (ASF) file is broadcast or seekable.</span></span> <span data-ttu-id="5f793-106">此值會對應至在 ASF 規格中定義之檔案屬性物件的旗標欄位。</span><span class="sxs-lookup"><span data-stu-id="5f793-106">This value corresponds to the Flags field of the File Properties Object, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="5f793-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="5f793-107">Data type</span></span>

<span data-ttu-id="5f793-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5f793-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="5f793-109">備註</span><span class="sxs-lookup"><span data-stu-id="5f793-109">Remarks</span></span>

<span data-ttu-id="5f793-110">此屬性適用于 ASF 內容的表示描述項。</span><span class="sxs-lookup"><span data-stu-id="5f793-110">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="5f793-111">屬性的值是下列旗標的位 OR：</span><span class="sxs-lookup"><span data-stu-id="5f793-111">The value of the attribute is a bitwise OR of the following flags:</span></span>



| <span data-ttu-id="5f793-112">旗標</span><span class="sxs-lookup"><span data-stu-id="5f793-112">Flag</span></span> | <span data-ttu-id="5f793-113">描述</span><span class="sxs-lookup"><span data-stu-id="5f793-113">Description</span></span>                                                                                                                                                                                                                                                                                       |
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f793-114">0x01</span><span class="sxs-lookup"><span data-stu-id="5f793-114">0x01</span></span> | <span data-ttu-id="5f793-115">廣播旗標。</span><span class="sxs-lookup"><span data-stu-id="5f793-115">Broadcast flag.</span></span> <span data-ttu-id="5f793-116">檔案正在建立的進程中。</span><span class="sxs-lookup"><span data-stu-id="5f793-116">The file is in the process of being created.</span></span>                                                                                                                                                                                                                                      |
| <span data-ttu-id="5f793-117">0x02</span><span class="sxs-lookup"><span data-stu-id="5f793-117">0x02</span></span> | <span data-ttu-id="5f793-118">搜尋旗標。</span><span class="sxs-lookup"><span data-stu-id="5f793-118">Seekable flag.</span></span> <span data-ttu-id="5f793-119">檔案是可搜尋的。</span><span class="sxs-lookup"><span data-stu-id="5f793-119">The file is seekable.</span></span><br/> <span data-ttu-id="5f793-120">如果有音訊資料流程，且最大的資料封包大小等於最小的資料封包大小，檔案就是可搜尋的。</span><span class="sxs-lookup"><span data-stu-id="5f793-120">A file is seekable if an audio stream is present and the maximum data packet size equals the minimum data packet size.</span></span> <span data-ttu-id="5f793-121">如果檔案中有音訊串流和影片串流，且具有相符的簡單索引物件，它也可以是可搜尋的。</span><span class="sxs-lookup"><span data-stu-id="5f793-121">It can also be seekable if the file has an audio stream and a video stream with a matching Simple Index Object.</span></span><br/> |



 

<span data-ttu-id="5f793-122">[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會從 ASF 中繼資料產生這個屬性。</span><span class="sxs-lookup"><span data-stu-id="5f793-122">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

<span data-ttu-id="5f793-123">如果已設定廣播旗標，表示描述項中的下列屬性無效：</span><span class="sxs-lookup"><span data-stu-id="5f793-123">If the broadcast flag is set, the following attributes in the presentation descriptor are not valid:</span></span>

-   [<span data-ttu-id="5f793-124">**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 檔案 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="5f793-124">**MF\_PD\_ASF\_FILEPROPERTIES\_FILE\_ID**</span></span>](mf-pd-asf-fileproperties-file-id-attribute.md)
-   [<span data-ttu-id="5f793-125">**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 建立 \_ 時間**</span><span class="sxs-lookup"><span data-stu-id="5f793-125">**MF\_PD\_ASF\_FILEPROPERTIES\_CREATION\_TIME**</span></span>](mf-pd-asf-fileproperties-creation-time-attribute.md)
-   [<span data-ttu-id="5f793-126">**MF \_ PD \_ ASF \_ FILEPROPERTIES 封 \_ 包**</span><span class="sxs-lookup"><span data-stu-id="5f793-126">**MF\_PD\_ASF\_FILEPROPERTIES\_PACKETS**</span></span>](mf-pd-asf-fileproperties-packets-attribute.md)
-   [<span data-ttu-id="5f793-127">**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 播放 \_ 持續時間**</span><span class="sxs-lookup"><span data-stu-id="5f793-127">**MF\_PD\_ASF\_FILEPROPERTIES\_PLAY\_DURATION**</span></span>](mf-pd-asf-fileproperties-play-duration-attribute.md)
-   [<span data-ttu-id="5f793-128">**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 傳送 \_ 持續時間**</span><span class="sxs-lookup"><span data-stu-id="5f793-128">**MF\_PD\_ASF\_FILEPROPERTIES\_SEND\_DURATION**</span></span>](mf-pd-asf-fileproperties-send-duration-attribute.md)

<span data-ttu-id="5f793-129">此外， [**mf \_ pd \_ asf \_ FILEPROPERTIES \_ MAX \_ packet \_ size**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) 屬性和 [**MF \_ pd \_ asf \_ FILEPROPERTIES \_ MIN \_ packet \_ size**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) 屬性值會設定為實際的封包大小。</span><span class="sxs-lookup"><span data-stu-id="5f793-129">In addition, the [**MF\_PD\_ASF\_FILEPROPERTIES\_MAX\_PACKET\_SIZE**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) attribute and [**MF\_PD\_ASF\_FILEPROPERTIES\_MIN\_PACKET\_SIZE**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) attribute values are set to the actual packet size.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f793-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f793-130">Requirements</span></span>



| <span data-ttu-id="5f793-131">需求</span><span class="sxs-lookup"><span data-stu-id="5f793-131">Requirement</span></span> | <span data-ttu-id="5f793-132">值</span><span class="sxs-lookup"><span data-stu-id="5f793-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f793-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5f793-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5f793-134">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f793-134">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5f793-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5f793-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5f793-136">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f793-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5f793-137">標頭</span><span class="sxs-lookup"><span data-stu-id="5f793-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f793-138"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="5f793-138"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f793-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f793-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f793-140">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="5f793-140">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5f793-141">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5f793-141">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="5f793-142">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5f793-142">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="5f793-143">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="5f793-143">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="5f793-144">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="5f793-144">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="5f793-145">ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="5f793-145">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="5f793-146">簡報描述項</span><span class="sxs-lookup"><span data-stu-id="5f793-146">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




