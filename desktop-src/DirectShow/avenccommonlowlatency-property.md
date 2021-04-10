---
description: 指定是否應將輸出資料流程結構化，以便編碼的資料流程具有低解碼延遲。
ms.assetid: a000a2d4-afcf-4b88-9bbc-f42758744de2
title: 'AVEncCommonLowLatency 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a13dd59b7aa09f6b0f2aa6a4c31031d090d41c85
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187556"
---
# <a name="avenccommonlowlatency-property"></a><span data-ttu-id="df5a7-103">AVEncCommonLowLatency 屬性</span><span class="sxs-lookup"><span data-stu-id="df5a7-103">AVEncCommonLowLatency property</span></span>

<span data-ttu-id="df5a7-104">指定是否應將輸出資料流程結構化，以便編碼的資料流程具有低解碼延遲。</span><span class="sxs-lookup"><span data-stu-id="df5a7-104">Specifies whether the output stream should be structured so that the encoded stream has a low decoding latency.</span></span>

<span data-ttu-id="df5a7-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="df5a7-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="df5a7-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="df5a7-106">Data type</span></span>

<span data-ttu-id="df5a7-107">**變異 \_BOOL** (**VT \_ bool**) </span><span class="sxs-lookup"><span data-stu-id="df5a7-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="df5a7-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="df5a7-108">Property GUID</span></span>

<span data-ttu-id="df5a7-109">**CODECAPI \_ AVEncCommonLowLatency**</span><span class="sxs-lookup"><span data-stu-id="df5a7-109">**CODECAPI\_AVEncCommonLowLatency**</span></span>

## <a name="remarks"></a><span data-ttu-id="df5a7-110">備註</span><span class="sxs-lookup"><span data-stu-id="df5a7-110">Remarks</span></span>

<span data-ttu-id="df5a7-111">解碼延遲會定義為必須緩衝的資料量。</span><span class="sxs-lookup"><span data-stu-id="df5a7-111">Decoding latency is defined as the amount of data the decoder must buffer.</span></span> <span data-ttu-id="df5a7-112">例如，在 MPEG 影片編碼器上將此屬性設定為 **VARIANT \_ TRUE** 會限制編碼器可使用的 GOP 結構類型。</span><span class="sxs-lookup"><span data-stu-id="df5a7-112">For example, setting this property to **VARIANT\_TRUE** on an MPEG video encoder limits the types of GOP structures the encoder can use.</span></span>

## <a name="requirements"></a><span data-ttu-id="df5a7-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="df5a7-113">Requirements</span></span>



| <span data-ttu-id="df5a7-114">需求</span><span class="sxs-lookup"><span data-stu-id="df5a7-114">Requirement</span></span> | <span data-ttu-id="df5a7-115">值</span><span class="sxs-lookup"><span data-stu-id="df5a7-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df5a7-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="df5a7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="df5a7-117">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="df5a7-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="df5a7-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="df5a7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="df5a7-119">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="df5a7-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="df5a7-120">標頭</span><span class="sxs-lookup"><span data-stu-id="df5a7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="df5a7-121"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="df5a7-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df5a7-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df5a7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df5a7-123">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="df5a7-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="df5a7-124">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="df5a7-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




