---
description: 指定編碼器支援的編碼傳遞數目。
ms.assetid: 8b476164-fd44-4277-89bd-ba9929bf93a2
title: 'AVEncCommonMultipassMode 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4302cf0a9524f16dee8e7b84060065a4c750e4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846668"
---
# <a name="avenccommonmultipassmode-property"></a><span data-ttu-id="cb858-103">AVEncCommonMultipassMode 屬性</span><span class="sxs-lookup"><span data-stu-id="cb858-103">AVEncCommonMultipassMode property</span></span>

<span data-ttu-id="cb858-104">指定編碼器支援的編碼傳遞數目。</span><span class="sxs-lookup"><span data-stu-id="cb858-104">Specifies the number of encoding passes that the encoder supports.</span></span>

<span data-ttu-id="cb858-105">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="cb858-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="cb858-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="cb858-106">Data type</span></span>

<span data-ttu-id="cb858-107">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="cb858-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="cb858-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="cb858-108">Property GUID</span></span>

<span data-ttu-id="cb858-109">**CODECAPI \_ AVEncCommonMultipassMode**</span><span class="sxs-lookup"><span data-stu-id="cb858-109">**CODECAPI\_AVEncCommonMultipassMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="cb858-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="cb858-110">Property value</span></span>

<span data-ttu-id="cb858-111">這個屬性會以值範圍的形式傳回。</span><span class="sxs-lookup"><span data-stu-id="cb858-111">This property is returned as a range of values.</span></span> <span data-ttu-id="cb858-112">若要取得支援的範圍，請呼叫 [**ICodecAPI：： GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange)。</span><span class="sxs-lookup"><span data-stu-id="cb858-112">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="cb858-113">備註</span><span class="sxs-lookup"><span data-stu-id="cb858-113">Remarks</span></span>

<span data-ttu-id="cb858-114">解碼延遲會定義為必須緩衝的資料量。</span><span class="sxs-lookup"><span data-stu-id="cb858-114">Decoding latency is defined as the amount of data the decoder must buffer.</span></span> <span data-ttu-id="cb858-115">例如，在 MPEG 影片編碼器上將此屬性設定為 **VARIANT \_ TRUE** 會限制編碼器可使用的 GOP 結構類型。</span><span class="sxs-lookup"><span data-stu-id="cb858-115">For example, setting this property to **VARIANT\_TRUE** on an MPEG video encoder limits the types of GOP structures the encoder can use.</span></span>

<span data-ttu-id="cb858-116">若要設定目前的編碼階段，請設定 [**AVEncCommonPassStart**](avenccommonpassstart-property.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="cb858-116">To set the current encoding pass, set the [**AVEncCommonPassStart**](avenccommonpassstart-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb858-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb858-117">Requirements</span></span>



| <span data-ttu-id="cb858-118">需求</span><span class="sxs-lookup"><span data-stu-id="cb858-118">Requirement</span></span> | <span data-ttu-id="cb858-119">值</span><span class="sxs-lookup"><span data-stu-id="cb858-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb858-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cb858-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cb858-121">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb858-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="cb858-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cb858-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cb858-123">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb858-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="cb858-124">標頭</span><span class="sxs-lookup"><span data-stu-id="cb858-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb858-125"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="cb858-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb858-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb858-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb858-127">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="cb858-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="cb858-128">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="cb858-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




