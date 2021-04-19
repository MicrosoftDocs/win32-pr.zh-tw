---
description: 為變數位元速率指定位速率和對應緩衝區視窗的清單， (VBR) Advanced 系統格式 (ASF) 檔。
ms.assetid: e45d055f-d404-47e9-b3c8-ac743b290138
title: 'MF_PD_ASF_METADATA_LEAKY_BUCKET_PAIRS 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7426d15a806a8c61c9a2ea1fdfb0565372c5f48f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991883"
---
# <a name="mf_pd_asf_metadata_leaky_bucket_pairs-attribute"></a><span data-ttu-id="f6763-103">MF \_ PD \_ ASF \_ 中繼資料 \_ 有漏洞 \_ BUCKET \_ 配對屬性</span><span class="sxs-lookup"><span data-stu-id="f6763-103">MF\_PD\_ASF\_METADATA\_LEAKY\_BUCKET\_PAIRS attribute</span></span>

<span data-ttu-id="f6763-104">為變數位元速率指定位速率和對應緩衝區視窗的清單， (VBR) Advanced 系統格式 (ASF) 檔。</span><span class="sxs-lookup"><span data-stu-id="f6763-104">Specifies a list of bit rates and corresponding buffer windows for a variable bit rate (VBR) Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="f6763-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="f6763-105">Data type</span></span>

<span data-ttu-id="f6763-106">位元組陣列</span><span class="sxs-lookup"><span data-stu-id="f6763-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="f6763-107">備註</span><span class="sxs-lookup"><span data-stu-id="f6763-107">Remarks</span></span>

<span data-ttu-id="f6763-108">此屬性適用于 ASF 內容的表示描述項。</span><span class="sxs-lookup"><span data-stu-id="f6763-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="f6763-109">[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會產生這個屬性，此屬性會套用至 ASF 內容的表示描述項。</span><span class="sxs-lookup"><span data-stu-id="f6763-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute that applies to the presentation descriptor for ASF content.</span></span>

<span data-ttu-id="f6763-110">屬性值的格式如下：</span><span class="sxs-lookup"><span data-stu-id="f6763-110">The value of the attribute has the following format:</span></span>

``` syntax
struct {
    WORD wReserved;
    WM_LEAKY_BUCKET_PAIR bucket[2];
};
```

<span data-ttu-id="f6763-111">**WM \_ 有漏洞 \_ BUCKET \_** 組結構的定義如下：</span><span class="sxs-lookup"><span data-stu-id="f6763-111">The **WM\_LEAKY\_BUCKET\_PAIR** structure is defined as follows:</span></span>

``` syntax
typedef struct _WMLeakyBucketPair {
  DWORD  dwBitrate;
  DWORD  msBufferWindow;
} WM_LEAKY_BUCKET_PAIR;
```

<span data-ttu-id="f6763-112">針對每個位元速率， **msBufferWindow** 成員會指出播放開始之前要緩衝的內容量（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f6763-112">For each bit rate, the **msBufferWindow** member indicates how much content is buffered before playback begins, in milliseconds.</span></span> <span data-ttu-id="f6763-113">緩衝區的大小（以位元組為單位）等於 **msBufferWinow** x **dwBitrate** /8000。</span><span class="sxs-lookup"><span data-stu-id="f6763-113">The size of the buffer in bytes equals **msBufferWinow** x **dwBitrate** / 8000.</span></span>

> [!Note]  
> <span data-ttu-id="f6763-114">這個屬性會對應至 Windows Media 格式 SDK 中的 **ASFLeakyBucketPairs** 屬性。</span><span class="sxs-lookup"><span data-stu-id="f6763-114">This attribute corresponds to the **ASFLeakyBucketPairs** attribute in the Windows Media Format SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f6763-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f6763-115">Requirements</span></span>



| <span data-ttu-id="f6763-116">需求</span><span class="sxs-lookup"><span data-stu-id="f6763-116">Requirement</span></span> | <span data-ttu-id="f6763-117">值</span><span class="sxs-lookup"><span data-stu-id="f6763-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6763-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f6763-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f6763-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6763-119">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f6763-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f6763-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f6763-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6763-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f6763-122">標頭</span><span class="sxs-lookup"><span data-stu-id="f6763-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6763-123"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="f6763-123"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6763-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f6763-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6763-125">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="f6763-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f6763-126">**IMFAttributes：： GetBlob**</span><span class="sxs-lookup"><span data-stu-id="f6763-126">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="f6763-127">**IMFAttributes：： SetBlob**</span><span class="sxs-lookup"><span data-stu-id="f6763-127">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="f6763-128">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="f6763-128">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="f6763-129">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="f6763-129">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="f6763-130">ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="f6763-130">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="f6763-131">簡報描述項</span><span class="sxs-lookup"><span data-stu-id="f6763-131">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




