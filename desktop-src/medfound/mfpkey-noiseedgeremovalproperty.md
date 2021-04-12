---
description: 指定編解碼器是否應嘗試偵測出雜訊的框架邊緣並將其移除。
ms.assetid: fdb4f3a8-1447-4e1e-a208-0f9b717f7626
title: 'MFPKEY_NOISEEDGEREMOVAL 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30acd92bae7693d0714e42d6b4f832a521557bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192252"
---
# <a name="mfpkey_noiseedgeremoval-property"></a><span data-ttu-id="3197f-103">MFPKEY \_ NOISEEDGEREMOVAL 屬性</span><span class="sxs-lookup"><span data-stu-id="3197f-103">MFPKEY\_NOISEEDGEREMOVAL Property</span></span>

<span data-ttu-id="3197f-104">指定編解碼器是否應嘗試偵測出雜訊的框架邊緣並將其移除。</span><span class="sxs-lookup"><span data-stu-id="3197f-104">Specifies whether the codec should attempt to detect noisy frame edges and remove them.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="3197f-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="3197f-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="3197f-106">g \_ wszWMVCNoiseEdgeRemoval</span><span class="sxs-lookup"><span data-stu-id="3197f-106">g\_wszWMVCNoiseEdgeRemoval</span></span>

## <a name="data-type"></a><span data-ttu-id="3197f-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="3197f-107">Data Type</span></span>

<span data-ttu-id="3197f-108">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="3197f-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="3197f-109">預設值</span><span class="sxs-lookup"><span data-stu-id="3197f-109">Default Value</span></span>

<span data-ttu-id="3197f-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="3197f-110">FALSE</span></span>

## <a name="remarks"></a><span data-ttu-id="3197f-111">備註</span><span class="sxs-lookup"><span data-stu-id="3197f-111">Remarks</span></span>

<span data-ttu-id="3197f-112">雜訊畫面邊緣通常是垂直的空白間隔， (從廣播電視的畫面格) 資料 VBI。</span><span class="sxs-lookup"><span data-stu-id="3197f-112">A noisy frame edge is usually the vertical blanking interval (VBI) data from a frame of broadcast television.</span></span> <span data-ttu-id="3197f-113">VBI 是電視框架的前21個掃描行。</span><span class="sxs-lookup"><span data-stu-id="3197f-113">The VBI is the first 21 scan lines of the television frame.</span></span> <span data-ttu-id="3197f-114">這些掃描行不包含影片資料，而是包含廣播的相關資料。</span><span class="sxs-lookup"><span data-stu-id="3197f-114">These scan lines do not contain video data—they contain data about the broadcast.</span></span> <span data-ttu-id="3197f-115">當捕捉卡錄製電視信號時，通常會從框架中移除 VBI。</span><span class="sxs-lookup"><span data-stu-id="3197f-115">When a television signal is recorded by a capture card, the VBI is usually removed from the frame.</span></span> <span data-ttu-id="3197f-116">編解碼器所執行的雜訊邊緣偵測和更正只能更正有三個或更少的雜訊行的邊緣。</span><span class="sxs-lookup"><span data-stu-id="3197f-116">The noisy edge detection and correction performed by the codec can only correct an edge that has three or fewer lines of noise.</span></span> <span data-ttu-id="3197f-117">如果捕捉的影片包含三條以上的雜訊線，則用來捕捉影片的硬體有問題。</span><span class="sxs-lookup"><span data-stu-id="3197f-117">If captured video contains more than three noisy lines, there is a problem with the hardware used to capture the video.</span></span>

<span data-ttu-id="3197f-118">如果編解碼器設定為移除有雜訊的邊緣，則會複製與雜訊邊緣連續的線條以填滿框架。</span><span class="sxs-lookup"><span data-stu-id="3197f-118">If the codec is set to remove noisy edges, it duplicates lines adjacent to the noisy edge to fill in the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="3197f-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="3197f-119">Requirements</span></span>



| <span data-ttu-id="3197f-120">需求</span><span class="sxs-lookup"><span data-stu-id="3197f-120">Requirement</span></span> | <span data-ttu-id="3197f-121">值</span><span class="sxs-lookup"><span data-stu-id="3197f-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3197f-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3197f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3197f-123">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3197f-123">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3197f-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3197f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3197f-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3197f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3197f-126">標頭</span><span class="sxs-lookup"><span data-stu-id="3197f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3197f-127"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="3197f-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3197f-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3197f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3197f-129">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="3197f-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




