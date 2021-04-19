---
description: 指定杜比數位音訊串流中的音訊生產資訊旗標。 此屬性適用于杜比數位音訊編碼器。
ms.assetid: 72f5f988-37c3-40d4-9c1c-07086e60ea51
title: 'AVEncDDProductionInfoExists 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5069c8d30f0266b0727f735ede822be491c4a4a2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973357"
---
# <a name="avencddproductioninfoexists-property"></a><span data-ttu-id="0e29a-104">AVEncDDProductionInfoExists 屬性</span><span class="sxs-lookup"><span data-stu-id="0e29a-104">AVEncDDProductionInfoExists property</span></span>

<span data-ttu-id="0e29a-105">指定杜比數位音訊串流中的音訊生產資訊旗標。</span><span class="sxs-lookup"><span data-stu-id="0e29a-105">Specifies the audio production information flag in a Dolby Digital audio stream.</span></span> <span data-ttu-id="0e29a-106">此屬性適用于杜比數位音訊編碼器。</span><span class="sxs-lookup"><span data-stu-id="0e29a-106">This property applies to Dolby Digital audio encoders.</span></span>

<span data-ttu-id="0e29a-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="0e29a-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="0e29a-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="0e29a-108">Data type</span></span>

<span data-ttu-id="0e29a-109">**變異 \_BOOL** (**VT \_ bool**) </span><span class="sxs-lookup"><span data-stu-id="0e29a-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="0e29a-110">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="0e29a-110">Property GUID</span></span>

<span data-ttu-id="0e29a-111">**CODECAPI \_ AVEncDDProductionInfoExists**</span><span class="sxs-lookup"><span data-stu-id="0e29a-111">**CODECAPI\_AVEncDDProductionInfoExists**</span></span>

## <a name="remarks"></a><span data-ttu-id="0e29a-112">備註</span><span class="sxs-lookup"><span data-stu-id="0e29a-112">Remarks</span></span>

<span data-ttu-id="0e29a-113">如果值為 **VARIANT \_ TRUE**，混合層級和房間型別設定都有效。</span><span class="sxs-lookup"><span data-stu-id="0e29a-113">If the value is **VARIANT\_TRUE**, the mixing level and room type settings are valid.</span></span> <span data-ttu-id="0e29a-114">使用 [**AVEncDDProductionRoomType**](avencddproductionroomtype-property.md) 和 [**AVEncDDProductionMixLevel**](avencddproductionmixlevel-property.md) 屬性來指定這些設定。</span><span class="sxs-lookup"><span data-stu-id="0e29a-114">Specify these settings with the [**AVEncDDProductionRoomType**](avencddproductionroomtype-property.md) and [**AVEncDDProductionMixLevel**](avencddproductionmixlevel-property.md) properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e29a-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e29a-115">Requirements</span></span>



| <span data-ttu-id="0e29a-116">需求</span><span class="sxs-lookup"><span data-stu-id="0e29a-116">Requirement</span></span> | <span data-ttu-id="0e29a-117">值</span><span class="sxs-lookup"><span data-stu-id="0e29a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0e29a-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0e29a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0e29a-119">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e29a-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="0e29a-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0e29a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0e29a-121">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e29a-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="0e29a-122">標頭</span><span class="sxs-lookup"><span data-stu-id="0e29a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e29a-123"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="0e29a-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e29a-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0e29a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e29a-125">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="0e29a-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="0e29a-126">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="0e29a-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




