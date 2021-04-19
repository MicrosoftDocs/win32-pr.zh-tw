---
description: 包含來源讀取器的設定屬性。
ms.assetid: f7e5ef6a-5fc3-4f39-acc0-61ce79030211
title: 'MF_SOURCE_READER_MEDIASOURCE_CONFIG 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31f36b2a09810dd1c2563033ea65643f1dabcb3f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106993791"
---
# <a name="mf_source_reader_mediasource_config-attribute"></a><span data-ttu-id="376ca-103">MF \_ 來源 \_ 讀取器 \_ MEDIASOURCE \_ CONFIG 屬性</span><span class="sxs-lookup"><span data-stu-id="376ca-103">MF\_SOURCE\_READER\_MEDIASOURCE\_CONFIG attribute</span></span>

<span data-ttu-id="376ca-104">包含 [來源讀取器](source-reader.md)的設定屬性。</span><span class="sxs-lookup"><span data-stu-id="376ca-104">Contains configuration properties for the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="376ca-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="376ca-105">Data type</span></span>

<span data-ttu-id="376ca-106">**IPropertyStore \* *_ 儲存為 _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="376ca-106">**IPropertyStore\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="376ca-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="376ca-107">Get/set</span></span>

<span data-ttu-id="376ca-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)。</span><span class="sxs-lookup"><span data-stu-id="376ca-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="376ca-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)。</span><span class="sxs-lookup"><span data-stu-id="376ca-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="376ca-110">備註</span><span class="sxs-lookup"><span data-stu-id="376ca-110">Remarks</span></span>

<span data-ttu-id="376ca-111">這個屬性的值是屬性存放區之 **IPropertyStore** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="376ca-111">The value of this attribute is a pointer to the **IPropertyStore** interface of a property store.</span></span> <span data-ttu-id="376ca-112">您可以使用此屬性將設定屬性傳遞至媒體來源。</span><span class="sxs-lookup"><span data-stu-id="376ca-112">You can use this attribute to pass configuration properties to the media source.</span></span>

<span data-ttu-id="376ca-113">使用這個屬性搭配下列函數：</span><span class="sxs-lookup"><span data-stu-id="376ca-113">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="376ca-114">**MFCreateSourceReaderFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="376ca-114">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="376ca-115">**MFCreateSourceReaderFromURL**</span><span class="sxs-lookup"><span data-stu-id="376ca-115">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

<span data-ttu-id="376ca-116">就內部而言，來源讀取器會將 **IPropertyStore** 指標傳遞至來源解析程式。</span><span class="sxs-lookup"><span data-stu-id="376ca-116">Internally, the source reader passes the **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="376ca-117">如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。</span><span class="sxs-lookup"><span data-stu-id="376ca-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="376ca-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="376ca-118">Requirements</span></span>



| <span data-ttu-id="376ca-119">需求</span><span class="sxs-lookup"><span data-stu-id="376ca-119">Requirement</span></span> | <span data-ttu-id="376ca-120">值</span><span class="sxs-lookup"><span data-stu-id="376ca-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="376ca-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="376ca-121">Minimum supported client</span></span><br/> | <span data-ttu-id="376ca-122">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="376ca-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="376ca-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="376ca-123">Minimum supported server</span></span><br/> | <span data-ttu-id="376ca-124">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="376ca-124">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="376ca-125">標頭</span><span class="sxs-lookup"><span data-stu-id="376ca-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="376ca-126"><dt>Mfreadwrite。h</dt></span><span class="sxs-lookup"><span data-stu-id="376ca-126"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="376ca-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="376ca-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="376ca-128">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="376ca-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="376ca-129">來源讀取程式</span><span class="sxs-lookup"><span data-stu-id="376ca-129">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="376ca-130">來源讀取器屬性</span><span class="sxs-lookup"><span data-stu-id="376ca-130">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




