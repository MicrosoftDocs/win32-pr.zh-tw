---
description: 指定編碼影片的色度地點。 色度地點會定義每個色度樣本的位置，相對於 luma 範例。
ms.assetid: 05acb05f-37e1-4953-bd24-ae790d355bf9
title: 'AVEncVideoOutputChromaSubsampling 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 288e9020d1809dfc4b6590121dcce30bf604cd0e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385644"
---
# <a name="avencvideooutputchromasubsampling-property"></a><span data-ttu-id="ae93c-104">AVEncVideoOutputChromaSubsampling 屬性</span><span class="sxs-lookup"><span data-stu-id="ae93c-104">AVEncVideoOutputChromaSubsampling property</span></span>

<span data-ttu-id="ae93c-105">指定編碼影片的色度地點。</span><span class="sxs-lookup"><span data-stu-id="ae93c-105">Specifies the chroma siting for the encoded video.</span></span> <span data-ttu-id="ae93c-106">色度地點會定義每個色度樣本的位置，相對於 luma 範例。</span><span class="sxs-lookup"><span data-stu-id="ae93c-106">Chroma siting defines the positions of the chroma samples relative to the luma samples.</span></span>

<span data-ttu-id="ae93c-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="ae93c-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="ae93c-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="ae93c-108">Data type</span></span>

<span data-ttu-id="ae93c-109">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="ae93c-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="ae93c-110">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="ae93c-110">Property GUID</span></span>

<span data-ttu-id="ae93c-111">**CODECAPI \_ AVEncVideoOutputChromaSubsampling**</span><span class="sxs-lookup"><span data-stu-id="ae93c-111">**CODECAPI\_AVEncVideoOutputChromaSubsampling**</span></span>

## <a name="property-value"></a><span data-ttu-id="ae93c-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="ae93c-112">Property value</span></span>

<span data-ttu-id="ae93c-113">這個屬性的值是 [**eAVEncVideoChromaSubsampling**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideochromasubsampling) 列舉中的位 or 旗標。</span><span class="sxs-lookup"><span data-stu-id="ae93c-113">The value of this property is a bitwise OR of flags from the [**eAVEncVideoChromaSubsampling**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideochromasubsampling) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae93c-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae93c-114">Requirements</span></span>



| <span data-ttu-id="ae93c-115">需求</span><span class="sxs-lookup"><span data-stu-id="ae93c-115">Requirement</span></span> | <span data-ttu-id="ae93c-116">值</span><span class="sxs-lookup"><span data-stu-id="ae93c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae93c-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ae93c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ae93c-118">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae93c-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="ae93c-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ae93c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ae93c-120">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae93c-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="ae93c-121">標頭</span><span class="sxs-lookup"><span data-stu-id="ae93c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae93c-122"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="ae93c-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae93c-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae93c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae93c-124">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="ae93c-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="ae93c-125">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="ae93c-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




