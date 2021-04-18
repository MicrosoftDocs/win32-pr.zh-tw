---
description: 將目前的框架標示為 LTR 框架。
ms.assetid: D70A54D6-DA9B-40E5-B130-0AA9C5363DF0
title: 'CODECAPI_AVEncVideoMarkLTRFrame 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a377f30aec049bc5cbc850ea03ace9dcc640bd6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510818"
---
# <a name="codecapi_avencvideomarkltrframe-property"></a><span data-ttu-id="6e79e-103">CODECAPI \_ AVEncVideoMarkLTRFrame 屬性</span><span class="sxs-lookup"><span data-stu-id="6e79e-103">CODECAPI\_AVEncVideoMarkLTRFrame property</span></span>

<span data-ttu-id="6e79e-104">將目前的框架標示為 LTR 框架。</span><span class="sxs-lookup"><span data-stu-id="6e79e-104">Marks the current frame as a LTR frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="6e79e-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="6e79e-105">Data type</span></span>

<span data-ttu-id="6e79e-106">**ULONG** (VT \_ UI4) </span><span class="sxs-lookup"><span data-stu-id="6e79e-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="6e79e-107">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="6e79e-107">Property GUID</span></span>

<span data-ttu-id="6e79e-108">**CODECAPI \_ AVEncVideoMarkLTRFrame**</span><span class="sxs-lookup"><span data-stu-id="6e79e-108">**CODECAPI\_AVEncVideoMarkLTRFrame**</span></span>

## <a name="remarks"></a><span data-ttu-id="6e79e-109">備註</span><span class="sxs-lookup"><span data-stu-id="6e79e-109">Remarks</span></span>

<span data-ttu-id="6e79e-110">**H.264/AVC 編碼器：**</span><span class="sxs-lookup"><span data-stu-id="6e79e-110">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="6e79e-111">此控制項的值是與目前框架相關聯的 h.264 語法 *LongTermFramIdx* 值。</span><span class="sxs-lookup"><span data-stu-id="6e79e-111">The value of this control is the value of H.264 syntax *LongTermFramIdx* associated with the current frame.</span></span> <span data-ttu-id="6e79e-112">如果目前的框架不在基底圖層中，例如語法元素 *時態 \_ 識別碼* 不等於0，則這個屬性會以編碼順序套用至下一個基底圖層框架。</span><span class="sxs-lookup"><span data-stu-id="6e79e-112">If the current frame is not in the base layer, for example syntax element *temporal\_id* is not equal to 0, this property applies to the next base layer frame in encoding order.</span></span>

<span data-ttu-id="6e79e-113">如果使用 CODECAPI AVEncVideoMarkLTRFrame 屬性來發出標示 LTR 框架的暫止呼叫 \_ ，且編碼器尚未將框架標示為 ltr，則不應呼叫此屬性。</span><span class="sxs-lookup"><span data-stu-id="6e79e-113">This property should not be called if a pending call to mark an LTR frame has been issued using the CODECAPI\_AVEncVideoMarkLTRFrame property and the encoder has not yet marked a frame as LTR.</span></span> <span data-ttu-id="6e79e-114">換句話說，編碼器不應將 CODECAPI AVEncVideoMarkLTRFrame 要求排入佇列 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6e79e-114">In other words, the encoder should not queue up CODECAPI\_AVEncVideoMarkLTRFrame requests.</span></span> <span data-ttu-id="6e79e-115">如果在 \_ 其他 CODECAPI AVEncVideoMarkLTRFrame 要求仍在擱置中時提交 CODECAPI AVEncVideoMarkLTRFrame 要求 \_ ，則應捨棄較舊的要求。</span><span class="sxs-lookup"><span data-stu-id="6e79e-115">If a CODECAPI\_AVEncVideoMarkLTRFrame request is submitted while another CODECAPI\_AVEncVideoMarkLTRFrame request is still pending, the older request should be dropped.</span></span>

<span data-ttu-id="6e79e-116">CODECAPI \_ AVEncVideoMarkLTRFrame 屬性是動態的，可在編碼會話期間設定。</span><span class="sxs-lookup"><span data-stu-id="6e79e-116">The CODECAPI\_AVEncVideoMarkLTRFrame property is dynamic and can be set during the encoding session.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e79e-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e79e-117">Requirements</span></span>



| <span data-ttu-id="6e79e-118">需求</span><span class="sxs-lookup"><span data-stu-id="6e79e-118">Requirement</span></span> | <span data-ttu-id="6e79e-119">值</span><span class="sxs-lookup"><span data-stu-id="6e79e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6e79e-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6e79e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6e79e-121">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e79e-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="6e79e-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6e79e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6e79e-123">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e79e-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="6e79e-124">標頭</span><span class="sxs-lookup"><span data-stu-id="6e79e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e79e-125"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="6e79e-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e79e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e79e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e79e-127">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="6e79e-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




