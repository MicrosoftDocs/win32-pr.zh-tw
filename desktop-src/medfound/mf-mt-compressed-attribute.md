---
description: 指定媒體類型是否壓縮媒體資料。
ms.assetid: b44fb757-4390-4392-b1cb-37772b4ae3fb
title: 'MF_MT_COMPRESSED 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d049795f09845b5d32daf29ef033ab2e4b23007f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512820"
---
# <a name="mf_mt_compressed-attribute"></a><span data-ttu-id="39f17-103">MF \_ MT \_ 壓縮屬性</span><span class="sxs-lookup"><span data-stu-id="39f17-103">MF\_MT\_COMPRESSED attribute</span></span>

<span data-ttu-id="39f17-104">指定媒體類型是否壓縮媒體資料。</span><span class="sxs-lookup"><span data-stu-id="39f17-104">Specifies for a media type whether the media data is compressed.</span></span>

## <a name="data-type"></a><span data-ttu-id="39f17-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="39f17-105">Data type</span></span>

<span data-ttu-id="39f17-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="39f17-106">**UINT32**</span></span>

<span data-ttu-id="39f17-107">視為布林值。</span><span class="sxs-lookup"><span data-stu-id="39f17-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="39f17-108">備註</span><span class="sxs-lookup"><span data-stu-id="39f17-108">Remarks</span></span>

<span data-ttu-id="39f17-109">如果這個屬性為 **TRUE**，則媒體類型會是壓縮的格式。</span><span class="sxs-lookup"><span data-stu-id="39f17-109">If this attribute is **TRUE**, the media type is a compressed format.</span></span> <span data-ttu-id="39f17-110">否則，可能是媒體類型未壓縮，或壓縮類型未知。</span><span class="sxs-lookup"><span data-stu-id="39f17-110">Otherwise, either the media type is uncompressed or the compression type is not known.</span></span>

<span data-ttu-id="39f17-111">針對所有壓縮格式，這個屬性不一定會設定為 **TRUE** ，因此應用程式通常不會依賴這個屬性。</span><span class="sxs-lookup"><span data-stu-id="39f17-111">This attribute is not guaranteed to be set to **TRUE** for all compressed formats, so applications should generally not rely this attribute.</span></span> <span data-ttu-id="39f17-112">判斷格式是否壓縮的最可靠方式，是維護已知格式的清單。</span><span class="sxs-lookup"><span data-stu-id="39f17-112">The most reliable way to determine whether a format is compressed is to maintain a list of known formats.</span></span> <span data-ttu-id="39f17-113">如果應用程式無法辨識格式（如 [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md) 屬性中所指定），則不應假設任何關於格式壓縮的資訊。</span><span class="sxs-lookup"><span data-stu-id="39f17-113">If an application does not recognize a format, as specified in the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute, it should not assume anything about the compression of the format.</span></span>

<span data-ttu-id="39f17-114">若要判斷格式是否使用時態性壓縮 (表示某些範例會計算為先前範例) 的差異，請檢查 [**MF \_ MT \_ 所有 \_ 範例 \_ 獨立**](mf-mt-all-samples-independent-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="39f17-114">To determine whether a format uses temporal compression (meaning that some samples are computed as deltas from earlier samples), check the [**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**](mf-mt-all-samples-independent-attribute.md) attribute.</span></span>

<span data-ttu-id="39f17-115">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="39f17-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="39f17-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="39f17-116">Requirements</span></span>



| <span data-ttu-id="39f17-117">需求</span><span class="sxs-lookup"><span data-stu-id="39f17-117">Requirement</span></span> | <span data-ttu-id="39f17-118">值</span><span class="sxs-lookup"><span data-stu-id="39f17-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="39f17-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="39f17-119">Minimum supported client</span></span><br/> | <span data-ttu-id="39f17-120">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39f17-120">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="39f17-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="39f17-121">Minimum supported server</span></span><br/> | <span data-ttu-id="39f17-122">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39f17-122">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="39f17-123">標頭</span><span class="sxs-lookup"><span data-stu-id="39f17-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="39f17-124"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="39f17-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39f17-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39f17-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39f17-126">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="39f17-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="39f17-127">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="39f17-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="39f17-128">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="39f17-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="39f17-129">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="39f17-129">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="39f17-130">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="39f17-130">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




