---
description: 在 MPEG 4 媒體類型的 [範例描述] 方塊中指定目前的專案。
ms.assetid: c8c36abf-6905-4874-a6d2-90dd0725421b
title: 'MF_MT_MPEG4_CURRENT_SAMPLE_ENTRY 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c1f2a43eef1a520a49f5cfbb889f13149fa249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984982"
---
# <a name="mf_mt_mpeg4_current_sample_entry-attribute"></a><span data-ttu-id="3df77-103">MF \_ MT \_ MPEG4 \_ 目前的 \_ 範例 \_ 專案屬性</span><span class="sxs-lookup"><span data-stu-id="3df77-103">MF\_MT\_MPEG4\_CURRENT\_SAMPLE\_ENTRY attribute</span></span>

<span data-ttu-id="3df77-104">在 MPEG 4 媒體類型的 [範例描述] 方塊中指定目前的專案。</span><span class="sxs-lookup"><span data-stu-id="3df77-104">Specifies the current entry in the sample description box for an MPEG-4 media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="3df77-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="3df77-105">Data type</span></span>

<span data-ttu-id="3df77-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3df77-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="3df77-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="3df77-107">Get/set</span></span>

<span data-ttu-id="3df77-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="3df77-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="3df77-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="3df77-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="3df77-110">適用於</span><span class="sxs-lookup"><span data-stu-id="3df77-110">Applies to</span></span>

[<span data-ttu-id="3df77-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="3df77-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="3df77-112">備註</span><span class="sxs-lookup"><span data-stu-id="3df77-112">Remarks</span></span>

<span data-ttu-id="3df77-113">在 [檔] 或 [3GP] 檔案中，[範例描述] 方塊描述檔案中資料流程所使用的編碼方式。</span><span class="sxs-lookup"><span data-stu-id="3df77-113">In an MP4 or 3GP file, the sample description box describes the encoding used for a stream in the file.</span></span> <span data-ttu-id="3df77-114">[範例描述] 方塊可以包含多個專案。</span><span class="sxs-lookup"><span data-stu-id="3df77-114">The sample description box can contain multiple entries.</span></span> <span data-ttu-id="3df77-115">這個屬性會指定要使用的專案。</span><span class="sxs-lookup"><span data-stu-id="3df77-115">This attribute specifies which entry to use.</span></span> <span data-ttu-id="3df77-116">值是清單中以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="3df77-116">The value is a zero-based index into the list.</span></span>

<span data-ttu-id="3df77-117">目前唯一支援的值是0。</span><span class="sxs-lookup"><span data-stu-id="3df77-117">Currently, the only supported value is 0.</span></span> <span data-ttu-id="3df77-118">屬性已定義為未來的擴充性。</span><span class="sxs-lookup"><span data-stu-id="3df77-118">The attribute has been defined for future extensibility.</span></span>

<span data-ttu-id="3df77-119">MPEG-2 檔案來源一律會將值設定為0。</span><span class="sxs-lookup"><span data-stu-id="3df77-119">The MPEG-4 file source always sets the value to 0.</span></span> <span data-ttu-id="3df77-120">3GP 檔接收會忽略這個屬性的值（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="3df77-120">The MP4 and 3GP file sinks ignore the value of this attribute if it is present.</span></span>

<span data-ttu-id="3df77-121">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="3df77-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3df77-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="3df77-122">Requirements</span></span>



| <span data-ttu-id="3df77-123">需求</span><span class="sxs-lookup"><span data-stu-id="3df77-123">Requirement</span></span> | <span data-ttu-id="3df77-124">值</span><span class="sxs-lookup"><span data-stu-id="3df77-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3df77-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3df77-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3df77-126">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3df77-126">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="3df77-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3df77-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3df77-128">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3df77-128">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="3df77-129">標頭</span><span class="sxs-lookup"><span data-stu-id="3df77-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="3df77-130"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="3df77-130"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3df77-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3df77-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3df77-132">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="3df77-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3df77-133">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="3df77-133">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="3df77-134">MF \_ MT \_ MPEG4 \_ 範例 \_ 說明</span><span class="sxs-lookup"><span data-stu-id="3df77-134">MF\_MT\_MPEG4\_SAMPLE\_DESCRIPTION</span></span>](mf-mt-mpeg4-sample-description.md)
</dt> </dl>

 

 




