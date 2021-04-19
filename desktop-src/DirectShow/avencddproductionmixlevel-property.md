---
description: 指定杜比數位音訊串流中的混合層級（以分貝 (dB) ）。 此屬性適用于杜比數位音訊編碼器。
ms.assetid: fcb16d02-af4f-4626-99ee-2831172e5280
title: 'AVEncDDProductionMixLevel 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8a1726db6ab4841b4603a61bcfe39504742db42
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106977000"
---
# <a name="avencddproductionmixlevel-property"></a><span data-ttu-id="f2ae4-104">AVEncDDProductionMixLevel 屬性</span><span class="sxs-lookup"><span data-stu-id="f2ae4-104">AVEncDDProductionMixLevel property</span></span>

<span data-ttu-id="f2ae4-105">指定杜比數位音訊串流中的混合層級（以分貝 (dB) ）。</span><span class="sxs-lookup"><span data-stu-id="f2ae4-105">Specifies the mixing level, in decibels (dB), in a Dolby Digital audio stream.</span></span> <span data-ttu-id="f2ae4-106">此屬性適用于杜比數位音訊編碼器。</span><span class="sxs-lookup"><span data-stu-id="f2ae4-106">This property applies to Dolby Digital audio encoders.</span></span>

<span data-ttu-id="f2ae4-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="f2ae4-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="f2ae4-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="f2ae4-108">Data type</span></span>

<span data-ttu-id="f2ae4-109">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="f2ae4-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="f2ae4-110">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="f2ae4-110">Property GUID</span></span>

<span data-ttu-id="f2ae4-111">**CODECAPI \_ AVEncDDProductionMixLevel**</span><span class="sxs-lookup"><span data-stu-id="f2ae4-111">**CODECAPI\_AVEncDDProductionMixLevel**</span></span>

## <a name="property-value"></a><span data-ttu-id="f2ae4-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="f2ae4-112">Property value</span></span>

<span data-ttu-id="f2ae4-113">這個屬性具有線性範圍的值。</span><span class="sxs-lookup"><span data-stu-id="f2ae4-113">This property has a linear range of values.</span></span> <span data-ttu-id="f2ae4-114">若要取得支援的範圍，請呼叫 [**ICodecAPI：： GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange)。</span><span class="sxs-lookup"><span data-stu-id="f2ae4-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="f2ae4-115">備註</span><span class="sxs-lookup"><span data-stu-id="f2ae4-115">Remarks</span></span>

<span data-ttu-id="f2ae4-116">如果設定此屬性，請將 [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) 屬性設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="f2ae4-116">If you set this property, set the [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) property to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2ae4-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2ae4-117">Requirements</span></span>



| <span data-ttu-id="f2ae4-118">需求</span><span class="sxs-lookup"><span data-stu-id="f2ae4-118">Requirement</span></span> | <span data-ttu-id="f2ae4-119">值</span><span class="sxs-lookup"><span data-stu-id="f2ae4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f2ae4-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f2ae4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f2ae4-121">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f2ae4-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="f2ae4-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f2ae4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f2ae4-123">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f2ae4-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="f2ae4-124">標頭</span><span class="sxs-lookup"><span data-stu-id="f2ae4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2ae4-125"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="f2ae4-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2ae4-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2ae4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2ae4-127">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="f2ae4-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="f2ae4-128">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="f2ae4-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




