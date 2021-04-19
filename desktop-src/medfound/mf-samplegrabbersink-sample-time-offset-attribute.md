---
description: 範例抓取程式收到的每個樣本上的時間戳記之間的位移，以及範例抓取器呈現範例的時間。
ms.assetid: 8d06b415-aafc-4276-9a88-4b7262df62f1
title: 'MF_SAMPLEGRABBERSINK_SAMPLE_TIME_OFFSET 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d99f65c5023bbe8705e21269dfb07d6f24db4190
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979743"
---
# <a name="mf_samplegrabbersink_sample_time_offset-attribute"></a><span data-ttu-id="3e259-103">MF \_ SAMPLEGRABBERSINK \_ SAMPLE \_ TIME \_ OFFSET 屬性</span><span class="sxs-lookup"><span data-stu-id="3e259-103">MF\_SAMPLEGRABBERSINK\_SAMPLE\_TIME\_OFFSET attribute</span></span>

<span data-ttu-id="3e259-104">範例抓取程式收到的每個樣本上的時間戳記之間的位移，以及範例抓取器呈現範例的時間。</span><span class="sxs-lookup"><span data-stu-id="3e259-104">Offset between the time stamp on each sample received by the sample grabber, and the time when the sample grabber presents the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="3e259-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="3e259-105">Data type</span></span>

<span data-ttu-id="3e259-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="3e259-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="3e259-107">備註</span><span class="sxs-lookup"><span data-stu-id="3e259-107">Remarks</span></span>

<span data-ttu-id="3e259-108">您可以在 [**MFCreateSampleGrabberSinkActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate)函數所傳回的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)物件上設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="3e259-108">You can set this attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) object that is returned by the [**MFCreateSampleGrabberSinkActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) function.</span></span> <span data-ttu-id="3e259-109">這個屬性可讓範例抓取器的回呼函式接收比展示時間更早的範例。</span><span class="sxs-lookup"><span data-stu-id="3e259-109">This attribute enables the sample grabber's callback function to receive samples earlier than the presentation time.</span></span>

<span data-ttu-id="3e259-110">當範例抓取器收到新的範例時，它會在 time *t* − *offset* 上顯示範例，其中 *t* 是樣本上的時間戳記，而 *offset* 是這個屬性的值。</span><span class="sxs-lookup"><span data-stu-id="3e259-110">When the sample grabber receives a new sample, it presents the sample at time *t* − *offset*, where *t* is the time stamp on the sample and *offset* is the value of this attribute.</span></span> <span data-ttu-id="3e259-111">如果未設定此屬性，則預設值為零。</span><span class="sxs-lookup"><span data-stu-id="3e259-111">If this attribute is not set, the default value is zero.</span></span>

<span data-ttu-id="3e259-112">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="3e259-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e259-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e259-113">Requirements</span></span>



| <span data-ttu-id="3e259-114">需求</span><span class="sxs-lookup"><span data-stu-id="3e259-114">Requirement</span></span> | <span data-ttu-id="3e259-115">值</span><span class="sxs-lookup"><span data-stu-id="3e259-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3e259-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3e259-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3e259-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3e259-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3e259-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3e259-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3e259-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3e259-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3e259-120">標頭</span><span class="sxs-lookup"><span data-stu-id="3e259-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e259-121"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3e259-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e259-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3e259-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e259-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="3e259-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3e259-124">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="3e259-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="3e259-125">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="3e259-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="3e259-126">**IMFSampleGrabberSinkCallback**</span><span class="sxs-lookup"><span data-stu-id="3e259-126">**IMFSampleGrabberSinkCallback**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback)
</dt> <dt>

[<span data-ttu-id="3e259-127">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="3e259-127">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




