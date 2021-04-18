---
description: 指定傳送 Advanced 系統格式所需的時間（以 100-毫微秒單位） (ASF) 檔。 封包傳送時間是封包應該透過網路傳送的時間。 這不是封包的呈現時間。
ms.assetid: 2bd427e2-106d-4997-86aa-fae221e429eb
title: 'MF_PD_ASF_FILEPROPERTIES_SEND_DURATION 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: deed3f78208a0f0c7e555e8113f05ac0800cdb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978247"
---
# <a name="mf_pd_asf_fileproperties_send_duration-attribute"></a><span data-ttu-id="1ab52-105">MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 傳送 \_ 持續時間屬性</span><span class="sxs-lookup"><span data-stu-id="1ab52-105">MF\_PD\_ASF\_FILEPROPERTIES\_SEND\_DURATION attribute</span></span>

<span data-ttu-id="1ab52-106">指定傳送 Advanced 系統格式所需的時間（以 100-毫微秒單位） (ASF) 檔。</span><span class="sxs-lookup"><span data-stu-id="1ab52-106">Specifies the time, in 100-nanosecond units, needed to send an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="1ab52-107">封包的 *傳送時間* 是在網路上傳遞封包的時間。</span><span class="sxs-lookup"><span data-stu-id="1ab52-107">A packet's *send time* is the time when the packet should be delivered over the network.</span></span> <span data-ttu-id="1ab52-108">這不是封包的呈現時間。</span><span class="sxs-lookup"><span data-stu-id="1ab52-108">It is not the presentation time of the packet.</span></span>

## <a name="data-type"></a><span data-ttu-id="1ab52-109">資料類型</span><span class="sxs-lookup"><span data-stu-id="1ab52-109">Data type</span></span>

<span data-ttu-id="1ab52-110">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="1ab52-110">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="1ab52-111">備註</span><span class="sxs-lookup"><span data-stu-id="1ab52-111">Remarks</span></span>

<span data-ttu-id="1ab52-112">此屬性適用于 ASF 內容的表示描述項。</span><span class="sxs-lookup"><span data-stu-id="1ab52-112">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="1ab52-113">[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會從 ASF 中繼資料產生這個屬性。</span><span class="sxs-lookup"><span data-stu-id="1ab52-113">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ab52-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ab52-114">Requirements</span></span>



| <span data-ttu-id="1ab52-115">需求</span><span class="sxs-lookup"><span data-stu-id="1ab52-115">Requirement</span></span> | <span data-ttu-id="1ab52-116">值</span><span class="sxs-lookup"><span data-stu-id="1ab52-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ab52-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1ab52-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1ab52-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ab52-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1ab52-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1ab52-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1ab52-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ab52-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1ab52-121">標頭</span><span class="sxs-lookup"><span data-stu-id="1ab52-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ab52-122"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="1ab52-122"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ab52-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ab52-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ab52-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="1ab52-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1ab52-125">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="1ab52-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="1ab52-126">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="1ab52-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="1ab52-127">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="1ab52-127">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="1ab52-128">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="1ab52-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="1ab52-129">ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="1ab52-129">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="1ab52-130">簡報描述項</span><span class="sxs-lookup"><span data-stu-id="1ab52-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




