---
description: 指定解碼時應該使用的反強調篩選類型。 這個屬性會套用至 MPEG 音訊編碼器。
ms.assetid: 1c1f7ac0-48a1-46d6-a131-fe281f2c86ba
title: 'AVEncMPAEmphasisType 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e00b424f8b70176a04385b52c6ca278cfc0a5c53
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972313"
---
# <a name="avencmpaemphasistype-property"></a><span data-ttu-id="a6932-104">AVEncMPAEmphasisType 屬性</span><span class="sxs-lookup"><span data-stu-id="a6932-104">AVEncMPAEmphasisType property</span></span>

<span data-ttu-id="a6932-105">指定解碼時應該使用的反強調篩選類型。</span><span class="sxs-lookup"><span data-stu-id="a6932-105">Specifies the type of de-emphasis filter that should be used when decoding.</span></span> <span data-ttu-id="a6932-106">這個屬性會套用至 MPEG 音訊編碼器。</span><span class="sxs-lookup"><span data-stu-id="a6932-106">This property applies to MPEG audio encoders.</span></span>

<span data-ttu-id="a6932-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="a6932-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="a6932-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="a6932-108">Data type</span></span>

<span data-ttu-id="a6932-109">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="a6932-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="a6932-110">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="a6932-110">Property GUID</span></span>

<span data-ttu-id="a6932-111">**CODECAPI \_ AVEncMPAEmphasisType**</span><span class="sxs-lookup"><span data-stu-id="a6932-111">**CODECAPI\_AVEncMPAEmphasisType**</span></span>

## <a name="property-value"></a><span data-ttu-id="a6932-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="a6932-112">Property value</span></span>

<span data-ttu-id="a6932-113">這個屬性的值是 [**eAVEncMPAEmphasisType**](/windows/win32/api/codecapi/ne-codecapi-eavencmpaemphasistype) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="a6932-113">The value of this property is a member of the [**eAVEncMPAEmphasisType**](/windows/win32/api/codecapi/ne-codecapi-eavencmpaemphasistype) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6932-114">備註</span><span class="sxs-lookup"><span data-stu-id="a6932-114">Remarks</span></span>

<span data-ttu-id="a6932-115">這個屬性會在框架標題中設定強調位。</span><span class="sxs-lookup"><span data-stu-id="a6932-115">This property sets the emphasis bits in the frame header.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6932-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="a6932-116">Requirements</span></span>



| <span data-ttu-id="a6932-117">需求</span><span class="sxs-lookup"><span data-stu-id="a6932-117">Requirement</span></span> | <span data-ttu-id="a6932-118">值</span><span class="sxs-lookup"><span data-stu-id="a6932-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a6932-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a6932-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a6932-120">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a6932-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="a6932-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a6932-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a6932-122">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a6932-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a6932-123">標頭</span><span class="sxs-lookup"><span data-stu-id="a6932-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6932-124"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="a6932-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6932-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a6932-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6932-126">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="a6932-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="a6932-127">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="a6932-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

