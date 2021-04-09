---
description: 指定輸入影片的色度地點。 色度地點會定義每個色度樣本的位置，相對於 luma 範例。
ms.assetid: e9f8fef5-73da-424d-a239-09779b81a02b
title: 'AVEncVideoInputChromaSubsampling 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 958237a50c42ef7e5387c89cb7476a12ae72968f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935919"
---
# <a name="avencvideoinputchromasubsampling-property"></a><span data-ttu-id="cf59c-104">AVEncVideoInputChromaSubsampling 屬性</span><span class="sxs-lookup"><span data-stu-id="cf59c-104">AVEncVideoInputChromaSubsampling property</span></span>

<span data-ttu-id="cf59c-105">指定輸入影片的色度地點。</span><span class="sxs-lookup"><span data-stu-id="cf59c-105">Specifies the chroma siting for the input video.</span></span> <span data-ttu-id="cf59c-106">色度地點會定義每個色度樣本的位置，相對於 luma 範例。</span><span class="sxs-lookup"><span data-stu-id="cf59c-106">Chroma siting defines the positions of the chroma samples relative to the luma samples.</span></span>

<span data-ttu-id="cf59c-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="cf59c-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="cf59c-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="cf59c-108">Data type</span></span>

<span data-ttu-id="cf59c-109">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="cf59c-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="cf59c-110">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="cf59c-110">Property GUID</span></span>

<span data-ttu-id="cf59c-111">**CODECAPI \_ AVEncVideoInputChromaSubsampling**</span><span class="sxs-lookup"><span data-stu-id="cf59c-111">**CODECAPI\_AVEncVideoInputChromaSubsampling**</span></span>

## <a name="property-value"></a><span data-ttu-id="cf59c-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="cf59c-112">Property value</span></span>

<span data-ttu-id="cf59c-113">這個屬性的值是 [**eAVEncVideoChromaSubsampling**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideochromasubsampling) 列舉中的位 or 旗標。</span><span class="sxs-lookup"><span data-stu-id="cf59c-113">The value of this property is a bitwise OR of flags from the [**eAVEncVideoChromaSubsampling**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideochromasubsampling) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf59c-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf59c-114">Requirements</span></span>



| <span data-ttu-id="cf59c-115">需求</span><span class="sxs-lookup"><span data-stu-id="cf59c-115">Requirement</span></span> | <span data-ttu-id="cf59c-116">值</span><span class="sxs-lookup"><span data-stu-id="cf59c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf59c-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cf59c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cf59c-118">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cf59c-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="cf59c-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cf59c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cf59c-120">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cf59c-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="cf59c-121">標頭</span><span class="sxs-lookup"><span data-stu-id="cf59c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf59c-122"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="cf59c-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf59c-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf59c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf59c-124">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="cf59c-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="cf59c-125">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="cf59c-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




