---
description: 設定在 SPS 網路抽象層中 (SPS) 識別碼的順序參數集 (NAL) 單位（在 h.264 位串流中）。
ms.assetid: 583DD539-6EE8-4DD4-A0FE-D2BBE1A4302F
title: 'CODECAPI_AVEncH264SPSID 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e06fb78fc128b2eec5db2c61faf70ee10a5eba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111865"
---
# <a name="codecapi_avench264spsid-property"></a><span data-ttu-id="e54e7-103">CODECAPI \_ AVEncH264SPSID 屬性</span><span class="sxs-lookup"><span data-stu-id="e54e7-103">CODECAPI\_AVEncH264SPSID property</span></span>

<span data-ttu-id="e54e7-104">設定在 SPS 網路抽象層中 (SPS) 識別碼的順序參數集 (NAL) 單位（在 h.264 位串流中）。</span><span class="sxs-lookup"><span data-stu-id="e54e7-104">Sets the sequence parameter set (SPS) identifier in the SPS network abstraction layer (NAL) unit of the H.264 bit stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="e54e7-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="e54e7-105">Data type</span></span>

<span data-ttu-id="e54e7-106">**ULONG** (VT \_ UI4) </span><span class="sxs-lookup"><span data-stu-id="e54e7-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="e54e7-107">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="e54e7-107">Property GUID</span></span>

<span data-ttu-id="e54e7-108">**CODECAPI \_ AVEncH264SPSID**</span><span class="sxs-lookup"><span data-stu-id="e54e7-108">**CODECAPI\_AVEncH264SPSID**</span></span>

## <a name="property-value"></a><span data-ttu-id="e54e7-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="e54e7-109">Property value</span></span>

<span data-ttu-id="e54e7-110">在 SPS NAL 單位中指定 **seq \_ 參數 \_ 集 \_ 識別碼** 的值。</span><span class="sxs-lookup"><span data-stu-id="e54e7-110">Specifies the value of **seq\_parameter\_set\_id** in the SPS NAL unit.</span></span> <span data-ttu-id="e54e7-111">**Seq \_ 參數 \_ 集 \_ 識別碼** 語法元素會識別 sequence 參數集。</span><span class="sxs-lookup"><span data-stu-id="e54e7-111">The **seq\_parameter\_set\_id** syntax element identifies the sequence parameter set.</span></span> <span data-ttu-id="e54e7-112">產生的位資料流程可以與其他位資料流程串連，以產生較長的位資料流程，其中包含多個具有不同 SPS 識別碼的序列參數集。</span><span class="sxs-lookup"><span data-stu-id="e54e7-112">The resulting bit stream can be concatenated with other bit streams, to produce a longer bit stream that contains multiple sequence parameter sets with different SPS identifiers.</span></span>

<span data-ttu-id="e54e7-113">有效範圍是 0 31，如 h.264/AVC 規格中所指定。</span><span class="sxs-lookup"><span data-stu-id="e54e7-113">The valid range is 0 31, as specified in the H.264/AVC specification.</span></span>

## <a name="requirements"></a><span data-ttu-id="e54e7-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="e54e7-114">Requirements</span></span>



| <span data-ttu-id="e54e7-115">需求</span><span class="sxs-lookup"><span data-stu-id="e54e7-115">Requirement</span></span> | <span data-ttu-id="e54e7-116">值</span><span class="sxs-lookup"><span data-stu-id="e54e7-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e54e7-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e54e7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e54e7-118">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e54e7-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="e54e7-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e54e7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e54e7-120">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e54e7-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="e54e7-121">標頭</span><span class="sxs-lookup"><span data-stu-id="e54e7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e54e7-122"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="e54e7-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e54e7-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e54e7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e54e7-124">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="e54e7-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="e54e7-125">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="e54e7-125">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

