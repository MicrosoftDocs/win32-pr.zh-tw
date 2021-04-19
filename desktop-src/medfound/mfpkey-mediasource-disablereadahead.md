---
description: 啟用或停用媒體來源的預先讀取。
ms.assetid: b2b8711f-ba63-4fba-bb88-8d254135eb21
title: 'MFPKEY_MediaSource_DisableReadAhead 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d06fe354431a24e15152268ba0ea6352e535c5e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990630"
---
# <a name="mfpkey_mediasource_disablereadahead-property"></a><span data-ttu-id="371d2-103">MFPKEY \_ MediaSource \_ DisableReadAhead 屬性</span><span class="sxs-lookup"><span data-stu-id="371d2-103">MFPKEY\_MediaSource\_DisableReadAhead property</span></span>

<span data-ttu-id="371d2-104">啟用或停用媒體來源的預先讀取。</span><span class="sxs-lookup"><span data-stu-id="371d2-104">Enables or disables read-ahead in a media source.</span></span>



<span data-ttu-id="371d2-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="371d2-105">Data type</span></span>

<span data-ttu-id="371d2-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="371d2-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="371d2-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="371d2-107">PROPVARIANT member</span></span>

<span data-ttu-id="371d2-108">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="371d2-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="371d2-109">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="371d2-109">VT\_BOOL</span></span>

<span data-ttu-id="371d2-110">**boolVal**</span><span class="sxs-lookup"><span data-stu-id="371d2-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="371d2-111">備註</span><span class="sxs-lookup"><span data-stu-id="371d2-111">Remarks</span></span>

<span data-ttu-id="371d2-112">應用程式可以使用此屬性來設定某些媒體來源。</span><span class="sxs-lookup"><span data-stu-id="371d2-112">Applications can use this property to configure some media sources.</span></span> <span data-ttu-id="371d2-113">若要設定屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。</span><span class="sxs-lookup"><span data-stu-id="371d2-113">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="371d2-114">如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。</span><span class="sxs-lookup"><span data-stu-id="371d2-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="371d2-115">如果值為 **VARIANT \_ TRUE**，就不會在位元組資料流程中向前讀取媒體來源。</span><span class="sxs-lookup"><span data-stu-id="371d2-115">If the value is **VARIANT\_TRUE**, the media source will not read ahead in the byte stream.</span></span> <span data-ttu-id="371d2-116">如果您打算從媒體來源讀取有限數量的資料，這項設定可以優化效能，例如，從影片檔案取得縮圖影像。</span><span class="sxs-lookup"><span data-stu-id="371d2-116">This setting can optimize performance if you plan to read a limited amount of data from the media source—for example, to get a thumbnail image from a video file.</span></span>

<span data-ttu-id="371d2-117">針對一般音訊/影片播放，此屬性應該設定為 **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="371d2-117">For typical audio/video playback, this property should be set to **VARIANT\_FALSE**.</span></span> <span data-ttu-id="371d2-118">預設值為 **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="371d2-118">The default value is **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="371d2-119">並非每個媒體來源都支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="371d2-119">Not every media source supports this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="371d2-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="371d2-120">Requirements</span></span>



| <span data-ttu-id="371d2-121">需求</span><span class="sxs-lookup"><span data-stu-id="371d2-121">Requirement</span></span> | <span data-ttu-id="371d2-122">值</span><span class="sxs-lookup"><span data-stu-id="371d2-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="371d2-123">用戶端</span><span class="sxs-lookup"><span data-stu-id="371d2-123">Client</span></span><br/> | <span data-ttu-id="371d2-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="371d2-124">Windows 7</span></span><br/>                                                               |
| <span data-ttu-id="371d2-125">標頭</span><span class="sxs-lookup"><span data-stu-id="371d2-125">Header</span></span><br/> | <dl> <span data-ttu-id="371d2-126"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="371d2-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="371d2-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="371d2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="371d2-128">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="371d2-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




