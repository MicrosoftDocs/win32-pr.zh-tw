---
description: 指定杜比數位音訊串流的房間類型。 此屬性適用于杜比數位音訊編碼器。
ms.assetid: d19b6b9d-9606-48a8-ac8e-cdbf15588a8f
title: 'AVEncDDProductionRoomType 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc2eed0bb491fc982a5102507e5b55bf610880a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109633"
---
# <a name="avencddproductionroomtype-property"></a><span data-ttu-id="6cfb2-104">AVEncDDProductionRoomType 屬性</span><span class="sxs-lookup"><span data-stu-id="6cfb2-104">AVEncDDProductionRoomType property</span></span>

<span data-ttu-id="6cfb2-105">指定杜比數位音訊串流的房間類型。</span><span class="sxs-lookup"><span data-stu-id="6cfb2-105">Specifies the room type for a Dolby Digital audio stream.</span></span> <span data-ttu-id="6cfb2-106">此屬性適用于杜比數位音訊編碼器。</span><span class="sxs-lookup"><span data-stu-id="6cfb2-106">This property applies to Dolby Digital audio encoders.</span></span>

<span data-ttu-id="6cfb2-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="6cfb2-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="6cfb2-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="6cfb2-108">Data type</span></span>

<span data-ttu-id="6cfb2-109">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="6cfb2-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="6cfb2-110">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="6cfb2-110">Property GUID</span></span>

<span data-ttu-id="6cfb2-111">**CODECAPI \_ AVEncDDProductionRoomType**</span><span class="sxs-lookup"><span data-stu-id="6cfb2-111">**CODECAPI\_AVEncDDProductionRoomType**</span></span>

## <a name="property-value"></a><span data-ttu-id="6cfb2-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="6cfb2-112">Property value</span></span>

<span data-ttu-id="6cfb2-113">這個屬性的值是 [**eAVEncDDProductionRoomType**](/windows/win32/api/codecapi/ne-codecapi-eavencddproductionroomtype) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="6cfb2-113">The value of this property is a member of the [**eAVEncDDProductionRoomType**](/windows/win32/api/codecapi/ne-codecapi-eavencddproductionroomtype) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cfb2-114">備註</span><span class="sxs-lookup"><span data-stu-id="6cfb2-114">Remarks</span></span>

<span data-ttu-id="6cfb2-115">*房間類型* 指的是在生產期間使用的空間大小。</span><span class="sxs-lookup"><span data-stu-id="6cfb2-115">*Room type* refers to the size of the room used during production.</span></span> <span data-ttu-id="6cfb2-116">如果設定此屬性，請將 [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) 屬性設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="6cfb2-116">If you set this property, set the [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) property to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cfb2-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="6cfb2-117">Requirements</span></span>



| <span data-ttu-id="6cfb2-118">需求</span><span class="sxs-lookup"><span data-stu-id="6cfb2-118">Requirement</span></span> | <span data-ttu-id="6cfb2-119">值</span><span class="sxs-lookup"><span data-stu-id="6cfb2-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6cfb2-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6cfb2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6cfb2-121">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6cfb2-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="6cfb2-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6cfb2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6cfb2-123">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6cfb2-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="6cfb2-124">標頭</span><span class="sxs-lookup"><span data-stu-id="6cfb2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cfb2-125"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="6cfb2-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cfb2-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6cfb2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cfb2-127">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="6cfb2-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="6cfb2-128">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="6cfb2-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

