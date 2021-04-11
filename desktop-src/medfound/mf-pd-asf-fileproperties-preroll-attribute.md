---
description: 指定在播放 Advanced 系統格式 (ASF) 檔之前，緩衝資料的時間量（以毫秒為單位）。
ms.assetid: 6aebe1cf-bd45-4b02-a3c8-6599bb683d7c
title: 'MF_PD_ASF_FILEPROPERTIES_PREROLL 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 502ba715cc2802f9710d579e0c7afd6477b83454
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193773"
---
# <a name="mf_pd_asf_fileproperties_preroll-attribute"></a><span data-ttu-id="919d2-103">MF \_ PD \_ ASF \_ FILEPROPERTIES 預先進行 \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="919d2-103">MF\_PD\_ASF\_FILEPROPERTIES\_PREROLL attribute</span></span>

<span data-ttu-id="919d2-104">指定在播放 Advanced 系統格式 (ASF) 檔之前，緩衝資料的時間量（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="919d2-104">Specifies the amount of time, in milliseconds, to buffer data before playing an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="919d2-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="919d2-105">Data type</span></span>

<span data-ttu-id="919d2-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="919d2-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="919d2-107">備註</span><span class="sxs-lookup"><span data-stu-id="919d2-107">Remarks</span></span>

<span data-ttu-id="919d2-108">此屬性適用于 ASF 內容的表示描述項。</span><span class="sxs-lookup"><span data-stu-id="919d2-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="919d2-109">[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會從 ASF 中繼資料產生這個屬性。</span><span class="sxs-lookup"><span data-stu-id="919d2-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="919d2-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="919d2-110">Requirements</span></span>



| <span data-ttu-id="919d2-111">需求</span><span class="sxs-lookup"><span data-stu-id="919d2-111">Requirement</span></span> | <span data-ttu-id="919d2-112">值</span><span class="sxs-lookup"><span data-stu-id="919d2-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="919d2-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="919d2-113">Minimum supported client</span></span><br/> | <span data-ttu-id="919d2-114">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="919d2-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="919d2-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="919d2-115">Minimum supported server</span></span><br/> | <span data-ttu-id="919d2-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="919d2-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="919d2-117">標頭</span><span class="sxs-lookup"><span data-stu-id="919d2-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="919d2-118"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="919d2-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="919d2-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="919d2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="919d2-120">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="919d2-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="919d2-121">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="919d2-121">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="919d2-122">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="919d2-122">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="919d2-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="919d2-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="919d2-124">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="919d2-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="919d2-125">ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="919d2-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="919d2-126">簡報描述項</span><span class="sxs-lookup"><span data-stu-id="919d2-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




