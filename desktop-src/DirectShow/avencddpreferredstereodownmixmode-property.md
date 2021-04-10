---
description: 指定杜比數位音訊串流慣用的身歷聲 downmix 模式。 此屬性適用于杜比數位音訊編碼器。
ms.assetid: 3cf9fba7-6895-4dfb-9aef-571c512b7955
title: 'AVEncDDPreferredStereoDownMixMode 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aea695491175c8cb7d769673fcb09dd6ad2ae9f6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846660"
---
# <a name="avencddpreferredstereodownmixmode-property"></a><span data-ttu-id="fabf6-104">AVEncDDPreferredStereoDownMixMode 屬性</span><span class="sxs-lookup"><span data-stu-id="fabf6-104">AVEncDDPreferredStereoDownMixMode property</span></span>

<span data-ttu-id="fabf6-105">指定杜比數位音訊串流慣用的身歷聲 downmix 模式。</span><span class="sxs-lookup"><span data-stu-id="fabf6-105">Specifies the preferred stereo downmix mode for a Dolby Digital audio stream.</span></span> <span data-ttu-id="fabf6-106">此屬性適用于杜比數位音訊編碼器。</span><span class="sxs-lookup"><span data-stu-id="fabf6-106">This property applies to Dolby Digital audio encoders.</span></span>

<span data-ttu-id="fabf6-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="fabf6-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="fabf6-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="fabf6-108">Data type</span></span>

<span data-ttu-id="fabf6-109">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="fabf6-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="fabf6-110">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="fabf6-110">Property GUID</span></span>

<span data-ttu-id="fabf6-111">**CODECAPI \_ AVEncDDPreferredStereoDownMixMode**</span><span class="sxs-lookup"><span data-stu-id="fabf6-111">**CODECAPI\_AVEncDDPreferredStereoDownMixMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="fabf6-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="fabf6-112">Property value</span></span>

<span data-ttu-id="fabf6-113">這個屬性的值是 [**eAVEncDDPreferredStereoDownMixMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencddpreferredstereodownmixmode) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="fabf6-113">The value of this property is a member of the [**eAVEncDDPreferredStereoDownMixMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencddpreferredstereodownmixmode) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="fabf6-114">備註</span><span class="sxs-lookup"><span data-stu-id="fabf6-114">Remarks</span></span>

<span data-ttu-id="fabf6-115">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="fabf6-115">This property is read/write.</span></span>

## <a name="requirements"></a><span data-ttu-id="fabf6-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="fabf6-116">Requirements</span></span>



| <span data-ttu-id="fabf6-117">需求</span><span class="sxs-lookup"><span data-stu-id="fabf6-117">Requirement</span></span> | <span data-ttu-id="fabf6-118">值</span><span class="sxs-lookup"><span data-stu-id="fabf6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fabf6-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fabf6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fabf6-120">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fabf6-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="fabf6-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fabf6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fabf6-122">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fabf6-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="fabf6-123">標頭</span><span class="sxs-lookup"><span data-stu-id="fabf6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fabf6-124"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="fabf6-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fabf6-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fabf6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fabf6-126">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="fabf6-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="fabf6-127">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="fabf6-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




